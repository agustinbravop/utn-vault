En los [[Códigos]], la **distancia de Hamming** es el número de posiciones en las que las palabras $u$ y $w$ difieren entre sí, tal que:

$$A^n \times A^n \overset d \rightarrow \Bbb Z \subseteq \Bbb R \ \ ; \ \ (u, w) \rightarrow d(u,w)$$

Donde se verifica que la distancia de Hamming $d$ es una **métrica**, debido a sus propiedades:

- $d(u,w) \ge 0$
- $d(u,w)=0 \iff u=w$.
- $d(u,w) = d(w,u)$$.
- $d(u,v) \le d(u,w)+d(w,v)$.

Se dice la *distancia mínima* de un código $C$ a $d(C) = \min \set{d(u,v)/u,v \in C, u \ne v}$.

Un código $C$ es *$t$-detector* si el número de errores $k$ es $1\le k\le t$ y la palabra resultante no es del código. Es *exactamente $t$-detector* si además no es $(t-1)$-detector.

Un código $C$ es *$t$-corrector* si la decodificación permite corregir todos los errores de tamaño $t$ o menor en una palabra. $C$ es *exactamente $t$-corrector* $\iff d(C) = 2t+1 \ \lor \ 2t+2$.

Se usa la nomenclatura $(n, m, d)$-código, donde $n$ es la longitud, $m$ el tamaño, y $d$ la distancia.
