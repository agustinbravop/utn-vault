El **cálculo lambda** es un sistema formal diseñado para explorar la definición de [[Función|funciones]], las aplicaciones, y la [[Recursividad]]. Esto genera un nuevo [[Paradigma Funcional]].

```
5 + 3 * 2  // Expresión reducible (redex)
5 + 6      // Reducción a una expresión equivalente
11         // Expresión irreducible
```

Sea la **reducción** $f(x) = E[x] \implies f(u) = E[x := u]$ de manera que cada aparición de $x$ en la expresión se sustituye por $u$. Existe un conjunto de [[Reducciones Lambda]].

Es común escribir el operador siempre al frente, antes de los argumentos:

```
+ 5 (* 3 2)
+ 5 6
11
```

El cálculo lambda nos permite **definir** funciones de un solo argumento: $\lambda x . B$ (por ejemplo $\lambda x.+ \ x \ 2$) y **aplicarlas** mediante $f \ A$, siendo $A$ un argumento (por ejemplo $(\lambda x . + \ x \ 2 ) \ 3$.

## Sintaxis

El cálculo lambda es una [[Gramáticas Libres de Contexto|Gramática Libre de Contexto]].

```
<expr> ::= <const>
		| <var>
		| (λ <var>.<expr>)
		| (<expr> <expr>)
```

Convenciones:

1. La aplicación es asociativa por la izquierda: $M \ N \ P \ Q \rightarrow (((M \ N) \ P ) \ Q)$.
2. La abstracción es asociativa por la derecha: $\lambda x . \lambda y . M \rightarrow (\lambda x . (\lambda y . M))$.
3. La aplicación es prioritaria sobre la abstracción: $\lambda x . M \ N \rightarrow \lambda x . (M \ N)$.
4. Se puede suprimir símbolos $\lambda$ en abstracciones consecutivas: $\lambda x . \lambda y . \lambda z . M \rightarrow \lambda x y z . M$.

El [[Variables#Alcance|alcance]] de una variable es la porción de la expresión donde el identificador es accesible. Una variable puede estar:

- **Ligada**: si aparece en el ámbito de una variable instanciable.
- **Libre**: si una expresión tiene ocurrencias que no están ligadas.

Ej: en $\lambda y . z \ (\lambda x. x \ y))$ las variables $x$ e $y$ están ligadas, pero la $z$ está libre.
