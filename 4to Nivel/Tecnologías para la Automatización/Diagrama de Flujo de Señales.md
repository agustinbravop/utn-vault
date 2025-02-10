Un **diagrama de flujo de señales** permite hallar la [[Función de Transferencia]] de un [[Sistema de Control]] sin tener que reducir el [[Diagrama de Bloques Funcionales]] mediante el [[Álgebra de Bloques]].

En estos diagramas, las señales son nodos y los bloques son ramas. Elementos;

- **Rama**: conecta dos nodos. Tiene sentido y transmitancia.
- **Trayectoria**: cualquier camino posible entre dos nodos.
- **Trayectoria directa**: camino entre dos nodos sin pasar dos veces por un nodo.
- **Trayectoria cerrada**: el nodo de inicio y de fin es el mismo.
- **Lazo cerrado**: trayectoria directa cerrada.

![[Diagrama de Flujo de Señales.png]]

## Fórmula de Mason

La **fórmula de Mason** es un método para encontrar la función de transferencia dado el diagrama del flujo de señal.

Es un método alternativo a la resolución de las ecuaciones algebraicas. Calcula la función transferencia entre el nodo entrada $R(s)$ y el nodo salida $C(s)$:

$$G(s)=\frac{C(s)}{R(s)} = \sum_{i=1}^n \frac{P_i\Delta_i}{\Delta} = \frac{1}{\Delta} \sum_{i=1}^n P_i\Delta_i$$

El método consiste en calcular el determinante $\Delta$, lo que involucra enumerar los lazos cerrados del sistema:

$$\begin{align}\Delta = 1 &-\sum \text{ lazos individuales} \\
&+ \sum \text{ productos de todas las combinaciones de lazos disjuntos tomados de a dos} \\
&- \sum \text{ productos de todas las combinaciones de lazos disjuntos tomados de a tres} \\
& \ \ \vdots \\
\end{align}$$
