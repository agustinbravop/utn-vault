Una [[Gramáticas Libres de Contexto|GLC]] $G=(N,T,P,\Sigma)$ es **bien conformada** si cada producción adopta una forma:

$$\begin{cases}\Sigma\rightarrow\lambda \\ \Sigma\rightarrow A \\A \rightarrow \alpha\end{cases} \  \ \ \begin{cases}A\in N \\ \alpha \in (N \cup T)^* - N \ \ (\text{sin producciones no generativas}) \\ \text{ y toda produción es útil}\end{cases}$$

Dada una GLC cualquiera, se puede construir una gramática bien conformada fuertemente equivalente. En una gramática bien conformada, se cumple que cada producción sin $\Sigma$ tiene la forma $A\rightarrow \alpha$ con $|\alpha| \gt 1$ o $\alpha \in T^*-\lambda$ (sólo terminales).

Para derivar un string de longitud $n$ se requiere como máximo $2n$ pasos de derivación.
