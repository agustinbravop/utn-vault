Los problemas de **programación no lineal** son una evolución general de los problemas de [[Programación Lineal]], en los cuales la función objetivo y las restricciones **ya no son lineales**.

La **teoría clásica de la optimización** utiliza el cálculo diferencial para determinar los puntos extremos de funciones.

Se establecerán las condiciones necesarias y suficientes para determinar los puntos extremos no restringidos. Para problemas con restricciones de igualdad, se usan los métodos jacobiano y lagrangiano. Para problemas con restricciones de desigualdad, se establecen las condiciones de Kuhn-Tucker.-

Para evitar una resolución analítica, se pueden utilizar métodos numéricos para resolver estos problemas, implementando [[Algoritmos de Programación No Lineal]] en computadoras.

## Problemas sin Restricciones

Un punto $X_0 (x_1^0, \dots, x_j^0, \dots, x_n^0)$ es _máximo_ si $f(X_0+h)\le f(X_0) \ \forall \ h$ pequeño. Análogamente, $x_o$ es _mínimo_ si $f(X_0+h)\ge f(X_0)$. Además, puede ser _global_ o _local_.

Un punto máximo _débil_ tiene algún punto en su proximidad con mismo valor de $f$. Si no, es un [[Punto Crítico]] _fuerte_. Esto también sucede en puntos de inflexión o de silla.

Si $x_o$ es punto extremo de $f(X_0) \implies \nabla f(X_0) = 0$, lo cual es una condición necesaria para un _punto estacionario_. Según la matriz hessiana $H$, que determina una condición suficiente:

- Si $H$ es positiva definida, entonces $X_0$ es punto mínimo.
- Si $H$ es negativa definida, entonces $X_0$ es punto máximo.

El problema es que a veces la matriz hessiana no es ni positiva definida ni negativa definida.

### Método de Newton-Raphson

El **método de Newton-Raphson** sirve para optimizar numéricamente funciones no restringidas. Sean las ecuaciones simultáneas $f_i(X)=0$, y sea $X^k$ un punto dado.

Se aproximan $f_i (X) \approx f_i(X^k) + \nabla f_i (X^k)(X-X^k)$ para $f_i(X)=0$. Matricialmente se describe: $A_k + B_k (X-X^k) =0 \implies X = X^k - B^{-1}_k \cdot A_k$, si es que $B_k$ es no singular.

Se comienza en un punto inicial $X^0$. Al aplicar la ecuación matricial anterior se determina un nuevo punto $X^{k+1}$ a partir de $X^{k}$. Se itera hasta que $X^m \approx X^{m-1}$. El problema es que este método numérico no garantiza la convergencia, y tampoco hay manera de ubicar un "buen" punto inicial.

## Problemas con Restricciones de Igualdad

En estos problemas se utilizan los métodos jacobiano y lagrangiano. Se busca minimizar $z = f(X)$ sujeta a $g(X)=0$ con $g=(g_1,g_2,\dots,g_m)^T$. Las funciones $f(X)$ y $g_i(X)$ se suponen doble y continuamente diferenciables.

### Método de Jacobi

El método de Jacobi o de las derivadas restringidas es el siguiente:

Cuando $\Delta x_j \rightarrow 0$, las ecuaciones se reducen a $\partial f(X) = \nabla f(X)\partial X$ y $\partial g(X) = \nabla g(X)\partial X$. Para ser factible, se debe cumplir $g(X)=0 \implies \partial g(X)=0 \implies \partial f(X) - \nabla f(X)\partial X = 0 \ \land \ \nabla g (X) \partial X = 0$.

Esto son $m$ ecuaciones con $n$ incógnitas (ya que $\partial f(X)$ es variable dependiente). Si $m \gt n$, se pueden eliminar ecuaciones redundantes. Si $m = n$, la solución es $\partial X = 0$ y $X$ no tiene proximidad factible, por lo que solo un punto es factible.

Si $m \lt n$: se define $X = (Y,Z)$ para obtener $\nabla f(Y,Z) = (\nabla_Y f, \nabla_Z f)$ y $\nabla g(Y,Z) = (\nabla_Y g, \nabla_Z g)$. Sea $J = \nabla_Y g = (\nabla_Y g_1, \dots, \nabla_Y g_m)$ la matriz jacobiana y sea $C = \nabla_Z g = (\nabla_Z g_1, \dots, \nabla_Z g_m)$ la matriz de control. Se reescriben las ecuaciones como:

$$
\begin{align}
\partial f(Y,Z) &= \nabla_Y f \partial Y + \nabla_Z f \partial Z \\
J \partial Y = - C \partial Z \implies \partial Y = - J^{-1} C \partial Z \implies \partial f (Y,Z) &= -\nabla_Y f J^{-1} C \partial Z + \nabla_Z f \partial Z \\
\partial f (Y,Z) &= (\nabla_Z f - \nabla_Y f J^{-1} C) \partial Z
\end{align}
$$

Se define el _vector gradiente restringido_ $\nabla_C f$:

$$\nabla_C f = \frac{\partial_C f(Y,Z)}{\partial_C Z} = \nabla_Z f - \nabla_Y f J^{-1}C$$

