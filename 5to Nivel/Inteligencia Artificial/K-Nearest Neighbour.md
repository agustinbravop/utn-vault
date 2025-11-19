KNN es un algoritmo de [[Inteligencia Artificial]] que clasifica datos por proximidad.

Existen métodos de **lazy evaluation** que no tienen un proceso previo de entrenamiento, sino que intentan clasificar recién cunado llega una nueva instancia. Estos métodos lazy se caracterizan por tres propiedades:

1. Evaluación posterior a la llegada de una instancia.
2. Clasificación de acuerdo a instanias similares.
3. Necesitan representar las instancias en espacios $r$-dimensionales.

El algoritmo tiene dos etapas:

$$
\begin{aligned}
&\textbf{Training algorithm } \\[6pt]
&\qquad\textbf{for each training example } <x,f(x)>: \\[4pt]
&\qquad\qquad \text{add the example to the list training\_examples} \\[4pt]
\end{aligned}
$$

$$
\begin{aligned}
&\textbf{Classification algorithm } \\[6pt]
&\qquad\text{given a query instance $x_q$ to be classified:} \\[4pt]
&\qquad\qquad \text{let $x_1 \dots x_k$ denote the $k$ instances from training\_examples that are nearest to $x_q$} \\[4pt]
&\qquad\qquad \text{return $\hat f(x_q) \longleftarrow \underset{v\in V} {\text{argmax}} \sum^k_{i=1} \delta (v, f(x_i))$} \\[4pt]
&\qquad\qquad\qquad \text{where $\delta(a,b)=1$ if $a=b$ and where $\delta(a,b)=0$ otherwise.} \\[4pt]
\end{aligned}
$$

Una variante de KNN es el KNN ponderado.
