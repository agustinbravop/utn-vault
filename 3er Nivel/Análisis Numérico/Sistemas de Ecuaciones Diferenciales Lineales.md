Sea un sistema de ecuaciones diferenciales lineales de primer orden, definido en forma normal:

$$\begin{align}
\frac{dx_1}{dt} &= a_{11} (t)x_1 + a_{12} (t)x_2 + \dots + a_{1n} (t)x_n f_1(t) \\
\frac{dx_2}{dt} &= a_{21} (t)x_1 + a_{22} (t)x_2 + \dots + a_{2n} (t)x_n f_2(t) \\
\vdots \\
\frac{dx_n}{dt} &= a_{n1} (t)x_1 + a_{n2} (t)x_2 + \dots + a_{nn} (t)x_n f_n(t) \\
\end{align}$$

Suponiendo que $a_{ij}(t)$ y $f_i(t)$ son continuos en un intervalo $I$. Si todas las $f_i$ son cero, se considera que el sistema lineal es *homogéneo*. Trabajando de forma matricial, se expresa el sistema como:

$$X'= A \cdot X + F$$

El *vector solución* es cualquier $X=\left( \matrix{x_1(t) \\ \vdots \\ x_n(t)}\right)$ que satisfaga el sistema de EDOs en el intervalo $I$.

El **principio de superposición** dice que si $X_1, X_2, \dots, X_k$ son soluciones de un sistema homogéneo en $I$, entonces $X = c_1X_1+c_2X_2+\dots+c_kX_k$ también lo es.

## Solución General de Sistemas Homogéneos

La solución general de sistemas homogéneos, siendo $X_1, \dots, X_n$ un conjunto fundamental de soluciones, es:

$$X = c_1 X_1 + c_2X_2 + \dots + c_nX_n$$

Para sistemas no homogéneos, una *solución particular* $X_p$ en el intervalo $I$ es un vector libre cuyos elementos son funciones que satisfacen al sistema, y $X = X_c + X_p$, siendo $X_c$ la *solución general* *del sistema homogéneo asociado* o función complementaria del sistema no homogéneo.

Sean $\lambda_1, \lambda_2, \dots, \lambda_n$ valores propios reales y distintos de la matriz de coeficientes $A$ de un sistema homogéneo, y sean $K_1,K_2,\dots,K_n$ los autovectores correspondientes. Entonces, la solución general es:

$$X = c_1K_1e^{\lambda_1 t} + c_2K_2e^{\lambda_2 t} + \dots + c_nK_ne^{\lambda_n t}$$

Para un sistema lineal homogéneo de primer orden $X'=AX$, una solución es de la forma $X=c_1X_1+c_2X_2$ con $X_i =K_ie^{\lambda_i t}$ para $i=1,2$.

$$\begin{align}
\text{si } \ X = Ke^{\lambda t} \implies X'&= K \lambda e^{\lambda t} \\ 
\text{y } \ X' &=AX \\
\text{substituyendo: } \ K\lambda e^{\lambda t} &= A K e^{\lambda t} \\
\lambda K &= AK \\
(A - \lambda I)K &= 0 \implies \text{det}(A-\lambda I) = 0 \ \text{ si existe una solución no trivial}
\end{align}$$

Donde $(A-\lambda I)K=0$ es la *ecuación matricial*, y $\text{det}(A-\lambda I)=0$ es la *ecuación característica*.

### Autovalores Reales Iguales

Supongamos $\lambda_1$ de multiplicidad 2, y que solo hay un autovector relacionado con este autovalor. Entonces, debemos construir una segunda solución de la forma $X=c_1X_1+c_2X_2$ con:

$$\begin{gather}
X_1 =\left( k_1 \atop k_2 \right) e^{\lambda_1 t} = Ke^{\lambda t} \\
X_2 = K t e^{\lambda_1 t} + P e^{\lambda_1 t} \\
(A-\lambda_1 I)K = 0 \\
(A-\lambda_1 I) P = K
\end{gather}$$

### Autovalores Complejos

Sea $A$ la matriz de coeficientes con elementos reales de un sistema homogéneo, y $k_1$ un autovector correspondiente al autovalor [[Números Complejos|complejo]] $\lambda_1 = \alpha + i \beta$, entonces $K_1e^{\lambda_1 t}$ y $\overline K_1e^{\overline \lambda_1 t}$ son soluciones.

Sea $\lambda_1 = \alpha + i \beta$ un valor propio complejo de la matriz de coeficientes $A$ de un sistema homogéneo, y sean $B_1 = \text{Re}(k_1)$ y $B_2=\text{Im}(k_1)$, entonces:

$$\begin{align}X_1 = [B_1 \cos (\beta t) - B_2 \sin (\beta t)] e ^{\alpha t} \\
X_2 = [B_2 \cos (\beta t) - B_1 \sin (\beta t)] e ^{\alpha t}
\end{align}$$

Donde $X_1$ y $X_2$ son soluciones.

## Matriz Fundamental

Si $X_1, X_2, \dots, X_n$ es un conjunto fundamental de soluciones de $X'=AX$ en $I$, su solución general es la combinación lineal $X=c_1X_1+c_2X_2+\dots+c_nX_n$ que se puede expresar matricialmente como:

$$X = \phi (t) \cdot C \ \text{ con } \ C = \left( \matrix{c_1\\ \vdots \\ c_n}\right) \ \text{ y } \ \phi (t) = \left( \matrix{x_{11} & x_{12} & \dots & x_{1n} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} & x_{n2} & \dots & x_{nn}} \right)$$

Donde $\phi (t)$ es la *matriz fundamental* del sistema.

Para un sistema no homogéneo con solución $X=X_c + X_p$, se tiene que:

$$X_p = \phi(t) \int \phi^{-1}(t) \cdot F(t) dt$$
