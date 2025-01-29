Se aplican cuatro pruebas de la [[Estadística]] para validar si un conjunto de [[Números Pseudoaleatorios]] se puede considerar aleatorios, y por ende es apto para su uso en un estudio de [[Simulación]].

Si no se rechaza el conjunto $r_i$ en ninguna de las pruebas, se dice entonces que ese conjunto se puede utilizar como un **conjunto de números estadísticamente aleatorios**. Las pruebas son:

1. Prueba de medias.
2. Prueba de varianza.
3. Prueba de uniformidad.
4. Prueba de independencia.

Las pruebas se realizan en ese orden. Si tan solo una prueba falla, entonces el conjunto de números no se puede considerar estadísticamente aleatorio.

## Prueba de Medias

El conjunto $r_i$, con valores entre $0$ y $1$, debe tener un valor esperado igual a $0.5$. 

Sean las hipótesis $H_0: \mu_{r_i} = 0.5$ y $H_1 : \mu_{r_i} \ne 0.5$ y el promedio $\overline r = \frac{1}{n} \sum r_i$, se calculan los límites de aceptación:

$$\text{LI}_\overline{r} = \frac{1}{2} - z_{\alpha /2} \left(\frac{1}{\sqrt{12n}}\right)\ ; \ \text{LS}_\overline{r} = \frac{1}{2} + z_{\alpha /2} \left(\frac{1}{\sqrt{12n}}\right)$$

Si la media está entre $\text{LI}_\overline{r}$ y $\text{LS}_\overline{r}$, entonces se concluye que no se puede rechazar la hipótesis $H_0$ y por ende el conjunto de números pseudoaleatorios pasa esta prueba de medias. Se puede continuar con la prueba de varianza. Es común utilizar un $\alpha$ del $0.05$ (95% de confianza).

## Prueba de Varianza

Esta prueba se utiliza para evaluar si el conjunto de pseudoaleatorios tiene una distribución uniforme. Sean las hipótesis $H_0 : \sigma^2_{r_i} = \frac{1}{12}$ y $H_1 : \sigma^2_{r_i} \ne \frac{1}{12}$ y la varianza $V(r)=\frac{\sum(r_i-\overline r)^2}{n-1}$. Se calculan los límites de aceptación:

$$\text{LI}_{V(r)} = \frac{\chi^2_{(1-\alpha) / 2,\ n-1}}{12(n-1)} \ ; \ \text{LS}_{V(r)} = \frac{\chi^2_{\alpha / 2,\ n-1}}{12(n-1)}$$

Si $\text{LI}_{V(r)} \le V(r) \le \text{LS}_{V(r)}$, entonces con un nivel de aceptación de $1-\alpha$ no se puede rechazar que el conjunto $r_i$ tiene una varianza de $\frac{1}{12}$. Pasa la prueba de varianza.

## Prueba de Uniformidad

Existen algunas alternativas:

- Prueba de Chi-Cuadrado.
- Prueba de Kolmogorov-Smirnov.

Se plantean dos hipótesis: $H_0: r_i \sim U(0,1)$ y $H_1:r_1 \text{ no son uniformes}$. Se particiona el conjunto de $n$ números pseudoaleatorios en $m=\sqrt n$ intervalos fijos. Sean $E_i$ la frecuencia esperada y $O_i$ la frecuencia observada en cada intervalo.

La prueba de Chi-Cuadrado propone determinar $\chi^2_0 = \sum \frac{(E_i - O_i)^2}{E_i}$ y compararlo con el valor de tabla $\chi^2_{\alpha, \ m-1}$. Si $\chi^2_0 \lt \chi_{\alpha,\ m-1}$, entonces no se puede rechazar que $r_i$ sigue una distribución uniforme. 

La prueba de Kolmogorov-Smirnov propone calcular los siguientes valores:

$$\begin{align}D^+&=\max_{1\lt i \lt n} \left\{\frac{i}{n}-r_i\right\} \\
D^-&=\max_{1\lt i \lt n} \left\{\frac{i}{n}-r_i\right\} \\
D &= \max \set{D^+;\ D^-}
\end{align}$$

Se busca en la tabla de valores críticos de Kolmogorov-Smirnov el valor crítico $D_{\alpha, \ n}$. Si $D \lt D_{\alpha,\ n}$, entonces no se ha detectado *diferencia significativa* entre la distribución de los números del conjunto $r_i$ y la distribución uniforme. Se pasa a la siguiente prueba.

## Prueba de Independencia

En esta prueba se comparan los números entre sí para corroborar la independencia entre números consecutivos. Hay muchas alternativas:

- Prueba de series.
- Prueba de poker.
- Prueba de huecos.
- Prueba de corridas arriba y abajo.
- Prueba de corridas arriba y abajo de la media.

Sean las hipótesis $H_0 : r_i \sim \text{Independientes}$ y $H_1 : r_i \sim \text{Dependientes}$.

La prueba de series propone calcular el estadístico de prueba $\chi^2=\sum \frac{(E_i-O_i)^2}{E_i}$, el cual debe ser menor o igual al valor de tabla $\chi^2_{\alpha, \ n-1}$.

En la prueba de corridas arriba y abajo, se arma una secuencia $S$ compuesta de unos y ceros donde por cada valor: si $r\le r_{i-1} \implies s_i=0$, sino $s_i=1$. La secuencia tiene $n-1$ valores. Se define $C_0$ igual a la cantidad de subsecuencias consecutivas de unos y ceros en $S$.

$$\mu_{C_0} =\frac{2n-1}{3}; \ \sigma_{C_0}^2 = \frac{16n-29}{90};\ z_0=\left|\frac{C_0-\mu_{C_0}}{\sigma_{C_0}}\right|$$

La prueba de corridas arriba y abajo no puede rechazar el conjunto solo si $z_0 \le z_{\alpha / 2}$.

Si las cuatro pruebas pasaron, entonces el conjunto $r_i$ se puede usar como un conjunto de números estadísticamente aleatorios.
