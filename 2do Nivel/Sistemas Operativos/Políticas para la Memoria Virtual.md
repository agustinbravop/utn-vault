A la [[Memoria Virtual]] de un [[Sistema Operativo]] se le aplican varias políticas.

## Políticas de Recuperación

Relacionadas a la [[Asignación por Paginación Simple]].

- Paginación bajo demanda.
- Paginación adelantada.

## Política de Ubicación

Los huecos y segmentos en memoria principal son de tamaño variable. Se usa una lista enlazada con el tamaño de cada hueco (espacio contiguo de memoria no asignada). El algoritmo puede ser first fit, best fit, o worst fit. Si no hay un hueco apropiado para ubicar un proceso nuevo, interviene la política de reemplazo.

## Política de Reemplazo

Determina la página a reemplazar. Si es **local**, la página víctima pertenece al mismo proceso. Si es **global**, la página víctima puede ser de cualquier proceso.

1. **FIFO**: reemplaza la página más antigua. Las páginas se reemplazan en orden cíclico.
2. **Óptimo**: tiene en cuenta la cadena de referencia a futuro y reemplaza a la página que dentro de más tiempo va a ser referenciada. No se puede implementar, solamente sirve para comparar su performance óptima contra la performance de otros algoritmos.
3. **LRU**: Least Recently Used. Reemplaza la página menos usada recientemente. Si cada página guarda el valor del reloj al ser referenciada, se reemplaza la que tiene el menor valor.

El bit $M$ permite hacer **buffering**: si $M=0$ entonces es una página que no requiere swap out, y por ende es más barata de reemplazar.

## Política de Asignación

Determina cuántas páginas asignar a un proceso. Puede ser:

- **Equitativa**: o fija. Asigna el mismo número de páginas a todos los procesos.
- **Proporcional**: o variable. Asigna en función del tamaño de cada proceso.

## Política de Limpieza

- Limpieza bajo demanda.
- Limpieza adelantada.
