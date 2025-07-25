La realidad física impone una finitud en los sistemas físicos. En estos autómatas los símbolos, estados y tiempos son finitos y discretos. Sus propiedades son:

1. **Finitud**: número finito de estados, componentes físicos y símbolos.
2. **Discretitud**: símbolos procesables, cantidad de estados asumibles, tiempos.
3. **Acciones secuenciales**: se descompone la solución en una serie de etapas.
4. **Determinístico**: no está sujeto a incertidumbre. Ante la misma entrada, da la misma salida.

El comportamiento de la máquina se describe por la serie de acciones y estados que toma.

![[Autómata de Estado Finito.png]]

Sea el autómata de estado finito $M$ con $n$ partes que pueden asumir $k$ estados cada una de manera que los estados posibles son $k^n$. Sea $q(t)$ el estado de $M$ en el momento $t$. $Q$ es el conjunto de estados finitos de $M$. $q_I$ es el estado inicial de $M$ previo a cuaqluier estímulo, y es único. $s(t)\in S$ y $r(t)\in R$ son alfabetos finitos.

- **Función de transición de estados de $M$**: $f: Q \times S \rightarrow Q$.
- **Función de salida de $M$**: $g: Q \times S \rightarrow R$.

Formalmente se define $M=(Q,S,R,f,g,q_I)$, donde $Q,S,R$ son discretos finitos, $f$ y $g$ son funciones, y $q_I\in Q$.

Para aceptar $\lambda$ (el string vacío) se puede sacar $g$ de $M$ y  agregar $h: Q \rightarrow R$, que es la salida asociada al estado. $h$ asocia a cada estado una respuesta independiente de la entrada.

## Secuencias de Estados

Sea $M$ con $f: Q \times S \rightarrow Q$:

- Si $f(q,s)=q'$, se dice que $q'$ es el sucesor debido a $s$ del estado $q$, tal que $q \overset s \rightarrow q'$.
- Si $\omega =s(1) s(2)\dots s(t)$ genera $q'=q(t)$, $q'$ es sucesor debido a $\omega$, tal que $q \overset \omega \implies q'$.
- Si $M$ es $M_t$ con $g: Q\times S\rightarrow R$, $\varphi = r(1)r(2)\dots r(t)$ es la respuesta de $M$ al estímulo $\omega$, donde $r(i)=g(q(i-1),s(i))$ con $i=1,2,\dots, t$.
- Si $M$ es $M_s$ con $h:Q\rightarrow R$, se da que $r(i)=h(q(i))$ con $i=0,1,2,\dots, t$.

Una $M_t$ y una $M_s$ son *similares* si para cada estímulo posible la respuesta de $M_s$ es igual a la de $M_t$ pero precedida por un símbolo arbitrario y fijo.

![[Mt y Ms similares.png]]

> Teorema: por cada $M_s$ existe una $M_t$ similar y viceversa.

![[Construcción de una Mt a partir de una Ms.png]]

![[Construcción de una Ms a partir de una Mt.png]]

## Equivalencia

Dos máquinas de estado finito $M_1$ y $M_2$ son *equivalentes* sí y solo sí:

$$S_1 =S)2 ; R_1 = R-2 ; \text{ si } s_1(t) = s_2(t) \implies r_1(t)=r(2t) \ \forall t \ge 1$$

La equivalencia se denota $M_1 \sim M_2$ y se representa visualmente como:

![[Equivalencia.png]]

La equivalencia cumple las propiedades de:

1. **Reflexividad**: $M \sim M$.
2. **Simetría**: si $M_1\sim M_2 \implies M_2 \sim M_1$.
3. **Transitividad**: si $M_1\sim M_2 \ \land M_2 \sim M_3 \implies M_1 \sim M_3$.

### Estados Equivalentes

Dos estados $q_a$ y $q_b$ pertenecientes a $M=(Q,S,R,f,-,q_I)$ son equivalentes sí y solo sí $M_a=(Q,S,R,f,-,q_a)$ y $M_b = (Q,S,R,f,-,q_b)$ son equivalentes. Es decir, si se inicializa la máquina en ambos estados, la salida será la misma si las entradas son las mismas. Propiedades:

