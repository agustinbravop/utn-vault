Las **magnitudes a medir** en la [[Evaluación de las Prestaciones]] de un sistema informático son **dimensiones** del sistema a analizar. Ellas caracterizan el comportamiento del hardware y software o hacen referencia a como el usuario o responsable del sistema ven el comportamiento.

Las tres **dimensiones** son:

1. **Consumo de tiempos**.
2. **Utilización de recursos o dispositivos**.
3. **Trabajo realizado por el sistema o componentes del mismo**.

## Variables

Cada una de estas magnitudes no es medible, sino que se contabiliza mediante una **variable** (que sí es medible) correspondiente a una de las tres magnitudes. La mayoría mide algo del rendimiento del **hardware** o del **sistema operativo**, y deben definirse en términos del sistema informático (no en términos de la aplicación).

### Variables Externas

Son perceptibles por el usuario:

- **Productividad o throughput**: cantidad de trabajo útil ejecutado por unidad de tiempo.
- **Capacidad**: productividad máxima alcanzable.
- **Tiempo de respuesta**: tiempo entre la solicitud de un trabajo y la recepción de su respuesta.

### Variables Internas

Son intrínsecas al sistema, visibles para el responsable del sistema:

- **Factor de utilización de un componente**: porcentaje de tiempo en uso de un [[Componentes de un SI|componente]].
- **Solapamiento de componentes**: porcentaje de tiempo en uso simultáneo.
- **Overhead**: porcentaje de tiempo usado en tareas no imputables directamente a un trabajo.
- **Factor de carga de multiprogramación**: relación entre el tiempo de respuesta de un trabajo en un entorno de multiprogramación y su tiempo de respuesta en monoprogramación.
- **Factor de ganancia de multiprogramación**: relación entre el tiempo total de ejecución necesario en monoprogramación y multiprogramación.
- **Frecuencia de fallo de página**: fallos de página por unidad de tiempo (en un sistema operativo de memoria virtual paginada).
- **Frecuencia de swapping**: programas expulsados de memoria por unidad de tiempo a causa de falta de espacio o reorganización.

### Variables Relativas al Comportamiento

Las variables de comportamiento no están directamente relacionadas con las [[Prestaciones de un SI]] de un elemento en particular, sino que surgen del comportamiento. Se aplican al sistema informático en su totalidad. Son:

- **Fiabilidad**: probabilidad de que el sistema trabaje correctamente. **Tiempo medio entre fallos**.
- **Disponibilidad**: probabilidad de que el SI esté **disponible ahora** y trabajando correctamente.
- **Seguridad**: probabilidad de que el sistema **funcione sin comprometer** la seguridad y sin perjudicar a otros sistemas con los que interactúa.
- **Performabilidad**: probabilidad de que las prestaciones del sistema estén por encima de un cierto nivel en un instante dado. Asociado a la **resistencia a fallos**.
- **Mantenibilidad**: probabilidad de que el sistema averiado pueda volver al estado operacional dentro de un período de tiempo dado. Asociado a su **reparabilidad**.

Suelen ser perceptibles por el usuario. Por ejemplo, si una transacción falla muchas veces, el usuario percibe una baja fiabilidad.
