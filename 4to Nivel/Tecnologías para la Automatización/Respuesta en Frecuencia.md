La **respuesta en frecuencia** es la respuesta en estado estable de un [[Sistema de Control]] a una entrada senoidal, luego de que todos los efectos transitorios han decaído a cero.

Si a un sistema lineal se le aplica una entrada senoidal, la salida será una señal senoidal de la **misma frecuencia**, aunque puede variar en amplitud y fase. Se definen:

- **Ganancia**: cociente entre la amplitud de la salida y la amplitud de la entrada.
- **Fase**: corrimiento de fase de la senoidal de salida en relación con el de la entrada.

La _respuesta en frecuencia_ del sistema es la variación de la ganancia y fase respecto de la frecuencia.

$$\text{Sea } G(s) = \frac{S_o(s)}{S_i(s)} = \frac{K(s-z_1)(s-z_2)\dots(s-z_m)}{(s-p_1)(s-p_2)\dots(s-p_n)} \implies S_o (s) = \frac{K(s-z_1)\dots(s-z_m)}{(s-p_1)\dots(s-p_n)} S_i(s)$$

Sea $s=jw$ tal que $G(jw)$ es la _función de respuesta en frecuencia_. Se puede hallar $w$ y $k$ a partir del patrón de polos y ceros en un diagrama del plano [[Números Complejos|complejo]]. Además, se cumple que:

$$
\begin{align}|G(jw)|&=\frac{K\cdot (\text{producto de las longitudes de las líneas}) - \text{ceros}}{(\text{producto de las longitudes de las líneas}) - \text{polos}} \\
\angle G(jw)&= \sum \angle\text{ líneas ceros} - \sum \angle \text{ líneas polos}
\end{align}
$$

Se utilizan herramientas gráficas para representar $G(jw)=\frac{|Y(jw)|}{|X(jw)|}$ y $\angle G(jw)=\angle \frac{Y(jw)}{X(jw)}$:

- [[Diagrama de Bode]].
- [[Diagrama de Nyquist]].
