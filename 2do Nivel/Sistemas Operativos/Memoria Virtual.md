La **memoria virtual** busca aumentar el tamaño de memoria y mejorar el **nivel de multiprogramación** del [[Sistema Operativo]]. Permite que el SO mantenga ciertas páginas en memoria secundaria, útil para cuando la memoria principal no es suficiente para la cantidad de procesos.

A la tabla de páginas de la [[Asignación por Paginación Simple]], se le agrega un bit de presente/ausente. Una página presente está en memoria principal, y una página ausente está en disco.

Hacer un **swap out** de una página presente significa serializarla al disco. Hacer un **swap in** de una página ausente significa traerla a memoria principal. Si la memoria está llena, y se necesita hacer un swap in de una página ausente, entonces primero hay que realizar un swap out de otra página presente. Estas operaciones son costosas, y por ende se debe **minimizar la cantidad de swaps**.

Un **fallo de página** sucede cuando se necesita acceder a una página ausente. Implica un swap in.

## Rendimiento

Implementar memoria virtual afecta al rendimiento del sistema. Esto se puede gestionar mediante [[Políticas para la Memoria Virtual]]. Hay que tener cuidado de no caer en el problema de la [[Hiperpaginación]].

![[Memoria Virtual 2024-11-03 17.18.57.excalidraw.svg]]
