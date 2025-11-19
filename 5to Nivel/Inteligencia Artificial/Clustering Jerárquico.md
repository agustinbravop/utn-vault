Este tipo de [[Clustering]] genera **clusters anidados**. Existen dos clases de métodos:

- **Clustering aglomerativo**: es bottom-up. Va desde las hojas hasta la raíz.
- **Clustering divisivo**: es top-down. Divide clusters en subconjuntos.

## Algoritmo Aglomerativo

$$
\begin{aligned}
&\textbf{Algorithm } \text{Agglomerative}(D) \\[6pt]
&\qquad \text{Make each data point in the data set } D \text{ a cluster} \\[4pt]
&\qquad \text{Compute all pair-wise distances of } \mathbf{x}_1, \mathbf{x}_2, \ldots, \mathbf{x}_n \in D \\[4pt]
&\qquad\textbf{repeat} \\[4pt]
&\qquad\qquad \text{find two clusters that are nearest to each other} \\[4pt]
&\qquad\qquad \text{merge the two clusters to form a new cluster } c \\[4pt]
&\qquad\qquad \text{compute the distance from } c \text{ to all other clusters} \\[4pt]
&\qquad\textbf{until } \text{there is only one cluster left}
\end{aligned}
$$

Este algoritmo genera/construye clusters anidados o **dendogramas**.

![[Clustering Jerárquico.png]]

Hay diversos métodos para determinar la **distancia** entre dos clusters:

- **Single-Link**: la distancia más cercana entre dos puntos de dos clusters.
- **Complete-Link**: callcular todas las distancias máximas y elegir la mínima.
- **Average**-Link****: promedia las otras dos distancias.

Single-Link puede sufrir el *chain effect*, mientras que Complete-Link es susceptible a outliers. 

Este algoritmo es computacionalmente complejo y escala mal a enormes volúmenes de datos, pero tiende a dar mejores resultados que el algoritmo [[K-means]].
