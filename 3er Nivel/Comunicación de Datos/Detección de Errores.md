Todo sistema de transmisión tiene **ruido** que debe ser corregido. Dentro del [[Software de Redes]], se suelen detectar en la capa 2. Los errores pueden ser de dos tipos:

- **Aislados**: alteran a un solo bit del mensaje.
- **En ráfaga**: se alteró una secuencia de bits en el que la mayoría son erróneos. A mayor frecuencia de transmisión, las ráfagas suelen ser más largas.

Algunas definiciones:

1. $P_b$: probabilidad de que un bit recibido sea erróneo (*bit error rate*).
2. $P_1$: probabilidad de que una trama llegue sin errores.
3. $P_2$: probabilidad de tener un error no detectado (si se usa un algoritmo de detección).
4. $P_3$: probabilidad de tener errores detectados y ningún error sin detectar.
5. $F$: número de bits por trama. Se cumple que $P_1 = (1-P_b)^F$ y $P_2 = (1-P_1)$.

Generalmente las técnicas de detección de errores añaden bits de control que el receptor utiliza para validar el mensaje. Se utiliza la [[Teoría de la Codificación]] para construir [[Códigos]].

## Comprobación de Redundancia Cíclica

El método CRC es de los más habituales y potentes. El receptor divide sucesivamente la trama recibida (mediante polinomios, aritmética binaria, etc) y valida que el resto sea cero.