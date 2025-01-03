En la [[Teoría de la Estimación Estadística]], se puede realizar una **estimación puntual**, un procedimiento de estimación en el que se estima el parámetro mediante un solo valor muestral.

Siendo que las estadísticas varían de muestra a muestra pero los parámetros son fijos, se considera $\overline x = \hat \mu_x \ne \mu_x$, donde $\hat \mu_x$ es el *parámetro estimado*.

**Estimador No Viciado**: es aquél cuya esperanza da el parámetro a estimar. Si $E(\overline x) = \mu_x \implies \overline X$ es un estimador no viciado. Como referencia, $M_e$ y $M_o$ sí son estimadores viciados.

$$\begin{align}
E(S^2_x) &= E\left(\frac{1}{n}\sum_{i=1}^n(x_i-\overline x)^2\right) \\
&= \frac{1}{n} \sum_{i=1}^n E((x_i-\mu_x)^2 - E((\overline x - \mu_x)^2) \\
&= \frac{1}{n}\sum\sigma^2_x-\frac{\sigma_x^2}{n} \\
E(S^2_x) &= \sigma^2_x\left(\frac{n-1}{n}\right)\end{align}$$

Se observa que si $n \rightarrow \infty \implies \frac{n-1}{n} \rightarrow 1 \implies$ solo se debe corregir si $n \le 30$ (un $n$ menor a treinta no se lo considera suficientemente grande). Se define una varianza corregida $S_c^2$:

$$S^2_c = \frac{1}{n-1} \sum_{x=1}^n(x_i-\overline x)^2 \implies S^2_c = \frac{n}{n-1}S_x^2$$
