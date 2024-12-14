En la implementación de un [[Sistema de Archivos]], la cuestión más importante es cómo mantener un registro acerca de qué bloques de disco van con cuál [[Archivo]].

## Contigua

Es el esquema de asignación más simple.

![[Asignación Contigua.png]]

## Lista Enlazada

Alternativamente, se puede mantener cada archivo como una **lista enlazada** de bloques de disco. No se pierde espacio debido a la [[Fragmentación]] del disco, pero el acceso aleatorio es lento (como en toda lista enlazada).

![[Asignación por Lista Enlazada.png]]

## Lista Enlazada con Tabla de Memoria

![[Asignación por Lista Enlazada con Tabla de Memoria.png]]

Este enfoque acelera el recorrido de la lista enlazada pero requiere cargar la tabla de memoria entera en memoria principal, lo cual es inviable para discos grandes.

## Nodos-i

![[Asignación por Nodos-i.png]]

Este método asocia cada archivo a una estructura de datos conocida como **nodos-índice**, la cual lista los atributos y direcciones de disco de los bloques del archivo. Esta estructura de datos solo está en memoria cuando se abre el archivo, y ocupa menos espacio que FAT.
