Sea $M=(Q,S,U,P,I,F)$ un [[Autómatas Push-Down|APD]] propio. Una secuencia de movimientos $(q,\varphi,\sigma)\implies (q',\varphi',\sigma')$ es un **traverse** de $\omega$ desde el estado $q$ al $q'$ si se cumple que:

1. $\sigma = \sigma'$.
2. $\varphi \omega = \varphi'$.
3. $\forall (q_i,\varphi,\sigma_i): |\sigma_i| \ge |\sigma|$ que ocurre dentro de la secuencia de movimientos.

Si la secuencia es traverse se indica:

$$(q,\varphi,\sigma)\overset T \implies (q',\varphi\omega,\sigma)$$

El **conjunto Traverse** se define de la siguiente manera:

$$T(q,q')=\set{\omega\in S^*/(q,\varphi,\sigma)\overset T\implies(q',\varphi\omega,\sigma); \ \varphi\in  S^*,\sigma \in U^*}$$

Un traverse _trivial_ observa el string vacío: $(q,\varphi,\sigma)\overset T \implies (q,\varphi,\sigma)$ de forma que $\lambda \in T(q,q)\forall q\in Q$.

Propiedades:

1. Si $(q,\varphi,\sigma)\overset T \implies(q',\varphi\omega,\sigma)$ es un traverse de $\omega$ para algún $varphi \in S^*$ y algún $\sigma \in U^*$, entonces es traverse de $\omega \ \forall\ \varphi \in S^*$ y $\forall \ \sigma \in U^*$.
2. Si $\varphi = \omega = \lambda \implies (q,\lambda,\lambda)\overset T \implies (q',\omega,\lambda)$ es una _secuencia de aceptación_ de $\omega$, si $q \in I$ y $q'\in F$.
3. Un APD $M$ acepta $\omega \iff \omega \in T(q,q'); \ q\in I, q'\in F$, por lo tanto el lenguaje reconocido por $M$ es $L(M) = \underset {q\in I \atop q'\in F} \bigcup T(q,q')$.
4. Sea $M$ un $APDP: \lambda \in T(q,q')\iff q=q'$, por lo que cada traverse no trivial de un APDP debe contener como mínimo un `scan`.

Sea $(q,\varphi,\sigma)\overset T \implies (q',\varphi\omega,\sigma)$ un traverse realizado por un APD, siendo $\sigma$ el contenido inicial y final de la pila. Se analiza:

- Se considera _write básico_ un `write` que se realiza desde una configuración con pila igual a $\sigma$.
- Se considera _read básico_ un `read` que deja a la pila conteniendo $\sigma$.
- Un write básico y un read básico forman un par de igualdad o coincidencia. Para que la secuencia sea traverse, **todo elemento escrito a la pila debe ser leído** (para $\sigma$ constante).
- Por ende, un traverse que contiene un read básico también contiene el write básico correspondiente, y viceversa.

Sea $M$ un APDP y $(q,\varphi,\sigma)\overset T \implies (q',\varphi\omega,\sigma)$ un traverse de $\omega$ realizado por $M / \omega \in T(q,q')\implies$ exactamente una de las siguientes afirmaciones es cierta:

1. $S: (q,\varphi,\sigma) \overset S \rightarrow (q',\varphi s,\sigma)$ donde $\omega = s$.
2. $TS: (q,\varphi,\sigma) \overset T \implies (q'',\varphi \psi,\sigma) \overset S \rightarrow (q',\varphi \psi s,\sigma)$ donde $\omega = \psi s \land \psi \in T(q,q'')$.
3. $TWTR: (q,\varphi,\sigma) \overset T \implies (q'',\varphi \psi,\sigma) \overset W \rightarrow (p,\varphi \psi,\sigma u) \overset  T \implies (p',\varphi \psi \theta,\sigma u) \overset R \rightarrow (q',\varphi\psi\theta,\sigma)$ donde $\omega=\psi\theta$.
4. $WTR: (q,\varphi,\sigma)\overset W \rightarrow (p,\varphi,\sigma u) \overset T \implies (p',\varphi \theta,\sigma u) \overset R \rightarrow (q',\varphi\theta,\sigma)$ donde $\omega = \theta$ y $\theta \in T(p,p')$.

![[Conjuntos Traverse.png]]

Para todo $\omega \in S^*$ de una [[Gramáticas Libres de Contexto|GLC]] $G$, sea $N$ un no terminal, se verifica $N(q,q')\overset * \implies \omega \iff \omega \in T(q,q')$ y cada tipo de traverse se puede correlacionar a una producción (derivación):

| Expresiones iniciales                                                                                                                                                                                                | Resultado final con $N$                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| $(q, \varphi, \sigma) \xrightarrow{S} (q', \varphi S, \sigma)$                                                                                                                                                       | $N(q, q') \Rightarrow s$                 |
| $(q, \varphi, \sigma) \xRightarrow{T} (q'', \varphi \psi, \sigma) \xrightarrow{S} (q', \varphi \psi S, \sigma)$                                                                                                      | $N(q, q') \Rightarrow N(q, q'')s$        |
| $(q, \varphi, \sigma) \xRightarrow{T} (q'', \varphi \psi, \sigma) \xrightarrow{W} (p, \varphi \psi, \sigma u) \xRightarrow{T} (p', \varphi \psi \theta, \sigma u) \xrightarrow{R} (q', \varphi \psi \theta, \sigma)$ | $N(q, q') \Rightarrow N(q, q'')N(p, p')$ |
| $(q, \varphi, \sigma) \xrightarrow{W} (p, \varphi, \sigma u) \xRightarrow{T} (p', \varphi \theta, \sigma u) \xrightarrow{R} (q', \varphi \theta, \sigma)$                                                            | $N(q, q') \Rightarrow N(p, p')$          |

Todo conjunto traverse relevante a la construcción de $G$ es $\set{T(q,q')/q\in B,q'\in Q}$ por lo que queda $N=\set{N(q,q')/q\in B,q'\in Q}$ con $B=I\cup \set{q'/q]  \text{ write}(u,q')\in P}$, siendo $q$ un estado inicial o sucesor de un `write`.

## Tabla: Construcción de una GLC a Partir de un APDP

Dado un APDP $M=(Q,S,U,P_M,I,F)$, se puede construir una GLC $G=(N,S,P_G,\Sigma)$ tal que $L(G)=L(M)$. Sean $B=I\cup \set{q' / q] \text{ write}(u,q') \in P_M}$ y $N=\set{N(q,q')/q\in B, q'\in Q}$. Las producciones de $G$ son las siguientes:

| Regla | Si $M$ tiene                                                                      | Luego $G$ tiene                          |
| :---: | --------------------------------------------------------------------------------- | ---------------------------------------- |
|   1   | $q']\ \texttt{scan}\,(s, q') \ \ \ \ q \in B$                                     | $N(q, q') \rightarrow s$                 |
|   2   | $q'']\, \texttt{scan}\,(s, q') \ \ \ \ q \in B$                                   | $N(q, q') \rightarrow N(q, q'')s$        |
|   3   | $q'']\ \texttt{write}\,(u, p)$ <br> $p']\ \texttt{read}\,(u, q') \ \ \ \ q \in B$ | $N(q, q') \rightarrow N(q, q'')N(p, p')$ |
|   4   | $q]\ \texttt{write}\,(u, p)$ <br> $p']\ \texttt{read}\,(u, q') \ \ \ \ q \in B$   | $N(q, q') \rightarrow N(p, p')$          |
|   5   | $q \in I$, $q' \in F$                                                             | $\Sigma \rightarrow N(q, q')$            |
|   6   | $I \cap F \ne \emptyset$                                                          | $\Sigma \rightarrow \lambda$             |
