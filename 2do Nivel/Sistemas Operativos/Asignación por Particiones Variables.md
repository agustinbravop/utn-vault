Las **particiones variables** son una asignación para la [[Administración de Memoria]] que soluciona el problema de la [[Fragmentación]] interna en la [[Asignación por Particiones Fijas]].

![[Asignación por Particiones Variables.png]]

El problema de las particiones variables es que a lo largo del tiempo generan **fragmentación externa**, lo que se soluciona con **compactación**. Para proteger el acceso a memoria, el [[Proceso#Bloque de Control de Proceso|PCB]] de cada proceso almacena su dirección de memoria base y el límite (tamaño de memoria asignado).
