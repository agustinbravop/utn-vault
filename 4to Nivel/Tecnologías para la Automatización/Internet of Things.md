Cada componente desempeña una función clara, y son integrados en una [[Redes de Datos|red de datos]] para crear una solución completa del **internet de las cosas** (_Internet of Things_, IoT).

La pila de tecnologías IoT cubre todas las tecnologías requeridas. Un _stack IoT_ consta de:

1. Dispositivos.
2. Gateway (que conecta los dispositivos al exterior).
3. Plataforma IoT.
4. Aplicaciones.

![[Internet of Things.png]]

Un _transductor_ ([[Sensores]] y [[Actuadores]]) es un dispositivo que convierte energía de una forma a otra.

En las soluciones IoT, e común **distribuir el procesamiento**. Un dispositivo IoT necesita algo de **inteligencia** (_computing power_), por lo cual se utilizan microcontroladores (como los ESP32 o Raspberry Pi Pico).

La comunicación puede ser:

- **Unidireccional**: un sensor solo envía datos al gateway.
- **Bidireccional**: un sensor envía y recibe datos del gateway.
- **Local**: no se comunica con el gateway.

Para la **selección de dispositivos**, hay varios criterios a considerar:

1. **Movilidad**: ¿Fijo o móvil?
2. **Alimentación**: ¿Requieren batería?
3. **Potencia de procesamiento**: ¿Cuánto CPU?
4. **Transmisión de datos**: volumen y frecuencia.
5. **Conexión**: ¿Serán inalámbricos?
6. **Densidad**: cantidad de dispositivos.

## Gateway IoT

Un **gateway IoT** concentra toda la información obtenida por los dispositivos. Es la puerta de enlace entre un dispositivo y una plataforma. Hay de HW y de SW.

Se encargan de:

1. Conectividad.
2. Traducción de [[Protocolo|protocolos]].
3. Agregado y preprocesamiento de datos.
4. Cifrado.
5. Gestión.
6. Control remoto.

Ejemplos de gateway IoT: The Things Network, Home Assistant.
