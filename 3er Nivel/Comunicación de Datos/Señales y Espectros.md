Los diferentes tipos de información (voz, video, imágenes, texto) se pueden representar con señales electromagnéticas ([[Ondas Electromagnéticas]]), formadas por una serie de **frecuencias constituyentes**.

La señal puede ser **analógica** o **digital**.

![[Señales y Espectros.png]]

El medio de transmisión puede ser **guiado** (camino físico) o **inalámbrico** (las ondas se propagan por el aire, agua, o vacío).

En función del tiempo, las señales repiten un patrón, es decir que son funciones periódicas continuas (sinusoidales) o discretas (cuadradas). Sea $s(t+T)=s(t)$ para $-\infty \lt t \lt + \infty$ donde $T$ es el período y $f = \frac{1}{T}$ es la frecuencia. Está también la longitud de onda $\lambda$ que es la diferencia de un ciclo. Se define la velocidad de propagación $v =\lambda f$ que suele ser la velocidad de la luz.

Una señal puede estar compuesta de muchas frecuencias. Si todas las frecuencias tienen un múltiplo (factor) común, a este se lo denomina _frecuencia fundamental_.

El **espectro** de una señal es el conjunto de frecuencias que la constituyen. Así, el _ancho de banda absoluto_ de la señal es el ancho del espectro (que suele ser infinito). Si la mayor parte de la energía se concentra en cierta banda, ese es el ancho de banda _efectivo_, que consiste en la porción del espectro que contiene la mayor parte de la potencia.

Por cuestiones prácticas, un medio de transmisión solo puede transferir una banda limitada de frecuencias, lo que limita la _velocidad máxima de transmisión_. Además, a mayor limitación en el ancho, mayor distorsión y probabilidad de errores.

El ancho de banda de una señal está centrado sobre una _frecuencia central_, y se cumple que a mayor frecuencia central, mayor ancho de banda y velocidad de transmisión.

La densidad de potencia espectral describe las potencias de una señal en función de la potencia. **Potencia media** para una señal:

$$\text{Señal limitada: } P=\frac{1}{t_1-t_2} \int_{t_1}^{t_2} |x(t)|^2 dt. \ \text{Señal periódica: } P = \frac{1}{T} \int_0^T|x(t)|^2dt$$

**Densidad de potencia espectral:** $S(f)=\sum_{n=-\infty}^\infty |C_n|^2 \cdot \delta(f-nf_0)$, donde $\delta$ es el _impulso unitario_:

$$\delta(t) = \begin{cases} 0 &\text{si } t \ne 0 \\ \infty &\text{si } t = 0 \end{cases} \ \land \int_{-\infty}^\infty \delta(t) dt= 1$$
