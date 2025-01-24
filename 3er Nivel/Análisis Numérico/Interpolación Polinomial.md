La **interpolación polinomial** consiste en determinar el polinomio único de grado $n$ que se ajuste perfectamente a $n+1$ puntos, proporcionando una forma para calcular valores intermedios. Existen varias alternativas para ajustar curvas:

1. Polinomio interpolante.
2. Trazadores.
3. Polinomios trigonométricos.
4. Sumas exponenciales.
5. [[Método de los Mínimos Cuadrados]].

Dado un conjunto de $n+1$ puntos, hay un y solo un polinomio de grado $n$ definido como $f(x) = a_0 + a_1x + \dots + a_nx^n$ que pasa por todos los puntos del conjunto.

Veremos tres métodos para la interpolación.

## Forma de Lagrange

La forma de Lagrange calcula el *polinomio interpolante* de manera explícita.

$$P_n(x) = y_0 L_{n,0} (x) + y_1 L_{n,1} (x) + \dots + y_n L_{n,n} (x) \ \text{ para } \set{(x_0,y_0),(x_1,y_1),\dots,(x_n,y_n)}$$

Donde $L_{n,k}(x)$ se define como:

$$L_{n,k}(x) = \prod_{{i=0} \atop {i\ne k}}^n \frac{x-x_i}{x_k-x_i} = \frac{(x-x_0)(x-x_1)\dots (x-x_{k-1})(x-x_{k+1})\dots (x-x_{n})}{(x_k-x_{0})(x_k-x_{1})\dots (x_k-x_{k-1})(x_k-x_{k+1})\dots (x_k-x_{n})}$$

Para cada punto $(x_i,y_i)$ se pone $y_i$ de coeficiente y se busca $L_{n,i}(x)$ tal que $L_{n,i}(x_i)=1$.

## Diferencias Divididas de Newton

Este método genera sucesivamente *aproximaciones polinómicas* de grado cada vez mayor.

Sean los puntos $(x_0,y_0), (x_1,y_1), \dots, (x_n,y_n)$ con abscisas distintas entre sí, y un polinomio interpolador:

$$P_n(x) = a_0+a_1(x-x_0)+a_2(x-x_0)(x-x_1)+\dots+a_n(x-x_0)\dots(x-x_{n-1})$$

Siendo $a_0 = P_n(x_0)=f(x_0)=f[x_0]$. Por ejemplo, para $a_1$:

$$P_n(x)=f(x_1)=f(x_0)+a_1(x-x_0)\implies a_1=\frac{f(x_1)-f(x_0)}{x_1-x_0} = f[x_0,x_1]$$

En general, para $k=0,\dots,n$:

$$a_k=f[x_0,\dots,x_k]=\frac{f[x_1,\dots,x_k]-f[x_0,\dots,x_{k-1}]}{x_k-x_0}$$

De manera que el polinomio interpolador queda:

$$P_n(x) = f[x_0]+\sum_{k=1}^nf[x_0,\dots,x_k](x-x_0)\dots(x-x_{k-1})$$

La aproximación es *sucesiva* porque se parte de la diferencia dividida de orden cero $f[x_0]=f(x_0)$. Luego, la de orden 1: $f[x_0,x_1]=\frac{f(x_1)-f(x_0)}{x_1-x_0}$. Luego, la de orden 2: $f[x_0,x_1,x_2]=\frac{f[x_1,x_2]-f[x_0,x_1]}{x_2-x_0}$. Y así sucesivamente...

## Trazadores Cúbicos

Los trazadores cúbicos naturales o *cubic splines* se utilizan para crear una *función interpolante* como una unión de polinomios cúbicos, uno para cada intervalo, con derivadas primera y segunda continuas.

Sean $n+1$ puntos $(x_0,y_0)\dots (x_n,y_n)$ con $x_0\lt\dots\lt x_n$, buscamos la función a tramos $f$ que en cada subintervalo $[x_k, x_{k+1}]$ defina un polinomio $S_k(x)$ de grado $\le 3$ de tal manera que los *trazadores* $S_i(x)$ en $[x_i,x_{i+1}]$ y $S_{i++1}(x)$ en $[x_{i+1},x_{i+2}]$ coincidan en $x_{i+1}$ al igual que sus derivadas primera y segunda. Así, el trazador cúbico $S(x)$ será:

$$S(x) \begin{cases}S_0(x) & x \in [x_0, x_1] \\ \ \ \vdots \\ S_{n-1}(x) & x \in [x_{n-1}, x_n] \end{cases}$$

Donde se cumple que:

$$\begin{align}S_i(x)&=a_i+b_i(x-x_i)+c_i(x-x_i)^2+d_i(x-x_i)^3 &\forall \ i=0,1,\dots,n-1 \\
S(x_i)&=y_i &\forall \ i = 0,1,\dots,n \\
S_i(x_{i+1})&=S_{i+1}(x_{i+1}) &\forall \ i = 0,1,\dots,n-2 \\
S_i'(x_{i+1})&=S_{i+1}'(x_{i+1}) &\forall \ i = 0,1,\dots,n-2 \\
S_i''(x_{i+1})&=S_{i+1}''(x_{i+1}) &\forall \ i = 0,1,\dots,n-2 \\
\end{align}$$

Y se satisface una de estas dos condiciones:

- **Frontera libre o natural**: $S''(x_0)=S''(x_n)=0$.
- **Frontera sujeta**: $S'(x_0)=f'(x_0) \ \land \ S'(x_n)=f'(x_n)$.

Para construir el trazador cúbico se buscan los coeficientes $a_i$, $b_i$, $c_i$ y $d_i$ de cada polinomio cúbico $S_i(x)$ a partir de las condiciones que se deben cumplir por definición. Para ello, se resuelve un sistema de ecuaciones $4n \times 4n$.

Los splines cúbicos proporcionan un excelente ajuste a formas complicadas sin requerir cálculos complejos, mientras que los polinomios interpolantes generan interpolaciones con muchas oscilaciones si sucede que hay muchos datos o puntos a interpolar.
