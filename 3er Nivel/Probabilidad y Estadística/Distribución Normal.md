La [[Distribuciones de Probabilidad de Variable Continua|distribución]] **normal** o de **Gauss-Laplace**:

$$f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$$

Para $-\infty \lt x \lt \infty$, $E(x) = \mu$, $V(x) = \sigma^2$.

![[Distribución Normal.png]]

En la práctica no se calculan las probabilidades, sino que se utiliza una tabla de la **variable estandarizada** $z$:

$$z = \frac{x-\mu_x}{\sigma_x} \text{ tal que } f(z) = \frac{1}{\sqrt{2\pi}} e^{-\frac{z^2}{2}}$$

Los valores en esta tabla se pueden buscar de manera *directa* o de manera *inversa*.

Se calcula la esperanza $E(z) = \overline z = E_z = \mu_z$:

$$E(z) = E\left( \frac{x-\mu_x}{\sigma_x}\right) = \frac{1}{\sigma_x} \underbrace{ [E(x) - \mu_x]}_{E(x)=\mu_x \implies 0} \implies E(z) = 0$$

Ahora, la varianza $V(z)$:

$$V(z) = E((z-E(z))^2) = E(z)^2 = E \left[\frac{(x-\mu_x)^2}{\sigma^2_x}\right] = \frac{1}{\sigma_x^2} E\left[ (x-E(x))^2 \right] = \frac{\cancel{\sigma_x^2}}{\cancel {\sigma_x^2}} \implies V(z) = 1$$ 