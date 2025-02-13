En los [[Modelos para la Información Geográfica]], el **modelo de representación raster** establece una malla coordenada de ***píxeles***.

El modelo raster se centra en las propiedades del espacio por sobre la precisión de la localización. Cada píxel toma el valor de la [[Información Geográfica]] en esa posición.

![[Representación Raster.png]]

**Sistematicidad**: se divide el espacio en unidades mínimas según algún patrón. La posición de una celda depende de las restantes (hay una relación implícita).

La *celda* puede también ser hexagonal o triangular, pero casi siempre es cuadrada. Para definir una [[Capa de Información Geográfica]] raster, se necesita la localización geográfica exacta de solo una celda, y definir una distancia entre celdas, para calcular las coordenadas de las celdas restantes.

La *orientación* habitualmente es Norte-Sur (el norte arriba y el sur abajo de la imagen) para simplificar el trabajo con capas raster dentro del [[Sistema de Información Geográfica]].

La *resolución* o el tamaño de la celda determina la precisión con la que se recoge una variable. A mayor resolución, mayor precisión y nivel de detalle.

Las imágenes (ya sean escaneadas o de un sensor digital) son un caso especial de capa raster. Presentan *bandas* que indican la reflectancia de cierta longitud de onda ([[Fotometría]]). Las imágenes comunes utilizan las tres bandas `rgb`: rojo, verde, y azul.

A diferencia de la [[Representación Vectorial]], en una capa raster las relaciones topológicas vienen implícitas, por lo que tienen una [[Topología]] débil.

## Modelos de Almacenamiento Raster

Una capa raster se modela como una *matriz de datos* que almacena:

1. **Tamaño de celda**: es simple (un valor).
2. **Coordenadas de las celdas**: es simple (un valor).
3. **Valores de las celdas**: es complejo (varios valores enumerados). Listar cada valor es ineficiente, por lo que aparecen técnicas de compresión (con y sin pérdida de información).

Si hay varias bandas, se las puede estructurar de varias maneras:

1. **BSQ**: *Band Sequential*. Ordenado por banda.
2. **BIP**: *Band Interleaved by Pixel*.
3. **BIL**: *Band Interleaved by Lines*.

![[Modelos de Almacenamiento Raster.png]]
