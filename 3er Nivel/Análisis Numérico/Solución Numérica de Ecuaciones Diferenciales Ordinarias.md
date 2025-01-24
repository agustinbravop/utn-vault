Aunque es posible demostrar de forma abstracta que (casi) cualquier ecuación diferencial ordinaria (EDO) posee una solución, al menos localmente, en general resulta muy difícil expresar explícitamente de qué solución se trata. En ingeniería, muchas ecuaciones no poseen soluciones de forma cerrada.

Dado que no siempre es posible expresar la solución de forma implícita o explícita, muchas veces debemos conformarnos con una aproximación, la cual representa a la solución real mediante un conjunto de puntos con cierto margen de error.

Estos métodos numéricos son viables y fáciles de usar gracias a las computadoras, pero jamás deben emplearse de forma aislada. All analizar [[Sistemas Dinámicos]]. un ingeniero debe usar técnicas cualitativas para determinar si la solución del está acotada, si es [[Estabilidad|estable]], si tiene asíntotas, etc.

Los siguientes métodos numéricos requieren que todas las EDOs sean de primer orden, y solo hallan soluciones particulares, por lo que requieren condiciones iniciales explícitas.

## Método de Euler

Sea $y'=f(x,y)$, $y(x_0)=y_0$, y $h\ne 0$, es posible obtener aproximaciones de la solución en los puntos $x_1$, $x_2$, $\dots$, $x_n$, donde $x_i=x_{i-1}+h$, $h=\frac{b-a}{n}$, $i=1,2,\dots,n$, mediante el método *recurrente* de Euler:

$$y_i=y_{i-1}+hf(x_{i-1},y_{i-1})$$

Siendo $(x_0,y_0), (x_1,y_1),\dots,(x_n,y_n)$ los puntos de la solución aproximada.

Se puede definir un error relativo local en el $n$-ésimo paso:

$$\overline E_n = \frac{|y(x_n)-y_n|}{|y(x_n)|}$$

## Método de Euler Mejorado

El método de Euler **mejorado** ofrece un mejor rendimiento. Utilizando las mismas condiciones que el método de Euler original:

$$y_i=y_{i-1}+\frac{h}{2} \left[f(x_{i-1}, y_{i-1})+f(x_i,z_i)\right] \ \text{ con } z_i=y_{i-1}+hf(x_{i-1},y_{i-1})$$

Donde se observa que el valor de $z_i$ se obtiene mediante el método de Euler original.

## Método de Runge-Kutta de Cuarto Orden

Los métodos de Runge-Kutta son una familia de métodos desarrollados por 2 alemanes en 1900. El método de cuarto orden ofrece un muy buen rendimiento:

$$\begin{align}y_i&=y_{i-1}+\frac{1}{6}(p_i+2q_i+2r_i+s_i) \\
\text{Donde: } \ \\
p_i&=f\left(x_{i-1}, y_{i-1}\right)h \\
q_i&=f\left(x_{i-1} + \frac{h}{2}, y_{i-1} + \frac{p_i}{2}\right)h \\
r_i&=f\left(x_{i-1} + \frac{h}{2}, y_{i-1} + \frac{q_i}{2}\right)h \\
s_i&=f\left(x_{i-1} + h, y_{i-1} + r_i\right)h \\
\end{align}$$
