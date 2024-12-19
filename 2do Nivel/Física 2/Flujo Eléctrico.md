El flujo eléctrico es la cantidad de líneas del [[Campo Eléctrico]] que atraviesan una superficie. Hallar el flujo de un campo vectorial $\Phi$ involucra evaluar ese campo vectorial sobre esa superficie. El flujo eléctrico total es la suma del flujo puntual para cada punto de la superficie: $\Phi E_T = \sum_{i=1}^n \Phi E_i$.

$$\Phi E = \oint \vec{E} \ d\vec{A}$$

Dado que $\vec{E} \cdot d \vec{A} = E \cdot dA \cdot \cos(\alpha)$, si $\alpha = 90 \degree \implies \Phi = 0$. Analizando una superficie gaussiana:

![[Superficie Gaussiana.png]]

$$E = k \frac{q}{r^2} \ , \ \Phi_E = \oint E \ dA = E \ \oint dA = E \ 4 \pi r^2 = \frac{1}{\cancel{4 \pi} \varepsilon_0} \frac{q}{\cancel{r^2}} \cancel{4 \pi} \cancel{r^2} = \frac{q}{\varepsilon_0}$$

## Ley de Gauss

Suponiendo simetría perfecta y un campo eléctrico constante para que el campo sea o paralelo o perpendicular a la superficie en cuestión. La **Ley de Gauss** permite hallar la carga neta que la superficie encierra:

$$\Phi_E = \oint \vec E \ d \vec A = \oint E \ dA \cos(\alpha) = \frac{q}{\varepsilon_0}$$

Se deduce que el flujo eléctrico en la esfera no depende del radio de la esfera. Toda línea que entra a la superficie también sale, por ende el flujo neto es **independiente** de la forma de la superficie. El vector superficie $d \vec A$ es normal a la superficie.

Siendo $\rho$ la densidad del volumen $V$, se obtiene la **forma diferencial** de la Ley de Gauss:

$$\oint \vec E d \vec s = \oint \vec \nabla \cdot \vec E dV = \frac{1}{\varepsilon_0} \oint \rho dV \implies \vec\nabla \cdot \vec E = \frac{\rho}{\varepsilon_0}$$
