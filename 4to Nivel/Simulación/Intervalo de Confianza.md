Después de ejecutar una [[Simulación]] varias veces, se tiene un conjunto de resultados. Los resultados varían por cada corrida porque entre corrida y corrida cambian los [[Números Pseudoaleatorios]] utilizados.

Para sacar una conclusión estadísticamente válida según la [[Teoría de la Decisión Estadística]], no se puede simplemente utilizar el [[Medidas de Posición|promedio]] o mediana de los resultados, sino que debemos usar un **intervalo de confianza**.

Intervalo de confianza para una [[Distribución Normal]], utilizando la [[Distribución t de Student|t de Student]] con un nivel de confianza $\alpha$:

$$IC = \left[ \overline x - \frac{s}{\sqrt r}(t_{\alpha / 2, \ r-1}),\ \overline x + \frac{s}{\sqrt r}(t_{\alpha / 2, \ r-1})\right]$$

Intervalo de confianza para otra distribución (genérico):

$$IC = \left[ \overline x - \frac{s}{\sqrt {r \alpha}}, \ \overline x + \frac{s}{\sqrt {r \alpha}}\right]$$

Se puede usar un software de bondad de ajuste como _StatFit_ para encontrar la distribución que mejor explica el conjunto de resultados de la simulación. Se acostumbra usar un nivel de confianza $\alpha$ igual a $0.05$ (un $5\%$ de probabilidad de cometer un falso negativo).

El intervalo de confianza tendrá un límite inferior y un límite superior, estando el promedio del conjunto de valores entre ambos límites. El _delta del intervalo_ o rango del entorno es la distancia entre los límites y el punto medio.

El resultado exacto se encuentra dentro del intervalo.
