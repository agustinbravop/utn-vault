Los **árboles de decisión** son un modelo de [[Inteligencia Artificial]] de clasificación que usa [[5to Nivel/Inteligencia Artificial/Aprendizaje|Aprendizaje]] supervisado. Tienen _nodos de decisión_ (que intentan clasificar un ejemplo) y nodos _hoja_ (que aplican una clase).

![[Árboles de Decisión.png]]

**El árbol se construye particionando el conjunto de entrenamiento con tal de encontrar subconjuntos disjuntos lo más puros posibles** (aquellos cuyos ejemplos son de la misma clase). Los caminos generados en el árbol son mutuamente excluyentes y exhaustivos.

El $(X/Y)$ debajo de cada clase representa que $X$ de cada $Y$ ejemplos del conjunto de entrenamiento que llegan a ese nodo hoja tienen la clase del nodo hoja. Indica la _pureza_ del subconjunto. Esto se puede relacionar al [[Modelo de Reglas de Asociación]], donde $X$ representa el **conteo de soporte** y $X/Y$ representa la **confianza**. Por lo general sucede que $X\lt Y$.

Un árbol de decisión puede convertirse en un conjunto de reglas _si-entonces_. El problema es que no se pueden encontrar todas las reglas, por lo que solo se obtienen un subconjunto de todas las reglas posibles.

Se pueden crear muchos árboles de decisión a partir del mismo dataset. La cuestión es encontrar el que tenga mejor precisión y sea más fácil de entender. Siempre es conveniente el árbol de decisión que sea más útil para el usuario.

Existen muchos algoritmos para construir árboles de decisión. El más representativo es el **C4.5** de Quinlan. Este algoritmo asume que los datos son discretos. Es recursivo. En términos simples, siendo $D$ un conjunto de ejemplos, $A$ un conjunto de atributos, y $T$ un nodo actual:

1. Si $D$ es puro o $A=\varnothing$, hacer $T$ un nodo hoja etiquetado con la clase $c_j$ más común en $D$.
2. Sino, evaluar la impureza de $D$ ($p_0$) y la impureza que cada atributo de $A$ contribuye ($p_1$) para elegir el atributo $A_g$ que da la mayor reducción de impureza según $p_0-p_1$. Si $A_g$ reduce la impureza por encima de un _threshold_, entonces $T$ será un nodo de decisión sobre $A_g$ con una rama por cada valor distinto de $A_g$ y se debe particionar $D$ en un subconjunto disyunto por cada valor distinto de $A_g$ para hacer la llamada recursiva $\text{decisionTree}(D_j, A-\set{A_g},T_j)$.

$$
\begin{aligned}
&\textbf{Algorithm } \text{decisionTree}(D, A, T) \\[6pt]
&\textbf{if } D \text{ contains only training examples of the same class } c_j \in C \;\textbf{then} \\[6pt]
&\qquad \text{make } T \text{ a leaf node labeled with class } c_j; \\[6pt]
&\textbf{elseif } A = \varnothing \;\textbf{then} \\[6pt]
&\qquad \text{make } T \text{ a leaf node labeled with } c_j, \text{ the most frequent class in } D \\[6pt]
&\textbf{else} \quad \\[6pt]
&\qquad p_0 \gets \text{impurityEval-1}(D); \\[6pt]
&\qquad \textbf{for each } A_i \in A(=\{A_1, A_2, \dots, A_k\}) \;\textbf{do} \\[6pt]
&\qquad\qquad p_i \gets \text{impurityEval-2}(A_i, D); \\[6pt]
&\qquad \textbf{endfor} \\[6pt]
&\qquad \text{Select } A_g \in \{A_1, A_2, \dots, A_k\} \text{ that gives the biggest impurity reduction,} \\
&\qquad\qquad \text{computed using } p_0 - p_i; \\[6pt]
&\qquad \textbf{if } p_0 - p_g < threshold \;\textbf{then} \\[6pt]
&\qquad\qquad \text{make } T \text{ a leaf node labeled with } c_j, \text{ the most frequent class in } D; \\[6pt]
&\qquad \textbf{else} \\[6pt]
&\qquad\qquad \text{Make } T \text{ a decision node on } A_g; \\[6pt]
&\qquad\qquad \text{Let the possible values of } A_g \text{ be } v_1, v_2, \dots, v_m. \\
&\qquad\qquad \text{Partition } D \text{ into } m \text{ disjoint subsets } D_1, D_2, \dots, D_m \text{based on the } m \text{ values of } A_g. \\[6pt]
&\qquad\qquad \textbf{for each } D_j \in \{D_1, D_2, \dots, D_m\} \;\textbf{do} \\[6pt]
&\qquad\qquad\qquad \textbf{if } D_j \neq \varnothing \;\textbf{then} \\[6pt]
&\qquad\qquad\qquad\qquad \text{create a branch (edge) node } T_j \text{ for } v_j \text{ as a child node of } T; \\[6pt]
&\qquad\qquad\qquad\qquad \text{decisionTree}(D_j, A - \{A_g\}, T_j) \\[6pt]
&\qquad\qquad\qquad \textbf{endif} \\[6pt]
&\qquad\qquad \textbf{endfor} \\[6pt]
&\qquad \textbf{endif} \\[6pt]
&\textbf{endif} \\[6pt]
&\textbf{endif}
\end{aligned}
$$

**El éxito de la construcción del árbol depende de la evaluación de la pureza**. Dos de las _funciones de impureza_ más utilizadas son la _ganancia de información_ y la _tasa de ganancia de información_. Ambas están basadas en la _entropía_:

$$\text{entropy}(D)=-\sum_{j=1}^{|C|} Pr(c_j) \log_2 Pr(c_j)$$

Usando entropía:

$$
\begin{align}
\text{impurityEval-1}(D): \text{entropy}(D)&=-\sum_{j=1}^{|C|} Pr(c_j) \log_2 Pr(c_j) \\[8pt]
\text{impurityEval-2}(D,A_i): \text{entropy}_{A_i}(D)&=-\sum_{j=1}^{v} \frac{|D_j|}{|D|} \times \text{entropy}(D_j) \\[8pt]
\text{gain}(D,A_i) &= \text{entropy}(D) - \text{entropy}_{A_i}(D) \\[8pt]
\text{gainRatio}(D, A_i) &= \frac{\text{gain}(D, A_i)}{- \sum_{j=1}^{s} \left( \frac{|D_j|}{|D|} \times \log_{2}\frac{|D_j|}{|D|} \right)}
\end{align}
$$

La ganancia de información es buena medida siempre que no haya un atributo con muchos valores distintos en proporciones muy distintas, ya que es sensible a valores "sobre-representrados". En esos casos conviene usar la tasa de ganancia de información.

Cambiar la función de impureza puede afectar los árboles generados.

Un árbol de decisión construido con atributos continuos representa un particionamiento del espacio de datos.
