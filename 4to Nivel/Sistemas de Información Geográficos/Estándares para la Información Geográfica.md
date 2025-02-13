Un _estándar_ es un documento o práctica que busca armonizar aspectos técnicos. La _interoperabilidad_ implica que se puede sustituir unos elementos por otros con la seguridad de que van a poder interaccionar sin dificultades.

Los estándares permiten la interoperabilidad. También:

1. Permiten integración de sistemas.
2. Reducen costos.
3. Fomentan la innovación.

Hay estándares:

- **De facto**: definidos por el mercado. Ej: ESRI Shapefile.
- **"De iure"**: impuestos con carácter legal. Ej: ETAP de la ONTI.
- **Abiertos**: su definición está disponible y es de uso libre.

Los **estándares abiertos** siguen los principios fundamentales de:

1. Disponibilidad.
2. Máxima posibilidad de elección para los usuarios finales.
3. Gratuidad.
4. No discriminación.
5. Extensión o subconjunto.
6. Evitar prácticas predatorias.

Entidades creadoras de estándares:

- **OGC**: _Open Geospatial Consortium_. Es específico para la [[Información Geográfica]].
- **ISO**: _International Standards Organization_.
- **W3C**: _World Wide Web Consortium_.

Estas organizaciones colaboran entre sí.

## Estándares OGC

Estándares OGC para la representación y obtención de información geográfica:

1. **GML**: _Geographic Markup Language_.
2. **WFS**: _Web Feature Services_. Genera representaciones digitales de los datos geográficos vectoriales en GMLL. Tres operaciones: `GetCapabilities`, `DescribeFeatureType`, y `GetFeature`.
3. **SFS**: _Simple Features for SQL_. Define tipos, operaciones, y esquemas para hacer el CRUD de objetos espaciales mediante [[SQL]]. El esquema OGC SFS-SQL define las tablas `GEOMETRY_COLUMNS` y `SPATIAL_REF_SYS`.
4. **FE**: _Filter Encoding_. Para almacenar expresiones de filtrado en XML.
5. **WCS**: _Web Coverage Service_. Genera coberturas (grids) bajo demanda.

Estándares OGC para [[Mapas]] y [[Visualización de la Información Geográfica]]:

1. **WMS**: _Web Map Service_. Genera representaciones digitales de los datos geográficos [[Representación Vectorial|vectoriales]] y [[Representación Raster|raster]] en formato imagen, lo cual es muy conveniente. Tres operaciones: `GetCapabilities`, `GetMap`, y `GetFeatureInfo`.
2. **WMTS**: _Web Map Tile Service_. Es muy similar a WMS. Tres operaciones: `GetCapabilities`, `GetTile`, `GetFeatureInfo`.
3. **SLS**: _Styled Layer Description_. Define cómo almacenar parámetros de representación. Está basado en XML.

Estándares OGC para procesamiento:

1. **WPS**: _Web Processing Service_. Es poco utilizado, pero existe. El dueño del servicio define los procesos. Tres operaciones: `GetCapabilities`, `DescribeProcesss`, y `Execute`.

Estándares OGC para [[Metadatos para la Información Geográfica]]:

1. **CSW**: _Catalogue Services for the Web_. Permite la publicación y acceso a catálogos de metadatos para datos. Operaciones: `GetCapabilities`, `DescribeRecord`, `GetRecords`, `GetRecordsById`, y `Transaction`.
