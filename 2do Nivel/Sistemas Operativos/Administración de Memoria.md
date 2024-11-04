La **memoria** es un recurso escaso y jerarquizado ([[Jerarquía de Memorias]]). El **administrador de memoria** del [[Sistema Operativo]] abstrae y administra esa jerarquía. Se encarga de su protección, reubicación, y organización lógica y física.

Asignación de espacio contiguo:

- [[Asignación por Particiones Fijas]].
- [[Asignación por Particiones Variables]].

Asignación de espacio no contiguo:

- [[Asignación por Paginación Simple]].
- [[Asignación por Paginación Múltiple]].
- [[Asignación por Segmentación]].

## Mapeo

El SO debe poder **mapear la memoria disponible**.

### Mapas de Bits

![[Mapa de Bits.png]]

Un bit para cada palabra de memoria. Un $0$ indica que es una palabra **libre**, y un $1$ indica que es una palabra **asignada** a un proceso.

### Lista Enlazada

![[Lista Enlazada.png]]

Es más rápida de recorrer y modificar, pero requiere mayor tamaño.

### Buddy System

![[Buddy System.png]]

La memoria se va paginando en **potencias de $2$**, **bajo demanda**. Ante un proceso nuevo, la memoria se divide en dos hasta que no entre en una de las dos partes, y lo aloja en esas dos. Ambas partes del mismo tamaño son *buddies*. Cuando se libera una parte, también se libera su *buddy* (si es que también está libre).
