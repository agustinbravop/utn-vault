Una [[Gramáticas Libres de Contexto|GLC]] $G=(N,T,P,\Sigma)$ está en **forma normal** si cada producción tiene la forma:

$$\begin{cases}\Sigma \rightarrow \lambda & A\rightarrow BC\\ \Sigma \rightarrow A & A\rightarrow a\end{cases} \  \ \ \begin{cases}A,B,C \in N \\ a \in T\end{cases}$$

Cada paso extiende en uno la longitud o genera un símbolo terminal, asegurando que para un string de longitud $n$ se requieren exactamente $2n$ pasos de derivación. Dada una GLC cualquiera, se puede construir con expansiones una GFN fuertemente equivalente.

Sea $CC(A,\omega)$ la función recursiva que verifica si $A\implies\omega$. Existe un algoritmo de [[Análisis Sintáctico]] $CC(A,\omega)$ que funciona de la siguiente manera:

1. Si $|\omega| \gt 1$, dividirlo en $\varphi$ y $\psi$, $\omega = \varphi\psi$. Para cada regla de la forma $A\rightarrow UV$, intentar $CC(U,\varphi)$ y $CC(V,\psi)$.
2. Si $|\omega|=1$, buscar una regla $A\rightarrow \omega$.

## Análisis Sintáctico CYK

La forma normal permite aplicar el algoritmo de análisis sintáctico CYK (Cocke-Younger-Kasami), el cual dado un string $\omega$ y una GLC $G$ en forma normal permite decidir si $\omega \in L(G)$. Procedimiento:

$$
\begin{align}
&\text{Para } i=1\dots n \text{ hacer}  \\
&\ \ \ \ t_{i1}=\set{A/A\rightarrow a_i} \\
&\text{Para } j=2\dots n \text{ hacer}  \\
&\ \ \ \ \text{Para } i=1\dots (n-j+1) \text{ hacer}  \\
&\ \ \ \ \ \ \ \ t_{ij}=\phi \\
&\ \ \ \ \ \ \ \ \text{Para } k=1\dots (j-1) \text{ hacer}  \\
&\ \ \ \ \ \ \ \ \ \ \ \ t_{ij}=t_{ij} \ \cup \ \set{A/A\rightarrow BC, \text{ con } B \in t_{ik} \text { y } C \in t_{i+kj-k}} \\
&\text{Si } \Sigma \rightarrow S \text{ y } S \in t_{1n} \text{ entonces } \omega \in L(G)
&\end{align}
$$
