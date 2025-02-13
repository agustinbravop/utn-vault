Los **metadatos** son datos acerca de los datos. En particular, dan un **contexto geoespacial** a la [[Información Geográfica]]. Responden preguntas acerca de los datos:

1. ¿Qué?
2. ¿Por qué? (motivo para usarlos)
3. ¿Cuándo? (fecha de creación)
4. ¿Quién?
5. ¿Dónde?
6. ¿Cómo?

Pueden ser de tipo:

- **Global**: autor, fecha, etc.
- **Espacial**: tipo de [[Capa de Información Geográfica]], geometría, [[Sistema de Referencia de Coordenadas]], etc.
- **Temática**: unidades de medida de las variables, etc.

![[Metadatos para la Información Geográfica.png]]

Los metadatos cumplen dos funciones:

1. Garantizar el uso correcto de los datos.
2. Facilitar la gestión, localización, y consulta de los datos.

A los creadores, los metadatos les sirven para:

1. Evitar duplicaciones.
2. Distribuir información confiable.
3. Publicitar los datos producidos.
4. Reducir la carga de trabajo.

A los usuarios, les sirven para:

1. Encontrar los datos.
2. Facilitar su comprensión e interpretación.

[[Estándares para la Información Geográfica|Estándares]] ISO:

- **ISO 19115**: define cómo describir información geográfica a través de 400+ elementos. Secciones: *Metadata Entity*, *Identification*, *Extent*, *Constraint*, *Distribution*.
- **ISO 19139**: define un esquema de implementación XML para ISO 19115.

Los **perfiles de metadatos** definen qué elementos son opcionales y qué otros son obligatorios. Todos los metadatos de las organizaciones que adoptan un perfil deben cumplir dicho perfil, para lograr *consistencia*.

Los metadatos facilitan la construcción de [[Infraestructuras de Datos Espaciales]].
