IPv6, documentado en la RFC 1883-7, comenzó como [[IP]] new generation. Es un [[Protocolo]] definido en el RFC 2460 y busca reemplazar a IPv4.

Surge por el problema del espacio de direcciones IP agotado, y además es una oportunidad para corregir y adecuar IPv4 a las tecnologías actuales. IPv6 incluye aspectos de seguridad.

Una dirección IPv6 tiene 128 bits (mucho más que los 32 bits de IPv4). Se simplifica el encabezado (que de mínimo tiene 40 bytes).

![[IPv6.png]]

Las direcciones IPv6 definen prefijos que indican el uso de la dirección. Pueden embeber direcciones IPv4 para así facilitar la migración o **interoperabilidad**.

![[Prefijos de Direcciones IPv6.png]]

La representación se hace con segmentos de 16 bits separados por un símbolo de "dos puntos", lo cual es 4 caracteres en hexadecimal. Ejemplo:

```
FEDC:BA98:7654:3210:0000:0000:0000:0089
					\____________/
			     se abrevia con "::"
```

 A un encabezado IPv6 se lo puede extender con cabeceras extendidas opcionales, lo cual mejora la eficiencia. Hay 6 tipos de **cabeceras de extensión**:

1. **Opciones salto a salto**: sirven para enviar un *jumbograma* (paquete enorme).
2. **Opciones de destino**.
3. **Enrutamiento**.
4. **Fragmentación**: ahora el origen calcula los dragmentos.
5. **Autenticación**: se usa el algoritmo de hashing MD5.
6. **Encriptación**: se usa ESP para encriptar en modo transporte o modo túnel.

IPv6 soporta dos mecanismos para la autoconfiguración:

- **[[DHCP]]**: *Dynamic Host Configuration Protocol*.
- **ND**: Neighbor Discovery.

Existen tres enfoques para la **interoperabilidad** entre IPv4 e IPv6:

1. Pilas duales: cada estación debe tener ambos stacks de protocolos.
2. Túneles: gateways realizan la conversión entre IPv6 e IPv4 cuando un paquete entra o sale de un "túnel" que solo maneja IPv4.
3. Traductores: un NAT-PT gateway (*Network Address Translator and Protocol Translator Gateway*) conecta segmentos de routers IPv6 con sus vecinos IPv4.

En todos estos casos, se trata de adecuar los routers IPv4, ya que se consideran imposibles de eliminar por completo al 100%.
