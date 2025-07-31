En una gramática regular hay una correspondencia entre conjuntos de strings indicados por las letras no terminales de una gramática y ciertos conjuntos de string asociados con los estados de un [[Aceptor de Estado Finito]]. Son alternativas a las [[Expresiones Regulares]].

Dada cualquier gramática, se define su lenguaje $L(G,A)$ como el conjunto de strings terminales:
$$L(G,A)=\set{\omega \in T^* / A \overset * \implies \omega \text{ en } G}$$
Sea $M=(Q,S,P,I,F)$ un AEF. Es conjunto final $E(q)$ el conjunto de strings de entrada que llevan a $M$ desde el estado $q$ hasta un estado de aceptación:
$$E(q)=\set{\omega\in S^* / q \overset \omega \implies q' \text{ con } q' \in F}$$

- Donde $E(q)$ siempre contiene a $\lambda$ siendo $q \in F$.
- Si $q$ no pertenece a $F \implies \lambda \notin E(q)$.
- $\omega$ es admisible $\iff$ existe $q\overset \omega \implies q'$ en $M$ con $q \in I$ y $q'\in F$,

El lenguaje reconocido por $M$ es la unión de todos los $E(q) \ \forall \ q \in I$ (estados iniciales).

Proposición 1: sea $M=(Q,S,P,I,F)$ un AEF y $E(q)$ el conjunto final correspondiente a $q$:

1. $\lambda \in E(q) \iff q \in F$,
2. si $\omega = s\varphi \implies \omega \in E(q) \iff \varphi \in E(q') / q\overset s \rightarrow q'$ en $M$ para algún $q'\in Q$.
3. $L(M) = \underset {q\in I} \cup E(q)$,

Proposición 2: los conjuntos finaes de un AEF $M=(Q,S,P,I,F)$ satisfacen un sistema de ecuaciones lineales de conjuntos por derecha. $\forall q \in Q: E(q) = \underset {q'\in Q} \cup V(q,q') E(q') \cup W(q)$ donde:
$$V(q,q')=\set{s\in S/M \text{ tiene } q \overset s \rightarrow q'} \text{ y } W(q) = \begin{cases} \lambda \text{ si } q \in F \\ \phi \text{ de otra manera} \end{cases}$$

Cada conjunto $V(q,q')$ tiene los símbolos de entrada que llevan a $M$ de $q$ a $q'$. Se pueden desarrollar ecuaciones lineales de conjuntos en las cuales las incógnitas aparecen como máximo una vez en cada término. Al desarrollar un sistema, notar:

- Si $q$ es estado trampa, entonces $E(q) = \phi:$ se pueden eliminar términos que incluyan $E(q)$.
- Si $q$ es estado inaccesible, entonces el conjunto de ecuaciones para $E(q)$ puede ser omitido.

## Tabla: Construcción de una GRLD a partir de un AEF

Dado un AEF $M=(Q,S,P_M,I,F)$ con conjuntos finales $\set{E(q)/q\in Q}$, se puede construir una gramática lineal $G=(N,S,P_G,\Sigma)$ con $N=\set{N(q)/q\in Q}$ tal que $L(G,N(q)) = E(q), q\in Q$.

| Regla | Si $M$ tiene                       | Luego $G$ tiene              | Razón                   |
| :---: | :--------------------------------- | :--------------------------- | :---------------------- |
|   1   | $I \cap F \ne \emptyset$           | $\Sigma \rightarrow \lambda$ | $\lambda \in L(M)$      |
|   2   | $q \in I$                          | $\Sigma \rightarrow N(q)$    | $E(q) \subseteq L(M)$   |
|   3   | $q \xrightarrow{s} q'$, $q' \in F$ | $N(q) \rightarrow s$         | $s \in E(q)$            |
|   4   | $q \xrightarrow{s} q'$             | $N(q) \rightarrow sN(q')$    | $E(q) \supseteq sE(q')$ |

Las secuencias de estados en $M$ desde $q\in I$ hasta $q'\in F$ tienen una correspondencia uno a uno con las derivaciones de strings terminales a partir de $\Sigma$ en $G$.

## Tabla: Construcción de un AEF a partir de una GRLD

Es el proceso inverso. Dada una gramática lineal $G=(N,T,P_G,\Sigma)$, se puede construir un AEF $M=(Q,T,P_M,I,\set{q_F})$ con $Q=\set{q_A / A \in N} \cup \set{q_F}$ y conjuntos finales $\set{ E(q) / q \in Q}$ tal que $L(G,a) = E(q_A)$ para $A \in N \cup \set{\Sigma}$.

| Regla | Si $G$ tiene             | Luego $M$ tiene                     | Razón                             |
|:-----:|:-------------------------|:------------------------------------|:----------------------------------|
| 1     | $\Sigma \rightarrow \lambda$     | $q_F \in I$                        | $\lambda \in L(G)$                |
| 2     | $\Sigma \rightarrow A$           | $q_A \in I$                        | $L(G, A) \subseteq L(G)$          |
| 3     | $A \rightarrow s$                | $q_A \xrightarrow{s} q_F$          | $s \in L(G, A)$                   |
| 4     | $A \rightarrow sB$               | $q_A \xrightarrow{s} q_B$          | $L(G, A) \supseteq sL(G, B)$      |

## Equivalencia entre GRLD y GRLI

Se establece una correspondencia uno a uno entre todas las producciones de $G$ y $G'$ de forma que una derivación $\Sigma \implies s_1 A_1 \implies \dots \implies s_1\dots s_kA_k\implies s_1\dots s_ks_{k+1}$ en $G$ corresponde a $\Sigma \implies A_k s_{ s+1}\implies \dots \implies A_1 s_2 \dots s_k s_{k+1} \implies s_1 s_2 \dots s_k s_{k+1}$ en $G'$ y por lo tanto $L(G)=L(G')$.

| Si $G$ tiene          | Luego $G'$ tiene      |
|:----------------------|:----------------------|
| $\Sigma \rightarrow sA$  | $A \rightarrow s$       |
| $A \rightarrow sB$       | $B \rightarrow As$      |
| $A \rightarrow s$        | $\Sigma \rightarrow As$ |
| $\Sigma \rightarrow s$   | $\Sigma \rightarrow s$  |
| $\Sigma \rightarrow \lambda$ | $\Sigma \rightarrow \lambda$ |

Se define el conjunto inicial $B(q)=\set{ \omega / q' \overset \omega \implies q , q' \in I}$ de forma que $L(G, N(q)) = B(q)$ para una GRLI con $N = \set{N(q) / q \in Q}$.
