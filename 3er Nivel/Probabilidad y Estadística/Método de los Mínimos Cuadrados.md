El método de los mínimos cuadrados para el [[Ajustamiento Lineal]], formulado por Gauss, propone encontrar una recta $\hat Y_i = a_1 + b_1 X_i$ analizando los desvíos del modelo de regresión.

![[Método de los Mínimos Cuadrados.png]]

Un _desvío_ es $e_i = Y_i - \hat Y_i$, siendo $Y_i$ un valor empírico de la ordenada.

$$
\begin{align}
a_1 &= \frac{\sum Y_i \sum X_i^2 - \sum Y_i X_i \sum X_i}{n \sum X_i^2 - (\sum X_i)^2} \\
b_1 &= \frac{n \sum Y_i X_i - \sum Y_i \sum X_i}{n \sum X_i^2 - (\sum X_i)^2}
\end{align}
$$

Siendo $a_1$ un coeficiente que indica la cantidad promedio de $Y_i$ cuando $X_i = 0$ (ordenada al origen), y $b_1$ un coeficiente que indica la variación promedio de $Y_i$ para una variación unitaria de $X_i$ (pendiente).

$$\sum_{i=1}^n Y_i = n a_1 + b_1 \sum^n_{i=1} X_i \implies \sum^n_{i=1}Y_i - n a_1 - b_1 \sum^n_{i=1}X_i = \sum^n_{i=1} (Y_i - a_1 - b_1X_i) = \sum^n_{i=1}(Y_i - \hat Y_i) = 0$$

Dado $\sum (Y_i - \hat Y_i) =0$, la recta de ajustamiento se comporta como una [[Medidas de Posición|medida de posición]] _dinámica_.

## Método Abreviado

Se transforma la variable $X_i$ para simplificar las ecuaciones de $a_1$ y $b_1$. Sea $x_i = X_1 - \overline X$ tal que se cumple $\sum x_i = \sum (X_i - \overline X) = 0$, aplicando una propiedad de la media aritmética.

$$
\begin{align}
\sum_{i=1}^n Y_i = n a_1' + \cancel {b_1' \sum_{i=1}^n x_i} = n a'_1 \implies a'_1 &= \frac{\sum_{i=1}^n Y_i}{n} = \overline Y \\
\sum_{i=1}^n Y_i x_i = \cancel{a_1' \sum_{i=1}^n x_i} + b_1' \sum_{i=1}^n x_i^2 = b_1' \sum_{i=1}^n x^2_i \implies b_1' &= \frac{\sum_{i=1}^n x_i Y_i}{\sum_{i=1}^n x_i^2} \\
\hat Y_i &= a'_1 + b'_1 x_i
\end{align}
$$

Ahora, dado $\hat Y_i = a_1' + b'_1$:

$$
\begin{align}
\hat Y_i + a_1' + b_1' x_i = a_1' + b_1' (X_i - \overline X) = a_11' + b_1' X_i - b_1' \overline X &= (a_1' - b_1' \overline X) + b_1' X_i \\
a_1 &= (a_1' - b_1' \overline X) = \overline Y - b_1 \overline X \\
b_1 &= b_1'
\end{align}
$$

En el gráfico, se dice que la variable $x_i$ es _centrada_ porque a cada $X_i$ se le resta $\overline X$. Este desplazamiento no afecta a la pendiente, lo cual explica que $b_1 = b_1'$.

## Caso Inverso

Ahora, se imagina una alternativa en la que $Y_i$ es la variable independiente.

Sea un ajustamiento inverso con una segunda recta ajustada $\hat X_i = a_2 + b_2 Y_i$. Por lo general, la recta original y la inversa no coinciden, es decir, $a_1 \ne a_2$ y $b_1 \ne b_2$.

$$a'_2 = \frac{\sum X_i}{n} = \overline X \ \land \ b_2' = \frac{\sum y_i X_i}{\sum y_i^2}$$

![[Caso Inverso del Método de los Mínimos Cuadrados.png]]

En el gráfico se evidencia que ambas rectas se intersectan en el punto $(\overline X, \overline Y)$.
