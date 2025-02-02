La **programación lineal** (PL) es una disciplina dentro de la [[Investigación Operativa]] que trata la planificación de las actividades para obtener un resultado óptimo: el resultado de entre las alternativas de solución que mejor alcance la meta especificada.

Es una **técnica cuantitativa** ampliamente aplicada en sistemas (descritos por un modelo matemático) con relaciones lineales para optimizar el uso de los recursos. Esa mejor manera de usar los **recursos escasos** se logra usando un modelo del sistema llamado *modelo de programación lineal*.

Historia:

1. Las ideas básicas de la PL surgen de un estudio sobre la asignación de recursos de la fuerza aérea de EEUU en la Segunda Guerra Mundial.
2. George Dantzig formula el problema de la programación lineal en 1947.

El problema que concierne a la PL es el uso eficiente de recursos limitados. De las alternativas de soluciones existentes, se busca encontrar la solución óptima. Aún con aplicaciones parciales, se pueden obtener importantes ahorros de costos.

La PL **supone** las propiedades de:

1. Proporcionalidad.
2. Aditividad.
3. Divisibilidad.
4. Certidumbre.
5. Objetivo único.
6. No negatividad.

## Elaboración del Modelo Matemático

¿Qué se produce? ¿Qué se desea calcular? ¿Cuánto producir de qué producto? Para estas respuestas, no existe la producción negativa, por ende la **condición de no negatividad** establece que $X_i \gt 0 \ \forall \ i$.

¿Cuál es el objetivo de la empresa? Todos los varios objetivos se subordinan a un único objetivo: **maximizar ganancias** o **minimizar costos**. Se representa el objetivo con una *función objetivo* que debe ser lineal y única. Se busca maximizar o minimizar el valor de la función objetivo.

¿Cuáles son las **restricciones**? Condicionan los valores que las variables pueden tomar. Una condición con varias variables forma una *ligadura* entre esas variables.

Para plantear el modelo, se usan los 3 pilares de la programación lineal:

1. La condición de no negatividad.
2. La función objetivo.
3. Las restricciones.

Se definen *variables reales* o de decisión, para las cuales se buscará un valor óptimo. También se definen *variables slacks* o de holgura (o de excedente, o surplus), que representan los **recursos ociosos** ("lo que le falta al valor para llegar al máximo" o "lo que el valor está por sobre el mínimo").

Métodos para resolver el modelo:

- **Solución gráfica**: en un papel, resuelve solo hasta dos variables de decisión (dos dimensiones).
- **Método Simplex**: método algebraico para cualquier cantidad de variables de decisión.

Resolver el modelo implica resolver el problema, pero solo si el modelo es fiel a la realidad.

## Solución Gráfica

El método de solución gráfica es sencillo, pero en el plano solo resuelve hasta dos variables reales. 

Ejemplo: sea un taller metalúrgico cuyos equipos usan insumos para fabricar una pieza $A$ con $\$ 4$ de utilidad unitaria y otra pieza $B$ con $\$ 3$. Los recursos se representan en la siguiente tabla:

| Operación | Pieza $A$ | Pieza $B$ | Tiempo Disponible (seg/semana) |
| --------- | --------- | --------- | ------------------------------ |
| Estampado | 3         | 8         | 48000                          |
| Soldado   | 12        | 6         | 42000                          |
| Pintado   | 9         | 9         | 36000                          |

El objetivo es diseñar un programa semanal que maximice las ganancias, por lo que la función objetivo se define como $\text{maximizar } z = 4 x_1 + 3x_2 \ \text{ (\$/semana)}$. Las variables en juego son:

- $x_1$: unidades de piezas $A$ a fabricar por semana (variable de decisión).
- $x_2$: unidades de piezas $B$ a fabricar por semana (variable de decisión).
- $x_3,x_4,x_5$: sobrante de tiempo en segundos por semana para cada operación (variables slack).

Restricciones:

