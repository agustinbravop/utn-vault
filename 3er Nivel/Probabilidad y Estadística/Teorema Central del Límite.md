El **teorema central del límite** es uno de los enunciados más importantes de la [[Probabilidad]].

> Sea $X_1, X_2, \dots, X_n$ una secuencia de variables aleatorias independientes distribuidas idénticamente, cada una con media $\mu_X$ y varianza $\sigma^2_X$. La suma de esa secuencia $S_n = \sum X_i = X_1 + X_2 + \dots + X_n$ es una nueva variable aleatoria con una [[Distribución Normal]] aproximada $S_n \sim N(n\mu_X, n \sigma^2_X)$ para un $n$ suficientemente grande.

Si se estandariza $S_n$ de la siguiente manera:

$$Z = \frac{S_n - n\mu_X}{\sqrt{n\sigma_X^2}} = \frac{S_n - n\mu_X}{\sigma_X \sqrt n}$$

Se obtiene una variable aleatoria $Z$ tal que, para un $n$ grande, se cumple:

$$P\left(\frac{S_n - n\mu_X}{\sigma_X \sqrt n}\lt z\right) = P(Z\lt z) = \Phi(z) \ \ \ \forall \ z \in \Bbb R$$

Donde $\Phi(z)$ es la función de distribución $N(0,1)$. Es decir, $n \rightarrow \infty \ \land \ Z \rightarrow N(0,1)$. Si se analiza $Z$:

$$Z = \frac{S_n - n\mu_X}{\sigma_X \sqrt n} = \frac{\frac{1}{n}\sum X_i - \mu_X}{\sigma_X \frac{\sqrt n}{n}} = \frac{\overline X - \mu_X}{\frac{\sigma_X}{\sqrt{n}}} = \frac{\overline X - \mu_\overline X}{\sigma_\overline X} \implies \overline X \sim N(\mu_\overline X, \sigma_\overline X^2)$$

De manera que la distribución de muestreo de $\overline X$ es aproximadamente normal si el tamaño muestral $n$ es grande. En general, se considera que si $n \gt 30$ entonces la aproximación es buena.

![[Teorema Central del Límite.png]]

## Distribución para el Caso de Muestreo sin Reposición

Las conclusiones siguen siendo válidas, excepto que el total de muestras realizables es $\left( N\atop n \right)$. Además, la varianza es diferente:

$$\sigma_\overline X^2 = \frac{\sigma_X^2}{n} \frac{N-n}{n-1}$$

Donde $\frac{N-n}{n-1}$ es un factor de corrección que se acerca a $0$ cuando $N \approx n$. También se cumple que:

$$\overline X \sim N\left(\mu_\overline X, \frac{\sigma^2_X}{n}\frac{N-n}{n-1}\right) \ \ \ \text{si }n \rightarrow \infty$$

## Distribución de Muestreo del Desvío Estándar

$$
\begin{rcases}
E(S_X) = \mu_{S_X} = \sigma_X \\
V(S_X) = \sigma^2_{S_X} = \frac{\sigma^2_X}{2n}
\end{rcases} \implies S_X \sim N\left(\sigma_X, \frac{\sigma^2_X}{2n}\right) \ \ \ \text{si } n \rightarrow\infty
$$

## Resumen

|                            | **Media Poblacional**                      | **Varianza Poblacional**                                                        | **Desvío Estándar Poblacional**                                                              |
| -------------------------- | ------------------------------------------ | ------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| **Media Muestral**         | $E(\overline X) = \mu_\overline X = \mu_X$ | $V(\overline X)=\sigma^2_\overline X = \frac{\sigma^2}{n}$                      | $DS(\overline X) = \sigma_\overline X = \frac{\sigma X}{\sqrt n}$                            |
| **Desvío Estándar**        | $E(S_X) = \mu_{S_X} = \sigma_X$            | $V(S_X) = \sigma^2_{S_X} = \frac{\sigma^2_X}{2n}$                               | $DS(S_X)=\sigma_{S_X}=\frac{\sigma_X}{\sqrt {2n}}$                                           |
| **Media (sin reposición)** | $E(\overline X) = \mu_\overline X = \mu_X$ | $V(\overline X) = \sigma^2_{\overline X} = \frac{\sigma^2_X}{n}\frac{N-n}{N-1}$ | $DS(\overline X) = \sigma_{\overline X} = \frac{\sigma^2_X}{\sqrt n} \sqrt{\frac{N-n}{N-1}}$ |
