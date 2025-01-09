Los [[Códigos]] **lineales** son espacios vectoriales sobre un cuerpo finito (un alfabeto):

$$K^n = \set{ (x_1 \dots x_n) / x_1, \dots, x_n \in K} \ \land \ C \subseteq K^n;\ v, w \in C; \ \alpha, \beta \in K \implies \alpha v + \beta w \in C$$

Un código lineal binario tiene un número de palabras que es potencia de 2. Se $C$ un código y $v \in C$ una palabra: el *peso* $w$ de $v$ es el número de símbolos no nulos de $v$. Dada la [[Distancia de Hamming]], se verifica para códigos lineales que $d(u,v) = w(u-v)$ y $w(u)=d(u,0)$.

Formalmente se define el peso de $C$ como $w(C) = \text {min} \set{w(v)/v \in C, v \ne 0}$. Si el código es lineal, entonces también se cumple que $d(C) = w(C)$.

## Matriz Generatriz

Sea $C$ un $[n,k]$-código lineal (CL) sobre un cuerpo $K$ con $C \subseteq K^n$. Se define una *matriz generatriz* de $C$ como $M_{k \times n} (K)$, cuyas filas forman una base de $C$. Las filas son un conjunto linealmente independiente y $M$ tiene rango $k$ igual al número de filas.

Si $G \in M_{k \times n}(K) \ \land \ k \le n \implies G$ es matriz generatriz de un CL sobre $K \implies rg(G) = \rho (G) = k$. Se tiene que $C = \set{ x G / x \in K^k}$, y aplicando un isomorfismo de $k$-espacios vectoriales: $K^k \overset f \rightarrow C$ y $x \rightarrow xG$. 

Interesa encontrar matrices generatrices sencillas para que la **decodificación** sea sencilla.

1. Sea $\sigma$ una *permutación posicional* en la que cada palabra $u = u_1 \dots u_n$  con $u_i \in A$ se sustituye $u$ por $u_{\sigma(1)}$. Ej: $\sigma = \begin{pmatrix}  1 & 2 & 3 & 4 & 5\\ \sigma(1) & \sigma(2) & \sigma(3) & \sigma(4) & \sigma(5) \end{pmatrix} = \begin{pmatrix}  1 & 2 & 3 & 4 & 5\\ 3 & 2 & 1 & 5 & 4 \end{pmatrix}$.
2. Sea $\pi_i: A \rightarrow A$ una *permutación de símbolos* en la que cada palabra $u = u_1 u_2 \dots u_n$ se sustituye $u_i$ por $\pi_i(u_i)$. Ej: $\Bbb Z_2 \overset {\pi_3} \rightarrow {\Bbb Z_2} \ ; \ \pi_3 = (10) \ ; \ 10110 \rightarrow 10010$. Cada elemento va a la posición del siguiente y el último va a la primera posición.

Se dice que $C'$ es *equivalente* a $C$ cuando $C'$ se obtiene de $C$ al aplicar las operaciones anteriores. Es una *relación de equivalencia*. Los **códigos equivalentes** conservan longitud, tamaño, y distancia. Sea $C$ de longitud $n$ sobre $A$ y $u \in A^n \implies \exists \ C' / u \in C'\ \land \ C \equiv C'$.

Una matriz generatriz $G$ se dice normalizada o *estándar* cuando es $G = (I_k | A)$, donde $I_k$ es la matriz identidad de $M_{k \times k} (K)$.

Si un código tiene una matriz generatriz estándar, entonces es un **código sistemático**. Por ejemplo, el código ASCII con un bit de paridad.

Se verifica que:

1. Todo código lineal es equivalente a un código sistemático.
2. Todo código sistemático tiene una única matriz generatriz estándar.
3. Si $C$ es un $[n,k]$-código sistemático $\implies$ para cada $u = u_1 \dots u_n \in K^k$ existe una única palabra del código $C_u \in C$ de la forma $C_u = \underbrace{u_1 \dots  u_k}_{\text{información}} \underbrace{ x_{k+1} \dots x_n}_{\text{redundancia}}$. Es decir, se toma todo $K^k$ y se le añaden $n-k$ símbolos.

## Decodificación

La decodificación puede ser:

- **De Canal**: si las palabras recibidas no son del código, se las sustituye por una del código. Para esto se usa un código [[Detección de Errores|detector de errores]].
- **De Fuente**: se toma la información y se la pasa a su formato original. Una vez recibido $xG$ se recupera $x$ resolviendo un sistema de ecuaciones lineales con solución única. Tiene rango $k$, es decir que hay $k$ ecuaciones linealmente independientes.

## Matriz de Control

El código **dual** u ortogonal de un $C$ $[n,k]$-código es $C^{\perp} = \set{ x \in X^n / xy=0, \forall y \in C} \subseteq K^n$. Si $C$ es un ${n,k}$-código entonces $C^{\perp}$ es un $[n, n-k]$-código.

Se llama *matriz de control* a cualquier generatriz de $C^\perp$. Si $H$ es matriz de control de $C$, se cumple que $C = \set{x \in K^n / xH^t=0}$ cuando $C$ es un $[n,k]$-código y $H \in M_{(n-k)\times n}(K)$.

Un código lineal se dice *autodual* cuando $C = C^\perp$.

Sea $C$ un código lineal sistemático con matriz generatriz estándar $G = (I_k | A)$ de manera que se define una matriz de control $P = (A^t | - I_{n-k})$ de $C$. La matriz es estándar cuando tiene la forma $P = (B | I_{n-k})$.

Es más fácil obtener las palabras del código al tener la matriz de control estándar. También existe un método directo, partiendo desde las matrices de control, para obtener el peso $w(C)$.
