Prolog es un lenguaje de programación lógica basado en el [[Paradigma Lógico]]. Propone programar con **lógica de predicados**, la cual es similar a la [[Paradigma Lógico#Lógica Proposicional|lógica proposicional]] pero además tiene acceso a los elementos constitutivos de cada proposición, porque expresa **cualidades** y **relaciones** entre objetos.

Los objetos se denominan argumentos o términos del predicado.

```prolog
amigo(matias, X) :- gusta(X, rock)  % matias es amigo de los que les gusta el rock
gusta(diego, rock)                  % relación: a diego le gusta el rock
gusta(matias, julia)                % relación: a matias le gusta julia
```

## Unificación

La **unificación** soluciona cómo resolver dos predicados con el mismo símbolo predicativo pero distintos argumentos. Se hace mediante la sustitución: un conjunto de asignaciones del tipo `X := t` con una sola asignación a cada variable y que tiene alcance clausular.

Dada una sustitución $\theta$ y un predicado $P$, la _aplicación_ de $\theta$ a $P$ produce un nuevo predicado $P_\theta$ donde toda variable asignada en $\theta$ se cambia por su término correspondiente.

Dadas dos expresiones $E_1$ y $E_2$, se llama _unificador_ a una sustitución $\theta$ tal que $E_{1\theta} = E_{2\theta}$, por lo que se vuelven expresiones idénticas. Por ejemplo, dados `padre(Z, diego)` y `padre(jorge, diego)`, se ve que $\theta = \set{Z := \text{jorge}}$ es unificador.

Supóngase $E_{1\theta_1 \theta_3} = E_{2 \theta_2}$, se dice que $\theta_1$ es _más general_ que $\theta_2$ porque asigna menos variables.

### Algoritmo de Unificación de Robinson

1. Si $E_k = F_k \implies$ $E$ y $F$ son unificables, y un MGU es $\theta = \cup \theta_i$, con $0 \le i \le k$.
2. Si $E_k \ne F_k \implies$ se busca el primer par de discordancia $D_k$ entre $E_k$ y $F_k$.
3. Si $D_k$ posee una variable y un término se continúa. Sino, $E_k$ y $F_k$ no son unificables.
4. Si la variable de $D_k$ aparece en el término entonces no unifican. Sino, podemos continuar.
5. Se construye un $\theta_{k+1}$ que vincule la variable con el término de $D_k$. Usando esta nueva sustitución, se construyen $E_{k+1} = E_k \ \theta_{k+1}$ y $F_{k+1} = F_k \ \theta_{k+1}$. Se hace $k = k +1$ y se vuelve al paso 1.

Sean $R$ un símbolo predicativo, sean $t_i$ y $s_i$ unificables con un MGU $\theta$, y sean $C_1$ y $C_2$ cláusulas. Se define la **regla de resolución** $C_1 \lor R(t_1, ..., t_n), C_2 \lor \neg R(s_1, ..., s_n) \vdash C_1 \ \theta \lor C_2 \ \theta$.
