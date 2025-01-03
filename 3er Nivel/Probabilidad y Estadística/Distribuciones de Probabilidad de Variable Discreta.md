Una _variable aleatoria_ se considera como una función que asigna un número real a cada resultado de un experimento aleatorio.

Una **distribución de probabilidad** de una variable aleatoria discreta está constituida por el conjunto $(x_1, x_2, \dots, x_N)$ de todos los valores de $X$ asociados con sus correspondientes probabilidades $p_i$ tales que se cumple la _condición de cierre_: $\sum p_i = 1$.

Una distribución de probabilidad es un **sistema completo de sucesos**. Algunas distribuciones de probabilidad para variables aleatorias discretas importantes son:

- [[Distribución Binomial]].
- [[Distribución de Poisson]].
- [[Distribución Hipergeométrica]].

## Función de Distribución

Acumulando las probabilidades se obtiene la función de distribución, análoga a la frecuencia relativa acumulada de los [[Intervalos de Clase]].

$$F(X_u) = P(X \le X_u) = \sum_{i=1}^u p_i = p_1 + p_2 + \dots + p_u$$

![[Distribuciones de Probabilidad de Variable Discreta.png]]

## Esperanza Matemática

La esperanza matemática $E(X)$ representa el número que se espera obtener en promedio.

$$E(X) = \sum_{i=1}^N x_i p_i$$

## Varianza

La [[Medidas de Dispersión|varianza]] de la variable aleatoria es una varianza [[Población|poblacional]].

$$
\begin{align}
V(X) &= \sum_{i=1}^N [x_i - E(X)]^2 \cdot p_i = \sum_{i=1}^N x^2_i p_i - E(X)^2 \\
V(X) &=  \sigma_x^2 \\
DS(X) &= \sigma_x
\end{align}
$$

Siendo $DS(X)$ el desvío estandar.
