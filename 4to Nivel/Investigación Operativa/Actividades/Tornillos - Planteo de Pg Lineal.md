## Enunciado

Una fábrica produce cinco clases de tornillos de precisión en tres grupos de máquinas automáticas. Cada producto puede hacerse en cualquiera de los tres grupos de máquinas, pero el tiempo requerido en cada grupo es distinto, como se muestra en el siguiente cuadro (en hs.) 

Productos 1 2 3 4 5 
Grupo de máq. 1 0,4 0,2 0,4 0,2 0,4 
Grupo de máq. 2 0,8 0,6 0,6 0,2 0,6
Grupo de máq. 3 1,0 1,0 0,8 0,6 1,0

La disponibilidad semanal es de 2400 horas/máquina para cada grupo. Las órdenes para cada tipo de tornillo son respectivamente de 800, 1800, 1400, 1800 y 800 unidades. Se sabe estadísticamente que un 10% en el grupo 1, 8% en el grupo 2 y 5% en el grupo 3 de la producción sale fallada. Si el costo de trabajo para cada grupo de máquinas es de $12, $9 y $ 15 respectivamente, establecer el programa de producción que minimice el costo total.

## Planteo del Modelo Matemático

Variables de decisión:
$x_{ij}$ = horas de producción en el grupo de máquinas $i$ del producto $j$. Para $i = 1,2,3 \ ; \ j = 1,2,3,4,5$.

Objetivo: minimizar $z = 0,4 x_{11} + 0,2 x_{12}$
minimizar z = 


Restricciones:
1. 0,4 x1 + 0,8 x2 + 1,0 x3