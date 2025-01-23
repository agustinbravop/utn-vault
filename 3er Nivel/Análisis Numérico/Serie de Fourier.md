En el [[Análisis de Fourier]], una función $f(t)$ se dice *periódica* de período $T$ si $f(t) = f(t+T) \ \forall \ t$.

- Una función $f(t)$ es *par* $\iff f(-t) = f(t)$. 
- Una función $f((t)$ es *impar* $\iff f(-t)=-f(t)$.

La única función tanto par como impar es $f(x)=0$. Para todas se cumple que:

$$\begin{align}f_\text{par} \cdot f_\text{par} &= f_\text{par} \\
f_\text{impar} \cdot f_\text{impar} &= f_\text{par} \\
f_\text{impar} \cdot f_\text{par} &= f_\text{impar}\end{align}$$

Se define una **serie de Fourier** de la siguiente manera:

$$\begin{align} f(t) &= \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos(n\omega_0t)+b_n \sin (n\omega_0 t)) \\
a_0 &= \frac{2}{T} \int_{-\frac{T}{2}}^\frac{T}{2} f(t)dt \\
a_n &= \frac{2}{T} \int_{-\frac{T}{2}}^\frac{T}{2} f(t) \cos(n\omega_0t)dt \\
b_n &= \frac{2}{T} \int_{-\frac{T}{2}}^\frac{T}{2} f(t) \sin(n\omega_0t)dt \\
\omega_0 &=\frac{2\pi}{T}
\end{align}$$

Si $f(t)$ es par, entonces $b_n = 0$. Si $f(t)$ es impar, entonces $a_0 = a_n = 0$.

## Desarrollo en Semi-intervalos

Una **serie de senos** es simétrica al origen (impar):

$$b_n = \frac{4}{T} \int_{0}^\frac{T}{2} f(t) \sin(n\omega_0t)dt$$

Una **serie de cosenos** es simétrica al eje de las $y$ (par):

$$\begin{align}
a_0 &= \frac{2}{T} \int_{-\frac{T}{2}}^\frac{T}{2} f(t) dt \\
a_0 &= \frac{2}{T} \int_{-\frac{T}{2}}^\frac{T}{2} f(t) \cos(n\omega_0t)dt \\
\end{align}$$

Una serie de Fourier es una mezcla de series de senos con series de cosenos.

Las series de Fourier son útiles para representar señales de manera eficiente.
