Una [[Gramáticas Libres de Contexto|GLC]] $G=(N,T,P,\Sigma)$ está en **forma stándard** (o *Forma Normal de Greibach*) si cada producción tiene la forma:

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

$$\begin{align}X&\rightarrow \alpha_1,\dots \ \ \ \ \ \  X\rightarrow \alpha_n \\
X&\rightarrow X \beta_1, \dots \ \ \  X\rightarrow X \beta_m 
\end{align}$$

En $G'$ se reemplazan esas reglas por:

$$\begin{align}X&\rightarrow \alpha_1,\dots \ \ \ \ \ \  X\rightarrow \alpha_n \\
X&\rightarrow X \beta_1, \dots \ \ \  X\rightarrow X \beta_m 
\end{align}$$
1