Sea $G$ una GLC con las siguientes definiciones:

- **Regla $A$ de $G$**: $A\rightarrow \alpha$.
- ***Handle***: $x$ en $A\rightarrow x\beta$.
- **Producción útil**: $A\rightarrow \alpha$ es útil $\iff \Sigma \overset * \implies \varphi A \psi \implies \varphi \alpha \psi \overset * \implies \omega$ con $\omega \in T^*$.
- **No terminal útil**: $A$ es útil $\iff$ es parte izquierda de una producción útil.
- **Producción no generativa**: $A\rightarrow B$.
- **No terminal recursivo por izquierda**: $A$ en $A\overset * \implies A \psi$.
- **No terminal recursivo por derecha**: $A$ en $A\overset * \implies \psi A$.
- **No terminal cíclico**: $A \overset * \implies A$. Es causado por producciones no generativas.

## Transformaciones Gramaticales

Dos GLC $G_1$ y $G_2$ son *débilmente equivalentes* si $L(G_1)=L(G_2)$. $G_1$ y $G_2$ son *fuertemente equivalentes* si son débilmente equivalentes y para cada string terminal $\omega$ las derivaciones por izquierda mínimas de $\omega$ en $G_1$ tienen una correspondencia uno a uno con las de $G_2$. Una derivación es *mínima* si ninguna forma sentencial se repite en la derivación.

### Sustitución

Sea $A\rightarrow \varphi B \psi$ y $B \rightarrow \beta_1,\beta_2,\beta_3,\dots,\beta_n$, la $G'$ es obtenida por sustitución de acuerdo a:

1. $A\rightarrow \varphi B \psi$ no está en $G'$.
2. Todas las otras producciones están en $G'$.
3. Cada $A\rightarrow \varphi \beta_i \psi$ está en $G'$ con $i=1,2,3,\dots,n$.

Si ninguna producción de $G'$ introducida por la regla 3 ha sido previamente introducida por la regla 3, $G$ y $G'$ son fuertemente equivalentes. Se puede perder la equivalencia fuerte si se introduce por sustitución una producción duplicada.

### Expansión

Sea $A\rightarrow \varphi \psi$ con $\varphi, \psi \in (N\cup T)^* -\lambda$, se la reemplaza por una de dos opciones:

- $A\rightarrow X\psi \ , \ X\rightarrow \varphi$, o
- $A\rightarrow \varphi X \ , \ X\rightarrow \psi$.

Siendo $X$ un nuevo no terminal. Se dice que se expandió la regla $A\rightarrow \varphi \psi$. Siempre se mantiene la equivalencia fuerte entre $G$ y $G'$. 

Se observa que sustitución y expansión son transformaciones inversas.

### Eliminación de Producciones Inútiles

Sea una producción inútil $A\rightarrow \alpha / \cancel \exists \Sigma \overset * \implies \varphi A \psi \implies \varphi \alpha \psi \overset * \implies \omega$ con $\omega \in T^*$.

Para eliminar producciones inútiles, se puede utilizar el **marcado $T$**, que marca cada regla de $G$ si hay una derivación de un string terminal. Las producciones no marcadas nunca terminan, por lo que se eliminan. Pasos:

1. Sean $P_0=N_0=\phi$ con $(i=0)$.
2. Sea $P_{i+1}=\set{A\rightarrow \alpha \in P/\alpha \in (Ni\cup T)^* }$ y $N_{i+1}=\set{A \in N / A \rightarrow \alpha \in P_{ i+1}}$ el marcado de producciones terminables.
3. Repetir hasta que $P_i=P_{i+1}\implies P_{i+1}=P_T$ y $N_{i+1}=N_T$.

Luego se utiliza el **marcado $\Sigma$**, que marca cada regla ya marcada por $T$ si es alcanzable desde $\Sigma$. Si no es alcanzable, se elimina. Pasos:

1. Sea $P_T$ del marcado $T$ y $Q_1=\set{\Sigma\rightarrow \alpha\in P_T}$ con $(i=1)$.
2. Sea $Q_{i+1} = Q_i\cup \set{A\rightarrow\alpha\in P_T/B\rightarrow\varphi A \psi \in Q_i}$ el marcado de producciones alcanzables.
3. Repetir hasta que $Q_i=Q_{i+1} \implies Q_{i+1}=P_\Sigma$.

Aseguramos que cada producción de $P$ como $A\rightarrow \alpha$ es terminable de la forma $\Sigma \overset * \implies \varphi A \psi \implies \varphi \alpha \psi \overset * \implies \omega$. Así, por cada producción de $P$ de $G$ se puede decidir si es o no útil en $G$.

El **test de vacío** dice que para cualquier GLC $G$ es posible decidir si $L(G,A)=\phi \ \forall \ A \in N$. En particular, si la gramática genera o no strings, $L(G) = L(G,\Sigma)=\phi$.

### Eliminación de Producciones No Generativas

Sea la producción no generativa $A\rightarrow B$, se desea eliminarla porque puede causar no terminales cíclicos. Las secuencias de pasos de derivación no generativos consecutivos de $G$ pueden ser representadas por un [[Aceptor de Estado Finito|AEF]] $M(G)$ con solo transiciones lambda.

