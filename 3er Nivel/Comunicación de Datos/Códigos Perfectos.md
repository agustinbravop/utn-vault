En [[Códigos]], sea $A$ un alfabeto con $|A|=q$, $v \in A^n$, $r \in \Bbb R$, y $r \ge 0$ tal que:

$$S_q(v,r)=\set {w \in A^n/ d(v,w)\le r}$$

Donde $S_q$ es una _esfera_ de radio $r$ y centro $v$ con volumen $|S_q(v,r)| = V_q(n,r)=\sum_{k=0}^r \left(n \atop k \right) (q-1)^k$.

Teniendo $C \subseteq A^n$, se define el _radio de empaquetamiento_ de $C$ como el mayor entero $r$ tal que todas las esferas de radio $r$ son disjuntas. El _radio de recubrimiento_ es el menor entero $s$ tal que la unión de todas las esferas de radio $s$ es $A^n$. Se tiene $r=\text{pr}(C)$ y $s = \text{cr}(C)$.

- $C$ es $t$-corrector $\iff$ las esferas $S_q(v,t)$ de radio$t$ con $v \in C$ son disjuntas.
- $C$ es exactamente $t$-corrector $\iff t=\text{pr}(C)$.
- $C$ es _perfecto_ $\iff \text{pr}(C) = \text{cr}(C)$, es decir, existe un $r$ tal que $S_q$ son disjuntas y recubren $A^n$.

**Condición de Empaquetamiento de Esferas**: sea $C$ un $(n,m,d)$-código $q$-ario. $C$ es perfecto sí y solo si $d=2t+1$ (es impar) y $n \cdot V_q(n,t)=q^n$.

**Tasa de Corrección de Errores**: sea $C$ un $(n,m,d)$-código: $\delta(C) = \frac{\lfloor\frac{ d-1}{2}\rfloor}{n}$. La tasa de corrección de errores $\delta$ es el número de errores que se corrigen en relación a la longitud de las palabras.

Sea $A_q(n,d) =\text{max} \set { m/\exists \ (n,m,d)\text{-código} \ q\text{-ario}}$ tal que un $(n, A_q(n,d), d)$-código es _optimable_.

**Problema Principal de la Teoría de Códigos**: determinar la cota de Singleton $A_q(n,d) \le q^{n-d+1}$.

**Teorema del Canal Ruidoso**: nos dice que existen buenos códigos, pero no nos dice cómo obtenerlos.

La capacidad de un BSC con probabilidad de paso $p$ es $C(p) = 1 + p \cdot \log_2 p + (1-p) \cdot \log_2 (1-p)$. Si $R(C) \lt C(p) \implies \forall \varepsilon \gt 0 \exists$ un $(n,m)$-código $C' / R(C')\ge R(C) \ \land \ p_{C'} \lt \varepsilon$. Podemos mejorar la tasa de transmisión hasta alcanzar la **capacidad** del BSC.
