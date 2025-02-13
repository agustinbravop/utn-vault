La **topología** en los [[Modelos para la Información Geográfica]] es un conjunto de _relaciones espaciales_ que se establecen por el hecho de que una entidad geográfica tenga una **posición** que la relaciona con otras.

Estas relaciones pueden ser obvias para el ser humano, pero un [[Sistema de Información Geográfica]] las debe establecer mediante un lenguaje y reglas específicas.

Una [[Capa de Información Geográfica]] tiene topología si almacena de algún modo estas relaciones. En caso contrario, la capa es de tipo puramente cartográfico. Según el tipo de capa:

- [[Representación Raster]]: las relaciones topológicas vienen implícitas.
- [[Representación Vectorial]]: se registran las relaciones topológicas de modo **explícito**.

Las _relaciones topológicas_ son importantes porque permiten automatizar procesos de análisis o edición de datos geográficos. Para lograr la _consistencia topológica_ es necesaria una validación y corrección topológica de la información gráfica.

Existen herramientas para la rectificación de los errores de topografía.

**Errores de topografía** que pueden provocar una edición incorrecta de los datos:

1. **Solapamiento**: superposición de dos bordes.
2. **Arcos colgantes**: sub-trazos y sobre-trazos al intersectar líneas.
3. **Slivers**: astillas generadas por el cruce de dos polígonos que no coinciden.
4. **Cruces**: límites de un polígono que se cruzan.

![[Errores de Topología.png]]

Relaciones topológicas importantes:

1. **Contigüidad o adyacencia**: polígonos que comparten parte de su entorno.
2. **Conectividad**: un arco (entidad) está conectado a otro si comparten un nodo.
3. **Inclusión**: permite determinar qué entidades se encuentran dentro de otras.
4. **Proximidad**: permite el cálculo analítico de la proximidad de dos entidades.

![[Relaciones Topológicas.png]]

Algunas propiedades topológicas pueden calcularse, pero otras no.

Un modelo vectorial sin topología ("_spagetti_") es más simple, ya que solo recoge las propiedades geométricas de cada unidad. Para agregar topología, se requiere un almacenamiento explícito. Hay dos estrategias:

- **DIME**: _Dual Independent Map Encoding_ (de 1967). Cada línea recta entre dos puntos se trata como una unidad.
- **Arco-Nodo**: es el más popular. Un _arco_ es una sucesión de segmentos rectos. Un _vértice_ es un punto que solo pertenece a una entidad. Un _nodo_ son puntos iniciales y finales de un arco, o si conectan 3 o más arcos. Los _polígonos adyacentes_ comparten uno o más arcos.

![[Modelo Vectorial con Topología.png]]
