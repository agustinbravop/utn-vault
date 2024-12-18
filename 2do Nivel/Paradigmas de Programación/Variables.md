Conceptos avanzados asociados a una [[Variable]], relevantes para los [[Sistemas de Tipos]] de los lenguajes de programación.

**Declaración**: es cuando se reserva una celda de memoria con un identificador.\
**[[Asignación]]**: es cuando se escribe un valor en la celda de memoria previamente reservada.

## Tiempo de Vida

El tiempo de vida de una variable es el intervalo entre su creación y su eliminación. Puede ser:

- **Corto**: se crean y se usan en un programa, son **volátiles**.
- **Largo**: son archivos y bases de datos, son **persistentes**.

## Enlace

Un **enlace** es una asociación fija entre un identificador y un valor.

## Ámbito

Un **ámbito**, ambiente, entorno, o *namespace*, es un **conjunto de enlaces**. Cada expresión se interpreta en un ámbito particular en el cual todos los identificadores usados deben estar enlazados en ese ámbito.

## Alcance

El alcance de una variable es la porción o bloque del programa sobre el cual la declaración de una variable es efectiva (está definida). Una declaración local de un bloque es *visible* en todos los sub-bloques, a menos que un sub-bloque la redeclare. Esa redefinición *esconde* la previa. Puede ser:

**Ocurrencia de Enlace**: es el punto en el que se declara un identificador. Ej: `const n = 7`.\
**Ocurrencia de Aplicación de un Identificador**: cuando denota el valor al que está enlazado. Ej: en `n * (n + 1)` se usa el valor de `n`.

El alcance puede ser:

- **Estático**: determina qué ocurrencia de enlace se corresponde con la de aplicación según el anidamiento de bloques.
- **Dinámico**: determina esa correspondencia con el flujo de ejecución. Usa la declaración más reciente.
