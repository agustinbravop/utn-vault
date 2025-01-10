En la [[Transmisión de Datos]], se pueden utilizar *codificadores* y *moduladores* para la conversión de [[Señales y Espectros|señales]] analógicas a digitales y viceversa.

![[Codificación de Datos 2025-01-08 22.08.10.excalidraw.svg]]

Debido a esto, la codificación de datos se puede dar de cuatro maneras:

1. Codificar datos digitales en señales digitales.
1. Codificar datos digitales en señales analógicas.
1. Codificar datos analógicos en señales digitales.
1. Codificar datos analógicos en señales analógicas.

## Datos Digitales en Señales Digitales

La señal puede ser:

- **Polar**: tiene un valor positivo y otro valor negativo.
- **Unipolar**: tiene un mismo signo algebraico para el valor de tensión.

La *razón de modulación* es la velocidad con la que cambia el nivel de señal, medida en baudios. Un *baudio* equivale a un elemento o pulso de señal por segundo.

El *esquema de codificación* es la correspondencia entre los bits de los datos y los elementos (pulsos) de señal. El pulso suele ocupar la mitad del *intervalo significativo* $\tau$. Cuando el pulso ocupa todo $\tau$, la señal será NRZ (sin retorno a cero).

![[Intervalo Significativo.png]]

Algunas técnicas o formatos de codificación con señal digital:

![[Formatos de Codificación con Señal Digital.png]]

1. **NRZ-L**: No return to zero. Son fáciles y eficaces, pero sin sincronización.
2. **NRZI**: no return to zero, invert on ones.
3. **Bipolar-AMI**: multinivel alternante, lo que permite sincronizar y detectar errores.
4. **Manchester**: es *bifase*, tiene una transición en mitad del intervalo de duración del bit.
5. **Manchester diferencial**.

Se busca evitar secuencias largas y poder detectar errores sin reducir la velocidad de datos.

## Datos Digitales en Señales Analógicas

Se logra con dispositivos *módem* (modulador-demodulador). Parámetros y técnicas de modulación:

1. **ASK**: Amplitude-Shift Keying. Una amplitud representa el cero y la otra representa el uno. Esto es sensible a cambios repentinos en la [[Potencia Efectiva#Ganancia y Pérdida|ganancia]].
2. **FSK**: Frequency-Shift Keying. Dos frecuencias distintas, equidistantes a la portadora. Sirve para transmisión full duplex.
3. **PSK**: Phase-Shift Keying. Se desplaza la fase de la portadora para representar un cambio de bit. Si desplazo 90° la fase, puedo representar un 0 o un 1. Si la desplazo cada 45°, puedo representar 00, 01, 10, o 11. Esto vuelve más compleja la electrónica, pero permite transmitir mayor volumen de información.

![[Modulación de Señales Analógicas.png]]

La señal resultante siempre ocupa un ancho de banda *centrado* en la frecuencia de la portadora.

## Datos Analógicos en Señales Digitales

Al envío de datos digitales en señales digitales se le agrega un digitalizador previo para digitalizar los datos analógicos, y un modulador posterior para poder recuperarlos.

La **modulación** puede ser:

1. **PCM**: Por Codificación de Impulsos. Se basa en el teorema de muestreo (la [[Frecuencia de Nyquist]] que propone muestrear a una frecuencia $f \lt 2 f_\text{max}$).
2. **PAM**: Por Amplitud de Impulsos. Representa muestras como pulsos cortos con amplitud proporcional al valor original. Es susceptible al error de cuantización.
3. **DM**: Modulación Delta. Se aproxima la entrada analógica con una función escalera, que en cada muestreo sube o baja un nivel de cuantificación, proporcionalmente al signo de la derivada de la señal. El problema es que producen errores si la señal entrante varía abruptamente.

## Datos Analógicos en Señales Analógicas

Este último caso sirve para transmitir datos en frecuencias mayores. La modulación combina una señal de entrada con una *portadora* a frecuencia $f_c$ para producir una señal con ancho de banda centrado en $f_c$. 

Se puede modular en amplitud, frecuencia, y/o fase. Modulación en amplitud:

![[Modulación en Amplitud.png]]
