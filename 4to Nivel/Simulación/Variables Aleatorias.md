Las **variables aleatorias** son aquellas que tienen un *comportamiento probabilístico* en la realidad, y es importante conocer la distribución de [[Probabilidad]] que explica su comportamiento.

Sabemos que:

- La suma de probabilidades asociadas a todos los valores posibles de la variable aleatoria $x$ es $1$.
- La probabilidad de que un valor de $x$ se presente es $\ge 0$.
- El valor esperado de la variable es la media de la misma.

En un estudio de [[Simulación]], se debe determinar el tipo de distribución de una variable aleatoria a partir de un conjunto de observaciones para saber cómo generar los valores de esa variable.

Prueba de Chi-Cuadrado para determinar si una distribución de probabilidad se ajusta a una variable aleatoria:

1. Obtener al menos $30$ datos de la variable aleatoria a analizar.
2. Calcular la media y varianza de los datos.
3. Crear un histograma de $m=\sqrt n$ intervalos, con la frecuencia observada $O_i$ de cada intervalo.
4. Establecer la hipótesis nula mediante una distribución de probabilidad que se ajuste a la forma del histograma.
5. Calcular $E_i$ a partir de la función de probabilidad propuesta.
6. Calcular el estadístico de prueba $\chi^2_0 = \sum \frac{(E_i-O_i)^2}{E_i}$.
7. Definir el nivel de significancia $\alpha$ y determinar el valor crítico de la prueba $\chi^2_{\alpha, \ m-k-1}$.
8. Si $\chi^2_0 \lt \chi_{\alpha,\ m-k-1}^2$, entonces no se puede rechazar la hipótesis nula (la distribución se ajusta).

Hoy en día existe software que realiza el *auto-fit* de manera automática para, dado un conjunto de datos, encontrar las distribuciones de probabilidad que mejor se ajustan a ellos.

## Métodos para Generar Variables Aleatorias

Los conjuntos de [[Números Pseudoaleatorios]] varían entre $0$ y $1$. Se necesitan métodos para, utilizando estos números y la distribución de probabilidad que explica el comportamiento de nuestra variable aleatoria, generar valores de la variable.

### Método de la Transformada Inversa

Este método es el más directo. Simula variables aleatorias continuas. Pasos:

1. Definir la función de densidad $f(x)$ que represente la variable a modelar.
2. Calcular la función de probabilidad acumulada $F(x)$.
3. Despejar la variable aleatoria $x$ para obtener la función acumulada inversa $F^{-1}(r)$. El problema es que no todas las funciones tienen una inversa fácil de encontrar, lo cual limita la aplicación de este método.
4. Generar valores de $x$ con números pseudoaleatorios $r_i \sim U(0,1)$ en $F^{-1}(r)$.

![[Método de la Transformada Inversa.png]]

### Método del Rechazo

