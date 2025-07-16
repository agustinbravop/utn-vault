Los lenguajes son abstractos y las máquinas también son abstractas, es decir que no tienen existencia física. Por ende se utilizan modelos lingüísticos (gramáticas) y matemáticos (autómatas) para modelarlos.

![[Jerarquía de Chomsky 2025-07-12 23.41.34.excalidraw.svg]]

La jerarquía de Chomsky relaciona lenguajes con autómatas. Breve historia:

- 1930: Máquina de Turing, Church, Kleene y Post en funciones recursivas y formalización.
- 1938: Shannon: redes de *switching relays* para representar el álgebra de Boole.
- 1950: Caldwell & Huffman: enfoque formal de circuitos de cambio secuencial $\rightarrow$ autómatas finitos.
- 1950: Chomsky caracteriza las gramáticas y los lenguajes formales.

Un **lenguaje** es un conjunto de sentencias que satisfacen ciertas propiedades de construcción (la **gramática**). Un **alfabeto** es el conjunto de símbolos atómicos (indivisibles) que forman los strings. El string completo es un miembro del lenguaje, una unidad. En términos de lenguajes de programación, cada archivo de un programa sería un string completo.

Una gramática detecta errores léxicos (asociados a un *lexer*) y sintácticos (asociados a un *parser*). La **semántica** (asociada a un *interpreter*) es el significado de un string, y queda fuera del alcance de la gramática. En otras palabras, una gramática asegura que el string esté bien escrito pero no asegura que tenga sentido.

![[Jerarquía de Chomsky 2025-07-13 00.00.02.excalidraw.svg]]

## Máquinas

Existen varios tipos de máquinas abstractas. Solo algunas nos interesan para el análisis de lenguajes.

Un **aceptor** $M$ acepta una sentencia de entrada si la sentencia pertenece al lenguaje $L$.

![[Aceptor.png]]

Un **generador** parte de un estado inicial y emite una secuencia de símbolos, generando un lenguaje $L$ determinado por todas las posibles combinaciones de secuencias que la máquina $M$ pudiera generar. Es necesario que sea no determinístico para poder generar distintas secuencias.

![[Generador.png]]

Un **traductor** siempre debe ser determinístico.

![[Traductor.png]]
