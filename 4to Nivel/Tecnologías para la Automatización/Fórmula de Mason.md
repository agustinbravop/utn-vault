La **fórmula de Mason** es un método para encontrar la [[Función de Transferencia]] dado un [[Diagrama de Flujo de Señales]].

Es un método alternativo a la resolución de las ecuaciones algebraicas que propone el [[Álgebra de Bloques]]. Calcula la función transferencia entre el nodo entrada $R(s)$ y el nodo salida $C(s)$:

$$G(s)=\frac{C(s)}{R(s)} = \sum_{i=1}^n \frac{P_i\Delta_i}{\Delta} = \frac{1}{\Delta} \sum_{i=1}^n P_i\Delta_i$$

El método consiste en calcular el determinante $\Delta$, lo que involucra enumerar los lazos cerrados del sistema:

$$\begin{align}\Delta = 1 &-\sum \text{ lazos individuales} \\
&+ \sum \text{ productos de todas las combinaciones de lazos disjuntos tomados de a dos} \\
&- \sum \text{ productos de todas las combinaciones de lazos disjuntos tomados de a tres} \\
& \ \ \vdots \\
\end{align}$$
