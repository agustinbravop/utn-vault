En el apunte de la [[Programación Lineal]] se vio lo que se considera el _problema primal_, y su [[Análisis de Sensibilidad]]. También se puede plantear el mismo problema o modelo matemático como un _problema dual_: otra cara de la misma moneda en la que las restricciones y las variables de decisión intercambian lugares.

La solución óptima del **problema de programación dual** proporciona:

- Herramientas alternativas para comprobar la optimalidad de soluciones.
- Interpretaciones económicas de los problemas de programación lineal.

Se formula la función objetivo, variables, y coeficientes de manera sistemática a partir del modelo de programación lineal primal:

$$
\begin{align}\text{maximización} &\longrightarrow \text{minimización} \\
\text{minimización} &\longrightarrow \text{maximización} \\
\\
\text{variables de decisión} &\longrightarrow \text{slacks} \\
\text{slacks} &\longrightarrow \text{variables de decisión} \\
\\
\text{coeficientes de la función objetivo} &\longrightarrow \text{disponibilidades de los recursos} \\
\underbrace{\text{disponibilidades de los recursos}}_\text{primal} &\longrightarrow \underbrace{\text{coeficientes de la función objetivo}}_\text{dual} \\
\end{align}
$$

La _matriz de coeficientes tecnológicos_ cambia: $\underbrace{ A }_\text{primal} \longrightarrow \underbrace{A^T\cdot(-1)}_\text{dual}$.

Los signos de las restricciones y de las variables se invierten. Un dual de minimización tiene todas sus restricciones de la forma $\ge$, mientras que un dual de maximización las tiene de la forma $\le$.

Ejemplo:

![[Análisis de Dualidad.png]]

El valor óptimo resultante de la función objetivo debería ser el mismo en ambos problemas.

Si se agrega una nueva restricción (no redundante) al modelo, de manera que empeore el valor óptimo actual, se puede determinar una nueva solución óptima mediante una iteración más del método Simplex dual.
