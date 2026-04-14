1. Cada negocio comienza con un sistema transaccional OLTP.
2. Luego el negocio quiere hacer consultas sobre sus datos.
3. Cuando las consultas son complejas podemos escalar la [[Base de Datos]].
4. Pero, cuando algunas preguntas son muy difíciles, no alcanza con solo una BD.
5. Y con mayor cantidad de datos, la complejidad también crece.
6. Y cada vez se generan más datos.

Se necesita **big data** cuando se presentan las 3 Vs:

1. **Volumen**: cantidad de datos.
2. **Variedad**: tipos de datos no estructurados.
3. **Velocidad**: de la generación de datos.

Ahora los datos se almacenan en clusters con escalado horizontal.

Aparecen Hadoop y luego Hive, Spark, Spark SQL, etc. Se pueden usar herramientas open-source pero tener una infraestructura on-premise es muy caro (en mantenimiento y conocimiento). Por esto, aparece cloud computing.

La evolución muestra una tendencia hacia la escalabilidad y flexibilidad:

1. Batch $\longrightarrow$ streaming.
2. On-premise $\longrightarrow$ cloud-native.
3. BI corporativo $\longrightarrow$ análisis autoservice.
4. SQL tradicional $\longrightarrow$ procesamiento distribuido.

Surgen nuevas arquitecturas diferentes al [[Data Warehouse]].

## Data Lake

Un data lake es un data warehouse de datos desorganizados. Es una infraestructura escalable para almacenar datos sin procesar y luego procesarlos. El [[ETL]] se vuelve un ELT.

## Data Lakehouse

Combina DL con DW. Surge de la empresa Databricks. A un data lake se le agrega una capa superior de metadata, cache, e indexado. Esto permite hacer transacciones ACID.

La infraestructura cloud puede volverse muy compleja. Surgen dos empresas que lo simplifican todavía más:

- **Databricks**: Delta Lake y Spark. Foco en analítica y ML. Es más innovadora.
- **Snowflake**: DW tradicional en la nube. Soporta SQL.

Ambas tecnologías se pueden montar en varios cloud providers.
