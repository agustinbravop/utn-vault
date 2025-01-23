La **función de transferencia** de un *sistema lineal invariante en el tiempo* se define como la razón de la [[Transformada de Laplace]] de la salida del sistema a la transformada de Laplace de la entrada del sistema, bajo el supuesto de que todas las condiciones iniciales son cero (el sistema está en un estado de reposo).

![[Función de Transferencia 2025-01-22 16.35.43.excalidraw.svg]]

Sea un sistema lineal invariante en el tiempo caracterizado por una ecuación diferencial de la forma:

$$a_n\frac{d^nx}{dt^n} + a_{n-1}\frac{d^{n-1}x}{dt^{n-1}} + \dots + a_0 x = b_m\frac{d^mu}{dt^m} +  \cdots + b_0u$$

Se aplica Laplace y se obtiene:

$$\begin{align} (a_ns^n + a_{n-1}s^{s-1} + \dots a_0) Y(s) &= (b_ms^m+\dots+b_0)X(s) \\
Y(s) &= \frac{b_ms^m+\dots+b_0}{a_ns^n + \dots a_0} X(s) \\
Y(s) &= \frac{B(s)}{A(s)} X(s)
\end{align}$$

Donde $\frac{B(s)}{A(s)}$ es la función de transferencia del sistema. $A(s) = 0$ es la *ecuación característica* del sistema, y su orden es el *orden* del sistema. Sus raíces son los *polos* de la función de transferencia. Las raíces de $B(s)=0$ son los *ceros* de la función de transferencia.

$$F(s) = \frac{B(s)}{A(s)} = k \frac{(s-z_1)(s-z_2)\dots(s-z_m)}{(s-p_1)(s-p_2)\dots(s-p_n)}$$
