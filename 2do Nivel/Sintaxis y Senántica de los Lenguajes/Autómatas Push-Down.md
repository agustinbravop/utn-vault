Un Aceptor Push-Down (APD) es una tupla de 6 elementos $M=(Q,S,U,P,I,F)$ con:

1. $Q$: conjunto finito de estados.
2. $S$: alfabeto finito de entrada.
3. $U$: alfabeto finito de pila o stack.
4. $P$: es el programa de $M$. Es una secuencia finita de instrucciones.
5. $I\subseteq Q$: conjunto de estados iniciales.
6. $F\subseteq Q$: conjunto de estados finales.

En cada instrucción el estado $q$ es la *etiqueta* o *rótulo* de la instrucción y $q'$ es el estado sucesor. Cada $q$ en $Q$ rotula un único tipo de instrucción (`scan`, `write`, o `read`). Se considera una tupla $(q,\varphi,\sigma)$ con $q\in Q, \varphi \in S^*, \sigma \in U^*)$ la *configuración* de $M$. Una configuración describe el estado total de un APD en algún punto de su análisis de una cinta.

![[Instrucciones de los Autómatas Push-Down.png]]

Algunos conceptos:

1. $(q,\lambda,\lambda)$ es *configuración inicial* $\iff q \in I$ de $M$.
2. $(q',\omega,\lambda)$ es *configuración final* $\iff q'\in F, \omega \in S^*$ de $M$.
3. $\varphi$ es *string aceptado* por $M$ $\iff$ $M$ tiene secuencia de movimientos $(q_i,\lambda,\lambda)\implies(q_F,\varphi,\lambda)$, donde el stack debe estar vacío.
4. $L$ es el *lenguaje reconocido* $L(M) = \set{\omega \in S^* / (q_i,\lambda,\lambda) \implies (q_f,\omega,\lambda); q_i\in I, q_f\in F}$.
5. $M$ es *determinístico* $\iff$ para toda configuración nunca hay más de un movimiento posible.
6. Una instrucción $q] \text{ write} (u,q')$ es *impropia* si $q'$ es rótulo de una instrucción `read`.
7. Un APD es *propio* si su programa no contiene instrucciones impropias.

## Transformación de APD a APDP

Sean los APD $M$ y APDP $M'$: el siguiente procedimiento verifica que $L(M') = L(M)$.

1. $\forall q, q'$ con $(q,\varphi,\sigma)\overset {k \text{ writes}} \implies (q'',\varphi,\sigma\tau)\overset {k \text{ reads}} \implies (q',\varphi,\sigma)$ con $k \ge 1$ (1). Por cada instrucción $p] \text{ move}(-,q)$ se agrega $p \text{ move}(-,q')$. Si $q\in I$ en $M$ $\implies q'\in I$ en $M'$. Esto se repite para cada par $q$ y $q'$ para los cuales $M$ tiene una secuencia de movimientos como (1).
2. Se borran todas las instrucciones impropias. Las restantes forman el $P$ de $M'$.

## Tabla: Construcción de un Analizador Push-Down

