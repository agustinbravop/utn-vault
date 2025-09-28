Los modelos de **planificación** de [[Inteligencia Artificial]] diseñan planes para alcanzar una meta.

Estos métodos, dado un espacio de estados, intentan encontrar una secuencia de acciones que lleve el problema desde un estado inicial a un estado objetivo.

Estos sistemas no se preocupan por cómo ejecutar esa secuencia. No se los debe confundir con [[Búsqueda]]. No existe una relación fija entre el orden de la planificación y el orden de la ejecución.

No siempre es posible encontrar un camino de solución.

Hay 3 conceptos clave para evitar la **explosión combinatoria**:

1. Apertura en la representación de estados, objetivos y acciones.
2. Libertad para añadir acciones al plan siempre que sea necesario.
3. Divide y vencerás: generar sub-planes más sencillos.

Los **objetivos** y **estados**son conjuntos de sentencias, y las **acciones** son descripciones lógicas de las pre-condiciones y post-condiciones o efectos. Así, las acciones conectan estados.

## STRIPS

_STanford Research Institute Problem Solver_ es un lenguaje simple para representar estados y acciones.

Los **estados** se representan como conjunciones de literales sin funciones, es decir predicados aplicados a símbolos constantes. Por convención se asume que un literal no presente está negado.

Los **operadores** tienen 3 elementos:

1. Especificación de la acción.
2. Condición previa (pre-condición).
3. Efecto (post-condición).

Un operador $o$ es aplicable a un estado $s$ siempre que en ese estado se puedan concretizar las variables que contiene dicho operador.

Ejemplo de operador:

```
operador(ACCION: Ir(y)
		 PRECOND: En(x) Y Ruta(x, y)
		 EFECTO: En(y) Y -En(x))
```

Representación gráfica:

![[Operador STRIPS (Planning).png]]

Según la estrategia que usan, se tienen:

- **Planificadores de progresión**: aplican operadores partiendo del estado inicial. Tienen el problema de la explosión combinatoria.
- **Planificadores de regresión**: parten del estado objetivo para satisfacer pre-condiciones. Tienen el problema de operadores incompletos.

Una alternativa a buscar a través del espacio de estados es **buscar en el espacio de planes**. Esto involucra operadores de **refinamiento** (eliminan planes) y **modificación** (crean planes potencialmente incorrectos).

Una buena representación de planes asegura una búsqueda eficiente. Los planificadores aplican el **principio de compromiso mínimo**: resolver lo que actualmente sea de interés (un problema a la vez).

Hay planificadores de:

- **Orden parcial**: algunos pasos se ordenan en relación a los demás.
- **Orden total**: incluyen todas las posibilidades.

Formalmente, un plan contiene:

- Un conjunto de pasos del plan.
- Un conjunto de **restricciones de ordenamiento** de pasos del tipo $S_i \prec S_j$.
- Un conjunto de **vínculos causales** $S_i \rightarrow^{(c)} S_j$ (se lee _$S_i$ logra $c$ de $S_j$_).

Una **amenaza** para un vínculo causal es una acción que destruye el efecto del vínculo y que se puede intercalar entre la acción y su efecto. Las amenazas vuelven incompatibles algunos pasos. Se pueden eliminar modificando el orden de los pasos (introduciendo una restricción de orden).

Un plan **completo** es aquel en que cada condición previa de todos los pasos se logra con la ejecución de otro paso, es decir que todas las pre-condiciones se cumplen.

Un plan **linealizado** es aquel con un solo orden posible. Se puede linealizar un plan agregando restricciones de orden.

> Una solución es un plan completo y consistente.

Como ejemplo, sea el siguiente plan inicial para el problema de comprar comida en un supermercado y máquinas en una ferretería:

![[Plan Inicial (Planning).png]]

Una solución sería:

![[Plan Final (Planning).png]]

## Algoritmo POP

