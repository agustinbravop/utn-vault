Al trabajar con [[Canales]] en una [[Arquitectura de Computadoras]] para la entrada-salida de información, se debe elegir el modo de transferir los datos desde el periférico a la [[Computadora]] y viceversa.

Una **transferencia elemental** es la transferencia de una palabra desde una posición de la [[Unidad de Memoria]] a una unidad externa, o viceversa. Supone que se conoce:

- $DEM$: demanda de la transferencia.
- $SEN$: sentido de la transferencia (si es entrada o salida).
- $DIR$: dirección de almacenamiento en memoria de la palabra transferida.

Las técnicas de ejecución de una transferencia elemental dependen de cómo estos tres datos son suministrados al computador.

| Técnica                     | Tiempo máximo de espera del periférico                                                          | Tiempo restado al programa en curso                                   |
| --------------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **Programada**              | Hasta el final de la instrucción en curso más el inicio del programa solicitado de interrupción | Procesamiento de un programa de interrupción                          |
| **Por instrucción forzada** | Duración de la instrucción más larga del repertorio                                             | Una instrucción generalmente ejecutada en uno o dos ciclos de memoria |
| **Por robo de ciclo**       | Un ciclo de memoria                                                                             | Un ciclo de memoria                                                   |
| **por acceso directo**      | Un ciclo de memoria                                                                             | Nada, o un ciclo de memoria                                           |

## Transferencia Programada

El programa llega a una instrucción de transferencia. Las instrucciones son: `PRE (dir. periférico)`, `GBP (dir. periférico)`, `ENT (dir. memoria)` y `SAL (dir. memoria)`.

![[Transferencia Programada.png]]

## Transferencia por Instrucción Forzada

El periférico manda una **interrupción** de I/O y **suspende** al programa en curso hasta que se resuelva la transferencia. La unidad externa manda una instrucción y la mete en el registro de instrucción para ser ejecutada.

![[Transferencia por Instrucción Forzada.png]]

## Transferencia por Robo de Ciclo

La [[Unidad de Control]] termina el ciclo de memoria en curso y le **cede el próximo** a la unidad exterior. Cuando puede, le **roba un ciclo**. La dirección de memoria de la palabra a transferir va directo al registro $S$ de la memoria.

![[Transferencia por Robo de Ciclo.png]]

## Transferencia por Acceso Directo a Memoria

Se imagina que la memoria tiene dos _muelles_ de acceso, uno para el ordenador (programas) y otro para la unidad exterior (canales). Esto **independiza** la memoria y se acerca a una [[Simultaneidad de los Procesos IO]] total entre el procesamiento y la entrada-salida.

![[Transferencia por Acceso Directo a Memoria.png]]
