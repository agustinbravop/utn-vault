Un producto de datos o *data product* es una arquitectura para [[Ciencia de Datos]] definida de la siguiente manera:

> A data product is a node on the mesh that encapsulates three structural components (code, data and metadata) required for its function, providing access to the domain's analytical data as a product. - Dehghani

En la práctica, un producto de datos es una "entidad lógica autónoma" que describe datos para su consumo. Esta arquitectura implementa la filosofía de *data as a product*, y descentraliza los sistemas OLAP. Es similar a la idea de microservicios en el desarrollo de software.

Para implementar *data products* conviene separar los *concerns* de datos y tecnología, lo que permite:

- Hacer la arquitectura más costo-eficiente.
- Evitar acoplamiento entre datos y metadatos.

## CQRS

*Command Query Responsibility Segregation* es un patrón de diseño de aplicaciones basado en hacer una copia de los datos para reads intensivos. Como no se usa la misma base de datos para Reads y Writes, se puede escalar Reads o Writes por separado. Esto permite un consumo intensivo de datos.

![[CQRS.png]]

CQRS está muy relacionado al concepto de *materialized views* de [[Bases de Datos]] SQL.

La filosofía de CQRS es construir bases de datos de reads a partir de bases de datos operacionales, y **ofrecer esas *read replicas* como data products**.

## Diseño

Principios de diseño para data products:

- Resource-oriented read-optimized design (clustering data around subject areas).
- Data products and data vaults.
- Data product data is inmutable.
- Using the ubiquitous language (domain oriented).
- Capture directly from the source.
- Clear interoperability standards.
- No raw data (always encapsulate).
- Don't conform to consumers.
- Atomicity.
- Compatibility.

En el diseño a alto nivel de la plataforma, la arquitectura de data product debería tener como mínimo:

- Capacidades para capturar e ingestar datos.
- Capacidades para servir datos a diversos dominios.
- Capacidades de metadatos para gestionar datos.
- Capacidades de data engineering para desarrollar, desplegar y ejecutar el producto de datos.
- Capacidades de [[Gestión de Datos Maestros]] y calidad de datos.
- Capacidades de data marketplace para entregar una experiencia de consumo unificada.

Consideraciones:

- Capacidades para capturar datos.
- Método de ingesta.
- Paquetes de software complejos.
- Proveedores de SaaS y APIs externas.
- Linaje y metadatos.
- Calidad de datos.
- Historización de datos.
- Point-in-time (almacenar datos como referencias históricas).

Consideraciones para implementar una arquitectura de data product end-to-end:

- [[Cloud Computing]] es la infraestructura por defecto.
- Data lakes son una elección popular.
- Es popular procesar con Spark, Python y notebooks.
- Usar servicios extra (ej: dbt) para transformar y modelar datos.
- Es necesario orquestación y automatización de workflows.
- Es recomendado buscar el "modern data stack".
- Los servicios de gestión de metadatos suelen estar fuera de esta arquitectura.

Mejores prácticas para transicionar hacia el desarrollo de data products:

- Comenzar por lo pequeño.
- Crear una definición consistente de lo que un data product significa para la organización.
- La gobernanza es importante pero no urgente.
- Los primeros data products deberían marcar el ejemplo.
- No intentar satisfacer todos los casos de uso a la primera vez.
- Permitir centralización solo por debajo de la descentralización.

Al gestionar los datos como productos y ofrecer los data products como interfaces de dominio, se eliminan dependencias y se separan aplicaciones. La arquitectura de data products se debe diseñar de manera colaborativa y en base a las necesidades de la organización.

Data products y la mentalidad de data-as-a-product tratan de proveer datos. El siguiente paso es [[Transformar Datos en Valor]].
