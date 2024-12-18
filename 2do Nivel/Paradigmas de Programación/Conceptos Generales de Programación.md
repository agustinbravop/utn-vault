## Valor

Un **valor** es algo que se puede evaluar, almacenar, retornar, pasar como argumento, etc. Puede ser:

- **Simple o primitivo**: un `int`, `char`, `boolean`, `NULL`, puntero, etc. Son indivisibles.
- **Compuesto**: un [[Arreglo]], [[Lista]], [[Árbol]], [[Registro]]. Se componen de otros valores.

## Tipo

Un **tipo** es un conjunto de valores con un **comportamiento uniforme** y propiedades en común. La notación $v \in T$ indica que el valor $v$ pertenece al tipo $T$.

## Cardinalidad

La cardinalidad es la cantidad de valores distintos de un tipo. $\#T$ es la cardinalidad del tipo $T$.

## Producto Cartesiano

$$U = S \times T = \set{(x, y) / x \in S; \ y \in T} \implies \#U = \# (S \times T) = \#S \times \#T$$

## Unión Disjunta

$$U = S + T = \set{izq \ x / x \in S} \cup \set{der\ y / y \in T} \implies \#U = \# (S + T) = \#S + \#T$$

## Mapeo

Se **mapea** de un tipo al otro: $M = S \rightarrow T = \set{m / x \in S \implies m (x) \in T}$. Por ejemplo, una estructura `puesto: array[medalla] of 1..3` representa un mapeo `medalla -> {1, 2, 3}`.
