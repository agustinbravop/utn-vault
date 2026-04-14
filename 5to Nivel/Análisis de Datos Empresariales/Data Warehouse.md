Los **almacenes de datos empresariales** o *data warehouse* (DW) es un esquema tradicional para el [[Análisis de Datos Empresariales]]. Lleva más de 30 años. Sigue siendo efectivo para PyMEs y empresas nacionales, pero la arquitectura es insuficiente para la [[Big Data]] de multinacionales.

> Un **data warehouse** es un conjunto de datos históricos, integrados, no volátiles, y orientados a la resolución de un problema, para dar soporte a la toma de decisiones. - Inmon

Hay 4 etapas de diseño para procesos OLAP:

1. **Análisis de requerimientos**: orientado a queries. Los requerimientos son las consultas analíticas que los usuarios podrán hacer. Se debe plantear el objetivo principal y dividirlos en sub-objetivos, para plantear consultas que ayuden a analizar cada sub-objetivo.
2. **Diseño conceptual**: modelo multidimensional que deriva en relaciones desnormalizadas.
3. **Diseño lógico**: puede ser relacional, multidimensional, híbrido, etc.
4. **Diseño físico**: foco en las consultas.

Las estructuras de datos se optimizan para queries complejas con un nivel de concurrencia baja. Los usuarios suelen ser gerentes y directivos.

Metodologías de Data Warehouse:

1. **Relacional**: diseño top-down que comprende a la empresa (de Inmon).
2. **[[Modelo Multidimensional]]**: diseño bottom-up que resuelve un problema a la vez (de Kimball).
3. **Data vault**: metodología híbrida enfocada en flexibilidad (de Linsted).

También existe el *método simplificado* que se suele usar para definir KPIs. Buscamos derivar las queries (consultas) a partir de objetivos desglosados en sub-objetivos.

El modelo conceptual resulta ser un gráfico basado en el DER de [[Bases de Datos]].

![[Modelo Conceptual del Data Warehouse.png]]

## Modelo Lógico

El modelo lógico del DW representa los hechos y las dimensiones utilizando el modelo de datos de la base de datos sobre la cual se implementará el DW. Hay 3 alternativas básicas:

1. Relational OLAP (consultas en SQL).
2. Multidimentional OLAP (consultas en MDX).
3. Hybrid OLAP.

## Diseño Relacional de Data Warehouse

Bajo este diseño los hechos y dimensiones se almacenan en tablas. Hay 4 esquemas:

1. **Estrella**: integridad referencial entre hechos y dimensiones. Solo hechos normalizados.
2. **Snowflake**: normaliza tablas de dimensiones para evitar redundancia.
3. **Starflake**: dimensiones normalizadas y desnormalizadas.
4. **Constellation**: como starflake pero con más de una tabla de hechos.

La dimensión tiempo está presente en casi todos los DW. En OLAP se almacena de forma explícita para ganar performance.

## Slowly Changing Dimensions

Un DW es una base de datos histórica, por lo que debe soportar cambios en las dimensiones.

Hay 7 casos de slowly changing dimensions:

1. Las tuplas en la tabla de dimensión se versionan (inspirado en las BD temporales).
2. Solo se necesita guardar el valor actual y el último anterior.
3. Se agrega una columna por cada atributo sujeto a cambios.
4. Se crea una minidimensión que almacena la FK a la tabla de la minidimensión.
5. Como el tipo 4 pero se agrega la FK a la tabla de la minidimensión.
6. Extiende el tipo 2 con una columna que contiene el valor actual del atributo.
7. Similar al tipo 6, agregando una FK a la tabla de hechos.

La tipo 2 es la más común.

![[Slowly Changing Dimensions.png]]

## Diseño Físico Relacional de DW

El diseño físico depende mucho del motor de base de datos elegido. Debe haberse identificado claramente cuáles tablas son hechos y cuáles son dimensiones.

Un servidor que almacena un DW requiere mucha memoria para almacenar índices en RAM. La integridad de los discos no es muy importante, ya que se prioriza la alta performance. Un procesador multi-core dado que los cálculos en un DW son muchos pero no complejos.
