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

1. **ASK**: Amplitude-Shift Keying. 
2. **FSK**: Frequency-Shift Keying.
3. **PSK**: Phase-Shift Keying.

![[Modulación de Señales Analógicas.png]]

La señal resultante siempre ocupa un ancho de banda *centrado* en la frecuencia de la portadora.

