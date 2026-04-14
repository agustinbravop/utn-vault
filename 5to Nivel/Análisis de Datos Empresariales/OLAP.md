Arquitectura de un [[Data Warehouse]]:

![[Análisis de Datos.png]]

Un servidor OLAP expone los datos del DW en forma multidimensional. El [[Modelo Multidimensional]] modela al problema como un conjunto de hechos y dimensiones (que se usan para sumarizar los hechos). Se debe indicar una jerarquía de agregación para las dimensiones, es decir, deben estar normalizadas.

Una *consulta* consiste en obtener *medidas* sobre los *hechos* parametrizados por atributos de las *dimensiones* y restringidas por *condiciones* impuestas sobre las dimensiones.

## Cubo de Datos

El *data cube* de $n$ dimensiones calcula una métrica para cada celda o fact. La granularidad del data cube no debe ser la más fina. El cubo base está compuesto por los niveles inferiores de las jerarquías de las dimensiones.

**Operaciones OLAP** con el cubo de datos:

1. **Roll-up**: sumariza un cubo a lo largo de una dimensión hasta un nivel.
   ![[Roll-up.png]]
2. **Drill-down**: desagrega un cubo (inverso al roll-up).
   ![[Drill-down.png]]
3. **Dice**: obtiene un subcubo que satisface una condición booleana.
   ![[Dice.png]]
4. **Slice**: elimina una dimensión del cubo.
   ![[Slice.png]]
