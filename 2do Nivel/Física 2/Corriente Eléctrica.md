La corriente eléctrica es la [[Carga Eléctrica]] que atraviesa una sección transversal $S$ en el tiempo $t$:

$$I = \frac{Q}{t} = \frac{dQ}{dt} \ ; \ [\text{Ampere } A] = \frac{[\text{Coulomb } C]}{[\text{segundo}]}$$

El sentido convencional de la corriente eléctrica es opuesto al sentido del movimiento real de los electrones.

| $I$ en Ampere | Efectos                                           |
| ------------- | ------------------------------------------------- |
| 0.001         | Se puede sentir                                   |
| 0.005         | Doloroso                                          |
| 0.010         | Contracciones musculares involuntarias (espasmos) |
| 0.015         | Pérdida del control muscular                      |
| 0.070         | Si pasa por el corazón, trastornos graves         |

## Densidad de Corriente Eléctrica

La densidad de corriente eléctrica $\vec j$ es la corriente eléctrica por unidad de superficie. Es un vector con dirección y sentido iguales al vector superficie.

$$j = \frac{I}{A} \implies I = j A = \int \vec j d \vec A$$

La **velocidad de deriva** $\vec v_d$ es la velocidad a la que se mueve el electrón dentro del conductor. Está relacionada con la corriente macroscópica $I$. La distancia $l = v_d \Delta t$ es la distancia que los electrones viajan en el tiempo $\Delta t$. El volumen $V = Al = A V_d \Delta t$ es el volumen que los electrones atraviesan en el tiempo $\Delta t$. La cantidad de electrones libres por unidad de volumen es $n = \frac{N}{V}$.

La carga total $\Delta Q$ es $\Delta Q = \text{nro cargas N} \times \text{carga por partícula} = (nV)(-e) = -n A v_d \Delta t e$.

La corriente $I$ en el alambre es $I = \frac{\Delta Q}{\Delta t} = - n e A v_d$, y la densidad de corriente $\vec j$ en el alambre es $\vec j = \frac{I}{A} = -ne \vec v_d$.

## Ecuación de Continuidad

Relaciona la densidad de corriente $j$ con la densidad de carga $\rho$. Si la densidad de carga en $V$ es $\rho(x, y, z, t)$, entonces $Q = \int_V \rho (x, y,z,t)dV \ \land \ I = \frac{dQ}{dt} = \int_v \frac{\partial \rho(x,y,z,t)}{\partial t} dV$. Dado que $V$ es arbitrario, se elije uno tal que $\frac{\partial \rho}{\partial t} + \vec \nabla \vec J = 0$.

$$\begin{align}
I = \frac{dQ}{dt} = - \oint \vec J d \vec s = - \int_v \vec \nabla \vec J d V = \int_v \frac{\partial \rho}{\partial t} dV \implies \int_v \left(\frac{\partial \rho}{\partial t} + \vec \nabla \vec J \right) dV = 0 \implies \frac{\partial \rho}{\partial t} + \vec \nabla \vec J &= 0 \\
\vec \nabla \vec J &= - \frac{\partial \rho}{\partial t}
\end{align}
$$

Se deduce que solo hay flujo de corriente eléctrica si la cantidad de carga **varía con el tiempo**.

## Modelo Clásico de un Conductor

![[Modelo Clásico de un Conductor.png]]

$\vec F_e$ es generada por el [[Campo Eléctrico]] $\vec E$. $\vec F_r$ es el rozamiento de $q$ al "chocar" con otras cargas. Dado $\vec F_e = q \vec E$ y $\vec F_r = -k \vec v$, entonces $\vec F = \vec F_e - \vec F_r = q\vec E - k \vec v = m \vec a = m \frac{d\vec v}{dt} \implies \frac{q}{m}E = \frac{dv}{dt} + \frac{k}{m}v$.

Sea $\tau$ el tiempo medio de relajación $\tau = \frac{m}{k}$. Si $t$ es muy grande, entonces $v_{lim} = \frac{qE}{k} = \frac{qE}{m} \tau$.