El **algoritmo POP** (_Partial Order Planning_) es un planificador de orden parcial que comienza desde un plan inicial mínimo y en cada paso lo extiende logrando una pre-condición $c$ de un paso $S_{need}$ (principio de compromiso mínimo).

$$
\begin{aligned}
&\textbf{function } \text{POP}(initial, goal, operators) \;\textbf{returns} \; plan \\[6pt]
&\qquad plan \gets \text{Make-Minimal-Plan}(initial, goal) \\[6pt]
&\qquad \textbf{loop do} \\[6pt]
&\qquad\qquad \textbf{if } \text{Solution}?(plan) \;\textbf{then return } plan \\[6pt]
&\qquad\qquad S_{need}, \; c \gets \text{Select-Subgoal}(plan) \\[6pt]
&\qquad\qquad \text{Choose-Operator}(plan, operators, S_{need}, c) \\[6pt]
&\qquad\qquad \text{Resolve-Threats}(plan) \\[6pt]
&\qquad \textbf{end} \\[12pt]
\end{aligned}
$$

En $\text{Select-Subgoal}$ se elige un solo objetivo, respetando el principio de compromiso mínimo.

$$
\begin{aligned}
&\textbf{function } \text{Select-Subgoal}(plan) \;\textbf{returns } S_{need}, c \\[6pt]
&\qquad \text{pick a plan step } S_{need} \in \text{Steps}(plan) \\
&\qquad\qquad \text{with a precondition } c \text{ that has not been achieved} \\[6pt]
&\qquad \textbf{return } S_{need}, c \\[12pt]
\end{aligned}
$$

En $\text{Choose-Operator}$ se elige un paso existente o un operador y se agrega el vínculo causal y su restricción de orden asociada. Si se eligió un operador, se crea un nuevo paso que lo aplica.

$$
\begin{aligned}
&\textbf{procedure } \text{Choose-Operator}(plan, operators, S_{need}, c) \\[6pt]
&\qquad \textbf{choose } S_{add} \in operators \;\textbf{or } \text{Steps}(plan) \text{ that has } c \text{ as an effect} \\[6pt]
&\qquad \textbf{if } \text{no such step } \textbf{then fail} \\[6pt]
&\qquad \text{add the causal link } S_{add} \xrightarrow{c} S_{need} \text{ to } \text{Links}(plan) \\[6pt]
&\qquad \text{add the ordering constraint } S_{add} \prec S_{need} \text{ to } \text{Orderings}(plan) \\[6pt]
&\qquad \textbf{if } S_{add} \text{ is a newly added step from operators then} \\[6pt]
&\qquad\qquad add \; S_{add} \; \text{to } \text{Steps}(plan) \\[6pt]
&\qquad\qquad add \; Start \prec S_{add} \prec Finish \; \text{to } \text{Orderings}(plan) \\[12pt]
\end{aligned}
$$

En $\text{Resolve-Threats}$ se introduce una restricción de orden por cada amenaza. Si el plan no resulta consistente, entonces falla el algoritmo.

$$
\begin{aligned}
&\textbf{procedure } \text{Resolve-Threats}(plan) \\[6pt]
&\qquad \textbf{for each } S_{threat} \text{ that threatens a link } S_i \xrightarrow{c} S_j \in \text{Links}(plan) \;\textbf{do} \\[6pt]
&\qquad\qquad \textbf{choose either:} \\[6pt]
&\qquad\qquad\qquad \text{Promotion: Add } S_{threat} \prec S \;\; \text{to } \text{Orderings}(plan) \\[6pt]
&\qquad\qquad\qquad \text{Demotion: Add } S_j \prec S_{threat} \;\; \text{to } \text{Orderings}(plan) \\[6pt]
&\qquad\qquad \textbf{if not } \text{Consistent}(plan) \;\textbf{then fail} \\[6pt]
&\qquad \textbf{endfor} \\[6pt]
&\textbf{end}
\end{aligned}
$$
