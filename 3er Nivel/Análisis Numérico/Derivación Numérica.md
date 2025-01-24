Los métodos de **derivación numérica** permiten aproximar la derivada de una función en un punto teniendo solo un conjunto de datos experimentales.

Si se tiene el valor real, se puede calcular el *error* de la aproximación de la siguiente manera:

$$E_\text{absoluto} = |V_\text{real} - V_\text{aprox}| \ , \ E_\text{relativo} = \left| \frac{V_r - V_a}{V_r} \right| \ , \ E_\% = |E_r \cdot 100\%$$

Distintos métodos tienen errores mayores o menores, y se busca que sea lo menor posible. A menor error, mejor aproximación.

## Método de Diferencias Finitas

Este método propone aproximar la función por polinomios. $x_0$ es el punto bajo estudio, y $h_i$ es el espaciamiento constante de la tabla de valores experimentales que se posee, tal que $x_{0+1}=x_0+h$.

### Diferencias Finitas hacia Adelante

Primera diferencia:

$$f'(x_0)=\frac{f(x_{0+1}-f(x_0)}{h} \ , \ f''(x_0)=\frac{f(x_{0+2})-2f(x_{0+1})+f(x_0)}{h^2}$$

Segunda diferencia (mejor aproximación):

$$f'(x_0)=\frac{-f(x_2)+4f(x_1)-3f(x_0)}{2h} \ , \ f''(x_0)=\frac{-f(x_3)+4f(x_2)-5f(x_1)+2f(x_0)}{h^2}$$

### Diferencias Finitas hacia Atrás

Primera diferencia:

$$\begin{align}f'(x_0)&=\frac{f(x_0)-f(x_{-1})}{h} \\
f''(x_0)&=\frac{f(x_0)-2f(x_{-1})+f(x_{-2})}{h^2}\end{align}$$

Segunda diferencia:

$$\begin{align}f'(x_0) &=\frac{3f(x_0)-4f(x_{-1})+f(x_{-2})}{2h} \\
f''(x_0)&=\frac{2f(x_0)-5f(x_{-1})+4f(x_{-2})-f(x_{-3})}{h^2}\end{align}$$

### Diferencias Finitas Centrales

Primera diferencia:

$$\begin{align}f'(x_0)&=\frac{f(x_1)-f(x_{-1})}{2h} \\ f''(x_0)&=\frac{f(x_0)-2f(x_{-1})+f(x_{-2})}{h^2}\end{align}$$

Segunda diferencia:

$$\begin{align}f'(x_0)&=\frac{-f(x_2)+8f(x_1)-8f(x_{-1})+f(x_{-2})}{12h} \\
f''(x_0)&=\frac{-f(x_2)+16f(x_1)-30f(x_0)+16f(x_{-1})-f(x_{-2})}{12h^2}\end{align}$$
