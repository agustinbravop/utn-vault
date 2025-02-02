Luego de resolver un problema de [[Programación Lineal]], los parámetros del modelo (que son datos de entrada) pueden variar dentro de ciertos **límites** sin que cambie la estructura del convexo de soluciones, y sin cambiar la estructura de la solución óptima. 

Esto es el análisis de sensibilidad, que se puede dividir en dos análisis:

- El análisis del lado derecho de las restricciones.
- El análisis de los coeficientes objetivos.

## Lado Derecho de las Restricciones

¿Cómo es la sensibilidad de la solución óptima a cambios en la **disponibilidad de los recursos**?

Gráficamente, las rectas de las restricciones se desplazan sin alterar ni la función objetivo ni las variables de decisión. Ese desplazamiento de una recta, a la cual el vértice de la solución óptima pertenece, desplaza el punto óptimo $O$ a un nuevo vértice $O\ '$.

Se define el *valor unitario*, precio dual, precio sombra, o *valor marginal* del recurso cuya disponibilidad fue desplazada:

$$\frac{z_{O\ '}-z_O}{\Delta\text{recurso}} = \text{valor unitario}$$

El valor unitario representa la **tasa de cambio** de la función objetivo por cambio unitario de este recurso. 

El precio dual se mantiene solo dentro del *intervalo de factibilidad*: la variación del recurso solo es posible hasta que el desplazamiento de la recta mueva al punto óptimo de manera que coincida con otro punto del convexo, lo que significa cambiar la estructura de la solución óptima, y por ende es el límite de este análisis de sensibilidad.

## Coeficientes Objetivos

¿Cómo es la sensibilidad de la solución óptima a cambios en las unidades de ingreso?

Se hace variar la pendiente de la función objetivo sin cambiar el punto óptimo, por lo que, gráficamente, $z$ no puede cruzar las dos rectas de restricción que se cruzan en el punto óptimo.

$$\begin{rcases}z = c_1x_1+c_2x_2 \\
r_1: c_{1_{r_1}}x_1 + c_{2_{r_1}}x_2 \le n \\
r_2: c_{1_{r_2}}x_1 + c_{2_{r_2}}x_2 \le m
\end{rcases}\frac{c_{1_{r_1}}}{c_{2_{r_1}}} \le \frac{c_1}{c_2} \le \frac{c_{1_{r_2}}}{c_{2_{r_2}}} \ \ \text{ (intervalo de optimalidad)}$$
