Sea $V$ un alfabeto finito, una expresión regular en $V$ es un string finito compuesto por símbolos del conjunto $\set{q\in Q / \lambda [q] \cap F \ne \phi}$ y se forma de acuerdo a:

- $\lambda$ es una expresión regular.
- $\phi$ es una expresión regular,
- Si $a \in V$, $a$ es una expresión regular.

Si $\alpha$ y $\beta$ son expresiones regulares, también lo son $(\alpha \ \beta)$, $\alpha \cup \beta)$, y $(\alpha^ *)$.

Por ejemplo, una expresión regular $(0 \cup  1)^*$ describe el conjunto regular $\set{\set{0}\cup\set{1}}^*$. Ese conjunto es un lenguaje regular aceptable por un [[Aceptor de Estado Finito]].

Dos expresiones regulares son _equivalentes_ $\iff$ describen el mismo conjunto regular.

Propiedades de las expresiones regulares:

1. $(\alpha^*)^* = \alpha^*$
2. $\alpha^* \alpha^* = \alpha^*$
3. $(\lambda \cup \alpha)^* = \alpha^*$
4. $\alpha \alpha^* = \alpha^* \alpha$
5. $\alpha \alpha^* \cup \lambda = \alpha^*$
6. $\alpha(\beta \cup \gamma) = \alpha \beta \cup \alpha \gamma$
7. $\alpha(\beta \alpha)^* = (\alpha \beta)^* \alpha$
8. $(\alpha \cup \beta)^* = (\alpha^* \cup \beta^*)^*$
9. $(\alpha \cup \beta)^* = (\alpha^* \beta^*)^*$
10. $(\alpha \cup \beta)^* = \alpha^*(\beta \alpha)^* = (\alpha \beta)^* \alpha^*$
11. $\lambda \cup (\alpha \cup \beta)^* \beta = (\alpha^* \beta)^*$
12. $\lambda \cup \beta(\alpha \cup \beta)^* = (\beta \alpha^*)^*$
13. $\alpha = \beta \alpha \cup \gamma \iff \alpha = \beta^* \gamma$ (regla de Arden)
14. $\alpha = \alpha \beta \cup \gamma \iff \alpha = \gamma \beta^*$ (regla de Arden)

Dada una expresión regular $\gamma$ que describe al conjunto $X$, es posible construir una $\gamma ^R$ que describa al conjunto $X^R$ que contiene el reverso de cada string en $X$:

1. Si $\gamma = \lambda$, $\emptyset$, $\mathbf{a}$ con $a \in V$ $\implies \gamma^R = \gamma$
2. Si $\gamma = (\alpha \beta)$ $\implies \gamma^R = \beta^R \alpha^R$
3. Si $\gamma = (\alpha \cup \beta)$ $\implies \gamma^R = \alpha^R \cup \beta^R$
4. Si $\gamma = \alpha^*$ $\implies \gamma^R = \alpha^{R*}$

## Construcción de AEF a partir de Expresiones Regulares

> [!info] Teorema
>
> Dada la expresión regular $\gamma$ sobre el alfabeto finito $V$, se puede construir un AEF-$\lambda$ $M\ / \ L(M) = \gamma$.

Método 1 de construcción:

![[Construcción de AEF a partir de Expresiones Regulares.png]]
