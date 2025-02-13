El **diagrama de Bode** permite caracterizar la [[Respuesta en Frecuencia]] de un [[Sistema de Control]], y permite deducir la [[Estabilidad]] del sistema. Es una alternativa al [[Diagrama de Nyquist]]. En realidad, son dos gráficas unidas en el mismo diagrama:

- La **gráfica de magnitud** dibuja la ganancia en decibeles ($\text{dB}$), una escala logarítmica.
- La **gráfica de fase** representa la fase en grados o radianes, también en escala logarítmica.

Un decibel es $1 \text{ dB} = 10 \cdot \log_{10} \left(\frac{P_s}{P_e}\right)$, o si se usa voltaje: $1 \text{ dB} = 20 \cdot \log_{10} \left(\frac{V_s}{V_e}\right)$.

El _margen de ganancia_ (MG) son los decibeles que la ganancia puede incrementarse antes de que el sistema se vuelva inestable. Se mide en la _frecuencia de cruce de fase_, cuando la fase es $-180 \degree$.

El _margen de fase_ (MF) es el ángulo adicional que la fase puede disminuir antes de que el sistema se vuelva inestable. Se mide en la _frecuencia de cruce de ganancia_, cuando la ganancia es $0 \text{ dB}$.

![[Diagrama de Bode.png]]

Si MG y MF son positivos, el sistema es estable. Si uno es negativo, el sistema ya se vuelve inestable.
