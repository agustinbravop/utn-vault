La [[Arquitectura ABACUS]] en su [[Unidad Aritmético-Lógica]] usa [[Operadores Aritméticos]] con un **registro acumulador** (AC), es decir que son de carácter secuencial, lo que los hace más simples y baratos.

## Operadores Lógicos

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

## Suma-Sustracción de Coma Flotante

Para números representados en [[Coma Flotante]].

![[Operador Suma-Sustracción para Coma Flotante.png]]

Si $Z = 1 \implies$ las mantisas están alineadas. Si $Z = 0$ y $D=1 \implies E_a \lt E_b$. Si $Z = 0$ y $D = 0 \implies E_a \gt E_b$.

$RD$ es el registro de DESD y DESI. Representa la $M$ del resultado.

Hacer DESD o DESI hasta que $Z=1$ (y por ende $E_a=E_b$). Luego, sumar o sustraer. Si hubo desborde, hacer un DESD del $RD$ y luego un solo $CD++$. En cambio, si $S$ es igual al bit de mayor peso de $M$, se hacen DESI del $RD$ y $CD--$ hasta que $S$ es distinto al bit de mayor peso de $M$, quedando así **normalizado** el resultado.

## Operador Multiplicación

![[Operador de Multiplicación.png]]

$MC$ es el [[Registros|registro]] multiplicador-cociente, que asiste al registro AC.

La ejecución es en serie (bit por bit). 

Multiplicado $\to B$ \
Multiplicador $\to AC$ \
$DESD(AC) \to MC$ \ 
(1) Si $MC_0 \ne 0 \implies (B) + (AC) \to AC$ \
$DESD (AC)+(MC)$ \
Si es el último bit (si un descontador llegó a cero) $\implies$ fin \
Sino, ir a (1).

### Operador Multiplicación Celular

![[Operador Multiplicación Celular.png]]

Es **en paralelo** y realiza la multiplicación mucho más rápido. Es caro y de gran tamaño pero vale la pena porque la multiplicación es una operación muy importante.

## Operador División

![[Operador División.png]]

Divisor $\to B$ \
Dividendo $\to AC$ \
$DESD(AC) \to MC$ \
$DESI (AC)+(MC)$ \
(1) $(AC)-(B) \to AC$ (se resta por adelantado para comparar si $AC \gt B$) \
Si $AC \gt 0 \implies 1 \to MC_0$, \
sino $\implies$ $0 \to MC_0 \ , \ (AC)+(B) \to AC$ (se restaura la resta que no correspondía) \
Si es el $n$-ésimo desplazamiento (según un descontador) $\implies$ fin \
Sino, ir a (1).