- $x_i \ge 0$: condición de no negatividad.
- $r_1 : \ 3x_1+8x_2 \le 48000 \implies 3x_1+8x_2+x_3=48000$. Las *slacks* pasan restricciones a ecuaciones.
- $r_2 : \ 12x_1+6x_2 \le 42000 \implies 12x_1+6x_2+x_4=42000$.
- $r_3 : \ 9x_1+9x_2 \le 36000 \implies 9x_1+9x_2+x_5=36000$.

Representación gráfica:

![[Programación Lineal.png]]

La *región factible* (área sombreada de rosa) tiene las *soluciones factibles*. Su perímetro es el polígono de *soluciones básicas*, y uno de sus vértices es la *solución óptima*. Vértices:

| Vértice | $(x_1,x_2)$ | $x_3$ | $x_4$ | $x_5$ | $z=4x_1+3x_2$            |
| ------- | ----------- | ----- | ----- | ----- | ------------------------ |
| A       | (0, 0)      | 48000 | 42000 | 36000 | 0                        |
| B       | (0,4000)    | 16000 | 18000 | 0     | 12000                    |
| C       | (3000,1000) | 31000 | 0     | 0     | **15000** (sol. óptima!) |
| D       | (3500, 0)   | 37500 | 0     | 4500  | 14000                    |

La recta azul es la función objetivo para el valor óptima. Rectas paralelas a ella se denominan rectas de *isobeneficio*: la recta de beneficio $z'=0$ indica un beneficio nulo, y la más lejana al origen indica un beneficio máximo.

Solución: fabrique 3000 piezas $A$ y 1000 piezas $B$ para ganar 15000 pesos por semana. Le sobrarán 31000 segundos por semana en la operación de estampado, pero nada en puntado y soldado.

## Método Simplex

El **método Simplex** es un algoritmo iterativo que en cada iteración soluciona un sistema de ecuaciones para obtener una nueva solución a la que se le aplica la prueba de optimalidad. Se detiene cuando la solución es óptima. Sirve para $n$ variables de decisión.

> "La diferencia entre optimizar y *satisfizar* diferencia la teoría de la realidad". - Herbert Simon.

Para el método Simplex es fundamental el uso del computador, para operar con matrices. Cada iteración desplaza la solución a un nuevo vértice del polígono de soluciones factibles que tiene el potencial de mejorar el valor de la función objetivo. El proceso continua hasta que no se pueden obtener mejoras.

Gracias a la función objetivo, se encuentra la **solución básica factible óptima**.

Procedimiento, trabajando sobre una matriz que representa al modelo matemático y suponiendo que se trata de un problema de maximización:

1. **Encontrar la *columna pivot***: seleccionar la variable no básica con el coeficiente de mayor valor absoluto (valor negativo si el problema es de maximización, o valor positivo si el problema es de minimización). Esa variable *entra*.
2. **Encontrar la *fila pivot***: calcular los valores de la columna solución multiplicados por el coeficiente (solo si es mayor a cero) de la columna pivote y de la misma fila. Seleccionar el resultado de menor valor. Esa fila indica la variable que *sale*.
3. Dividir la fila pivote por el elemento pivote de manera que el pivote se vuelva 1. Hacer cero a los valores por encima o por debajo de la misma columna del elemento pivote.
4. Si en la primera fila (la de la función objetivo) no hay coeficientes negativos, entonces esta es la solución óptima. Sino, repetir desde el paso 1.

Este método se basa en resolver un sistema de ecuaciones lineales con el procedimiento de Gauss-Jordan, apoyado en criterios para el cambio de la solución básica hasta que converge a la solución óptima.

Si en cambio se desea minimizar $z$, la condición de parada será que no hayan coeficientes positivos en la fila de la función objetivo. También se puede plantear la maximización de $z^{-1}$.

**Casos especiales** que pueden suceder en un problema de programación lineal:

1. **Problema infactible**: ningún punto satisface todas las restricciones. No hay región factible.
2. **Restricciones redundantes**: dificultan el cálculo. Conviene ignorarlas.
3. **Región no acotada**: siempre hay otro punto más óptimo. Se debe acotar el objetivo.
4. **Múltiples soluciones**: una restricción es paralela a la función objetivo. Múltiples soluciones.
5. **Solución degenerada**: un solo punto cumple todas las restricciones. No se puede optimizar.
