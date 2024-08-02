Este [[Punto de Memoria]] requiere dos líneas de selección pero presenta muchos beneficios al compararse con el [[Punto de Memoria 2D]]. Surgen limitaciones físicas al tener que separar las capas entre sí para evitar interferencias electromagnéticas.

![[Punto de Memoria 3D.png]]

## Organización de una Memoria 3D

La [[Unidad de Memoria]] de ABACUS se puede organizar de la siguiente manera (para 4 palabras de 1 bit).

![[Organización de una Memoria 3D.png]]

Esta organización resulta **más simple y veloz** porque permite modular la memoria, aunque con una **menor capacidad** que la [[Punto de Memoria 2D#Organización de una Memoria 2D|organización 2D]]. A nivel físico, resulta caro **separar las capas** (cada capa almacena un bit de la longitud de cada palabra). En el diagrama se puede ver el plano $X_0$ que almacena el bit en la posición $0$ de la palabra. El decodificador $S_1$ selecciona las filas y $S_2$ selecciona las columnas.

Diagramar de esta manera permite tener en cuenta solo la **cantidad de palabras de memoria**. Luego, solo se agregan o quitan capas para determinar la longitud de la palabra deseada.
