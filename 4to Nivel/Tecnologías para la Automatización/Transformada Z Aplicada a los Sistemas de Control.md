La [[Transformada Z]] es una herramienta alternativa a la [[Transformada de Laplace Aplicada a los Sistemas de Control]], cumple la misma función pero está pensada para **variables discretas**. Se la utiliza debido a la incorporación de las computadoras electrónicas dentro de los sistemas de control.

![[Transformada Z Aplicada a los Sistemas de Control.png]]

Los sistemas de control en **tiempo discretos** son aquellos sistemas en los cuales una o más variables pueden cambiar solo en valores discretos de tiempo.

Esos instantes de tiempo son $kT$, donde $k\in \Bbb N$ y $T$ es el período de muestreo. Ese período de muestreo determina la frecuencia de medición del mundo físico y suele ser una limitación de diseño restringida por la [[Calidad de Servicio]] (**QoS**) necesaria.

La [[Frecuencia de Nyquist]] $f_s\ge 2 f_\text{max}$ determina que para reproducir una señal cuya frecuencia más alta es $f_\text{max}$, se necesita usar una frecuencia de muestreo $f_2$ que sea al menos el doble de alta.

La QoS quedará definida por el grado de proximidad entre cada uno de los valores muestreados y su consiguiente **interpolación**.

Según las respuestas, los sistemas de control discretos se clasifican en:

- **Sistema casual**: sus entradas dependen de las entradas actuales y las entradas inmediatamente anteriores. Son secuenciales. $r(t) = u(t) + u(t-1)$.
- **Sistema estrictamente casual**: la salida solo depende de los valores anteriores de las entradas, por lo que son todavía más simples. $r(t)=u(t-1)$. Este sistema se considera _no anticipativo_, ya que sus salidas no anticipan valores próximos $t+1$ de las entradas.

El control discreto es una secuencia de operaciones administradas por eventos o por tiempo, y cada operación tiene una condición definida para iniciarse.
