Las **señales de gobierno** o **micro-órdenes** activan distintos [[Circuitos Digitales]] de la [[Arquitectura ABACUS]]. Pueden ser **de nivel** o **impulsionales**. Se presumen de nivel y una flecha $\vec{}$ encima indica que son impulsionales. Son generadas por el [[Secuenciador Central]].

![[Señales de Gobierno de ABACUS.png]]

Toda señal de salida a [[Buses]] es de nivel, porque necesita estabilizar las lineas del bus.

Para la memoria:

1. $\vec{ENS}$: entrada a S (desde el bus S).
2. $\vec{ICM}$: inicio de un ciclo de memoria.
3. $\vec{PACM}$: puesta a cero de M.
4. $\vec{ENM}$: entrada a M.
5. $LEC$: lectura a memoria.
6. $ESC$: escritura a memoria.
7. $SRM$: salida de M (al bus M).

Para el control:

1. $\vec{ENI}$: entrada a I (desde el bus M).
2. $SRD$: salida de D (al bus S).
3. $\vec{ENP}$: entrada a P (desde el bus S).
4. $\vec{INCP}$: incremento de P.
5. $SRP$: salida de P (al bus S).

Para el procesamiento:

1. $ENA$: entrada al acumulador (desde el bus M). Es de nivel porque se lee directo del bus M para ahorrar un registro en la arquitectura.
2. $SAC$: salida de AC (al bus M).
3. $\vec{EAC}$: entrada al AC (desde la UAL).
4. $SUM, MUL, CAR, AND, SUS, DIV, XOR, ...$: instrucciones que activan operadores.
