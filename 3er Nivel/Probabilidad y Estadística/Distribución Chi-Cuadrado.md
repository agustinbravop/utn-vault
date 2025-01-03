La [[Distribuciones de Probabilidad de Variable Continua|distribución]] **Chi-Cuadrado** se aplica dada una sucesión $Z_1, $Z_2, \dots, Z_n$ de variables aleatorias independientes. Si $Z_i \sim N(0, 1)$:

$$Y = Z_1^2 + \dots + Z_n^2 = \sum_{i=1}^n Z_i^2 = \sum_{i=1}^n \left( \frac{x_i - \mu}{\sigma} \right)^2 \implies Y = \frac{\sum(x_i - \mu)^2}{\sigma^2}$$

Se establece que $Y \sim \chi_n^2$ es la distribución chi-cuadrado con $n$ grados de libertad.

Esta distribución tiene la _propiedad aditiva_: si $Y_1 \sim \chi_{n_1}^2 \ \land \ Y_2 \sim \chi_{n_2}^2 \implies (Y_1 + Y_2) \sim \chi^2_{n_1 + n_2}$.

![[Distribución Chi-Cuadrado.png]]

La distribución $\chi ^2$ tiene asimetría positiva, con $E(\chi^2) = n$ y $V(\chi^2) = 2n$.

Para cualquier $\alpha \in (0, 1)$ el valor $\chi^2_{\alpha, n}$ es tal que $P(Y \le \chi^2_{\alpha, n}) = \alpha$.

![[Densidad de Probabilidad de la Distribución Chi-Cuadrado.png]]

Ahora, sea una muestra aleatoria $X_1, X_2, \dots, X_n$ con variancia $\sigma^2$ distribuida [[Distribución Normal|normalmente]], entonces:

$$\chi^2_v = \frac{\sum_{i=1}^n (X_i - \overline X)^2}{\sigma^2} = \frac{n S^2_X}{\sigma^2} = \frac{(n-1)S^2_c}{\sigma^2}$$

Donde $S^2_c = \frac{n}{n-1} S^2_x$ es la _varianza corregida_ $S_c^2 \sim \chi_v^2$ con $v = n -1$ (un grado de libertad menos).
