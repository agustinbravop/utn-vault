*Designing Data-Intensive Applications* es un libro de Kleppmann y Riccomini muy importante.

Una aplicación es ***data-intensitve*** si la gestión de los datos es uno de los principales desafíos al desarrollarla. Se debe pensar en cómo procesar y almacenar grandes volúmenes de datos.

Estas aplicaciones suelen usar building blocks estándar ([[Bases de Datos]], caches, search indexes, stream processing, batch processing) unidos por código de aplicación. La pregunta es: ¿Qué tecnologías usar y cómo combinarlas?

También se debe considerar arquitecturas de [[Data Warehouse]] o [[Análisis de Datos Moderno]] como data lakes.

Hay dos tipos de sistemas con requerimientos diferentes:

- Sistemas operacionales (OLTP).
- Sistemas analíticos (OLAP).

Un *data product* es la salida de sistemas analíticos que es disponibilizada a los sistemas operacionales, y representa una retroalimentación.

## Arquitectura de Sistemas Cloud-Native

La era de la nube se enfoca en:

1. Automatización.
2. Servicios y máquinas virtuales efímeras.
3. Actualizaciones frecuentes.
4. Aprender de los incidentes.
5. Preservar el conocimiento de la organización.

Las nubes introducen el costo por uso, los límites de recursos, y la planificación financiera. Si bien la nube está cambiando el rol de los perfiles de operaciones, la necesidad de operaciones es más grande que nunca debido a los sistemas distribuidos.

Razones para usar un sistema distribuido:

1. Sistemas inherentemente distribuidos.
2. Peticiones entre servicios cloud.
3. [[Alta Disponibilidad]].
4. Escalabilidad.
5. Latencia.
6. Hardware especializado.
7. Compliance (normativas como GDPR, CCPA, etc).
8. Sustentabilidad.

Problemas de un sistema distribuido:

- Posibilidad de fallo en cada petición de red.
- Lentitud de la red.
- Troubleshooting es difícil.
- La consistencia de los datos es difícil.

Almacenamos datos porque su valor es mayor que el costo y riesgo de almacenarlo. Esto implica que algunos datos quizás no valgan la pena almacenar.

Es necesario balancear las necesidades del negocio contra las necesidades de las personas cuyos datos estamos recolectando y procesando.

> "En arquitectura de sistemas no hay soluciones, solo trade-offs." - Thomas Sowell.

Es necesario entender los trade-offs entre:

- OLTP vs OLAP.
- Data warehouse vs Data lake.
- Cloud vs self-hosted.
- Sistemas distribuidos vs una sola máquina.
- Necesidades del negocio vs necesidades de las personas.
