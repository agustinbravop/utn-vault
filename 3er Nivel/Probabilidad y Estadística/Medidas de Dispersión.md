En [[Estadística]], las **medidas de dispersión** complementan a las [[Medidas de Posición]], indicando el alejamiento de los valores de la variable respecto de algún valor de referencia. Amplían la información referida al conjunto de datos bajo estudio.

**Rango**: el rango $R$ es la diferencia entre los valores extremos del conjunto de datos ordenados, de manera que $R = x_M - x_m$. Sirve para agrupar los datos.

**Desvío medio**: es el promedio de los desvíos. $DM = \frac{1}{n} \sum |x_i - \overline x|$.

**Varianza**: para datos no agrupados es $S^2_x = \frac{1}{n} \sum(x_i - \overline x)^2$, mientras que para datos agrupados se usa una fórmula ponderada $S^2_x = \frac{1}{n} f_i \sum(x_i - \overline x)^2$ debido a que incluye la frecuencia absoluta.

**Desvío estándar**: $S_x = \sqrt S_x^2$.

**Coeficiente de variación**: es la única medida no absoluta, sirve para comparar distintos conjuntos de datos. $CV_x = \frac{S_x}{\overline x} \cdot 100$. Se considera bueno un $CV_x  \lt 50 \%$, pero puede ser mayor al 100%.

**Rango semi-intercuartílico**: se considera que muestra el "recorrido" de los datos. $Q = \frac{Q_3 - Q_1}{2}$.

**[[Medidas de Posición#Asimetría|Asimetría]]**: $As = \frac{\overline x - M_o}{S_x} \approx \frac{3 (\overline x - M_e)}{S_x}$. Heurísticamente, cuando se cumple $-0.2 \le As \le 0.2$ conviene usar la media aritmética, sino, conviene más usar la mediana o la moda.

**Asimetría basada en los cuartiles**: $As_q = \frac{Q_3 - 2Q_2 + Q_1}{Q_3 - Q_1}$.

## Propiedades de la Varianza

1. La varianza de un conjunto definido de datos es un valor constante mayor o igual a cero.
2. La varianza de una constante es cero: $S_x^2 = \frac{1}{n} \sum(a - \overline a)^2 = \frac{1}{n} \sum (a - a)^2 = 0$.
3. La varianza es una medida mínima si se la copara con otra medida que no se calcule con la media aritmética.
4. a) Sea $d_i = x_i \pm A \implies S^2_d = S^2_x$ tal que la varianza se mantiene igual.
5. b) Sea $d_i = c \cdot x_i \implies S_d^2 = c^2 S_x^2$ tal que la varianza se multiplica por el cuadrado de la constante.
6. Sea $d_i =  x_i + y_i \implies S^2_d = S_x^2 + S_y^2 + 2 S_{xy} = V(x) + V(y) + 2 \cdot  \text{Cov} (x, y)$, donde la _covarianza_ es $\text{Cov}(x,y) = \frac{1}{n} \sum (x_i - \overline x) (y_i - \overline y) = \frac{\sum x_i \cdot y_i}{n} - \overline x \cdot \overline y$.

## Variable Estandarizada

La **variable estandarizada** $z_i$ se obtiene a partir de la transformación algebráica, $z_i = \frac{x_i - \overline x}{S_x}$, donde $S_x$ es el desvío estándar, una de las medidas de dispersión más utilizadas.
