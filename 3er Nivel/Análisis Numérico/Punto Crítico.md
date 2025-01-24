En los [[Sistemas Dinámicos]], dada una solución $x(t)=x_0 \ \land \ y(t)=y_0 \ \ \forall \ t \in \Bbb R$, se define un solo punto $(x_0, y_0)$ que verifica $F(x_0,y_0) = G(x_0,y_0)=0$. Si bien analizaremos los puntos críticos $(0,0)$, el análisis es generalizable a todo el plano.

El punto crítico $(0,0)$ es _estable_ ([[Estabilidad]]) si $\forall \ R \gt 0 \ \exists \ r \gt 0, r \le R$ tal que toda trayectoria dentro del círculo $x^2+y^2 = r^2$ en $t=t_0$ permanece dentro de $x^2+y^2=R^2 \ \forall \ t \gt t_0$. Es estable si toda trayectoria cercana al punto permanece cerca luego de un tiempo tendiendo al infinito.

El punto crítico $(0,0)$ es _asintóticamente estable_ si es estable y además $\exists \ r_0 \gt 0$ tal que toda trayectoria dentro de $x^2+y^2=r_0^2$ en $t=t_0$ definida como $C\equiv(x(t),y(t))$ verifica que $x(t)\rightarrow 0 \ \land \ y(t) \rightarrow 0$ cuando $t \rightarrow + \infty$. Es asintóticamente estable si toda trayectoria cercana se aproxima al punto luego de un tiempo tendiendo al infinito.

Se dice que el punto crítico $(0,0)$ es _inestable_ cuando NO es estable.

![[Punto Crítico.png]]

Sea el sistema $\begin{rcases}\begin{cases}\frac{dx}{dt}=a_1x+b_1y \\ \frac{dy}{dt}=a_2x+b_2y\end{cases}\end{rcases} = AX$ con $(0,0)$ su único punto crítico. De esto se puede deducir que $|A|\ne 0 \implies \lambda_1, \lambda_2 \ne 0$, por lo que podemos usar los autovalores para clasificar analíticamente los puntos de equilibrio de un [[Sistemas de Ecuaciones Diferenciales Lineales]].

## Clasificación de Puntos Críticos en Sistemas Lineales

La naturaleza y estabilidad del punto crítico queda caracterizada por los autovalores de la matriz del sistema. Existen las siguientes clasificaciones:

1. **Nodo** estable o inestable.
2. **Nodo degenerado** estable o inestable..
3. **Nodo impropio degenerado** estable o inestable.
4. **Punto espiral** estable o inestable.
5. **Centro**.
6. **Punto de silla**.

![[Clasificación de Puntos Críticos en Sistemas Lineales.png]]
