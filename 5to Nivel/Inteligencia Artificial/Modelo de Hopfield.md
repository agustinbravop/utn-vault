El modelo de Hopfield es un algoritmo de [[Inteligencia Artificial]] para el [[5to Nivel/Inteligencia Artificial/Aprendizaje|Aprendizaje]] no supervisado offline.

Consiste en una [[Redes Neuronales|red]] monocapa con $N$ neuronas cuyas salidas son binarias. Cada neurona está conectada a las demás mediante conexiones laterales. Los pesos asociados a las conexiones entre pares de neuronas son simétricos. Es un modelo backforward.

![[Modelo de Hopfield.png]]

En su versión discreta, la red usa una función de transferencia escalón en $[-1,1]$. En las redes continuas se usa la función sigmoidal en $[-1,0]$.

Esta es una red **autoasociativa**: puede almacenar varios patrones durante el aprendizaje y después, cuando llega algún patrón distorsionado, puede clasificarlo en alguno de los que aprendió.

Cada neurona recibe una entrada del exterior y las salidas de las demás neuronas multiplicadas por los pesos de su conexión. Así se calcula el $net$ de cada neurona y su correspondiente salida. Este proceso se retroalimenta hasta que la red se estabiliza.

Funcionamiento:

1. En $t=0$ se aplica la información de entrada ($e_1, e_2, \dots, e_N$).
2. Iterar hasta alcanzar la convergencia (cuando $s_i(t+1)=s_i(t)$):

$$s_i(t+1)=f\left(\sum_{j=1}^N w_{ij}\ s_j(t) - \theta _i\right) \ \ \ \ \ \ \ \ \ 1 \le i \le N$$

En la etapa de aprendizaje se fijan los valores de los pesos. Esta red usa un aprendizaje no supervisado de tipo *hebbiano* (autoasociativo), tal que el peso de una conexión entre una neurona $i$ y otra $j$ se obtiene mediante el producto de los componentes $i$-ésimo y $j$-ésimo del vector que representa el patrón a almacenar.

Siendo $M$ patrones, y suponiendo una red discreta que trabaja con $[-1,1]$, se obtienen los pesos:

$$w_{ij}\begin{cases}
\sum_{k=1}^M e^{(k)}_ie^{(k)}_j & \text{si } i\ne j & 1\le i,j\le N \\
0 & \text{si } i = j & 1\le i,j\le N \\
\end{cases}$$

Con los ceros para eliminar la conexión autorecurrente. Representación matricial de los pesos:

$$W = \begin{bmatrix}
w_{11} & w_{12} & \dots & w_{1N} \\
w_{21} & w_{22} & \dots & w_{2N} \\
\vdots & \vdots & \ddots & \vdots \\
w_{N1} & w_{N2} & \dots & w_{NN} \\
\end{bmatrix}$$

Las informaciones que debe aprender la red son:

$$\begin{align}
E_1 &= \left[e^{(1)}_1 \ e^{(1)}_2 \ \dots \ e^{(1)}_N  \right] \\
E_1 &= \left[e^{(2)}_1 \ e^{(2)}_2 \ \dots \ e^{(2)}_N  \right] \\
&\ \ \vdots \\
E_1 &= \left[e^{(M)}_1 \ e^{(M)}_2 \ \dots \ e^{(M)}_N  \right] \\
\end{align}$$

Tal que el aprendizaje es:

$$W = \sum_{k=1}^M \left[E^T_k E_k - I\right]$$

Luego se presenta un patrón nuevo y se calcula:

$$\begin{align}S(t+1) &= E_d \cdot W \\
E_d &= S(t+1)\end{align}$$

Y se repite este proceso hasta que $S(t)=S(t+1)$. Si existe una repetición $S(t)=S(t+n)$ con $n\gt 1$ entonces la red no se estabiliza.

Estos modelos no clasifican, sino que **encuentran patrones similares**. Si se almacenan demasiados patrones en una red de Hopfield, la red puede no estabilizarse o incluso estabilizarse en patrones desconocidos.

## Condiciones de Recuperabilidad

Siendo la **capacidad** la cantidad de patrones que esta red puede almacenar, se conoce que:

$$\text{Capacidad} = \begin{cases}0.138 \cdot N & \text{para una recuperación buena} \\
\frac{N}{4 \ln (N)} & \text{para una recuperación perfecta}
\end{cases}$$

Se observa que este modelo es ineficiente: requiere muchas neuronas para almacenar pocos patrones. 

Esto no garantiza obtener una salida correcta estable si los patrones no son lo suficientemente diferentes entre sí. Para ello surge la **ortogonalidad**: se recomienda que la diferencia entre patrones sea al menos del 50%, calculada como:

$$\sum_{i=1}^N e^{(k)}_i \cdot e^{(k)}_i \le 0 \ \ \ \ \ \ \forall \ k \ne m$$
