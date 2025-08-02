Una **gramática formal** es una cuaterna $G = (N,T,P,\Sigma)$ tal que:

- $N$ es un conjunto finito de símbolos no terminales.
- $T$ es un conjunto finito de símbolos terminales. Sea $N \cap T = \phi$.
- $P$ es un conjunto finito de producciones.
- $\Sigma$ es un símbolo _sentencia_ o _elemento distinguido_, siendo $\Sigma \notin (N \cup T)$. Se considera que este es el nodo raíz del arbol de la gramática.

Cada **producción** en $P$ es un par ordenado de strings $(\alpha, \beta)$ donde $\alpha = \varphi A \psi$, $\beta = \varphi \omega \psi$, $\varphi,\omega\psi \in (N \cup T)^*$ y $A \in N \cup \set{\Sigma}$. Cada producción se escribe de la forma $\alpha \rightarrow \beta$, es decir que se cambia $A$ por $\omega$.

Si se cambia $A$ por $\lambda$ (siendo $\lambda$ el string vacío tal que $|\lambda|=0$), es decir que se borra un símbolo, se dice que hubo una _contracción_. Esto solo puede suceder en las gramáticas de tipo $L_0$ ([[Jerarquía de Chomsky]]). Esa capacidad de contracción distingue a las gramáticas de tipo $L_0$ de las de tipo $L_1$.

Un string de símbolos en $(N\cup T)^* \cup \set{ \Sigma}$ se conoce como forma sentencial. Sean formas sentenciales $\alpha \rightarrow \beta \in P$, $\omega = \varphi \alpha \psi$, y $\omega' = \varphi \beta \psi$. $\omega '$ se deriva inmediatamente de $\omega$ en $G: \omega \implies \omega '$. Si es derivable: $\omega_1 \overset * \implies \omega_n$.

El **lenguaje** $L(G)$ generado a partir de la gramática formal $G$ es el conjunto de strings terminales derivables a partir de $\Sigma$: $L(G)=\set{\omega \in T^* / \Sigma \overset * \implies \omega }$.

> Si a la izquierda se tiene más de un símbolo, entonces se trata de una gramática $L_0$ o $L_1$, ya que tiene contexto.

Ejemplo: sea la gramática $G_1: N = \set{A,B,C}, T+\set{a,b,c}, P: \Sigma \rightarrow A$ con estas producciones:

$$
\begin{align}
A &\rightarrow aABC \\
A &\rightarrow abC \\
CB &\rightarrow BC \\
bB &\rightarrow bb \\
bC &\rightarrow bc \\
cC &\rightarrow cc
\end{align}
$$

Strings que puede generar: `abc`, `aabbcc`, `aaabbbccc`, `aaaabbbbcccc`, etc. El lenguaje generado es $L(G_1) = \set{ a^k b^k c^k \ge 1}$. Se observa que $a^k b^k c^k$ es una correspondencia triple ya que cada símbolo debe aparecer la misma cantidad de veces. Se considera que la gramática $G_1$ es de tipo $L_1$ porque un autómata pushdown ($L_2)$ no puede manejar correspondencias triples (solo puede manejar correspondencias dobles anidadas) y no existen contracciones por lo que no se necesita un $L_0$.

Si una gramática permite llegar al mismo string por diferentes derivaciones, se dice que es una _gramática ambigüa_. No siempre se puede solucionar el problema de la ambigüedad.

## Tipos de Gramáticas

Dado $A \in N \cup \set{ \Sigma}$, $B \in N$, $a\in T$, $\varphi, \omega, \psi \in (N \cup T)^*$:

![[Tipos de Gramáticas.png]]

En resumen:

- Las tipo $0$ tienen producciones $P$ con contracción.
- Las tipo $1$ son similares a las tipo $0$ excepto que no producen contracción.
- Las tipo $2$ ya son libres de contexto porque sus producciones no presentan $\varphi$ y $\psi$.
- Las tipo $3$ solo permiten producciones por derecha ($A \rightarrow aB$) o por izquierda ($A\rightarrow Ba$).

Si $G$ es gramática regular, entonces $L(G)$ es lenguaje regular.

## Ambigüedad

Existe **ambigüedad** cuando para determinado string, la gramática provee árboles de derivación distintos. Es un problema que no siempre se soluciona, y no existe un método para solucionarlo.

Existen lenguajes _inherentemente ambiguos_ que no pueden ser generados por una gramática no ambigua. No hay manera de decidir si un $L(G)$ es inherentemente ambiguo. Por ejemplo, $L=\set{aîb^jc^k / i=j \lor j = k}$ es inherentemente ambiguo.

Una **derivación** se indica como $\varphi A \psi \implies \varphi B_1B_2\dots B_n \psi$ mediante $A\rightarrow B_1B_2\dots B_n$ donde $A \in (N\cup \set{\Sigma}) \ \land \ B_i \in (N\cup T)$. Una derivación $\omega_0 \implies \omega_1 \implies \dots \implies \omega_n$ es derivación por izquierda sí y solo sí el símbolo no terminal ubicado más a la izquierda de $\omega_i$ es reemplazado para obtener $\omega_{i+1}$. Esto se verifica para $0\le i\le n$ Formalmente:

$$\omega_i = \alpha A \beta , \omega_{i+1}=\alpha\omega\beta \text{ con } \alpha \in T^*,\ A \in N,\ \beta \in (N\cup T)^*,\ A\rightarrow \omega \in P$$

Un _árbol de derivación_ solo sirve para gramáticas de tipo 2 o 3 porque no muestran el orden de derivación. Hay una correspondencia 1 a 1 entre derivaciones por izquierda y árboles de derivación. Si existen dos derivaciones por izquierda que dan el mismo string, existe ambigüedad.
