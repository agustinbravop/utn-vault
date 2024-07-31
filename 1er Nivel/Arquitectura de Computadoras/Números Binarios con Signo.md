Los números binarios con signo se pueden representar con **punto fijo**. El bit de mayor peso o más importante (el que está más a la izquierda) representa el signo. Si es 1 entonces tiene signo negativo. Hay 3 representaciones:

1. **Signo-magnitud**: representa el nueve como: $1 \ 0 \ 0 \ 0 \ 1 \ 0 \ 0 \ 1$.
2. **Complemento a 1**: se complementa cada bit: $1 \ 1 \ 1 \ 1 \ 0 \ 1 \ 1 \ 0$.
2. **Complemento a 2**: o complemento a la base: $1 \ 1 \ 1 \ 1 \ 0 \ 1 \ 1 \ 0$.

El complemento a 2 es sumarle 1 al complemento a 1. Solo puede haber sobrecapacidad o **desbordamiento** al sumar si ambos números son positivos o ambos son negativos (y no siempre). Se detecta desbordamiento si el acarreo del bit de signo es distinto al acarreo del bit más significativo de la magnitud. Este acarreo debe ser considerado al cablear los [[Operadores Aritméticos]].

Por ejemplo, un sumador de dos operandos $B$ y $B'$, representados en complemento a dos, puede detectar si hubo desbordamiento o no, y almacena ese dato en un indicador.

![[Sumador de B y B' en Complemento a Dos.png]]
