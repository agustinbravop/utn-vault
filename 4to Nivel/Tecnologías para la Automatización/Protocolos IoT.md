Para una solución del [[Internet of Things]], se necesitan protocolos de red y de datos.

El [[Protocolo]] de [[Capa de Red]] utilizado es casi siempre [[IPv6]].

Para el protocolo de datos, hay más variedad:

1. **MQTT**: *Message Queuing Telemetry Transport*. Es probablemente el más utilizado en IoT. Usa [[TCP]] en la  [[Capa de Transporte]]. Usa operaciones `publish` y `suscribe` para transmitir datos entre cliente y servidor. Los paquetes son diminutos y requieren poco ancho de banda.
2. **CoAP**: construido sobre [[UDP]], es fácil de utilizar. Un servidor dispone sus recursos bajo una URL y acepta peticiones HTTP, permitiendo una [[RESTful API]].
3. **XMPP**: este es un estándar abierto basado en XML para la comunicación en tiempo real. Definido en RFC 6120.

Los **estándares IoT** son necesarios para la interoperabilidad sencilla. Algo importante es decidir cómo conectar los dispositivos a internet.

## Tipos de Redes

Las [[Redes de Datos]] se clasifican según su **radio de alcance**:

$$\text{Nano} \lt \text{BAN} \lt \text{PAN} \lt \text{LAN}\lt \text{CAN}\lt \text{MAN}\lt \text{RAN}\lt \text{WAN}$$

Decidir qué tipo de red y estándares usar depende de los requisitos o *restricciones* del problema.

Para redes LAN, de **corto alcance y bajo consumo**:

1. Bluetooth.
2. NFC.
3. Wi-Fi/[[Estándar 802.11]].
4. Z-Wave.
5. [[Zigbee]].

Para redes LPWAN, de **área extensa y baja potencia**:

6. 4G LTE para IoT.
7. 5G para IoT.
8. Cat-0.
9. Cat-1.
10. [[LoRaWAN]].
11. Sigfox.
12. NB-IoT/CAT-M2.

Se utilizan protocolos específicos para IoT debido a las características particulares de estos dispositivos y redes. Las necesidades son:

- **Bajo consumo energético**.
- **Baja latencia**.
- **Baja velocidad**.
