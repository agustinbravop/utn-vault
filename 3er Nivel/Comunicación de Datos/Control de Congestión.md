En la [[Conmutación de Paquetes]], en cada nodo hay una cola de paquetes para cada línea de salida. Si llegan más paquetes de los que se pueden enviar, la cola empieza a crecer. Si la cola sigue creciendo, eventualmente supera la memoria temporal del nodo.

Llegado este _punto de saturación_, se pierden paquetes por falta de memoria, y entonces la congestión se empieza a propagar a otros nodos: eventualmente **la red se congestiona**.

El objetivo de las técnicas de control de congestión es limitar el tamaño de las colas para evitar el colapso en el rendimiento de la red. Algunas técnicas son:

1. Enviar paquetes de control nodo a nodo.
2. Informar el retardo a otros nodos.
3. Usar paquetes de prueba extremo a extremo.
4. Etc...
