La **interfaz del canal** en los [[Canales]] de una [[Arquitectura de Computadoras]] es la "caja negra" que permite adaptar las señales del periférico a las especificaciones de la [[Computadora]].

La interfaz está formada físicamente por un cierto número de conectores, salidos del canal, en los cuales puede ir a enchufarse. Suele haber tres tipos de hilos:

1. De información: llevan en paralelo la información por transmitir.
2. De gobierno: habilitan la entrada o salida de información.
3. De sincronización: demanda y aceptación de demanda.

![[Interfaz del Canal.png]]

## Concentración

Una computadora suele tener **varios periféricos conectados**. Necesita una forma de comunicarse con cada uno en particular e identificarlo unívocamente.

### Concentración por Línea Ómnibus

A cada palabra de memoria transferida se le agrega un _header_ que tiene la dirección del periférico. La palabra y el header viajan por el bus hasta llegar al controlador de periférico que corresponde.

![[Concentración por Líneas Ómnibus.png]]

## Concentración por Multiplaje

Hay un hilo para cada unidad externa.

![[Concentración por Multiplaje.png]]
