La [[Arquitectura ABACUS]] usa [[Operadores Aritméticos]] con un **registro acumulador** (AC), es decir que son de carácter secuencial, lo que los hace más simples y baratos.

## Operaciones Lógicas

![[Operador Lógico Completo.png]]

Se propone un [[Biestables|biestable]] RCS (C de complemento o *toggle*) que sirva para realizar las operaciones lógicas AND, OR y XOR.

## Semi Sumador

Un semi sumador suma dos bits sin acarreo previo. Es útil para sumar los bits de menor peso (que no tienen acarreo de un bit previo).

Las ecuaciones lógicas son: $S = A \oplus B \ ; \ C = A B$. Un XOR es una suma alebráica sin *carry*.

![[Semi Sumador.png]]

## Sumador

Un sumador completo para sumar dos registros requiere considerar el carry bit a bit.

$S = C' \oplus A \oplus B \ ; \ C = C' (A + B) + AB$.

Un sumador en paralelo implica tener una cadena de circuitos `SUM` en los cuales el sumador del bit $i$ recibe como $C'$ el $C$ del bit $i - 1$.

![[Sumador en Paralelo.png]]

También se puede plantear un sumador en serie que es un solo circuito "en bucle", el cual suma dos palabras binarias bit por bit, uno a la vez.
