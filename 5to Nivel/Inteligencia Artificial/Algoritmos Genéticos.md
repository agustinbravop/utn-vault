Estos algoritmos de [[Inteligencia Artificial]] están inspirados en la naturaleza (son *bio-inspirados*).

Un algoritmo genético simula la evolución de una **pobación** de individuos mediante un proceso iterativo aplicado sobre un conjunto de estructuras. Cada estructura posee características que definen la **aptitud** del individuo. La aptitud es una medida de cuán buena es la solución que el individuo ofrece para el problema.

Se debe definir:

- La representación de las soluciones en los individuos.
- La función que medirá la aptitud de cada uno de los individuos.

La población de estructuras **evoluciona de generación en generación** aplicando tres **operadores**:

1. **Selección**: mantener los individuos más aptos.
2. **Cruce**: recombinar algunos individuos.
3. **Mutación**: alterar algunas características de algunos pocos individuos.

Algoritmo:

![[Algoritmos Genéticos.png]]

## Selección

Los individuos elegidos aportarán sus *genes* a la generación siguiente. Es conveniente elegir a los mejores individuos según su aptitud. Hay dos tipos de métodos:

- **Métodos proporcionales**.
- **Métodos basados en orden**.

### Selección por Ruleta

Este método probabilístico asigna ranuras de una ruleta a cada individuo de manera proporcional a su aptitud. No garantiza seleccionar al mejor individuo.

### Selección con Control de Capas

Las copias de cada individuo serán:

$$c_i = \frac{f_i}{f}$$

Donde $f_i$ es la aptitud del individuo y $f$ es la aptitud promedio.

### Selección Elitista

Preserva los mejores individuos y no los incluye en el proceso de cruce. Esta selección siempre se usa en combinación con otras variantes.

### Selección por Ranking

No es proporcional para **evitar la convergencia prematura**. Cada individuo recibe una cantidad de copias según su posición al ordenarlos por aptitud. Una implementación puede ser:

$$c=R_{\text{min}} + 2 \frac{(n-i)(1-R_\text{min})}{n-1}$$

Donde $R_\text{min}$ es el número mínimo de copias, $n$ es la cantidad de individuos, e $i$ es la posición del individuo en el ranking.

## Cruce

La población tiene un **tamaño fijo** y se usa el operador de cruce para contribuir a la diversidad de la población. El cruce se realiza sobre pares de estructuras padres para *intercambiar sus genes* y obtener nuevas estructuras hijas.

### Cruce Simple

Combina dos padres según un punto fijo de cruce.

![[Cruce Simple.png]]

### Cruce Multipunto

Se establecen varios puntos de cruce.

![[Cruce Multipunto.png]]

### Cruce Binomial

El aporte de cada padre depende de una probabilidad dada, que es $p$ para el primer padre y $q=\lnot p$ para el segundo padre. Si $p=0.5$ entonces el cruce es **uniforme**. Este cruce es probabilístico.

## Mutación

