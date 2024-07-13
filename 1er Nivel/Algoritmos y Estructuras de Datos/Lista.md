Una lista es una estructura de datos de memoria interna que utiliza un [[Puntero]] para ubicar a los elementos de su secuencia, lo que le permite tener una longitud dinámica.

Definición:

```
p: puntero a nodo
nodo: registro de
	dato: [información_a_almacenar]
	próximo: puntero a nodo
FIN_REGISTRO
```

## Clasificación de Listas

### Particularizadas

1. **Pilas**: los *stacks* permiten acceder a sus elementos de forma LIFO (Last In first Out). Tiene dos operaciones básicas para manejar los datos, apilar (*push*) y retirar (*pop*).
2. **Cola**: las *queues* son una lista ordinal de datos con modo de acceso FIFO (First In First Out). Siempre se insertan elementos al final y no permite el acceso aleatorio a un elemento concreto.

### Generalizadas

1. **Simplemente enlazadas**: es una colección de objetos, cada uno de los cuales tiene además un puntero al siguiente objeto en la lista. Es lineal y consecutiva.

![[Lista 2024-07-12 20.34.17.excalidraw.svg]]

2. **Doblemente enlazadas**: cada nodo apunta al siguiente pero también al **anterior**. Permiten hacer un recorrido de adelante para atrás o de atrás para adelante, y retroceder.
3. **Circular**: el último nodo apunta al primer nodo en lugar de apuntar al vacío. También pueden estar simplemente o doblemente enlazadas.
