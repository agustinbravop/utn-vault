El potencial eléctrico NO es la [[Energía Potencial Eléctrica]]. Es una magnitud escalar que se define como:

$$V = \frac{U}{q_0} \ ; \ [\text{Voltio } V] = \left[ \frac{\text{Joule } J}{\text{Coulomb } C} \right]$$

Para una distribución continua de carga:

$$V(t) = \frac{1}{4 \pi \varepsilon_0} \int \frac{dq}{r}$$

Dado un anillo circular delgado con radio $a$ y una [[Carga Eléctrica]] $Q$ distribuida uniformemente, se determina el potencial eléctrico en e punto $P$ sobre el eje del anillo a una distancia $x$ de su centro:

![[Potencial Eléctrico en un Anillo Circular Delgado.png]]

$$V_p = \frac{1}{4 \pi \varepsilon_0} \int \frac{dq}{r} = \frac{1}{4 \pi \varepsilon_0} \frac{1}{\sqrt{x^2 + a^2}} \int dq = \frac{1}{4 \pi \varepsilon_0} \frac{Q}{\sqrt{x^2 + a^2}}$$

## Diferencia de Potencial

La diferencia de potencial se define a partir de la diferencia de energía potencial:

$$V_b - V_a = \frac{U_a - U_b}{q_0} \text{ pero } \vec F = q_0 \vec E \land \Delta U = - \int _a^b \vec F d \vec l \implies V_B - V_a = - \int_a^b \vec E d \vec l$$

Si $\vec E = cte \implies V = E \times d$.

Si la diferencia de potencial entre dos placas es 6 V, y una carga +1 C se mueve, entonces gana 6 J al ir a los positivos (al subir la energía potencial eléctrica), y pierde 6 J al ir a los negativos.

Dado $V_{ba} = - \int_a^b \vec E d \vec l$, derivando: $- \frac{dV}{dl} = \vec E_l$, se entiende a $\left| \frac{dV}{dl} \right|$ como el gradiente del [[Campo Eléctrico]] $\vec E$ en una dirección particular.

Para determinar el campo eléctrico $E$ conociendo el potencial $V$:

$$\vec E = - \frac{\partial V}{\partial x} \vec i - \frac{\partial V}{\partial y} \vec j - \frac{\partial V}{\partial z} \vec k = - \vec \nabla V \implies \vec E = \vec \nabla V$$

1. **Ecuación diferencial de Gauss**: $\vec \nabla \cdot \vec E = \frac{\rho}{\varepsilon_0}$.
2. **Ecuación de Poisson**: $\nabla^2 V = - \frac{\rho}{\varepsilon_0}$.
3. **Ecuación de Laplace**: $\nabla^2 V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2} = 0$. Se puede usar en coordenadas cartesianas cuando en la zona de trabajo la densidad de carga $\rho$ es nula.

## Superficies Equipotenciales

Una superficie es **equipotencial** si el potencial tiene el mismo valor en todos sus puntos. Sobre una superficie equipotencial, el trabajo realizado es nulo:

$$V_b - V_a = \frac{U_b - U_a}{q_0} = 0 \implies - W_{ba} = \Delta U = 0$$

**Electronvoltio** ($eV$): es la energía que gana o pierde un sistema carga-campo cuando se desplaza una carga de magnitud $e$ (un electrón o un protón) a través de una diferencia de potencial de 1 Volt.

$$1 \ eV = 1.6 \times 10^{-19} \ C \times 1 \ V = 1.6 \times 10^{-19} \ J$$
