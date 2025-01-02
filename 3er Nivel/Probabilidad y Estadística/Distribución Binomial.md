La [[Distribuciones de Probabilidad de Variable Discreta|distribución]] **binomial** estudiada por el matemático Bernoulli propone un experimento que se realiza $n$ veces de forma independiente con solo **dos sucesos dicotómicos** posibles: $A$ y $\overline A$.

$$P(\text{en $n$ realizaciones se da $x$ veces $A$}) = \left(n \atop x \right) \ p^x q^{n-x}$$

Donde $q = 1-p$, y $\left(n \atop x \right)$ es una combinatoria:

$$\left(n \atop x \right) = \frac{n!}{x! (n-x)!}$$

Sea una secuencia $S_i$ un conjunto de $n$ realizaciones del experimento que resultan en $A$ o $\overline A$:

$$\begin{align}S_1 &= A_1 \cap A_2 \cap \dots \cap A_x \cap \overline A_{x+1} \cap \dots \cap \overline A_n \\
P(S_i) &= P(A_1 \cap \dots \cap \overline A_n) = P(A_1) \dots P(A_x) P(\overline A_{x+1}) \dots P(\overline A_n) \\
P(A)=p \ \land \ P(\overline A) = q \implies P(S_1) &= p^x q^{n-x}
\end{align}
$$

Cualquier otra secuencia $S_i$ con $i \ne 1$ va a tener los mismos sucesos pero en distinto orden, por lo que:

$$P(\text{en $n$ realizaciones $x$ veces $A$}) = P(S_1 \cup \dots \cup S_j) = P(S_1) + \dots P(S_j) = j \ p^x q^{n-x}$$

Siendo $j$ las permutaciones con repetición de $n$ elementos, o $n$ elementos tomados de a $x$:

$$j = \left( n \atop x \right) = \frac{n!}{x!(n-x)!}$$

## Condición de Cierre

Aplicando el binomio de Newton.

$$\sum_{i=1}^N p_i = 1 \implies \sum_{i=1}^N \left( N \atop i \right) \ p^i q^{N-i} = (p+q)^n = (\cancel p+1- \cancel p)^n = 1^n = 1$$

## Esperanza

$$\begin{align}
E(x) &= \sum_{x=0}^n x_i p_i = \sum_{x=0}^n x_i \left( n \atop x \right) p^x q^{n-x} = \sum_{x=1}^n x \frac{n!}{x!(n-x)!}p^x q^{n-x} \\
\text{haciendo $x!=x(x-1)!$:} \ E(x) &= \sum_{x=1}^n \cancel x \frac{n (n-1)!}{\cancel x (x-1)! [(n-1 - (x-1))]!} p \ p^{x-1} q^{(n-1)-(x-1)} \\
\text{sustituyendo $X=x-1$:} \ E(x) &= n p   \underbrace {\cancel{\sum_{X=1}^N \frac{N!}{X! (N-X)!} p^X q^{N-X}}}_\text{igual a $1$ por condición de cierre} = np \\
E(x) &= np
\end{align}$$

## Varianza

$$V(x) = \sum_{i=1}^N x_i^2 p_i - E(x)^2 = \dots = npq \implies V(x) = npq$$
