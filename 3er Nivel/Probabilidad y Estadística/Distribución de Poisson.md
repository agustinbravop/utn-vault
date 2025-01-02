La [[Distribuciones de Probabilidad de Variable Discreta|distribución]] **de Poisson** plantea un experimento con $n$ resultados dicotómicos independientes y de probabilidad constante. Las realizaciones del experimento se dan en un intervalo de tiempo continuo, con $n \rightarrow \infty$ y $p \rightarrow 0$. Se recomienda para $n \gt 30$.

Sea $\lambda = np$ y la probabilidad $P = \frac{e^{-\lambda}\lambda^x}{x!}$ que se obtiene al aplicar el límite con $n\rightarrow \infty$ a la [[Distribución Binomial]], y luego se debe desarrollar un poco más.

## Condición de Cierre

$$\sum_{x=0}^\infty \frac{e^{-\lambda}\lambda^x}{x!} = e^{-\lambda} \underbrace{\left[ \frac{\lambda^0}{0!} + \frac{\lambda^1}{1!} + \frac{\lambda^2}{2!} + \dots \right]}_\text{serie igual a $e^\lambda$} = e^{-\lambda} e^\lambda = 1$$

## Esperanza

$$E(x) = \sum_{x=0}^\infty x \ p(x) = \sum_{x=1}^\infty x \frac{e^{-\lambda}\lambda^x}{x!} = \sum_{x=1}^\infty \cancel x \frac{e^{-\lambda}\lambda \ \lambda^{x-1}}{\cancel x (x-1)!} = \lambda \underbrace{\cancel{\sum_{x=0}^\infty \frac{e^{-\lambda}\lambda^x}{x!}}}_\text{=1 (cond de cierre)} \implies E(x) = \lambda = np$$

## Varianza

$$\begin{align}
V(x) &= \sum_{x=0}^\infty x^2 p(x) - E(x)^2 = \sum_{x=0}^\infty x^2 \frac{e^{-\lambda}\lambda^x}{x!} - \lambda^2 \\
\text{reemplazando $x^2$ por $x(x-1)+x$:} \ V(x) &= \sum_{x=0}^\infty [x(x-1)+x] \frac{e^{-\lambda}\lambda^{x}}{x!} - \lambda^2 \\
&= 0 + 0 + \sum_{x=2}^\infty x(x-1)\frac{e^{-\lambda}\lambda^x}{x!}+\lambda-\lambda^2 \\
\text{y transformando $x! = x(x-1)(x-2)!$:} \ V(x) &= \lambda^2 \sum_{x=2}^\infty \frac{e^{-\lambda}\lambda^{x-2}}{(x-2)!} + \lambda - \lambda^2 \\
&= \lambda^2 \underbrace{\cancel{\sum_{x=0}^\infty\frac{e^{-\lambda}\lambda^x}{x!}}}_\text{=1 (cond de cierre)} + \lambda - \lambda^2 \\
&= \cancel{\lambda^2} + \lambda - \cancel{\lambda^2} \\
V(x) &= \lambda
\end{align}$$
