Las **maquinas de Turing** son máquinas abstractas propuestas por Alan Turing en "Proceedings of the London Mathematical Society" en 1936.

Se modela una computadora como una máquina que analiza una cinta lineal de papel separada en cuadrados con símbolos y realiza tres tipos de operaciones:

1. Reemplazar el símbolo del cuadrado actual por otro.
2. Mover la cabecera de la cinta un cuadrado a la izquierda, a la derecha, o quedarse quieto.
3. Pasar del estado actual a otro.

La cinta sirve como entrada y se la supone finita.

Formalmente, una máquina de Turing es una 5-tupla $T=(Q,\Sigma,\Gamma,q_0,\delta)$ donde:

- $Q$ es un conjunto finito de estados, que no incluye ni $h_a$ ni $h_r$ (estados de detención).
- $\Sigma$ es un conjunto finito del alfabeto de entrada, $\Sigma \subseteq \Gamma$.
- $\Gamma$ es el conjunto finito del alfabeto de cinta, se supone que no contiene $\Delta$ (espacio en blanco).
- $q_0$ es el estado inicial, $q_0\in Q$.
- $\delta$ es una función parcial $\delta : Q \times (\Gamma \cup \set{\Delta})\rightarrow (Q \cup \set{h_a,h_r})\times (\Gamma \cup \set{\Delta} )\times\set{R,L,S}$.

Sea el **movimiento** $\delta (q,X)=(r,Y,D)$ con $q\in Q; r\in Q\cup\set{h_a,h_r};X,Y\in\Gamma\cup\set{\Delta};D \in \set{R,L,S}$. Se interpreta que la MT pasa de $q$ a $r$, sustituye $X$ por $Y$ en el cuadrado, y según $D$ va uno a la derecha, a la izquierda, o se queda quieto. Si $r$ es $h_a$ o $h_r$, entonces $T$ se detiene. $\delta$ no está definida para ningún par $(h_a,X)$ o $(h_r,X)$. $T$ también puede fracasar si intenta mover la cabeza de la cinta más allá del extremo izquierdo.

Una **configuración** es un par $(q,x\underline a y)$ con $q\in Q;x,y\in (\Gamma\cup\set{\Delta})^*;a\in \Gamma\cup\set{\Delta}$. Sea $(q,x\underline\omega y)$ la cabeza que está en el primer símbolo de la cadena $\omega$. Sea $(q,x\underline a y \Delta)$ lo mismo que $(q,x\underline a y)$, implicando que los cuadrados a la derecha de $y$ están en blanco.

Sea la **secuencia de movimientos** $(q,x\underline a y) \vdash^*_T (r,z\underline b \omega)$ que puede incluir cero o más movimientos. Sea la configuración $(q,ab\underline a \Delta a)$ y $\delta (q,a)=(r,\Delta,L)$ tal que se escribe el siguiente movimiento:

$$(q,ab\underline a \Delta a) \vdash_T (r,a\underline b \Delta \Delta  a)$$

Y una configuración inicial es $(q_0,\underline\Delta x)$ correspondiente a la entrada $x$. $x\in\Sigma^*$ es aceptada por $T$ $\iff \exists (q_0,\underline \Delta x )\vdash^*_T (h_a,y\underline a z)$ con $y,z \in (\Gamma \cup \set{\Delta})^*; a \in \Gamma \cup \set{\Delta}$. El lenguaje aceptado por $T$ es el conjunto $L(T)$ de cadenas de entrada que $T$ acepta.

Al procesar una entrada $x$, $T$ puede:

1. Aceptarla al entrar en $h_a$.
2. Rechazarla al entrar en $h_r$.
3. O entrar en un _bucle infinito_. El observador no se entera si aceptó o no, por lo que sigue en movimiento perpetuo.

Los **diagramas de transición** de una MT son más complejos, pero útiles en ciertos casos. El movimiento $\delta(q,X)=(r,Y,D)$ se representa como $q \xrightarrow{X / Y, D} r$.

Ejemplo: la siguiente MT acepta el lenguaje $\set{ss/s\in\set{a,b}^*}$, es decir todo string que se divida en dos veces un mismo substring.

![[Máquinas de Turing.png]]

Conceptualmente el diagrama de esta MT separa el procesamiento en dos partes:

1. Validar la longitud par y posibilitar correlaciones: encontrar el centro de la cadena de entrada, y facilitar que la MT distinga los símbolos de la primera y segunda mitades. Para esto se trabaja simultáneamente hacia el centro desde ambos extremos, cambiando los símbolos a su versión en mayúsculas. Una vez que se llega al centro, se revierte la primera mitad a sus símbolos originales.
2. Validar correlaciones una a una: se comienza de nuevo al principio y se compara cada símbolo en minúsculas de la primera mitad contra su contraparte mayúscula de la segunda mitad. Se registra el avance al cambiar los símbolos en minúsculas a mayúsculas y borrar el mayúscula correspondiente.

Esta MT acepta el string `abab` de la siguiente manera: $(q_0,\underline \Delta abab) \vdash ^* (h_a, \Delta AB \underline \Delta)$.
