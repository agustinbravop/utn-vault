La **difracción** es el fenómeno que se produce cuando las [[Ondas]] alcanzan un obstáculo o apertura (de dimensión comparable a su propia longitud de onda).

![[Difracción.png]]

El **principio de Huygens** dice que todo punto de un frente de onda dado se toma como una fuente puntual que produce ondas esféricas secundarias que se propagan hacia adelante. Luego, la nueva posición del frente de onda es la superficie tangente a los frentes secundarios.

![[Difracción de Fresnel y de Fraunhofer.png]]

Los rayos se consideran paralelos para simplificar los cálculos.

![[Difracción (Cálculos).png]]

Sea $\delta = r_2 - r_1 = \frac{a}{2}\sin\theta$ de manera que la luz en $P$ se cancela ([[Interferencia]] destructiva) cuando $\delta = \frac{a}{2}\sin\theta = \frac{\lambda}{2}$. Si dividimos la pantalla en cuartos, sextos, etc, surge $\sin\theta = \pm 2 \frac{\lambda}{a} \ ; \ \pm 3 \frac{\lambda}{a} \ ; \ \dots$. Se establece la **condición de franja oscura**:

$$\sin\theta = m \frac{\lambda}{a} \ , \text{ para } \ m = \pm 1, \pm 2, \dots$$

Si $\theta$ es pequeño, entonces $\sin \theta \approx \tan\theta \approx \theta \implies \theta = m\frac{\lambda}{a} = \frac{y}{L} \implies y_\text{oscura}=Lm\frac{\lambda}{a}$.

![[Difracción (Arco).png]]

Considerando ahora que el arco es igual al ángulo por el radio:

$$E_0 = \beta R \implies R = \frac{E_0}{\beta} \implies \frac{E_P}{2} = \frac{E_0}{\beta}\sin\left(\frac{\beta}{2}\right) \implies E_P = E_0 \frac{\sin\left(\frac{\beta}{2}\right)}{\left(\frac{\beta}{2}\right)}$$

Se obtiene la **amplitud** $E_P$ para la franja oscura. Conociendo la intensidad:

$$I = I_0 \frac{\sin^2 \left(\frac{\beta}{2}\right)}{\left(\frac{\beta}{2}\right)^2}$$

Ahora:

$$\frac{\lambda}{2\pi} = \frac{\Delta r}{\Delta\varphi} =\frac{a\sin\theta}{\beta} \implies \beta = \frac{2\pi}{\lambda}a\sin\theta=2\pi m \implies I = I_0 \frac{\sin^2 \left(\frac{\pi a \sin\theta}{\lambda}\right)}{\left(\frac{\pi a \sin\theta}{\lambda}\right)^2}$$

![[Difracción (Franjas Sucesivas).png]]
