La **polarización** es un fenómeno característico de las [[Ondas Electromagnéticas]] debido a su naturaleza ondulatoria. Describe un estado particular de vibración del [[Campo Eléctrico]] $E$ y del [[Campo Magnético]] $B$ de la onda. En el caso de la luz no es visible directamente: se necesitan dispositivos especiales para su observación.

La luz natural normalmente no es polarizada. Se la puede polarizar mediante diferentes procesos físicos como la reflexión, dispersión, refracción, y birrefringencia. 

Según la dirección de propagación de la onda, la polarización puede ser:

1. Lineal.
2. Circular.
3. Elíptica.

## Polarización Lineal

Se define la dirección de polarización de una OEM como la *dirección de vibración* del campo eléctrico $E$.

![[Polarización Lineal.png]]

$$\begin{align}
&\begin{cases} \vec E_x(z, t) = \vec i E_{0_x} \sin(kz - \omega t) \\
\vec E_y(z, t) = \vec j E_{0_y} \sin(kz - \omega t) \\
\end{cases} \\
\tan \theta &= \frac{E_{0_y}}{E_{0_x}} \\
\vec E(z, t) &= (\vec i E_{0_x} + \vec j E_{0_y})\sin(kz-\omega t)
\end{align}$$

Siendo $\theta$ el ángulo en el que vibra el campo eléctrico neto.

## Polarización Circular

Sucede cuando hay una diferencia de fase de $\frac{\pi}{2}$ entre $E_x$ y $E_y$, pero misma amplitud $E_{0_x} = E_{0_y}$:

![[Polarización Circular.png]]

$$
\begin{align}
&\begin{cases} \vec E_x(z, t) = \vec i E_{0_x} \sin(kz - \omega t) \\
\vec E_y(z, t) = \vec j E_{0_y} \cos(kz - \omega t)
\end{cases} \\
&\begin{cases} E_0^2 = E_x^2 + E_y^2 \\ \frac{E_x^2}{E_0{^2}} + \frac{E_y^2}{E_0{^2}} = 1
\end{cases}
\end{align}
$$

La polarización es derecha si gira en sentido horario, y es izquierda si gira en sentido antihorario.

![[Polarización Circular en Movimiento.png]]

## Polarización Elíptica

Se consideran dos ondas de amplitudes distintas, y una diferencia de fase $\varphi$ entre ellas.

![[Polarización Elíptica.png]]

$$
\begin{gather}
\begin{cases} \vec E_x(z, t) = \vec i E_{0_x} \sin(kz - \omega t) \\
\vec E_y(z, t) = \vec j E_{0_y} \cos(kz - \omega t + \varphi)
\end{cases} \\
\left(\frac{E_x}{E_{0_x}}\right)^2 + \left(\frac{E_y}{E_{0_y}}\right)^2 - 2 \left(\frac{E_x}{E_{0_x}}\right)\left(\frac{E_y}{E_{0_y}}\right) \cos\varphi = \sin^2\varphi
\end{gather}
$$

Donde se nota que:

- Si $\varphi = \pm n \frac{\pi}{2}$, siendo $n$ un entero, entonces es polarización circular.
- Si $\varphi = \pm n\pi$, siendo $n$ un entero,, entonces es polarización lineal.

## Ley de Malus

La Ley de Malus establece que si la luz natural incide sobre un **polarizador lineal**, se transmitirá solo la componente de $\vec E$ paralela al eje de transmisión.

![[Ley de Malus.png]]

$$I_1 = \frac{I_0}{2} \ ; \ I_2 = \frac{I_0}{2}\cos^2\theta = I_1 \cos^2\theta$$

## Ángulo de Brewster

El ángulo de Brewster es un ángulo especial para el cual la luz reflejada está totalmente polarizada en dirección perpendicular al plano de incidencia.

![[Ángulo de Brewster.png]]

La **Ley de Snell** establece que $\frac{n_2}{n_1} = \frac{\sin\theta_1}{\sin\theta_2} = \frac{\sin\theta_p}{\sin(90\degree - \theta_p)}$, por ende:

$$\tan \theta_p = \frac{n_2}{n_1} \ ; \ \theta_p + \theta_2 = 90\degree$$

Siendo $\theta_p$ el ángulo de Brewster.
