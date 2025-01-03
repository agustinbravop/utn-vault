En la [[Teoría de la Probabilidad]], sea $E_1, E_2, \dots, E_n$ en un sistema completo de sucesos tales que:

$$P(E_1 \cup E_2 \cup \dots \cup E_n) = P(\Omega) = 1 \ \land \ P(E_i \cap E_j) = 0 \ \land \ P(E_i) \gt 0 \text{ con } i = 1, 2, \dots, n$$
![[Probabilidad Total.png]]

Sea un evento $A$ asociado a cada $E_i$ tal que $A = (E_1 \cap A) \cup (E_2 \cap A) \cup \dots \cup (E_n \cap A)$, por lo que su probabilidad de ocurrencia, aplicando la [[Teoría de la Probabilidad#Regla de la Suma|regla de la suma]], es:

$$
\begin{align}
P(A) &= P[(E_1 \cap A) \cup (E_2 \cap A) \cup \dots \cup (E_n \cap A)] \\
&= P(E_1)P(A/E_1) + \dots + P(E_n)P(A/E_n) \\
P(A) &= \sum_{i=1}^n P(E_i)P(A/E_i)
\end{align}
$$

Donde $P(A)$ es la _probabilidad total_.