$\nabla_C f(Y,Z)$ debe ser **nulo** en los puntos estacionarios. La matriz hessiana $H$ corresponde al vector independiente $Z$ con el $i$-ésimo renglón de la matriz hessiana restringida, siendo $\partial \nabla_C f / \partial Z_i$.

En un punto estacionario $X_0 = (Y_0,Z_0)$, se debe anular el gradiente restringido $\nabla_C f$. Entonces:

$$\partial f(Y_0, Z_0) = \nabla_{Y_0} f \cdot J^{-1} \partial g (Y_0, Z_0) \implies \frac{\partial f}{\partial g} = \nabla_{Y_0} f \cdot J^{-1}$$

### Método de Lagrange

Sea $\lambda = \nabla_{Y_0}J^{-1} = \frac{\partial f}{\partial g} \implies \partial f - \lambda \partial g = 0 \implies \frac{\partial}{\partial x_j} (f - \lambda g) = 0$. Esas ecuaciones, junto a las restricciones $g (X) = 0$, dan los valores factibles de $X$ y $\lambda$ que satisfacen las condiciones necesarias para puntos estacionarios: $\frac{\partial L}{\partial \lambda} = \frac{\partial L}{\partial X} = 0$.

Sea la _función de Lagrange_ $L(X, \lambda) = f(X) - \lambda g (X)$, y sea la _matriz hessiana de frontera_ $H^B = \left(\begin{array}{c|c}O & P\\ \hline P^T & Q \end{array}\right)$ con $P=(\nabla_{g_1} (X),\dots, \nabla_{g_m} (X))$ y $Q = \left|\left| \frac{\partial^2 L(X,\lambda)}{\partial x_i \partial x_j} \right|\right| \ \forall \ i,j$.

Dado el punto estacionario $(X_0, \lambda_0)$ de $L(X,\lambda)$ con $H^B$ evaluada en $(X_0,\lambda_0)$, se establecen las siguientes condiciones suficientes pero no necesarias para declarar que $X_0$ es:

- Punto máximo si, comenzando con el determinante mayor de orden $2m+1$, los últimos $n-m$ determinantes menores de $H^B$ alternan signos $(-1)^{m+1}$.
- Punto mínimo si, comenzando con el determinante menor de orden $2m+1$, los últimos $n-m$ determinantes menores de $H^B$ tienen el signo $(-1)^m$.

## Problemas con Restricciones de Desigualdad

Para estos problemas, se hace una ampliación del método de Lagrange con las condiciones de Karush-Kuhn-Tucker. Se define el problema como maximizar $z = f(X)$ sujeto a $g_i (X) \le 0$ con $i = 1, 2,\dots,m$.

Si el óptimo no restringido es no factible, el óptimo restringido debe ser un punto límite ne la frontera del espacio de soluciones, por lo que al menos una restricción es igualada.

La **extensión del método de Lagrange** consiste en hacer $k=1$ luego de resolver el problema sin restricciones. Se deben activar todas las $k$ restricciones, convirtiéndolas en igualdades, y optimizar el problema mediante Lagrange. Si la solución obtenida es factible, se tiene un óptimo local. Se debe considerar todos los conjuntos de restricciones activas, tomadas de $k$ en $k$. El mejor de todos los óptimos factibles es el óptimo global.

Las **condiciones necesarias de Karush-Kuhn-Tucker** son necesarias para identificar puntos estacionarios. Sea $S^2_i$ la variable de holgura no negativa agregada a la restricción $g_i (X) \le 0$. Sean $S=(S_1,\dots,S_m)^T$ y $S^2 = (S_1^2,\dots,S^2_m)^T$. La función de Lagrange es $L(X,S,\lambda) = f(X) - \lambda [g(X)+S^2]$.

Las condiciones de Karush-Kuhn-Tucker son las siguientes:

- $\lambda = \frac{\partial f}{\partial g}$ debe ser $\lambda \ge 0$ para un problema de maximización, o $\lambda \le 0$ para minimización.
- $\frac{\partial L}{\partial X} = \nabla f(X) - \lambda \nabla g (X) = 0$.
- $\frac{\partial L}{\partial S_i} = - 2 \lambda_i S_i = 0$ tal que si $\lambda_i \ne 0 \implies S^2_i = 0$ y el recurso se consume por completo. Sino, se cumple que $S_i^2 \gt 0 \implies \lambda_i = 0$ y el recurso no afecta a $f$ (el recurso sobra).
- $\frac{\partial L}{\partial \lambda} = - (g(X)+S^2)=0$. Con esta condición y la anterior, se ve que $\lambda_i g_i (X) = 0$.

Resumiendo, las condiciones necesarias de KKT son:

$$
\begin{align}\lambda \ge 0 \\
\nabla f(X) - \lambda \nabla g(X) = 0\\
\lambda_i g_i (X) = 0 \\
g(X) \le 0
\end{align}
$$

Si se satisfacen las condiciones de la siguiente tabla, entonces las condiciones necesarias de KKT se vuelven **condiciones suficientes**.

![[Programación No Lineal.png]]

La tabla es válida porque las condiciones dadas producen una función de Lagrange $L(X,S,\lambda)$ que es cóncava en el caso de maximización, y convexa en el caso de minimización.
