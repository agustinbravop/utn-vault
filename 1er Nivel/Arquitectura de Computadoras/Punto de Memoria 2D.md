![[Punto de Memoria 2D.png]]

$O$ es el valor del [[Punto de Memoria]] (el estado del [[Biestables|biestable]] cuando es seleccionado. Solo se lee $O$ si el punto está seleccionado por $S$ (señal de *select*). Solo se sobrescribe el punto con el valor de $I$ (señal de *input*) cuando el punto está seleccionado (con $S$) y con $W$ (señal de *write*) activado.

## Organización de una Memoria 2D

La [[Unidad de Memoria]] de ABACUS que utiliza un punto de memoria 2D se puede organizar de la siguiente manera (para 4 palabras de 2 bits, osea que tiene 4 direcciones 00, 01, 10 y 11):

![[Organización de Memoria 2D.png]]

Hau una dirección cableada para cada palabra (la cantidad de direcciones es la cantidad de palabras). Hay un $I_i$ y un $O_i$ para cada bit de palabra (la cantidad crece según la longitud de palabra).

Siempre hay un solo $LEC$ y un solo $ESC$. Para alargar la longitud de la palabra, se agregan puntos de memoria hacia la derecha del diagrama.
