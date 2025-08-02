Una [[Gramáticas Libres de Contexto|GLC]] $G=(N,T,P,\Sigma)$ está en **forma stándard** (o _Forma Normal de Greibach_) si cada producción tiene la forma:

$$\begin{cases}\Sigma \rightarrow \lambda \\ \Sigma \rightarrow A \\ A\rightarrow a\beta \end{cases} \  \ \ \begin{cases}A \in N \\ \beta \in (N\cup T)^* \\ a \in T\end{cases}$$

En una GFS cada paso de derivación, a excepción del primero, es $\varphi A \psi \implies \varphi a \beta \psi$ y genera al menos un terminal. Así, derivar un string de longitud $n$ requiere como máximo $n+1$ pasos de derivación.

## Conversión

Supongamos una GLC [[Gramáticas Bien Conformadas|bien conformada]] $G$, cada producción suya tendrá una de las formas:

$$\begin{cases}\Sigma \rightarrow \lambda & A\rightarrow a\alpha\\ \Sigma \rightarrow A & A\rightarrow B\beta\end{cases} \  \ \ \begin{cases}A,B \in N; a \in T \\ a,\beta \in (N\cup T)^* ; \beta \notin \lambda \end{cases}$$

Las primeras tres producciones están en forma stándard, y la cuarta (de forma $A\rightarrow B\beta$) se convierte por sustitución:

Sea una derivación por izquierda $A\implies X_1 \beta_1 \implies X_2\beta_2\beta_2 \implies \dots \implies X_k\beta_k\dots \beta_2\beta_1 \implies ...$. Esa derivación será finita mientras no se repita un no terminal en la secuencia $A,X_1,\dots,X_k,\dots$. Si en algún caso se da $X_i=X_j$ se da la derivación $X\overset *\implies X\beta_j\dots\beta_{i+1}$ que es un bucle infinito al derivar por izquierda!!

## Eliminación de No Terminales Recursivos por Izquierda

### Recursión Directa

Sea la GLC $G$ con las reglas $X$ de $G$:

$$
\begin{align}X&\rightarrow \alpha_1,\dots \ \ \ \ \ \  X\rightarrow \alpha_n \\
X&\rightarrow X \beta_1, \dots \ \ \  X\rightarrow X \beta_m
\end{align}
$$

En $G'$ se reemplazan esas reglas por:

$$
\begin{align}X&\rightarrow \alpha_1,\dots \ \ \ \ \ \  X\rightarrow \alpha_n \\
X&\rightarrow \alpha_1 Z, \dots \ \ \  X\rightarrow \alpha_n Z \\
Z&\rightarrow \beta_1, \dots \ \ \ \ \ \  Z\rightarrow \beta_m \\
Z&\rightarrow \beta_1Z, \dots \ \ \  Z\rightarrow \beta_mZ \\
\end{align}
$$

Se verifica por [[Expresiones Regulares|regla de Arden]]:

$$
\begin{align}
ER_G &= X \\
&= (\alpha_1\cup \dots \cup \alpha_n) \cup X(\beta_1\cup\dots\cup\beta_m) \\
&= (\alpha_1\cup\dots\cup\alpha_n)(\beta_1\cup\dots\cup\beta_m)^k \\
ER_{G'} &= X \\
&= (\alpha_1\cup \dots \cup \alpha_n) \cup (\alpha_1\cup\dots\cup\alpha_n)Z \\
&= (\alpha_1\cup\dots\cup\alpha_n)\cup(\alpha_1\cup\dots\cup\alpha_n)(\beta_1\cup\dots\cup\beta_m)^*(\beta_1\cup\dots\cup\beta_m) \\
&= (\alpha_1\cup\dots\cup\alpha_n)\cup(\lambda \cup (\beta_1\cup\dots\cup\beta_m)^*(\beta_1\cup\dots\cup\beta_m)) \\
&= (\alpha_1\cup\dots\cup\alpha_n)(\beta_1\cup\dots\cup\beta_m)^* \\
\implies ER_G &= ER_{G'}
\end{align}
$$

### Recursión Indirecta

Sea $M$ un subconjunto de $N$ en $G$. Sea $G(M) = \set{A\rightarrow \alpha / A \in M \ \land \ A \rightarrow \alpha \in G}$ una subgramática de $G$ donde cada regla de $G$ tiene parte izquierda $\in M$. El subconjunto $M$ se elije de manera que no hayan SNRI en $G(M)$. Procedimiento:

1. Sea $X\rightarrow Y\beta$ con $Y\in M$ y sean $Y\rightarrow \alpha_1,\dots \ ; \ Y\rightarrow\alpha_k$. Se reemplaza $X\rightarrow Y\beta$ por $X\rightarrow \alpha_1\beta,\dots,\alpha_k \beta$. De esta manera se transforman las recursiones indirectas en recursiones directas.
2. Se eliminan los SNRI de recursion directa introducidos en el paso 1.

Dada una GLC cualquiera, es posible construir una GFS fuertemente equivalente.
