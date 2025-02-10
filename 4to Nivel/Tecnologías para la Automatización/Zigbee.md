**Zigbee** es una tecnología del [[Internet of Things]] que busca solucionar las comunicaciones de **bajo ancho de banda, baja latencia, y bajo consumo energético**. Trabaja en rangos de frecuencia libres.

Todos los dispositivos se pueden comunicar entre sí. La idea es **compartir información** entre todos los miembros de la red.

Es un estándar de conectividad construido sobre IEEE 802.15.4. Velocidades de datos posibles:

1. 250 Kbps para 2.4 GHz.
2. 40 Kbps para 915 MHz.
3. 20 Kbps para 868 MHz.

La especificación de Zigbee es un [[Protocolo]] de placa de radio basado en paquetes y destinado a dispositivos de bajo coste que funcionan con baterías. Busca ser fácil de usar.

Zigbee es creado y ratificado por las empresas miembros de la *Zigbee Board Alliance*, hoy en día llamada *Connectivity Standards Alliance*. El estándar actual es el 3.0, que garantiza **interoperabilidad** entre fabricantes.

Características de Zigbee:

- Admite topologías de red en estrella o punto a punto.
- Admite hasta 255 dispositivos por red.
- Soporta dispositivos de baja latencia.
- CSMA-CA: Carrier Sense Multiple Access/Collision Avoidance.
- Ciclo de trabajo bajo.
- Baja latencia.
- Encriptación [[Ciberseguridad#Cifrado Simétrico|AES]] de 128 bits.

## Arquitectura

Una red Zigbee tiene diferentes tipos de nodos:

- **Full Function Device**: un FFD puede comunicarse con cualquier dispositivo. Puede actuar como:
	1. **PAN Coordinator**: envía tramas *beacon* y administra direcciones de la red.
	2. **Coordinator**: actúa como un router.
	3. **Dispositivo normal**.
- **Reduced Function Device**: solo puede hablar con un FFD.

Tipos de topologías:

![[Topologías de Zigbee.png]]

Combinando varios árboles se puede formar un clúster de árboles. También se pueden armar clústers de clústers

Zigbee soporta **redes de malla** (*mesh*), que son redes descentralizadas tal que múltiples vías conectan cada nodo. También permiten reconfigurar rutas cuando algún nodo falla o se desconecta.

## Stack de Protocolos

![[Stack de Protocolos Zigbee.png]]

