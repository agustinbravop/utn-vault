El **Master Data Management** (MDM) es similar al [[Data Warehouse]] pero tiene un caso de uso diferente:

- Debe ser en tiempo casi real.
- Garantiza que nuevos datos se introduzcan correctamente al inicio. Implica una retroalimentación a las aplicaciones operativas.

Arquitectura MDM:

![[Gestión de Datos Maestros.png]]

MDM permite validar y sincronizar los datos maestros, otorgando una versión única e la verdad. Este es un proceso de la empresa. Ejemplos de entidades de datos maestros:

- **Personas**: clientes, proveedores, empleados.
- **Cosas**: productos, equipamiento.
- **Lugares**: sucursales, líneas eléctricas.
- **Intangibles**: garantías, acciones, contratos.

MDM es importante para:

- Data quality.
- Compliance.
- Mejorar la eficiencia.
- Retener clientes.
- Fusiones y adquisiciones.
- Referencia cruzada.
- Golden records.

En Master Data Services (de SQL Server), los modelos (esquemas) encapsulan a las entidades, atributos y reglas de negocio. Cada miembro es una fila o row.