Sean $G=(N,P,T,\Sigma)$ y $M(G)=(Q,\phi,P',I,F)$ con:

$$\begin{align} Q &= \left\{ A \,\middle/\, A \rightarrow B \text{ ó } B \rightarrow A \in P;\; A, B \in N \right\} \\ P' &= \left\{ A \xrightarrow{\lambda} B \,\middle/\, A \rightarrow B \in P \right\} \\ I &= \left\{ A \in Q \,\middle/\, \Sigma \rightarrow A \in P \ \lor \ B \rightarrow \varphi A \psi \in P \text{ con } \varphi \psi \neq \lambda \right\} \\ F &= \left\{ A \in Q \,\middle/\, A \rightarrow \beta \in P \text{ con } \beta \notin N \right\} \end{align}$$

$G'=(N',T,P'' ,\Sigma)$ incluye un nuevo no terminal por cada secuencia de pasos no generativos en una derivación mínima. Eso en $M(G)$ es un camino sin ciclos.

$$\begin{align}N' = N &\cup \left\{[X_1 \ \dots \ X_n] \ ; X_1 = X \in I, \ X_n = Y \in F, \ X_i \ne X_j \text{ para } i \ne j, X_1 \xrightarrow{\lambda} \dots \xrightarrow{\lambda} X_n \text{ en } M(G) \right\} \\
&\cup \left\{ [X \ X] \;\middle|\; X \in I \cap F \right\}\end{align}$$

Así:

1. Toda producción sin un símbolo de $Q$ es copiada.
2. Por cada producción generativa $A\rightarrow \alpha_0 B_1 \dots V_k \alpha_k$ con $B_i \in Q$ en $G$ surge en $G'$ una producción $U\rightarrow \alpha_0 V_1\dots V_k \alpha_k$ donde:

$$U \in 
\begin{cases}
\{ A \} & \text{si } A \notin F \\
\{ [X \ \dots \ Y] \mid Y = A \} & \text{si } A \in F
\end{cases}
\ \ \ \ \ \ \ \ \ \
V_i \in 
\begin{cases}
\{ B_i \} & \text{si } B_i \notin I \\
\{ [X \ \dots \ Y] \mid X = B_i \} & \text{si } B_i \in I
\end{cases}$$

Se cumple que $G$ y $G'$ son fuertemente equivalentes siempre.

### Factorización por Izquierda

Sean $A\rightarrow\beta \alpha_1 \ \land \ A \rightarrow \beta  \alpha_k$ dos producciones con el mismo *handle* de una misma parte derecha. Esto provoca ambigüedad al diseñar un compilador por izquierda. Para evitarlo, se puede aplicar una factorización por izquierda:

$$\begin{align}
\forall \ A \in N \text{ de } G:& \text{ si }A\rightarrow \beta\alpha_1 , \dots, A\rightarrow\beta\alpha_k \text{ con } k \gt 1, \\
\text{ en } G' \text{ se las cambia por}:& \ A\rightarrow \beta A' \\
&\ A'\rightarrow \alpha_1,\dots,A'\rightarrow \alpha_k \text{ con }  k \ge 1
\end{align}$$

Es un caso especial de expansión, por lo que $G$ y $G'$ son fuertemente equivalentes.

Ejemplo:

$$\begin{align}
G: \Sigma &\rightarrow \lambda \ | \ S \\
S &\rightarrow SS \ | \ (S) \ | \ () \ | \ [S] \ | \ [ \ ] \\
\text{ luego de la}& \text{ factorización por izquierda resulta... } \\
G': \Sigma &\rightarrow \lambda \ | \ S \\
S &\rightarrow SS \ | \ (S' \ | \ [ S'' \\
S' &\rightarrow S) \ | \ ) \\
S'' &\rightarrow S]   \ | \ ]
\end{align}$$

### Eliminación de Producciones $\lambda$

Sea $A\rightarrow \lambda$ una producción lambda. $A$ es *anulable* $\iff A \overset * \implies \lambda$. Se acepta una definición no estricta de una GLC que tenga $A\rightarrow \lambda$ porque es *salvable*.

Identificación de no terminales anulables:

1. Sea $\Delta_1 =\set{A\in N / A \rightarrow \lambda \in P} ; i =1$.
2. Sea $\Delta_{i+1} = \Delta_i \cup \set{A\in N / A \rightarrow \omega \in P \ \land \ \omega \in \Delta_i^*}$.
3. Repetir hasta que $\Delta_i=\Delta_{i+1}  \implies \Delta_1 = \Delta$.

Procedimiento:

$\forall \ A \rightarrow \alpha_1 \dots \alpha_n$ de $G$ se agregan producciones $A\rightarrow \beta_1 \dots \beta_n$ donde $\beta_i \in \begin{cases}\set{\alpha_i} &\text{ si } \alpha_i \notin \Delta \\ \set{\alpha_i,\lambda} &\text{ si } \alpha_i \in \Delta\end{cases}$. Luego, se eliminan todas las producciones $\lambda$. Si $\Sigma \in \Delta \implies \Sigma \rightarrow \lambda \in P'$.

$G$ y $G'$ son fuertemente equivalentes, y toda producción $\lambda$ es *salvable*.

## Formas Canónicas de Gramáticas

Se pueden definir formas restringidas de gramáticas libres de contexto, conocidas como formas canónicas:

- [[Gramáticas Bien Conformadas]].
- [[Gramáticas en Forma Normal]].
