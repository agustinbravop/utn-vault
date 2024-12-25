A partir de una fuente de luz monocromática se puede emplear una barrera que contenga dos pequeñas rendijas para obtener dos fuentes de luz coherentes. Se observa una sucesión de franjas brillantes y oscuras, que corresponden a zonas de [[Interferencia]] constructiva y destructiva respectivamente.

![[Experiencia de Young de la Doble Rendija.png]]

Matemáticamente:

![[Interferencia en la Experiencia de Young de la Doble Rendija.png]]

Supóngase que $L \gt \gt d$ de manera que se puede considerar que $r_1 \parallel r_2$. Se define una *diferencia de camino* $\delta = r_2 - r_1 = d \sin(\theta)$.

- Interferencia constructiva: $\delta = r_2 - r_1 = d \sin(\theta_\text{brillante}) = m\lambda$.
- Interferencia destructiva: $\delta = r_2 - r_1 = d \sin(\theta_\text{oscuro}) = \left( m + \frac{1}{2}\right)\lambda$.

Sea $m$ el *número de orden* (0, $\pm$ 1, $\pm$ 2, ...). Cuando $d \gt \gt \lambda$, se puede considerar un $\theta$ tan pequeño que $\tan \theta = \frac{y}{L} \approx \sin\theta$ y así nos queda:

$$y_\text{brillante} = \frac{\lambda L}{d} m \ ; \ y_\text{oscura} = \frac{\lambda L}{d} \left(m + \frac{1}{2}\right)$$

## Distribución de Intensidad

En el punto $P$ los [[Campo Eléctrico|campos eléctricos]] son $E_1 = E_0 \sin(\omega t)$ y $E_2 = E_0 \sin(\omega t + \phi)$. Se halla la [[Intensidad Luminosa]] para las interferencias constructivas:

$$\begin{align}
\frac{\delta}{\lambda} =\frac{\phi}{2\pi} \implies \phi &= \frac{2\pi}{\lambda}\delta = \frac{2\pi}{\lambda}d \sin(\theta) \\
E_P &= E_1 + E_2 = E_0 [\sin(\omega t) + \sin (\omega t + \phi)] = 2 E_0 \cos\left(\frac{\phi}{2}\right)\sin\left(\omega t + \frac{\phi}{2}\right) \\
I &= \ <I(t)> \ = I_\text{max}\cos^2\left(\frac{\phi}{2}\right) = I_\text{max}\cos^2\left(\frac{\pi}{\lambda} d \sin(\theta) \right) \\
\text{para }\theta\text{ pequeño: } I &= I_\text{max}\cos{ 2\left(\frac{\pi d}{\lambda L}y\right)}
\end{align}$$

## Experimento con Interferencias y Difracción

Ahora también se tiene en cuenta el concepto de la [[Difracción]]:

![[Doble Rendija con Interferencia y Difracción.png]]

Dados $\phi = \frac{2\pi d}{\lambda} \sin\theta$ y $\beta = \frac{2\pi a}{\lambda} \sin\theta$ con una dimensión $d = 4a$. Se cumple que:

$$I = I_\text{max} \cos^2\left(\frac{\phi}{2}\right)\frac{\sin^2\left(\frac{\beta}{2}\right)}{\left(\frac{\beta}{2}\right)^2}$$

## Redes de Difracción

Usando ahora una rejilla de difracción, que es una serie de ranuras paralelas con mismo ancho $a$ y separación $d$ entre ellas:

![[Redes de Difracción.png]]

Las posiciones de los máximos están dadas por $d \sin\theta = m \lambda$ para $m = 0, \pm 1, \pm2, \dots$.
