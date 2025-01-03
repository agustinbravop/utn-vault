En [[Estadística]], el muestreo de una [[Población]] nos permite obtener parámetros estadísticos como las [[Medidas de Posición]] o las [[Medidas de Dispersión]], cuyo valor puede variar de muestra en muestra.

En todo muestreo existe cierto margen de error. La **teoría de las muestras** nos permite analizar la **calidad** de una muestra.

Sean $X_1, X_2, \dots, X_n$ una muestra de una población, siendo $\overline X = \frac{X_1, X_2, \dots, X_n}{n}$ la media muestral. Siendo $X_1, \dots, X_n$ valores de una variable aleatoria, $\overline X$ también lo es. Se calcula su valor esperado:

$$E(\overline X) = E\left(\frac{X_1, X_2, \dots, X_n}{n} \right) = \frac{1}{n} (E(X_1)+\dots + E(X_n)) = \frac{1}{n} n \mu_X \implies E(\overline X) = \mu_X$$

Y su varianza:

$$V(\overline X) = V\left(\frac{X_1, X_2, \dots, X_n}{n} \right) = \frac{1}{n^2} (V(X_1)+\dots+V(X_n))=\frac{1}{n^2}n\sigma^2_X \implies V(\overline X) = \frac{\sigma^2_X}{n}$$

Por ejemplo, sea una población $2, 3, 6, 8, 11$ con $N=5$, $\mu_X = 6$, y $\sigma^2_X = 10.8$, se seleccionan muestras con reposición siendo $n=2$, y se tienen $25$ muestras posibles:

| 2-2  | 2-3  | 2-6  | 2-8  | 2-11  |
| ---- | ---- | ---- | ---- | ----- |
| 3-2  | 3-3  | 3-6  | 3-8  | 3-11  |
| 6-2  | 6-3  | 6-6  | 6-8  | 6-11  |
| 8-2  | 8-3  | 6-6  | 8-8  | 8-11  |
| 11-2 | 11-3 | 11-6 | 11-8 | 11-11 |

Conclusiones:

1. El total de muestras con reposición de tamaño $n$ posibles es $N^n$.
2. Para realizar una investigación estadística es suficiente una sola muestra de tamaño $n$.
3. La media muestral resulta ser una variable mientras la muestra no esté definida.
4. $\mu_\overline X = \mu_X$.
5. $\sigma_\overline X^2 = \frac{\sigma_X^2}{n} \implies \sigma_\overline X = \frac{\sigma_X}{n}$.
6. En el muestreo con reposición, cuando $n \rightarrow \infty$, se ve que $\overline X \sim N\left( \mu_X, \frac{\sigma_X^2}{n}\right)$. Esto se debe al [[Teorema Central del Límite]]. Si el ejemplo fuera sin reposición, entonces el total de muestras posibles es $\left( N \atop n \right)$.
