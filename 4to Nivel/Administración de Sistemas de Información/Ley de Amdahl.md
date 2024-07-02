Esta ley representa el **incremento de prestaciones** obtenido en un sistema como consecuencia de la **mejora** de una o varias de sus **partes**.

![[Ley de Amdahl.png]]

Del gráfico se interpretan los tiempos de ejecución $T_{original}$ y $T_{mejorado}$.
$$T_{original} = T_{original} (1-f) + T_{original}* f$$
$$T_{mejorado} = T_{original} (1-f) + T_{original}* \frac{f}{k}$$

Si se divide entre ellos se llega a la **ley de Amdahl**.
$$\frac{T_{original}}{T_{mejorado}} = A = \frac{1}{1-f+\frac{f}{k}}$$

Observaciones:

- Si $f = 0 \implies A = 1$: si el componente mejorado no se usa, no hay aceleración.
- Si $f = 1 \implies A = k$: si solo se usa el componente mejorado, la aceleración es igual a la mejora del componente.
