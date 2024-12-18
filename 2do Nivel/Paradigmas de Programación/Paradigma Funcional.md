Hilbert es un matemático que preguntó si las matemáticas son o no:

1. **Completas**: Gödel formula en 1931 el Teorema de Incompletitud.
2. **Consistentes**: "ningún sistema consistente puede demostrarse a sí mismo".
3. **Decidibles**: Church y Turing descubren paralelamente que no son decidibles.

El [[Cálculo Lambda]] es un sistema formal diseñado para explorar la definición de [[Función|funciones]], las aplicaciones, y la [[Recursividad]]. Esto genera un nuevo [[Paradigma de Programación]].

## Programación Funcional

El modelo funcional puro propone:

1. Programas constituidos únicamente por definiciones de funciones.
2. No hay asignación de variables ni estructuras de iteración.
3. **Funciones puras**: el resultado solo depende de los parámetros de la función.
4. **Funciones de orden superior**: se puede devolver y recibir funciones como parámetro.

La reducción de expresiones se realiza mediante dos reglas:

- Regla de Cálculo o Selección: impaciente o perezosa.
- Regla de Búsqueda: determina la ecuación a utilizar.

Aprovecha la **transparencia referencial**, que se cumple cuando una operación es:

1. **Independiente**: no depende del estado externo a ellas.
2. **Stateless**: no mantiene estado de llamada en llamada.
3. **Determinística**: ante los mismos argumentos, siempre devuelve el mismo valor.

Esto nos permite evitar los efectos colaterales: un _side-effect_ se da cuando un cambio de estado sobrevive a la finalización de una operación. En el paradigma funcional, no hay variables globales.

[[Haskell]] es una implementación del modelo funcional.
