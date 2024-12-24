Un [[Imanes]] genera un campo magnético. Las líneas de fuerza salen del Norte y se dirigen al Sur. Las líneas de campo son cerradas, de manera que no existen ni fuentes ni sumideros.

![[Campo Magnético.png]]

## Intensidad del Campo Magnético

La intensidad del campo magnético es el valor que toma el campo magnético en cada punto del espacio.  Se define como $\vec B$, con dirección y sentido iguales a las líneas de fuerza.

![[Intensidad del Campo Magnético.png]]

Se define la **fuerza magnética** $F_m$ como $\vec F_m = q (\vec v \times \vec B)$. La dirección y sentido de $F_m$ están dados por $(\vec v \times \vec B)$, según la **regla de la mano derecha**.

$$\vec F_m = q (\vec v \times \vec B) \implies F_m = q v B \sin(\theta) \implies B = \frac{F_m}{q v \sin(\theta)} \ ; \ [\text{Tesla } T] = \frac{[\text{Newton } N]}{[\text{Coulomb } C] \frac{[\text{metro } m]}{[\text{segundos}]}}$$

Conversión de Gauss a Tesla: $1 \ G = 10^{-4} \ T$.

## Movimiento de una Carga

Los campos $\vec E$ y $\vec B$ desvían las trayectorias de las [[Cargas Eléctricas]] en movimiento, pero $\vec F_e$ es paralela al [[Campo Eléctrico]] $\vec E$ y $\vec F_m$ es perpendicular a $\vec v$.

![[Movimiento de una Carga.png]]

$$
\begin{rcases} \vec F_e= q \vec E \\ \vec F_m q \vec v \times \vec B \end{rcases} \
\vec F = \vec F_e + \vec F_m = q ( \vec E + \vec v \times \vec B)
$$

Se conoce a $\vec F = q ( \vec E + \vec v \times \vec B)$ como la **Fuerza de Lorentz**. Ahora, analizando otro caso:

![[Partícula Perpendicular a B Uniforme.png]]

$$F= m a_c \begin{cases} FF = F_B = q v B \\ a_c = \frac{v^2}{r}  \end{cases} \implies qvB = \frac{m v^2}{r} \implies r = \frac{mv}{qB}$$

Se puede calcular el **radio** de la circunferencia con $r = \frac{mv}{qB}$. Ahora, si $v$ forma un ángulo $\theta$ con $B$:

![[V Forma un Ángulo con B.png]]

El vector velocidad puede descomponerse en una componente $v_{\parallel} = v \cos(\theta)$ paralela al campo y otra componente $v_{\perp} = \sin(\theta)$. En el caso de $\theta = 0$, la componente paralela $v_{\parallel}$ no experimenta ninguna fuerza. La componente perpendicular $v_{\perp}$ produce un movimiento circular alrededor de las líneas de campo. Juntas, generan un **movimiento helicoidal**. Se halla:

$$r = \frac{mv_\perp}{qB} = \frac{mv}{qB} \sin(\theta) \ ; \ \Delta x = v_{\parallel} t = v \cos(\theta) t$$

Donde $\Delta x$ es el *paso*.

## Selector de Velocidades

Para que las partículas se muevan más o menos a la misma velocidad, se necesita un campo eléctrico y otro magnético, ambos uniformes y perpendiculares entre sí. Considerando que las ranuras $S_1$ y $S_2$ de un **selector de velocidades** están alineadas:

![[Selector de Velocidades.png]]

$$\vec F_b = q \vec v \times \vec B \ \land \vec F_e = q \vec E \ \land \ \vec F_T = 0 = F_b - F_e \implies \cancel{q} E = \cancel{q} v B \implies v = \frac{E}{B}$$

Las cargas con $v = \frac{E}{B}$ no se desvía, y pasarán por $S_2$. Esto no depende del signo de la carga. Un selector de velocidades sirve para, por ejemplo, construir un **espectrómetro de masas**, un instrumento para medir masas atómicas.

![[Espectrómetro de Masas.png]]

## Fuerza sobre un Conductor con Corriente

Se coloca un alambre recto en el campo magnético entre los polos opuestos de un imán de cerradura. Al fluir una corriente en el alambre, se ejerce una fuerza sobre el alambre. 

![[Fuerza sobre un Conductor con Corriente.png]]

Se descubrió experimentalmente que $F_m \propto IlB\sin(\theta)$. Si la constante de proporcionalidad es 1, entonces se deduce que $F_m = I l B \sin (\theta) \implies F_{ \text{max}} = I l B$. Vectorialmente: $\vec F_m = I \vec l \times \vec B$. Si $B$ no es uniforme, entonces $\vec F_m = \int I d\vec l \times \vec B \ ; \ |\vec F_m| = \int IB \sin(\theta)dl$.

## Acción del Campo Magnético sobre un Circuito Plano

Para un circuito, la fuerza magnética se obtiene integrando a lo largo del circuito.

![[Acción del Campo Magnético sobre un Circuito Plano.png]]

Si $B$ es uniforme: $\vec F = \vec B \oint_C i d\vec l = 0 \implies$ para un circuito general, la $F_m$ es nula. Esto no impide que pueda existir un momento de fuerza sobre el circuito. Considerando ahora $B$ en el plano de la espira de área $A = ab$:

![[Momento Magnético sobre una Espiga.png]]

$$A = ab \ ; \ F_1 = F_3 = 0 \ ; \ F_2 = F_4 = I a B$$

Ahora, si la espiga tiene un punto de apoyo:

![[Espiga con un Punto de Apoyo.png]]

$$\tau_\text{max} = F_2 \frac{b}{2} + F_4 \frac{b}{2} = IaBb \implies \tau_\text{max} = IBA$$

Donde $\tau_\text{max}$ es el *momento de fuerza*. Ahora, si la espiga forma un ángulo $\theta$ con $\vec B$:

![[Espiga forma un Ángulo con B.png]]

Se tiene $-F_2 = F_4$, y se cancelan por estar en la misma recta de acción.

$$\tau = F_1 \frac{a}{2} \sin(\theta) + F_3 \frac{a}{2} \sin\theta = I b B a \sin (\theta) = I A B \sin (\theta) \implies \vec \tau = I \vec A \times \vec B$$

Sea $\vec\mu = I \vec A$ el *momento dipolar magnético*, entonces queda $\vec\tau = \vec\mu \times \vec B \ ; \ |\vec \tau| = \mu B \sin (\theta)$.
