**LoRaWAN**, un tipo de LPWAN, es una tecnología alternativa a [[Zigbee]] pensada para redes del [[Internet of Things]] de **mayor alcance**. Este [[Protocolo]] fue desarrollado en Francia por Cycleo, empresa adquirida por Semtech en 2012.

Son redes de **baja potencia** para cuidar el consumo energético de los dispositivos y prolongar la duración de sus baterías.

La velocidad de datos de LPWAN oscila entre **0.3 kbits/s y 50 kbits/s** por canal.

La capa física se basa en CCSM: *Chirp Spread Spectrum Modulation*, para poder crear un enlace de comunicación de largo alcance. Las LPWAN pueden cubrir distancias de hasta **50 km**. 

Para evitar problemas de atenuación, se usan bandas de frecuencia de entre **433 MHz y 868 MHz**.

Topología básica:

![[Topología LoRaWAN Básica.png]]

Se pueden agregar *coordinadores* que solamente concentran información para hacer una topología más escalable:

![[Topología LoRaWAN con Coordinadores.png]]

Tipos de nodo:

1. **Clase A**: solo escucha datos luego de enviar datos. Ahorra mucha batería.
2. **Clase B**: sincroniza tiempos con el gateway. Es difícil de implementar.
3. **Clase C**: permanentemente escucha datos. Entra en modo emisión de datos solo cuando es necesario transmitir.

Stack de protocolos:

![[Stack de Protocolos LoRaWAN.png]]

Formato de las tramas de cada capa:

![[Tramas LoRaWAN.png]]
