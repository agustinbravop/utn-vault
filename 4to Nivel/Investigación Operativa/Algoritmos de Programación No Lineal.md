Los **algoritmos de programación no lineal** son métodos numéricos para resolver problemas de [[Programación No Lineal]] **con computadoras**.

## Algoritmos para Problemas sin Restricciones

### Método de Búsqueda Directa

El **método de búsqueda directa** consiste en identificar el intervalo de incertidumbre con el punto óptimo. Sea $I_{i-1} = (x_L,x_R)$ el intervalo actual de incertidumbre, con $x_L \lt x_1 \lt x_2 \lt x_R$. Para definir el siguiente intervalo $I_i$:

- Si $f(x_1) \gt f(x_2) \implies x_R = x_2, \ I_i = (x_L, x_2)$.
- Si $f(x_1) \lt f(x_2) \implies x_L = x_1, \ I_i = (x_1, x_R)$.
- Si $f(x_1) = f(x_2) \implies x_L = x_1, \ x_R = x_2, \ I_i = (x_1, x_2)$.

Dado un valor pequeño de desplazamiento $\Delta$, hay dos métodos para calcular $x_1$ y $x_2$:

| Método dicótomo                      | Método de la sección dorada                                   |
| ------------------------------------ | ------------------------------------------------------------- |
| $x_1 = \frac{1}{2} (x_R+x_L-\Delta)$ | $x_1 = x_R - \left(\frac{\sqrt{5} - 1}{2}\right) (x_R - x_L)$ |
| $x_2 = \frac{1}{2} (x_R+x_L+\Delta)$ | $x_2 = x_L + \left(\frac{\sqrt{5} - 1}{2}\right) (x_R - x_L)$ |

El método de la sección dorada necesita menos cálculos y converge más rápido (es más eficiente). El algoritmo termina cuando $I_k \le \Delta$, siendo $\Delta$ el _grado de exactitud_ deseado.

### Método del Gradiente

En el método del gradiente o del ascenso más pronunciado, se parte desde un punto inicial $X^0$ y se calcula sucesivamente $X^{k+1} = X^k + r^k \nabla f (X^k)$, siendo $t^k$ el _tamaño de paso_ óptimo en $X^k$ que maximiza el mejoramiento de $f$.

Se debe determinar el $r^k = r$ que maximice $h(r) = f[X^k + r \nabla f (X^k)]$, lo que se puede resolver por búsqueda directa.

El procedimiento termina cuando $X^k \approx X^{k+1}$, lo que es equivalente a $r^k \nabla f (X^k) \approx 0$.

## Algoritmos para Problemas con Restricciones

Lamentablemente para estos problemas no existe un algoritmo general que siempre funcione.

### Programación Separable

Se dice que $f$ es _separable_ $\iff f(x_1, \dots, x_n) = f_1(x_1) + \dots + f_n(x_n)$.

Hay funciones que no son separables pero se pueden hacer separables. Por ejemplo, $z = x_1 x_2$ se puede hacer separable con $y = x_1 x_2$, estando $z=y$ sujeta a $\ln y = \ln x_1 + \ln x_2$.

Se aproxima $f(x) \approx \sum_{k=1}^K f (a_k) t_k$ (siendo $a_k$ los _puntos de quiebre_ del intervalo $[a,b]$ con $a = a_1$ y $b=a_K$), lo que implica $x = \sum_{k=1}^K a_k t_k$, siendo $t_k \ge 0$ un _peso_ al que $\sum_{k=1}^K t_k = 1$.

### Programación Cuadrática

Sea el problema de maximizar $z = CX + X^T D T$ sujeta a $AX \le b$ y $X \ge 0$. La función $X^TDX$ define una **forma cuadrática**.

Si la matriz $D$ es simétrica y negativa definida, entonces $z$ es estrictamente cóncava. Si las restricciones son lineales, entonces el espacio de soluciones es convexo.

Se aplican las condiciones de KKT: sean $\lambda = (\lambda_1, \dots, \lambda_m)^T$ los multiplicadores de Lagrange para $AX - b \le 0 \ \land \ -X \le 0$. Con $U = (\mu_1, \dots, \mu_n)^T$, se llega a:

$$\left(\begin{matrix}-2D & A^T & -I & 0 \\ A & 0 & 0 & I\end{matrix}\right)\left(\begin{matrix}X \\ \lambda \\ U \\ S\end{matrix}\right) = \left(\begin{matrix}C^T \\ b\end{matrix}\right) \ \text{ con } \mu_j x_j = 0 = \lambda_i S_i \ \land \ \lambda, U, X, S \ge 0$$

### Programación Estocástica

La **programación estocástica** resuelve los problemas de optimización de $z = \sum_{j=1}^n c_j x_j$ sujeta a $P\set{\sum_{j=1}^n a_{ij}x_j\le b_i} \ge 1-\alpha_i$, donde $\alpha_i$ son las variables aleatorias $0 \lt \alpha_i \lt 1$.

### Método de Combinaciones Lineales

Con este **método de combinaciones lineales** se busca maximizar $z = f(X)$ sujeta a $AX \le b, X \ge 0$.

Se aproxima $f(X) \approx f(X^k)+\nabla f(X^k)(X-X^k) \implies$ maximizar $w_k(X)=\nabla f(X^k)X$. Se define a $X^{k+1}=(1-r)X^k+rX^*=X^k+r(X^*-X^k)$ como una _combinación lineal_ de $X^k$ y $X^*$. Se determina $r$ maximizando $h(r) = f(X^k + r(X^* - X^k))$.

Repetir hasta que $w_k(X^*)\le w_k(X^k)$.
