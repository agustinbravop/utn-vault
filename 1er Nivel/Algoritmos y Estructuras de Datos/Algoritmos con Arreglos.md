Un [[Arreglo]] es una estructura de datos que se puede tratar con muchos [[Algoritmo|algoritmos]].

## Recorrido

Implica observar el contenido de cada celda. Es **total** si recorre el arreglo completo, o **parcial** si solo visita un subconjunto. Es **natural** si sigue el sentido de la definición de su dimensión, o **antinatural** si ese no es el caso.

## Ordenamiento

Implica obtener una estructura ordenada (numéricamente, alfabéticamente, etc). Existen muchos **algoritmos de ordenación**.

Los simples o directos son:

- Selección.
- Inserción.
- Intercambio.

Los avanzados (pero más óptimos) son:

- Quicksort.
- Heapsort.
- Shell.

## Búsqueda

Implica buscar **un elemento específico** en cierto arreglo. Los algoritmos son:

1. **Lineal pura**: se recorre sí o sí el 100% del arreglo.
2. **Lineal con centinela**: para evitar recorrer hasta el final del arreglo, y parar cuando encontramos el elemento.
3. **Binaria**: recorre mucho más rápido el arreglo (gracias a una estrategia de divide y vencerás) pero solo se puede usar si está ordenado.