1. Todos los estados pertenecientes a una misma clase son mutuamente equivalentes.
2. Dos estados de distintas clases no son equivalentes.
3. Si dos estados de una máquina son equivalentes, entonces uno de ellos es redundante.

Si $q_a$ y $q_b$ no son equivalentes, entonces existe un $\omega$ que produce salidas diferentes.

> [!Info] Teorema de Equivalencia de Estados
>
> Los estados $q_a$ y $q_b$ de $M$ son equivalentes sí y solo sí:
>  1. $\forall s \in S: f(q_a,s) \sim f(q_b,s)$
>  2. $\text{para } M_t : \forall s \in S : g(g_,s)=g(q_b,s) \text{ y para } M_s:h(q_a)=h(q_b)$
>  
>  Este teorema no sirve para estados mutuamente recursivos entre sí porque se entra en un bucle.

Otras definiciones:

- $M$ es **reducida** $\iff \forall q, q'\in Q: q \text{ no}\sim q'$
- $q \in Q$ es **accesible** $\iff \exists \omega \in S^* / q_i \overset \omega \implies q$
- $M$ es **conectada** $\iff \forall q \in Q : q$ es accesible.
- $M$ es **mínima** si es reducida y conectada.

Si $q$ es accesible en una $M$ con $n$ estados $\implies \exists \omega / |\omega| \lt n \land q_I \overset \omega \implies q$.

## Estados Distinguibles y k-equivalencia

Los estados $q_a$ y $q_b$ de $M$ son **$k$-distinguibles** si $\exists \omega \in S^*$ con $|\omega| \le k$ tal que las respuestas de $M_a =(Q,S,R,f,g,q_a)$ y $M_b = (Q,S,R,f,g,q_b)$ a la entrada $\omega$ difieren al menos en un símbolo. $\omega$ es **string de distinción** entre $q_a$ y $q_b$. Si $q_a$ y $q_b$ no son k-distinguibles $\implies$ son k-equivalentes.

> [!info] Teorema de k-equivalencia
>
>Se dice que $q_a$ y $q_b$ son k-equivalentes sí y solo sí:
> 
> 1. Son 1-equivalentes: $\forall s \in S : g(q_a,s) =g(q_b,s)$, y
> 2. Para todo $s$, sus estados sucesores son $(k-1)$-equivalentes: $\forall s \in S : f(q_a,s) \sim_{k-1} f(q_b,s)$.
>    
>    $$q_a \sim q_b \iff q_a \sim_k q_b \forall k \ge 1$$

Una relación de equivalencia aplicada a un conjunto particiona al conjunto en clases mutuamente excluyentes y que colectivamente representan de forma exhaustiva al conjunto original. Si $P_1$ y $P_2$ son particiones de $X$ y cada bloque de $P_2$ es subconjunto de solo un bloque de $P_1$, se dice que $P_2$ es un refinamiento de $P_1$. Si $P_1 =\set{A_1,\dots,A_n} \land P_2 = \set{B_1, \dots , B_m}$ y $P_2$ es refinamiento de $P_1$ $\implies \forall B_j \in P_2 \ \exists  \ A_i \in P_1 / B_j \subseteq A_i \land m \ge n$.

## Algoritmo de Particionado

Este algoritmo tiene 3 etapas:

1. Generar $P_1$ de $Q$ agrupando los $q$ 1-equivalentes: se sabe que $q$ y $q'$ están en el mismo bloque de $P_1$ $\iff \forall s \in S: g(q,s)=g(q',s)$.
2. Obtener $P_{k+1}$ a partir de $P_k$: $q$ y $q'$ van en el mismo bloque $\iff$ están en el mismo bloque de $P_k$ (es decir $q \sim_k q')$ y $\forall s \in S: f(q,s) \sim_k f(q',s)$.
3. Repetir la etapa 2 hasta que $P_{m+1} = P_m$ para algún $m$ siendo $P_m$ la **partición final** de $Q$.

### Construcción de Máquina Reducida

Sea $M_t$, se puede construir una $M_t'$ reducida y equivalente a $M_t$. Cada $q'$ de $Q'$ corresponde a un bloque de la partición final $P_f$ del particionado de $M_t$. $q_I'$ corresponde al bloque inicial que contiene a $q_I$ de $M_t$ en su particionado.
