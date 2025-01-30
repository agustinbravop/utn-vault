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

Este método solo conviene usar cuando el método de la función inversa es inviable, lo cual es común cuando la función bajo estudio no tiene inversa fácil de definir. 

Se busca generar un valor que venga de la distribución de probabilidad bajo análisis. Antes de comenzar el proceso iterativo, definir un $M$ con valor $M \ge \max (f(x))$, siendo $f(x)$ una distribución de probabilidad *acotada* donde $a \le x \le b$. Pasos:

1. Generar dos pseudoaleatorios $r_1$ y $r_2$. 
2. Determinar un valor de la variable aleatoria como $x = a + (b - a) \cdot r_1$.
3. Evaluar la función de probabilidad $f(x)$ en $x = a + (b-a)\cdot r_1$.
4. Aceptar $x$ solo si se cumple que $r_2 \le \frac{f(x)}{M}$. Si no se cumple, descartar este valor $x$ y reiterar desde el paso 1 para generar otro valor.

Este método se apoya en la idea de que la condición $r_2 \le \frac{f(x)}{M}$ tiene una probabilidad de cumplirse de $\frac{f(x)}{M}$. Por eso, el valor se rechaza si $r_2 \gt \frac{f(x)}{M}$. Esto presenta una **ineficiencia** en el método: requiere muchas iteraciones para generar una cantidad suficiente de valores aleatorios.
