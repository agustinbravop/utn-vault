En la **integración numérica**, se aproxima el área bajo la curva de una función difícil de integrar o definida por un conjunto de puntos. 

Las reglas del trapecio y de Simpson ($1/3$ y $3/8$) son las fórmulas de Newton-Cotes, y son los métodos de integración numérica que analizaremos.

## Regla del Trapecio

Sea $f$ continua en $[a;b]$ y $I=\int_a^b f(x)dx \approx \int_a^bf_1(x)dx$, siendo $f_1$ un [[Interpolación Polinomial#Forma de Lagrange|polinomio de Lagrange]] de grado 1.

$$I \approx (b-a)\frac{f(a)+f(b)}{2} \ \text{ con un error } E_1(\varepsilon)=-\frac{1}{12}f''(\varepsilon)(b-a)^3$$

Si hubiesen **intervalos múltiples**, suponiendo que sobre $[a;b]$ hay $n+1$ puntos igualmente espaciados:

$$I \approx \frac{(b-a)}{2n}\left[f(x_0)+2\sum_{i=1}^{n-1}f(x_i)+f(x_n) \right] \ \text{ con un error } E \le \left|\frac{(b-a)h^2}{12}f''(\varepsilon)\right|$$

## Regla de Simpson de $1/3$

La regla de Simpson de $1/3$ o la **regla de las parábolas** subdivide a $[a;b]$ en $n$ subintervalos (pares) y cada conjunto de dos de ellos se aproxima por una parábola.

$$\begin{align}A &= \frac{h}{3} (E+4I+P) \\
E &= y_0 + y_n \\
I &= y_1 + y_3 + \dots + y_{n-1} \\
p &= y_2 + y_4 + \dots + y_{n-2} \\
\text{Error} &\le \left| \frac{(a-b)}{180}h^4f^{(4)}(\varphi)\right| \ \text{ con } \varphi \in [a;b]
\end{align}$$

## Regla de Simpson de $3/8$

La regla de Simpson de $3/8$ aproxima la función con un polinomio de Lagrange de tercer grado.

$$\begin{align}A &= \frac{3}{8} h [f(x_0)+3f(x_1)+3f(x_2)+f(x_3)] \ \text{ con } h = \frac{b-a}{3} \\
\text{Error} &\le \left|\frac{(a-b)}{80}h^4f^{(4)}(\varepsilon)\right| \ \text{ con } a\lt \varepsilon \lt b
\end{align}$$

Se considera que es una mejor aproximación que (o un refinamiento sobre) la regla de Simpson de $1/3$.
