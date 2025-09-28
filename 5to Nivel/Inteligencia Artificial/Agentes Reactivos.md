Dentro de las arquitecturas concretas de [[Agentes]], las **arquitecturas reactivas** en su variante con _subsumpción_ o inclusión en una categoría son las más representativas. Todas las acciones se corresponden con las percepciones. A diferencia de los [[Agentes Basados en Lógica]], en este caso los **comportamientos están jerarquizados**.

El algoritmo de acción consiste en ejecutar el primer comportamiento disparado y no inhibido por otros comportamientos disparados de mayor prioridad. Las capas bajas de comportamiento son más prioritarias. El símbolo $\prec$ representa una _relación de inhibición_: $b_1 \prec b_2$ se lee "$b_1$ inhibe a $b_2$".

$$
\begin{aligned}
&\textbf{function } action(p : P) : A \\[6pt]
&\textbf{var } fired : \wp(R) \\
&\textbf{var } selected : A \\[6pt]
&\textbf{begin} \\[6pt]
&\qquad fired := \{ (c,a) \mid (c,a) \in R \;\wedge\; p \in c \} \\[6pt]
&\qquad \text{for each } (c,a) \in fired \text{ do} \\
&\qquad\qquad \text{if } \neg (\exists (c',a') \in fired \text{ such that } (c',a') \prec (c,a)) \text{ then} \\
&\qquad\qquad\qquad \textbf{return } a \\
&\qquad\qquad \text{end-if} \\
&\qquad \text{end-for} \\[6pt]
&\qquad \textbf{return } null \\[6pt]
&\textbf{end function } action
\end{aligned}
$$

Estos agentes tienen dos características:

1. **Cumplimiento de tareas**: cada comportamiento es una acción: $\text{situación} \rightarrow \text{acción}$.
2. **Categorías de comportamiento**: dadas por la jerarquía de subsumpción.

Estos agentes son simples y tienen capacidad social pero no aprenden de la experiencia.
