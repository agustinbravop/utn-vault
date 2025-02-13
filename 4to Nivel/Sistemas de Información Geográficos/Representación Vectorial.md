En los [[Modelos para la Información Geográfica]], el **modelo de representación vectorial** codifica las entidades geométricas de una zona de modo explícito mediante puntos, líneas, o polígonos.

La *primitiva geométrica* recoge las propiedades de la componente espacial de la [[Información Geográfica]], y luego se le asocian los valores de la componente temática, por lo que ambas componentes están bien separadas (a diferencia de la [[Representación Raster]]).

En un [[Sistema de Información Geográfica]], una [[Capa de Información Geográfica]] solo puede contener un único tipo de primitiva.

![[Primitivas para la Representación Vectorial.png]]

Todo elemento queda definido por una serie de puntos y valores asociados. Dada la multiplicidad de atributos de la componente temática, se presta a almacenarse en [[Bases de Datos Espaciales]] (generalmente relacionales).

En una capa vectorial, se pueden agregar relaciones de [[Topología]] para facilitar ciertas operaciones.

## Modelos de Almacenamiento Vectorial

Una representación vectorial requiere bajo almacenamiento pero cálculo complejo. Se usan *índices* para reducir el espacio de búsqueda y mejorar el rendimiento del acceso a datos. Hay dos enfoques:

1. **Continuos**: simplifican las coordenadas de las entidades.
2. **Discretos**: discretizan el espacio. Son los más utilizados. Ejemplo: R-Tree.

Los datos espaciales tienen distintas necesidades de indexación. El esquema más utilizado es un R-Tree que almacena los MBR (*Minimum Bounding Rectangle*):

![[Modelos de Almacenamiento Vectorial.png]]
