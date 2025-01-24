Un sistema es **estable** si responde en forma limitada a una excitación limitada. Se analizan los polos de la [[Función de Transferencia]] $F(s)$, suponiendo que son [[Números Complejos]]:

- Si todos los polos están en la mitad izquierda del plano $s$ (de manera que su parte real es negativa), entonces es un sistema *estable*.
- Si se tiene un polo en el eje imaginario, el sistema es *marginalmente estable*.
- Si se tiene un polo en la mitad derecha, el sistema es *inestable*.

![[Estabilidad.png]]

La **estabilidad** es una propiedad del sistema y no depende de la función de entrada que se le aplique. Un sistema estable, con el tiempo, vuelve a las condiciones iniciales. Un sistema inestable es difícil de controlar. Dado que $F(s)$ caracteriza al sistema, se la puede usar para especificar condiciones de estabilidad.

Una función de transferencia caracteriza al comportamiento del sistema sin proporcionar información sobre su estructura física interna, de manera que dos sistemas físicamente distintos pueden tener la misma función de transferencia.

$F(s)$ nos permite predecir la forma de las señales sin necesidad de resolver la ecuación diferencial que describe al sistema. Además, si no se tiene esa ecuación diferencial, aún se puede obtener su función de transferencia de manera experimental, estimulando al sistema y estudiando su respuesta.

Dado un [[Sistemas de Ecuaciones Diferenciales Lineales]] no homogéneo $x'= Ax + f(t)$ con solución general de la forma $x(t) = x_h(t) + x_p(t)$, si el sistema es asintóticamente estable entonces se cumple que $\lim_{t\rightarrow +\infty} x_h(t)=0$ y $x(t) \approx x_p(t)$. Esto resulta útil en ingeniería, donde $f(t)$ es entrada del sistema y $x_p(t)$ es salida.

## Estabilidad según Lyapunov

Se asocia al sistema una función escalar $V(||x||)$ que analiza cómo el sistema se está comportando.

**Teorema de Estabilidad de Lyapunov**: es una condición suficiente pero no necesaria. Sea $x=0$ un punto de equilibrio de $x'=f(x)$ y sea $V(x)$ una función de Lyapunov tal que $x=0$ es estable si $V(0)=0$, $V(x)\gt 0 \text{ en } D-\set{0}$, y $V'(x)\le 0 \text{ en } D$. Además, si se cumple que $V'(x)\lt 0 \text{ en } D-\set{0}$, entonces $x=0$ es asintóticamente estable.

Sea $x'=Ax$ con $x(t_0)=x_0$ y $V(x)=x^TMx$ siendo $M$ una matriz $n \times n$ real y simétrica.

$$\begin{align} V'(x(t)) &= (x')^TMx + x^TMx'\\
V'&=x^TA^TMx+x^TMAx\\
V'&=x^T(A^TM+MA)x
\end{align}$$

El requerimiento de que $V(x)$ sea definida positiva es equivalente a que la matriz $M$ sea definida positiva, y que $V'$ sea definida negativa equivale a $P = A^TM+MA \lt 0$. Entonces, se define la *ecuación de Lyapunov* como $A^TM+MA=-P$, donde normalmente se hace $P = I$.

La estabilidad asintótica del sistema lineal se asegura si, siendo $P$ una matriz simétrica definida negativa, se puede encontrar una matriz simétrica definida positiva $M$. 

Una matriz cuadrada es definida positiva si $\forall \ x \ne 0 \rightarrow x^TMx\gt0$, por lo que todos sus autovalores propios deben ser positivos.
