> El *Ampere* es la intensidad de corriente que circulando por dos conductores rectilíneos de longitud infinita, sección circular y paralelos, separados entre sí un metro en el vacío, producirá una fuerza magnética entre ellos de $2 \times 10^{-7} \ N$ por cada metro de longitud de cada uno de los dos hilos.

Las líneas de campo de un alambre largo y recto por el que circula [[Corriente Eléctrica]] son circunferencias que enlazan el alambre conductor. La **Ley de Ampere** relaciona el [[Campo Magnético]] que rodea al conductor con la corriente enlazada:

![[Ley de Ampere.png]]

$$\oint \vec B \vec {dl} = \oint B dl = B \oint dl = Bl = B (2\pi R) \ \land \ B = \frac{\mu_0 I}{2\pi R} \implies \oint \vec B \vec {dl} = \mu_0 I$$

Donde $I$ es la corriente neta enlazada por la curva cerrada de la integral: $\oint \vec B \vec {dl} = \mu_0 \sum I_{\text{enlazadas}}$.

## Campo Magnético Adentro de un Solenoide

![[Campo Magnético Dentro de un Solenoide.png]]

En el exterior del solenoide se tiene $B =0$. En el interior, $B$ es homogéneo y paralelo al eje del solenoide. Se aplica la Ley de Ampere a la trayectoria cerrada $abcda$:

$$
\begin{align}
\oint \vec B \vec{dl} = \oint_a^b \vec B \vec{dl} + \cancel{\oint_b^c \vec B \vec{dl}} + \cancel{\oint_c^d \vec B \vec{dl}} + \cancel{\oint_d^a \vec B \vec{dl}} = Bd = \mu_0 N I \\
B = \mu_0 \frac{NI}{d} \ \land \ n = \frac{N}{d} \implies B = \mu_0 n I
\end{align}$$

Donde $N$ es el número de espiras que abarca la trayectoria, y $n$ es el número de espiras por unidad de longitud.

## Campo Magnético Adentro de un Toroide

![[Campo Magnético Adentro de un Toroide.png]]

Sea un *toroide* de radio $r$ y $N$ espiras de radio $a$, por el que circula una corriente $I$.

$$\oint \vec B \cdot \vec {ds} = \mu_0 N I = B2 \pi r \implies B = \frac{\mu_0NI}{2\pi r}$$

El campo no es uniforme, sino que depende de $\frac{1}{r}$. Si $r \gt \gt a$, entonces se considera que el campo es aproximadamente homogéneo en el interior del toroide. $r$ es el radio medio del toroide.

## Forma General de la Ley de Ampere

![[Forma General de la Ley de Ampere.png]]

Considerando una corriente no estacionaria $I$ (que varía con el tiempo) que carga un [[Capacitor]]. La [[Cargas Eléctricas]] $Q$ cambia, pero no existe ninguna corriente de conducción entre las placas. Aplicando la ley de ampere:

$$S_1: \oint \vec B \vec{dl} = \mu_0 I \ \land \ S_2: \oint \vec B \vec{dl} = 0 \text{ , pero } \mu_0 I \ne 0 \text{ , entonces?}$$

La ley de Ampere no prevé la existencia de discontinuidades en el circuito. Maxwell resuelve esta situación postulando la existencia de una corriente ficticia llamada *corriente de desplazamiento* $I_d$:

$$I_d = \varepsilon_0 \frac{d\phi_E}{dt} \text{, siendo } \phi_E = \int\vec E \cdot \vec {dA}$$

Se enuncia entonces la **Ley de Ampere-Maxwell**, que establece que las corrientes $I$ e $I_d$ actúan como fuentes del campo magnético, lo que implica que **los campos eléctricos variables producen campos magnéticos**:

$$\oint \vec B \cdot \vec{dl} = \mu_0 (I + I_d) = \mu_0 I + \mu_0 \varepsilon_0 \frac{d \phi_E}{dt}$$

En un capacitor de placas paralelas, siendo el flujo eléctrico $\phi_E = EA$, la corriente de desplazamiento está dada por $I_d = \varepsilon_0 \frac{d\phi_E}{dt} = \varepsilon_0 A \frac{dE}{dt}$.

Forma diferencial de la ley de Ampere-Maxwell:

$$\vec \nabla \times \vec B = \mu_0 \vec J + \mu_0 \varepsilon_0 \frac{\partial \vec E}{\partial t}$$
