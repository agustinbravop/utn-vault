Dada una ecuación característica $a_n s^n ++ a_{n-1}s^{n-1} + \dots + a_0 = 0$, es condición necesaria y suficiente para que todas sus raíces tengan parte real negativa que todos los determinantes $\Delta_1, \Delta_2, \dots, \Delta_n$ sean positivos, donde:

$$\Delta_r = \left|\matrix{a_{n-1} & a_{n-3} & \dots & a_{n-(2r-1)} \\ a_{n} & a_{n-2} & \dots & a_{n-2r} \\ 0 & a_{n-1} & \dots & a_{n-2r-1} \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \dots & a_{n-r}}\right|$$

Donde todas las $a_i$ con subíndice negativo o mayor que $n$ se reemplazan por $0$. Cada $a_i$ es un coeficiente de la ecuación característica. $n$ es el grado de la ecuación característica. $r$ es el número del determinante actual, osea $1 \le r \le n$.

Si se cumple el **criterio de estabilidad de Routh-Hurwitz**, se demuestra la [[Estabilidad]] de un sistema.
