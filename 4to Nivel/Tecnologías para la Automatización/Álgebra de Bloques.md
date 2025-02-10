El **álgebra de bloques** es el conjunto de reglas que rige el reemplazo de un conjunto de bloques funcionales por otro, manteniendo la funcionalidad del [[Diagrama de Bloques Funcionales]].

![[Álgebra de Bloques.png]]

Para aplicar las transformaciones, se asume que el [[Sistema de Control]] es lineal.

Algunos ejemplos de **operaciones básicas** con bloques funcionales que permiten **simplificar el sistema**:

![[Reglas del Álgebra de Bloques.png]]

## Sistemas con Entradas Múltiples

En general, los SC tienen más de una entrada. Para considerarlos desde la [[Teoría de Control]] clásica:

1. Considerar de a una las entradas, haciendo nulas a las demás.
2. Transformar el diagrama de bloques funcionales resultante a uno con una trayectoria directa y una de retroalimentación.
3. Tallar la salida del sistema provocada por la entrada analizada.
4. Repetir para cada señal de entrada.
5. Calcular la salida final como la suma algebraica de las salidas individuales provocadas por cada entrada.
