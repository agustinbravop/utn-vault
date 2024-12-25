La **interferencia** es el fenómeno que sucede cuando dos o más trenes de [[Onda]] se superponen. Una interferencia destructiva anula las ondas, y una constructiva las aumenta.

![[Interferencia.png]]

En la práctica, siempre que la amplitud de la onda no es muy grande, durante la interferencia se cumple el **principio de superposición**: $y = y_1 + y_2$. A los efectos de propagación, cada onda actúa como si la otra no estuviera, de manera que su movimiento no cambia.

Sean dos [[Ondas Electromagnéticas]] $y_1(x, t) = y_m \sin(kx - \omega t)$ y $y_2(x, t) = y_m \sin(kx - \omega t + \phi)$, con $k = \frac{2\pi}{\lambda}$ y $\omega = 2 \pi f$.

$$\begin{align}\text{dado: }\sin A + \sin B = 2 \cos\left(\frac{A-B}{2}\right) \sin\left(\frac{A+B}{2}\right) \\
y_1 + y_2 = y_m[\sin(kx - \omega t) + \sin(kx - \omega t + \phi)] \\
2 y_m \cos\left(\frac{\phi}{2}\right) \sin\left(kx - \omega t + \frac{\phi}{2}\right)
\end{align}$$

Donde se obtiene la amplitud $2 y_m \cos\left(\frac{\phi}{2}\right)$, con misma frecuencia y longitud de onda. 

- Interferencia constructiva: si $\phi = 0 \implies y = y_1 + y_2 = 2 y_m \sin(kx - \omega t)$. Para $\pi$ pares.
- Interferencia destructiva: si $\phi = \pi \implies y = y_1 + y_2 = 0$. Se cumple para $\pi$ impares.

Una fuente es *coherente* a otra fuente si la *diferencia de fase* $\phi$ es constante. Una fuente es *monocromática* si emite luz con una única longitud de onda (un solo color).
