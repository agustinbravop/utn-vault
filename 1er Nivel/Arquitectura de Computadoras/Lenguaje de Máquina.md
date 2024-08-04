El lenguaje de máquina es el sistema de códigos interpretable por un circuito [[Microprogramación|micro-programado]]. Cada instrucción del lenguaje determina acciones a ser tomadas por la máquina.

Un **programa** en LM consiste en una cadena de instrucciones junto a datos y operandos específicos a la [[Arquitectura de Computadoras]] en la que serpa ejecutado.

El formato de la instrucción puede variar mucho, sobre todo en [[CISC vs RISC]]:

```
[CO...][...DIR]                     ==> SUM (AC) + (DIR) -> AC
[CO...][...D1...][...D2]            ==> SUM (D1) + (D2) -> (D1)
[CO...][...D1...][...D2...][...DR]  ==> SUM (D1) + (D2) -> (DR)
```

## Simbología

- $M$: dirección de una palabra de memoria.
- $M + 1$: dirección de la palabra siguiente inmediata.
- $(M)$: contenido de la dirección $M$.
- $(M, M+1)$: contenido concatenado entre el de $M$ y el de $M+1$. Forma un _long_ o _double_.
- $(M) \to AC$: transferencia por copia del contenido de $M$ al acumulador.
