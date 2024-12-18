En un lenguaje de programación, los **tipos de dato** sirven:

1. A nivel de diseño, como documentación y soporte de la organización.
2. A nivel de programa, para asegurar operaciones correctas.
3. A nivel de implementación, para el acceso (y tamaño) de memoria.

## Control de Tipos

- **Estático**: se controla durante la compilación. El programa resultante es rápido de ejecutar, escalable, robusto, y mejor documentado.
- **Dinámico**: se controla durante la ejecución. Esto resulta en una programación más rápida, aunque genera un programa más lento y que ocupa más memoria.

## Equivalencia de Tipos

El lenguaje debe validar si hay **equivalencia** $T \equiv T'$ para una operación $T \oplus T'$. La equivalencia de tipos puede ser:

- **Estructural**: $T \equiv T' \iff T \land T' \ \text{tienen la misma estructura}$. Esto se vuelve muy largo para tipos complejos, lo cual es lento.
- **De Nombres**: $T \equiv T' \iff T \land T' \ \text{poseen los mismos nombres definidos en el mismo lugar}$. Esto es una equivalencia más segura.

Un tipo $T$ es **compatible** con un tipo $S$ si un valor de tipo $T$ es permitido en cualquier contexto en el cual un valor de tipo $S$ sería admisible. El **Principio de Completitud de Tipos** dice que las operaciones realizables por un tipo no deberían ser arbitrariamente restringidas al mismo (para no reducir la potencialidad).
