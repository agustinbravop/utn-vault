La **conmutación de circuitos** da soporte a las llamadas telefónicas. La [[Transmisión de Datos]] a larga distancia se efectúa a través de una red de nodos intermedios de conmutación (concepto de redes WAN).

Estos nodos trasladan los datos sin interesarse por su contenido. Se conectan entre sí mediante enlaces (que suelen estar [[Multiplexación|multiplexados]]) y forman una red de comunicación conmutada.

![[Conmutación de Circuitos.png]]

El proceso de comunicación punto a punto tiene tres pasos:

1. Establecimiento del circuito. Una vez el circuito fue establecido, la red se comporta como una conexión directa.
2. Transferencia de datos.
3. Desconexión del circuito.

Componentes de una **red pública de telecomunicaciones**:

1. **Abonados**: dispositivos que se conectan a la red. Son las estaciones.
2. **Bucle local**: enlace entre el abonado y la red.
3. **Centrales**: centros de conmutación que encaminan y conmutan el tráfico. Son los nodos.
4. **Centrales finales**: centrales que conmutan entre un abonado y otra central.
5. **Líneas principales**: líneas entre centrales.

En un sistema moderno:

- El conmutador digital debe proporcionar un camino.
- El camino debe ser transparente.
- Se debe permitir la transmisión full duplex.

La conmutación se puede hacer por _división en el tiempo_, o por _división en el espacio_.

## Encaminamiento

Se hace un compromiso entre eficiencia y flexibilidad. El _esquema_ puede ser:

- **Estático**: no se adapta a la carga, y por ende hay mucho equipamiento ocioso.
- **Dinámico**: la decisión de encaminamiento depende del tráfico actual. Esto trae mayor complejidad y flexibilidad.

Los _algoritmos_ pueden ser:

- **Alternativos**: rutas posibles predefinidas. Cada conmutador tiene unas rutas pre-planificadas en orden de preferencia para cada destino.
- **Adaptables**: reacciona a la distribución cambiante del tráfico, pero requiere transmitir cierta información de control, lo que puede ocupar más recursos de los que libera.

Las _señales de control_ son señales que gestionan la red al establecer, mantener, y terminar llamadas. Hay señales de supervisión, de direccionamiento, de información, y de gestión. Se pueden enviar:

- **Por intrabanda**: se envía información de control cuando no hay llamadas.
- **Por fuera de banda**: consume poco ancho de banda.
- **Por canal común**: es la tendencia actual. Se puede usar modo _asociado_ o _no asociado_.

## Conmutación Lógica

Existe una tendencia actual hacia la **conmutación lógica** o _softswitch_. Un _conmutador lógico_ es un dispositivo de propósito general que al usar un software especializado se vuelve un conmutador telefónico inteligente.
