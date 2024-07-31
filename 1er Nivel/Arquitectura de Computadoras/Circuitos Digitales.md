Una variable booleana o representa un ***bit*** (*b*inary dig*it*). Es un campo discreto. Una señal digital es un conjunto de variables booleanas. 

Un sistema digital o **circuito digital** es cualquier dispositivo destinado a generar y procesar señales digitales. Una [[Computadora]] digital usa **lógica binaria** (verdadero o falso, cero o uno, la corriente pasa o no).

Los circuitos puede ser:

- **Circuitos combinacionales**: la salida depende solo de la entrada. No necesita memoria.
- [[Circuitos Secuenciales]]: la salida depende de la entrada actual y de **estados pasados**.

Se pueden representar como funciones de lógica booleana, las cuales tienen dos formas normales:

- **Forma Normal Conjuntiva (FNC)**: conjunción de disyunciones de literales. Es una multiplicación de los maxitérminos falsos. Ejemplo: $(A + B) * (\bar{A} + B) * (\bar{A} + \bar{B})$.
- **Forma Normal Disyuntiva (FND)**: disyunción de conjunciones de literales. Es una suma de los minitérminos verdaderos. Ejemplo: $\bar{A} B + A \bar{B} + \bar{A} \bar{B}$.

## Compuertas Lógicas

La unidad lógica de los circuitos digitales son las **compuertas lógicas**, conectadas entre sí por cables o líneas que transmiten un cero o un uno.

![[Tabla de Compuertas Lógicas.png]]
