La **transformada de Laplace** transforma una función $f(t)$ en $F(s)$, de forma que es un **operador lineal**. Se define como:

$$L[f(t)] = F(s) = \int_0^\infty f(t) e^{-st}dt$$

Se utilizan tablas para las transformadas de funciones típicas. Ejemplos:

$$L[c]=\int_0^\infty c \cdot e^{-st}dt = \lim_{b \rightarrow \infty} \int_0^b c \cdot e^{-st}dt = \lim_{b \rightarrow \infty} \left(-\frac{c}{s}(e^{-sb}-1)\right) = -0+\frac{c}{s} = \frac{c}{s} \ \ \ \ \ \text{ para $s \gt 0$}$$

Transformada de una derivada:

$$L[f^{(n)}(t)]=s^nF(s) - s^{n-1} f(0) - s^{n-2}f'(0) - \dots - f^{(n-1)}(0)$$

Transformada de una integral:

$$L[\int_0^\infty f(t)dt]=\frac1s\int_0^\infty f(t) \cdot e^{-st} dt = \frac 1s\cdot F(s)$$

Derivada de la transformada:

$$L[t^nf(t)] = (-1)^n F^{(n)}(s) = (-1)^n \frac{d^n}{dt^n}L[f(t)]$$

Integral de la transformada:

$$\int_s^\infty F(u) du=L\left[\frac{f(t)}{t}\right]$$

## Producto de Transformadas

Sean $f$ y $g$ funciones continuas por partes en $[0, +\infty)$ para las cuales existen sus transformadas de Laplace $F$ y $G$. Se verifica que $L[f * g] = F(s) \cdot G(s)$, aplicando el _producto de convolución_ de $f$ y $g$:

$$f * g = \int_0^t f(\tau) g (t-\tau)d\tau$$

De manera que la transformada del producto de convolución es el producto de las transformadas.

## Transformada Inversa de Laplace

Si $L[f(t)]=F(s)$ es la transformada de Laplace, entonces se dice que $f(t)$ es la **transformada inversa de Laplace**.

Cumple ciertas propiedades:

1. **Pluralidad**: $L^{-1}$ es un operador lineal. $L^{-1}[af(s)+bg(s)] = a L^{-1}[f(s)] + b L^{-1}[g(s)]$.
2. **Primera propiedad de traslación**: $L^{-1}[f(s-a)]=e^{at}\cdot F(t)$.
3. **Segunda propiedad de traslación**: $L^{-1}[e^{-as} f(s)] = \begin{cases} F(t-a) & t \gt a \\ 0 & t \lt a \end{cases}$.
4. **Propiedad del cambio de escala**: $L^{-1}[f(ks)] = \frac{1}{k} F\left(\frac{t}{k}\right)$.
5. $L^{-1}[f^(n)(s)] = (-1)^n t^n F(t)$.
6. $L^{-1}[\int f(u)du] = \frac{F(t)}{t}$.
7. $L^{-1}[s f(s)] = F'(t) + F(0) \cdot \delta (t)$, donde $\delta(t)$ es el _impulso unitario_ o _función delta de Dirac_.
