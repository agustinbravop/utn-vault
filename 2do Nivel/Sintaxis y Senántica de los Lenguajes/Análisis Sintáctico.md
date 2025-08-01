El **análisis sintáctico** es la etapa en la que un compilador o traductor construye un árbol de derivación para un string. De manera simple:

1. El analizador comienza a aplicar producciones desde $\Sigma$ para llegar al string $\omega$. 
2. Ante una bifurcación (producciones alternativas), prueba una. Si falla, no logra *matchear*, por lo que hace *backtracking* hasta la bifurcación y prueba con otra, y así hasta alcanzar el string o quedarse sin alternativas.
3. Este procedimiento es **top-down** porque comenzamos a analizar desde la raíz (elemento $\Sigma$).

Un procedimiento **bottom-up** construye el árbol desde las hojas (elementos terminales) hasta la raíz.

En una **expansión**, se reemplaza $A$ por $\psi^R$ en la pila. 

![[Expansión.png]]

En un **matching**, si hay un terminal $t$ en la pila, se escanea (`scan`). Si $t=s$, el matching fue exitoso.

![[Matching.png]]
