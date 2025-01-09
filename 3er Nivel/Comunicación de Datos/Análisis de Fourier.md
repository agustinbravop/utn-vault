Cualquier [[Señales y Espectros|señal]] periódica se expresa como una suma de funciones sinusoidales, denominada **serie de Fourier**:

$$\begin{align}x(t) &= \frac{A_0}{2} + \sum_{n=1}^\infty [A_n \cdot \cos(2\pi n f_0 t) + B_n \cdot \sin(2 \pi n f_0 t) \\
A_0 &= \frac{2}{T} \int_0^Y x(t)dt \\
A_n &= \frac{2}{T}\int_0^T x(t)\cdot \cos(2\pi n f_0 t)dt \\
B_n &= \frac{2}{T}\int_0^T x(t)\cdot \sin(2\pi n f_0 t)dt
\end{align}$$

Cuando $A_0 \ne 0$, la señal $x(t)$ tiene una componente continua.

## Representación Amplitud-Fase

Se puede representar una serie de Fourier de una manera alternativa:

$$\begin{align}x(t) &= \frac{C_0}{2} + \sum_{n=1}^\infty C_n \cdot \cos(2 \pi n f_0 t + \theta_n) \\
C_0 &= A_0 \\
C_n &= \sqrt{A^2_n + B^2_n} \\
\theta_n &= \tan ^{-1} \left( \frac{-B_n}{A_n}\right)
\end{align}$$

Para una señal no periódica, el espectro es un continuo de frecuencias y se obtiene mediante la **transformada de Fourier**:

$$x(t) = \int_{-\infty}^\infty X(f) e^{j2\pi ft} df \ ; \ X(f) = \int_{-\infty}^\infty x(t) e^{-j2\pi f t}dt \ ;  \ j = \sqrt{-1}$$
