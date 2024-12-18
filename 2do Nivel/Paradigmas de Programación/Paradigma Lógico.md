En el [[Paradigma de Programación]] de la **programación lógica**, se declara una **serie de reglas** o proposiciones que luego son usadas por un _motor_ para encontrar la solución a una pregunta.

La programación lógica (en lenguajes como [[Prolog]], propone escribir reglas en lugar de pasos para resolver un problema, y delegar la resolución a un **motor de búsqueda** que encuentre la solución usando nuestras reglas.

Un **programa** es una serie de reglas que se pueden aplicar. Una **solución** es la serie de reglas que se aplican para llegar del estado inicial al estado final.

Sean $I$ el estado inicial y $C$ la condición de fin. Sea $P = (I, O, C)$ un problema, si la secuencia de aplicaciones $O_n (... (O_1 (I))$ satisface la condición de fin $C(O_n (... (O_1 (I))) \implies$ la secuencia de operadores $O_1 ... O_n$ soluciona $(I, O, C)$.

Un **algoritmo de control** extrae las reglas aplicables (que satisfacen la precondición), selecciona una regla a aplicar, y la aplica. Este proceso no es al azar, sino que sigue uno de dos métodos:

1. **Primero en Profundidad**: busca por a izquierda o por la derecha, haciendo backtracking. Necesita poca memoria, y puede encontrar la solución sin explorar gran parte del espacio de estados.
2. **Primero en Amplitud**: se clona en cada bifurcación y cada clon muere en un pasillo sin salida. Usa muchísima memoria, pero siempre encuentra la solución mínima. Funciona con árboles de profundidad infinita.

## Lógica Proposicional

```
Todo hombre es mortal
Todo investigador es hombre  // Proposiciones que son o verdaderas o falsas
------
Todo investigador es mortal  // Resultado
```

Un **literal proposicional** es una variable proposicional ($V$ o $F$): $p, q, r, s, ...$ Una **cláusula proposicional** es una disyunción de literales proposicionales: $q, q \lor \neg p_1$. Una **cláusula de Horn** es una cláusula proposicional con hasta un literal positivo como máximo.

Toda cláusula se puede pasar a forma disyuntiva sin perder equivalencia, y toda cláusula en forma disyuntiva se puede pasar a cláusula de Horn sin perder equivalencia.

Dado un programa $P$ y una consulta $Q$, se deduce $P \vdash_{res} Q$ por **reducción al absurdo**. La **regla de Robinson** es una regla de inferencia para deducir $C_1 \lor p \land C_2 \lor \neg p \vdash C_1 \lor C_2$.

La **resolución SLD** es una estrategia que establece qué cláusula y qué literal seleccionar:

1. **Selection Rule**.
2. **Linear Resolution**.
3. **Definite Clauses** (Cláusulas de Horn).

### Mundo Cerrado

La suposición de **mundo cerrado** dice que solo es verdadero lo que se puede deducir desde las reglas iniciales. Si una condición no es deducible, entonces es falsa.

En la programación lógica, los programas **solo expresan información positiva**. Esto no permite demostrar que un literal es negativo por consecuencia del programa lógico. Entonces, se usa mundo cerrado y cualquier consulta no derivable será falsa.
