K-means es uno de los mejores algoritmos de [[Clustering]] particional. 

Dado un conjunto de puntos y un número $k$ de clusters a identificar, el algoritmo particiona iterativamente el conjunto de puntos. Sea el conjunto de puntos o **instancias** $D=\set{\bf x_1, \bf x_2, \dots, \bf x_n}$ donde $\bf x_i$ es un vector en un **espacio euclidiano** y $r$ es el número de atributos de la instancia o dimensiones del espacio, tal que $\bf x_i=(x_{i1}, x_{i2}, \dots, x_{ir})$. El **centroide** de un cluster es la media de todos los puntos del cluster.

Una vez que todos los puntos del dataset han sido asignados a un cluster, se recalcula el centroide de cada cluster utilizando los puntos que corresponden a cada cluster. Esto se repite hasta alcanzar un **criterio de parada**:

- Hasta que ya no hay reasignación de datos en los diferentes clusters.
- Hasta que ya no hay cambios en los centroides.
- Hasta que se alcanzó un mínimo en la **suma de errores cuadráticos**:

$$SSE=\sum_{j=1}^k\sum_{x\\inC_j} \text{dist}(\bf x, \bf m_j)^2$$

K-means se puede usar siempre que se pueda calcular una media. Siendo $|C_j|$ el número de puntos en el cluster $C_j$, la media en el espacio euclidiano es:

$$\bf m_j = \frac{1}{|C_j|}\sum _{\bf x_i \in C_j}\bf x_i$$

La **distancia** de cada dato al centroide se calcula como:

$$\begin{align}
\text{dist}(\bf x_i, \bf m_i) &= ||\bf x_i - \bf m_j|| \\
&= \sqrt{(x_{i1} - m_{j1})^2 + \dots (x_{ir} - m_{jr})^2}
\end{align}$$

## Algoritmo

$$
\begin{aligned}
&\textbf{Algorithm } k\text{-}means(k, D) \\[6pt]
&\qquad \text{choose } k \text{ data points as the initial centroids (cluster centers)} \\[6pt]
&\qquad\textbf{repeat} \\[6pt]
&\qquad\qquad \textbf{for each data point } x \in D \textbf{ do} \\[6pt]
&\qquad\qquad\qquad \text{compute the distance from } x \text{ to each centroid;} \\[6pt]
&\qquad\qquad\qquad \text{assign } x \text{ to the closest centroid} \\[6pt]
&\qquad\qquad \textbf{endfor} \\[6pt]
&\qquad\qquad \text{re-compute the centroid using the current cluster memberships} \\[6pt]
&\qquad\textbf{until } \text{the stopping criterion is met} \\[6pt]
\end{aligned}
$$

La bibliografía recomienda ejecutar el algoritmo con al menos 500 iteraciones.

Existe una variante *k-modes* (usa modas en lugar de medias) para casos en los que no se pueda usar la media. La media también es sensible a los **outliers**.

Elegir las **semillas** o centroides iniciales de manera aleatoria puede distorsionar negativamente los clusters que el modelo creará (similar a encerrarlo en mínimos locales). Una heurística simple consiste en:

1. Calcular la media del dataset para que la primera semilla sea el punto más alejado de la media.
2. La segunda semilla será el punto más alejado de la primera semilla.
3. Los puntos sucesivos serán elegidos de manera que su distancia a los puntos ya seleccionados sea la máxima. Este método es empeora si existen outliers.
