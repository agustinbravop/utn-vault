Un **aceptor de estado finito** es un tipo de [[Autómata de Estado Finito]] $M=(Q,S,P,I,F)$ donde:

- $I\subseteq Q$ son los estados iniciales.
- $F\subseteq Q$ son los estados finales.
- $P\subseteq Q \times S \times Q$ es la relación de transición de $M$. Puede tener un comportamiento no determinístico.
- Si $(q,s,q') \in P$ entonces se da $q \overset s \rightarrow q'$ que es una _transición_ de $M$.

$M$ _acepta_ un string $\omega \in S* \iff : q\overset \omega \implies q'$ para algún $q\in I$ y algún $q'\in F$. El lenguaje reconocido por $M$ es $L(M) = \set{\omega \in S* / q \overset \omega \implies q' ; q \in I ; q'\in F}$.

Si las transiciones $P$ de $M$ constituyen una función $P: Q\times S \rightarrow Q$ y si $M$ tiene exactamente un estado inicial, $M$ es un aceptor de estados finitos **determinístico**.

## Conversión a Aceptores Determinísticos

Podemos imaginar que la $M$ en cierto instante ante cierta entrada se encuentra en cierta combinación de estados.

Dado el AEF no determinístico $M_n = (Q_n, S, P_n, I_n, F_n)$ se construye el AEF determinístico $M_d = (Q_d,S,P_d,I_d,F_d)/L(M_n)=L(M_d)$. Sea $X_{[\omega]} = \set{q'\in Q_n / q \overset \omega \implies q' \text{ para algún } q \in I_n}$ el conjunto de los estados alcanzables de $M_n$ para el string de entrada $\omega$. Para $\lambda: X_{[\lambda]} = I_n$.

Dado $X_{[\phi]}$ se tiene $X_{[\phi s]}=\set{q'\in Q_n / q'' \overset s \rightarrow q' \text{ para algún } q'' \in X_{[\phi]}}$ por lo que $X_{[\phi s]}$ solo depende de $X_{[\phi]}$ y de $s\in S$.

El número de conjuntos alcanzables $X_{[\omega]}$ distintos es finito y $X_{[\omega]} \subseteq Q_n$. Los $I_d$ de $M_d$ corresponden a los $X_{[\omega]}$ que contienen estados finales de $M_n$. $I_n = X_{[\lambda]} \implies I_d = \set{X_{[\lambda]}}$.

$F_d = \set{X \in Q_d / X \cap F_n \ne \phi}$ son los conjuntos alcanzables que tienen un $q_F \in F_n$.

El estado $X'$ es s-sucesor de $X$ en $M_d$ sí y solo sí $X'$ consiste de los s-sucesores en $M_n$ de $X$: $X \overset s \rightarrow X' \text{ en } M_d \iff X' = \set{ q' / q\overset s \rightarrow q ' \text{ en } M_n \text{ para } q \in X}$.

> [!info] Teorema
>
> Por cada AEFND $M_n$ se puede construir un AEFD $M_d$ tal que $L(M_d) = L(M_n)$.

## AEF con Transiciones Lambda

Un AEF-$\lambda$ es un aceptor de estados finitos no determinístico $M=(Q,S,P,I,F)$ en el que $P:Q\times (S\cup \set{\lambda}) \rightarrow \delta (Q)$.

### Equivalencia entre AEF-$\lambda$ y AEFND

> [!info] Teorema
>
> Dado un AEF-$\lambda$ se puede construir un AEFND equivalente tal que $L(M)=L(M')$.

Sea $\lambda[q] = \set{q} \cup \set{q'\in Q / q \overset \lambda \rightarrow \dots \overset \lambda \rightarrow q' \text{ en } M}$ o $\lambda [q] = \set{q} \cup \lambda [q'] \ \forall \ q' \in P(q,\lambda)$. Nótese que generalmente $\lambda [q] \ne P(q, \lambda)$.

Por definición: $q \in \lambda [q] \implies \lambda [\phi] =  \phi ; \lambda [ \set{ q_1, \dots , q_k}] = \lambda[q_1]\cup \dots \cup\lambda[q_k]$.

Procedimiento de construcción: sea $M'=(Q,S,P',I,F')$ donde $P ': Q \times S \rightarrow \delta (Q)$ es tal que $P'(q,s)=\lambda[P(\lambda [q],s)]$. Así, $M'$ simula todas las transiciones $\lambda$ de $M$ teniendo en cuenta todos los posibles caminos. Se obtiene $F'=\set{q\in Q / \lambda [q] \cap F \ne \phi}$. Los estados de aceptación de $M'$ incluye los de $M$ y los $q$ que llegan a un $q_F$ con transiciones $\lambda$.
