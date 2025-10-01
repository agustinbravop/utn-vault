Dentro de las arquitecturas concretas de los [[Agentes]], las arquitecturas basadas en lógica modelan un estado interno con [[Razonamiento]] lógico, de manera que el agente es capaz de tomar decisiones mediante **deducción** gracias a un conjunto $D$ de **predicados**.

$$
\begin{align}
\text {see} &: S \rightarrow P \\
\text {next} &: D \times  P \rightarrow D \\
\text {action} &: D \rightarrow A
\end{align}
$$

El algoritmo para la acción implica buscar la primera regla definida que se deba aplicar. Si no se encuentra una, se busca la primera regla que no está prohibida explícitamente.

$$
\begin{aligned}
&\textbf{function } action(\Delta : D) : A \\[6pt]
&\textbf{begin} \\[6pt]
&\qquad \text{for each } a \in A \text{ do} \\
&\qquad\qquad \text{if } \Delta \vdash_{\rho} Do(a) \text{ then} \\
&\qquad\qquad\qquad \textbf{return } a \\
&\qquad\qquad \text{end-if} \\
&\qquad \text{end-for} \\[6pt]
&\qquad \text{for each } a \in A \text{ do} \\
&\qquad\qquad \text{if } \Delta \nvdash_{\rho} \neg Do(a) \text{ then} \\
&\qquad\qquad\qquad \textbf{return } a \\
&\qquad\qquad \text{end-if} \\
&\qquad \text{end-for} \\[6pt]
&\qquad \textbf{return } null \\[6pt]
&\textbf{end function } action
\end{aligned}
$$

Estos agentes no son inteligentes porque siempre hacen la misma acción ante los mismos datos.
