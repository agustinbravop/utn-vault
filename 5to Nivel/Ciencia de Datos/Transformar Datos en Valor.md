Un [[Producto de Datos]] también debe ser consumido. Los casos de uso suelen necesitar datos de diferentes dominios y por ende diferentes data products. Cada problema de negocio tiene sus propios requerimientos y contexto.

Para evitar que algunos usuarios de negocio descarrilen la arquitectura de gestión de datos y la vuelvan un caos, es necesario crear entornos controlados que se integran profundamente con los servicios de gestión de datos y apoyar el modelo federado de muchos dominios de negocio, mientras se atacan las necesidades de usuarios.

![[Transformar Datos en Valor.png]]

Los data products están diseñados para entregar grandes volúmenes de data inmutable. Aplicaciones de consumidores usan los data products de manera directa como fuentes de datos. Siempre se requiere un paso de transformación hacia un formato específico del consumidor.

## Domain Data Stores

Domain Data Stores (DDS) almacenan y gestionan datos recientemente creados que se necesita para facilitar el uso de caso del consumidor. En este nivel, la data se puede clasificar como:

- **Copied data**: misma semántica que la data original del data product.
- **Integrated data**: transformada en un nuevo contexto.
- **Newly created data product data**: data integrada que será disponibilizada.

Un DDS puede ser consumidor de datos y proveedor de datos al mismo tiempo. 

Consideraciones de los DDS:

- Granularidad de casos de uso alineados por el consumidor.
- DDS vs data product.
- Requerimientos de negocio.
- Audiencia objetivo y modelo de operación.
- Requerimientos no funcionales.
- Data pipelines y data models.
- Pipelines SQL vs NoSQL.
- Acotando el rol de los DDS.
- [[Data Warehouse|Inmon vs Kimball vs data vault]].

## Business Intelligence

Herramientas de [[Inteligencia Empresarial]] (BI) ayudan a tomar una mirada estructurada de la data.

Las *capas semánticas* (semantic layers) son representaciones de datos que ayudan a los end users a acceder datos de manera autónoma mediante términos comunes de negocio. Beneficios de una semantic layer:

- Facilita que los usuarios consulten los datos.
- Pueden tener funcionalidades extra.
- Pueden construirse con virtualización de datos para esconder detalles de implementación.

La mayoría de herramientas de BI te permiten construir semantic layers. 

Los **datos gestionados** sirven para necesidades de negocio recurrentes, y se automatizan y estandarizan. Los **datos self-service** es para análisis ad hoc o de una sola vez.

Mejores prácticas para BI:

- Tomar decisiones efectivas sobre la estrategia de BI.
- Desarrollar playbooks y patrones de diseño para ayudar a los usuarios.
- Considerar establecer un centro de excelencia.
- Usar niveles de madurez para guiar las condiciones en las que BI se puede usar.
- Desarrollar una red de "campeones" (expertos reconocidos dentro de la organización).
- Requerir que los dominios muestren un reporte de ejemplo de la data que proveen.

## MLOps

Desplegar modelos de [[Inteligencia Artificial]] a producción es un desafío porque:

- Los modelos dependen mucho de las **pipelines** de datos.
- Muchos modelos se construyen en un entorno *sandbox* sin **escalabilidad** en mente.
- Producción necesita que todo esté monitoreado, evaluado y auditado.

El **framework MLOps** puede ayudar a organizaciones para *streamlinear* el proceso de desplegar modelos de machine learning a producción. Un buen proceso de MLOps puede ser perfectamente alineado con un modo de trabajo federado, y se posiciona bien en una arquitectura de [[Data Mesh]].

Pasos de MLOps:

1. Iniciar un proyecto.
2. Experimentación y tracking.
3. Data engineering.
4. Operacionalización del modelo (la parte más difícil).

Mejores prácticas para transformar datos en valor:

- Establecer una comunidad de modelado de datos.
- Guiar a los equipos.
- Alinear patrones de consumo analítico.
- Trabajar con equipos de operación.
