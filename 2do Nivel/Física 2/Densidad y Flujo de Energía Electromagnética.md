Las [[Ondas Electromagnéticas]] transportan energía de una región del espacio a otra. Esta energía esta asociada a los [[Campo Eléctrico|campos eléctricos]] y [[Campo Magnético|campos magnéticos]].

Energía total almacenada por unidad de volumen:

$$u = \frac{1}{2}\varepsilon_0 E^2 + \frac{1}{2} \frac{B^2}{\mu_0}$$

Pero dado que $\frac{E}{B}=c=\frac{1}{\sqrt{\varepsilon_0\mu_0}}$, podemos expresar la densidad de energía en términos del:

1. Campo $E$: $u = \varepsilon_0 E^2 + \frac{1}{2} \frac{\varepsilon_0 \mu0E^2}{\mu_0} = \varepsilon_0 E^2$.
2. Campo $B$: $u = \varepsilon_0 E^2 = \varepsilon_0 c^2 B^2 = \frac{B^2}{\mu_0}$.
3. Ambos: $u = \varepsilon_0 E^2 = \varepsilon_0 E cB \implies u = \sqrt{\frac{\varepsilon_0}{\mu_0}} EB$.

La energía transportada por unidad de tiempo y área es:

$$\begin{align}S = \frac{1}{A}\frac{dU}{dt}\frac{u \ d\text{Vol}}{dt} = \frac{1}{\cancel A}\frac{\varepsilon_0 E^2 \cancel A c \cancel{dt}}{\cancel {dt}} \implies S &= \varepsilon_0 c E^2 \\
\text{pero } c=\frac{1}{\sqrt{\varepsilon_0\mu_0}} \implies S = \cancel \varepsilon_0 c \frac{1}{\sqrt{\cancel \varepsilon_0\mu_0}^2} B^2 = \frac{c B^2}{\mu_0} \implies S &= \frac{EB}{\mu_0} \\
\vec S &= \frac{1}{\mu_0} (\vec E \times \vec B) \  \left[ \frac{\text W}{\text m^2} \right]
\end{align}$$

Con $S$ a lo largo de $\vec v$, es decir $S \perp E \perp B$. Se denomina a $\vec S$ como el *vector de Poynting*, que indica:

1. Dirección en la que se transporta la energía.
2. Dirección de desplazamiento de la onda.
3. Energía transportada por unidad de área y tiempo en un instante.
4. Su módulo da la intensidad de la onda.

Si $E$ y $B$ son sinusoidales, entonces $E^2 = \frac{E^2_{\text{max}}}{2}$.

## Irradiancia

Calculemos el valor promedio de $S$:

$$\overline S = \frac{1}{2}\varepsilon_0 c E^2_0 = \frac{1}{2}\frac{c}{\mu_0}B^2_0 \implies \overline S = \frac{E_0 B_0}{2 \mu_0} = \frac{E_\text{rms} B_\text{rms}}{\mu_0}$$

Donde $\overline S$ es la *irradiancia*, la potencia promedio transferida a través del área unitaria.

## Presión de Radiación

Cuando una superficie $A$ absorbe la energía $U$ de una onda, la onda le transfiere una cantidad de movimiento aplicándole una fuerza $F$. Maxwell demostró que si la superficie absorbe toda la energía, entonces se cumple que $p = \frac{U}{c}$.

$$P = \frac{F}{A} = \frac{1}{A} \frac{dp}{dt} = \frac{1}{Ac}\frac{dU}{dt}=\frac{1}{c} \left[\frac{\frac{dU}{dt}}{A}\right]$$

Una presión $P = \frac{S}{c}$ es propia de un **cuerpo negro**, que absorbe toda la energía. Por otro lado, una **superficie perfectamente reflectora** tiene una presión $P = \frac{2S}{c}$.
