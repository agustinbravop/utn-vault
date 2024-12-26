Sea $\vec F$ una fuerza conservativa, el trabajo que realiza la misma entre los puntos $a$ y $b$ está dado por:

$$W = \int_a^b \vec F d \vec l \implies \Delta U = U_b - U_a = - W_{ab} = - \int_a^b \vec F d \vec l$$

![[Energía Potencial Eléctrica en una Línea.png]]

El trabajo realizado por la fuerza eléctrica para llevar la carga $q_0$ desde el punto $a$ con posición $r_a$ hasta el punto $b$ con posición $r_b$ está dado por:

$$W_{ab} = \int_a^b \vec F d \vec l = q_0 \int_a^b \vec E d \vec l = q_0 \int_a^b E \cos (\theta) dl = \frac{q q_0}{4 \pi \varepsilon_0} \int_{r_a}^{r_b} \frac{dr}{r^2} \implies W_{ab} = \frac{q q_0}{4 \pi \varepsilon_0} \left( \frac{1}{r_a} - \frac{1}{r_b} \right)$$

Debido a que se trata de una fuerza conservativa, cualquier camino curvilíneo genera el mismo trabajo. La **fuerza eléctrica es conservativa** y la variación de la energía potencial eléctrica entre dos puntos es igual al trabajo realizado por la fuerza, cambiado de signo. Es una magnitud escalar que se mide en jules ($J$).

$$\Delta U = U_b - U_a = -W_{a \rightarrow b} = - \int_a^b \vec F d \vec l = \frac{q q_0}{4 \pi \varepsilon_0} \left( \frac{1}{r_b} - \frac{1}{r_a} \right)$$

Es conveniente definir la **energía potencial en un punto** como $U(r) = \frac{q q_0}{4 \pi \varepsilon_0} \frac{1}{r} = - \int_{\infty}^{r} \vec F d \vec l$ para $R_a = \infty; U_a = 0; U_b = 0; r_b = r$.
