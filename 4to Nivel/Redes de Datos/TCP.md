*Transmission Control Protocol* (TCP) es un [[Protocolo]] de la [[Capa de Transporte]] para aplicaciones que requieren confiabilidad. Se considera que TCP es mucho más complejo que [[UDP]].

Características:

- Orientado a la conexión (*stream*).
- Abstracción.
- Full-duplex.
- Funcionamiento: establecer la conexión $\longrightarrow$ transmisión $\longrightarrow$ liberar la conexión.

![[Encabezado TCP.png]]

Los números de secuencia (de 32 bits) son acumulativos. Son como punteros que indican la posición del próximo octeto de datos a ser recibido. Se usa uno para cada sentido de la conexión, lo que se conoce como *piggybacking*. El *Initial Sequence Number* se asigna de forma aleatoria, y luego se lo incrementa secuencialmente.

**Inicio de la conexión**: se usa un saludo de tres vías. Se usan temporizadores *timeout* por si no se recibe una respuesta.

![[Inicio de la Conexión TCP.png]]

**Finalización de la conexión**: se usa un saludo de cuatro vías. La conexión puede quedar en un estado intermedio `HALF_CLOSE` si el sitio 2 sigue enviando datos.

![[Finalización de la Conexión TCP.png]]

Existen unos Well-Known Ports (WKP, [[Puertos]] bien conocidos) cuyo uso suele estar reservado.

![[Well-Known Ports de TCP.png]]

TCP también se encarga de gestionar la [[Congestión en TCP]].

## Control de Flujo

TCP hace un poco de [[Control de Flujo]]. En cada segmento, el extremo TCP anuncia la cantidad de octetos que pueden quedar pendientes de confirmación.

La ventana $W$ del receptor puede ajustarse dinámicamente. Anunciar una ventana cero indica que no desea recibir más datos, pero sí mantener abierta la conexión.

## Opciones

Si bien TCP soporta una gran variedad de opciones, en verdad muy pocas se utilizan.

Una opción permite escalar la ventana de un número de 16 bits a 32 bits.

## Temporizadores TCP

Para cada conexión abierta, cada extremo TCP mantiene cuatro temporizadores:

1. **RTO timer**: ante un timeout, el segmento se reenvía.
2. **2MSL timer**: permite que expiren todos los segmentos al finalizar una conexión.
3. **PERSIST timer**: en cada timeout, se sondea si la ventana cero sigue siendo cero.
4. **KEEPALIVE timer**: espera hasta el timeout para matar una conexión por ausencia de datos.
