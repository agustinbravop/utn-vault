La arquitectura Intel 8086es una [[Arquitectura de Computadoras]] muy popular en su momento.

![[Arquitectura 8086.png]]

[[Registros]] de propósito general:

1. $AX$: **acumulador** para cálculos aritméticos.
2. $BX$: **base**. Puede ser índice para direccionamiento indexado.
3. $CX$: **contador**. Controla la cantidad de ciclos en un loop.
4. $DX$: **datos**. Sirve para I/O.

Registros apuntadores (sirven para el direccionamiento):

1. $SP$: _stack pointer_. Suma o resta 2 o 1 al hacer `PUSH` o `POP`.
2. $BP$: _base pointer_. Sirve para [[Direccionamiento Indirecto]] dentro de la pila (stack).
3. $SI$: _source index_. Sirve para operaciones con cadenas.
4. $DI$: _destination index_. Sirve para operaciones con cadenas.

El registro de banderas contiene 9 banderas:

1. $CF$: acarreo en instrucciones aritméticas.
2. $OF$: desbordamiento aritmético.
3. $ZF$: cero o comparación igual.
4. $SF$: resultado o comparación negativa.
5. $PF$: paridad, para verificar transferencias de bytes.
6. $AF$: auxiliar, indica si hay que ajustar operaciones con números BCD.
7. $DF$: controla la dirección hacia delante o atrás en operaciones con cadenas.
8. $IF$: indica si están disponibles las instrucciones de periféricos.
9. $TF$: modo _debug_, controla una operación paso a paso.

## Segmentos de la Memoria

La [[Unidad de Memoria]] tiene en total 1 MB de capacidad, repartido en 16 segmentos de 64 KB cada uno.

![[Segmentos de la Memoria de la Arquitectura 8086.png]]

[[Técnicas de Direccionamiento]] disponibles para obtener los operandos:

1. **De registro**: el más común. `MOV AX,BX`.
2. **[[Direccionamiento Inmediato|Inmediato]]**: el operando es un literal en la instrucción. `MOV BX,10`.
3. **[[Direccionamiento Directo|Directo]]**: se busca en una dirección de memoria. `MOV BX,[1000]` o `MOV AX,TABLA`.
4. **[[Direccionamiento Indirecto|Indirecto]] mediante registro**: solo se puede con $BX$, $BP$, $SI$ o $DI$. `MOV AX,[BX]`.
5. **[[Direccionamiento Relativo#Por Base y Desplazamiento|Por registro base]]**: con $BX$ o $BP$ y se le suma un desplazamiento. `MOV AX,[BP+2]`.
6. **[[Direccionamiento Relativo#Indexado|Indexado]]**: suma de un desplazamiento y un índice. `MOV AX,TABLA[DI]`.
7. **Indexado a base**: se considera además $BX$ o $BP$. `MOV AX,TABLA[BX][SI]`.

En los ejemplos mostrados de cada tipo, `TABLA` es una referencia a una variable o dato.

## Historia

1. **1971**: Intel lanza su primer microprocesador 4004 integrado para calculadoras.
2. **1972**: anuncian una versión mejorada del procesador.
3. **1974**: lazan el Intel 8080.
4. **1978 y 1979**: aparecen los microprocesadores 8086 y 8088, que pasaron a formar el "IBM PC". El 8088 es idéntico al 8086, pero con un bus de 8 bits en lugar de 16 bits (siendo más barato).
