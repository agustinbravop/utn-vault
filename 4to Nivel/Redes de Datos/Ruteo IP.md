El **ruteo IP** es el proceso (en [[IP]]) de seleccionar un camino entre los varios posibles. Lo realizan todos los hosts y [[Enrutadores]]. Características:

- Sin conexión.
- "Best effort".
- Información parcial (solo hace el salto al siguiente nodo).

Esto conlleva tres aspectos:

1. Qué información hay en la tabla de direcciones.
2. Cómo llegó allí.
3. Cómo usar esa información para tomar decisiones.

La tabla de enrutamiento contiene:

1. Dirección IP de la red de destino.
2. Máscara de subred.
3. Dirección IP del próximo salto.
4. Interfaz de salida.
5. Métricas (costos).
6. Protocolo origen de la información.
7. Etc...

Existe un algoritmo unificado de ruteo, que se ejecuta al darle un datagrama a enrutar y toda la tabla de ruteo:

```
Extraer dirección IP del destino `I_D`.
SI el prefijo de `I_D` coincide con algún prefijo:
	Estamos directamente conectados. Se envía el datagrama por esa red.
SINO:
	PARA cada entrada en la tabla de ruteo HACER:
		Sea `N` el AND bit a bit de `I_D` y la máscara de subred de la entrada.
		SI `N` es igual al prefijo de red de la entrada:
			Enrutar el datagrama por esa red.
        FIN_SI
    FIN_PARA
FIN_SI

SI no se encuentran coincidencias;
	Declarar error de ruteo.
FIN_SI
```

Se puede eliminar del algoritmo la porción referida a redes directamente conectadas si éstas también se agregan a la tabla. En las tablas de ruteo solo se guardan direcciones IP, no direcciones físicas. La ruta por defecto también se compara, al final.

Las direcciones IP no cambian durante el trayecto del datagrama. El ruteo IP **no modifica** el datagrama entrante. Solo los routers deben enrutar datagramas, a menos que se configure un host para hacerlo.
