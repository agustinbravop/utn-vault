Tipos de [[Corriente Eléctrica]]:

1. **Continua**: va siempre en el mismo sentido y tiene $I$ constante.
2. **Unidireccional**: mismo sentido pero con $I$ variable.
3. **Alterna simétrica**: sentido variable. Es periódica y con $I$ media nula.

El concepto de [[FEM Inducida]] sirve para construir un generador de corriente alterna sencillo: una espira que gira con velocidad angular constante en un campo magnético uniforme.

![[Generador de Corriente Alterna-1.png]]

A lo largo del tiempo sucede lo siguiente:

![[Corriente Alterna a lo Largo del Tiempo.png]]

Donde la *fem alterna* viene dada por $V(t) = V \cos(\omega t) = V \cos(2 \pi ft)$, donde:

1. $V(t)$: fem o voltaje instantáneo.
2. $V$: valor máximo o amplitud de la fem.
3. $\omega$: pulsación o frecuencia angular igual a $2 \pi f$.
4. $f$: número de oscilaciones completas realizadas por segundo. Suele ser 50 Herz.

Y se produce una corriente eléctrica que también varía con el tiempo de forma periódica. La corriente alterna viene dada por $i(t) = I \cos ( \omega t)$.

## Fasores

Un fasor es un vector que gira en sentido antihorario con frecuencia angular $\omega$. Los fasores representan cantidades alternantes. Un **diagrama de fasores** permite analizar el funcionamiento del circuito.

![[Diagrama de Fasores.png]]

## Circuito Resistivo

![[Corriente Alterna - Circuito Resistivo.png]]

$$V(t) = R i(t) \implies V \cos(\omega t) = R I \cos(\omega t) \implies \text{en fase}$$

## Circuito Capacitivo

![[Corriente Alterna - Circuito Capacitivo.png]]

$$\begin{gather}V(t) = V \cos(\omega t) \ \land \ i = \frac{dQ}{dt} \ \land \ C = \frac{Q}{V} \implies i(t) = \frac{dQ}{dt} = C\frac{dV(t)}{dt} \implies i(t) = - \omega C V \sin(\omega t) \\
i(t) = \omega CV \cos\left(\omega t + \frac{\pi}{2} \right) \implies \text{desfasaje en -90°}
\end{gather}$$

$V_C$ se retrasa a $I$ en $\frac{\pi}{2}$, lo que bloquea frecuencias bajas. El valor máximo es $I = \omega C V \implies V = \frac{I}{\omega C}$ y se define la *reactancia capacitiva* $X_C = \frac{1}{\omega C}$ de manera que $V = I X_C$ ([[Ley de Ohm]]).

## Circuito Inductivo

![[Corriente Alterna - Circuito Inductivo.png]]

$$\begin{gather}V(t) = V \cos (\omega t) \ \land \ V(t) = L \frac{di}{dt} \implies \frac{di}{dt} = \frac{V}{L} \cos(\omega t) \implies i(t) = \frac{V}{\omega L} \sin(\omega t) \\
i(t) = \frac{V}{\omega L} \cos\left(\omega t - \frac{\pi}{2}\right) \implies \text{ desfasaje en 90°}
\end{gather}$$

$V_L$ se adelanta a $I$ en $\frac{\pi}{2}$, lo que bloquea frecuencias altas. Se define la *reactancia inductiva* $X_L = \omega L$ de manera que $V = I X_L$.

## Impedancia

Conforme $\omega$ aumenta: $R$ se mantiene constante, $X_C$ baja, y $X_L$ sube.

![[Corriente Alterna - Circuito RLC.png]]

Sea un circuito RLC en serie, con $V = V_R + V_C + V_L$, queremos determinar la intensidad $I$ y la diferencia de fase $\phi$:

$$\begin{gather}V = \sqrt{V^2_R + (V_L - V_C)^2} = \sqrt{(IR)^2 + (IX_L - IX_C)^2} = I \sqrt{R^2 + (X_L - X_C)^2} = IZ \implies V = IZ \\
Z = \sqrt{R^2 + (X_L - X_C)^ 2} = \sqrt{R^2+\left(\omega L - \frac{1}{\omega C}\right)^2}
\end{gather}$$

Donde $Z$ es la *impedancia* del circuito, y se mide en ohms ($\Omega$). Entonces:

$$\begin{align}I &= \frac{V}{Z} \\
\tan(\phi) &= \frac{V_L - V_C}{R} = \frac{X_L - X_C}{R}
\end{align}
$$

Se observa que $\phi$ no depende de $V$.

## Valores Eficaces

$$\begin{align}i = I_0 \cos(\omega t) \implies i^2 = I_0^2 \cos^2 (\omega t) = I_0^2 \frac{1}{2} &(1 + \cos(2 \omega t)) = \frac{1}{2}I_0^2 + \cancel {\frac{1}{2}I^2 \cos(2 \omega t)} \implies i^2 = \frac{1}{2}I_0^2 \\
\sqrt i^2 = I_{\text{rms}} &= \frac{I_0}{\sqrt{2}} = 0.707 I_0 \\
V_{\text{rms}} &= \frac{V_0}{\sqrt 2} = 0.707 V_0
\end{align}$$

Donde $I_\text{rms}$ es el *valor eficaz* de la corriente alterna: es el valor que tendría que tener una corriente continua para producir la misma potencia.

En un circuito RLC, solo se disipa potencia en la $R$. Por la *fem alterna*: 

$$P(t) = \frac{V_0 \cos(\omega t))^2}{R} = vi$$

Potencia media de una [[Resistencia Eléctrica]]: $P_\text{med} = \frac{1}{2}VI = \frac{V}{\sqrt 2} \frac{I}{\sqrt 2} \implies P_\text{med} = V_\text{rms} I_\text{rms}$.

Potencia media de un [[Capacitor]] y una [[Autoinducción|inductancia]]: la mitad del tiempo es positiva, y la otra mitad del tiempo es negativa, por lo que $P_\text{med} = 0$.

Potencia media de un circuito de corriente alterna:

$$\begin{align}p = vi = V \cos(\omega t + \theta) I \cos (\omega t) = \  &V(\cos (\omega t)\cos(\theta) - \sin(\omega t)\sin(\theta))I\cos(\omega t) \implies \\
&VI\cos(\theta) \cos^2(\omega t) - VI \sin(\theta) \cos (\omega t) \sin(\omega t) \implies \\
&P_\text{med} = \frac{1}{2}VI\cos\theta \implies \\
&P_\text{med} = V_\text{rms}I_\text{rms} \cos(\theta)
\end{align}$$

Donde $\theta$ es el *factor de potencia* del circuito.