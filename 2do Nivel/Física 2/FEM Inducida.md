De la [[Ley de Faraday y Ley de Lenz]] surge una [[Fuentes de Fuerza Electromotriz|fem]] inducida. Su sentido siempre se opone al cambio original en el [[Flujo Magnético]] que la produjo, y su valor es el siguiente:

$$\varepsilon = -N \frac{d\phi_B}{dt}$$

Siendo $\phi_B = \int B \cos (\theta) dA$, va a haber [[Corriente Eléctrica]] siempre que varíe $B$, $\theta$, o $A$.

## Cálculo de la FEM Inducida

Sean $N$ espiras de área $A$ rotando con velocidad angular $\omega$ constante en un [[Campo Magnético]] $B$.

![[Cálculo de la FEM Inducida.png]]

$$
\begin{align}
\phi_B = \vec B \cdot \vec A = BA\cos\theta \ \land \ \omega = \frac{d\theta}{dt} \implies \theta = \theta_0 + \omega t \implies \phi_B = BA \cos(\omega t) \\
\frac{d\phi_B}{dt} = BA \ \omega \sin(\omega t) \implies \varepsilon = -N \frac{d\phi_B}{dt} = N B A \ \omega \sin(\omega t) \\
\varepsilon_{\text{max}} = NBA \ \omega \implies \varepsilon = \varepsilon_\text{max} \sin(\omega t)
\end{align}
$$

Donde $\varepsilon = \varepsilon_\text{max} \sin(\omega t)$ es una _fem alterna_. Los generadores de [[Corriente Alterna]] utilizan este concepto.

![[Generador de Corriente Alterna.png]]

## FEM de Movimiento para un Circuito Cerrado

Sea una varilla conductora que se desliza, y sea $B$ constante. Al variar el área del circuito, varía el flujo magnético.

![[FEM de Movimiento para un Circuito Cerrado.png]]

$$
\begin{align}A=Lx &\implies \phi_B = BA = BLx \\
\vec F_B = I \vec L \times \vec B_{\text{in}} &\implies F_B = ILB \\
\varepsilon = -\frac{d\phi_B}{dt} = -BL\frac{dx}{dt} = -BLv &\implies I = \frac{|\varepsilon|}{R} = \frac{BLv}{R}
\end{align}
$$

Aplicando la [[Ley de Ohm]], se obtiene $I = \frac{BLv}{R}$. Esto indica que la corriente $I$ genera un campo magnético $B$.

## FEM de Movimiento para un Circuito Abierto

Sea ahora una varilla que se mueve a velocidad $v$ constante dentro de un campo magnético $B$ uniforme.

![[FEM de Movimiento para un Circuito Abierto.png]]

$$
\begin{rcases} \vec F_B = q(\vec v \times \vec B) \\ \vec F_E = q \vec E \end{rcases}
\text{ en equilibrio} \implies \cancel qE = \cancel qvB \implies \Delta V = EL = vBL \implies |\varepsilon| = BLv
$$

La fem se induce incluso si no hay corriente.

## FEM Inducida y Campos Eléctricos

Si circula corriente entonces existe un [[Campo Eléctrico]] $\vec E$, y un flujo magnético variable produce fem y corriente, por lo que se crea un campo eléctrico debido al flujo magnético variable.

![[FEM Inducida y Campos Eléctricos.png]]

El trabajo para que una [[Cargas Eléctricas]] $q$ de una vuelta completa en el conductor es:

$$W = \Delta U = \Delta V q = \varepsilon q = \oint \vec F_e \vec{dl} = q E \oint \vec{dl} = qE 2 \pi r \implies \cancel \varepsilon = \cancel E 2 \pi r \implies E = \frac{\varepsilon}{2 \pi r}$$

Hay un **campo eléctrico no conservativo inducido** en la espira.

$$\phi_B = BA = B \pi r^2 \implies \varepsilon = - \frac{d\phi_B}{dt} = - \pi r^2 \frac{dB}{dt}$$

Se deduce que la variación del campo magnético $\vec B$ produce un campo eléctrico $\vec E$. Este campo eléctrico es **inducido**, NO electrostático.

| $\vec E$ inducido                                   | $\vec E$ electrostático                          |
| --------------------------------------------------- | ------------------------------------------------ |
| Asociado a variaciones del flujo magnético $\phi_B$ | Asociado a cargas eléctricas                     |
| Las líneas de campo son cerradas                    | Las líneas de campo nacen en $+$ y mueren en $-$ |
| El campo NO es conservativo                         | El campo es conservativo                         |
