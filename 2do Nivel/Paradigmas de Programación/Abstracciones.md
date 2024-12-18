En un [[Paradigma de Programación]], una **abstracción** es una entidad que engloba una computación. Nos permite concentrarnos en qué hace un procedimiento sin saber cómo está implementado. Puede ser:

- **De Control**: permite esconder código procedural.
- **De Datos**: permite ofrecer estructuras de datos sofisticadas sin referir a su implementación.

**Parámetro formal**: identificador que se usa en una abstracción. Ej: `fun circulo(r: real)`.\
**Parámetro actual**: expresión que devuelve un argumento. Ej: `circulo(1.0); circulo(a + b)`.\
**Argumento**: valor puntual que se pasa a una abstracción. Ej: `1.0, a + b`.

Una función puede ser:

- **Estricta**: una llamada puede evaluarse solo si sus argumentos pueden ser evaluados.
- **No estricta**: una llamada puede a veces evaluarse aún si algún argumento no se puede.

## Paso de Parámetros

El [[Paso de Parámetro]] puede ser por copia o por referencia:

- **Mecanismo de Copia**: el parámetro formal denota una variable local de la abstracción en la cual se almacena una copia del argumento. Esta copia es un **nuevo espacio en memoria** que se crea a la entrada y se elimina a la salida.
- **Mecanismo de Referencia**: el parámetro formal se **enlaza directamente** al argumento. Esto permite modificar el espacio de memoria original, y nos ahorra hacer una copia, pero puede llevar a comportamiento inesperado si se crean dos o más aliases de la misma variable.
- **Call by Name**: sea $f$ una función con un parámetro formal $x$ y sea $a$ una expresión de un tipo compatible con $x$. Una llamada a $f(a)$ es equivalente a ejecutar el cuerpo de $f$ con todas las ocurrencias de $x$ reemplazadas por $a$. Ej: macros del lenguaje [[C]].

### Orden de Evaluación

Sea el ejemplo `sqr(n: int) = n * n; sqr(p + q)`. El orden de evaluación puede ser:

- **Impaciente (*Eager*)**: se evalúa `p + q` y se enlaza el resultado a `n`. Luego retorna `n * n`.
- **Perezoso (*Lazy*)**: enlaza `n` a la expresión `p + q`y luego la evalúa cada vez que la necesita dentro del cuerpo, pero evalúa solo en el momento justo que lo necesita. Esto repite muchos cálculos pero sirve para evaluar variables cambiantes y así tratar estructuras infinitas.
