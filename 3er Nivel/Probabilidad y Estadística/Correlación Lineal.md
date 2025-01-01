En el [[Ajustamiento Lineal]], el *coeficiente de correlación lineal* $r$ permite medir de forma directa el **grado de relación lineal** entre dos variables $X_i$ e $Y_i$.

$$\begin{align}
r = \frac{\text{cov} (x, y)}{DS(x) \cdot DS(y)} = \frac{S_{xy}}{S_x S_y} = \frac{\frac{1}{n}\sum (X_i - \overline X ) (Y_i - \overline Y)}{\sqrt{ \frac{1}{n} \sum (X_i - \overline X )^2}\sqrt{ \frac{1}{n} \sum (Y_i - \overline Y )^2}} &= \frac{\frac{\sum X_i Y_i}{n} - \overline X \overline Y}{\sqrt{\frac{\sum X_i^2}{n} - \overline X^2} \sqrt{\frac{\sum Y_i^2}{n} - \overline Y^2}} \\
r &= \frac{\sum x_i y_i}{\sqrt{\sum x_i^2} \sqrt{\sum y_i^2}}
\end{align}$$

Pero ahora, recordando que el [[Método de los Mínimos Cuadrados]] abreviado define los coeficientes $b_1' = b_1 = \frac{\sum x_i Y_i}{\sum x_i^2} = \frac{\sum x_i y_i}{\sum x_i^2}$ y $b'_2 = b_2 = \frac{\sum x_i y_i}{\sum y_i^2}$, se las multiplica:

$$b_1 \cdot b_2 = \frac{(\sum x_i y_i)^2}{\sum x_i^2 \sum y_i^2} = r^2 \implies r = \pm \sqrt{b_1 b_2}$$
Donde $-1 \le r \le 1$. Se concluye que las rectas de ajustamiento $\hat Y_i$ y $\hat X_i$ tienen el mismo signo, el cual por convención también coincide con el signo de $r$. Si $r \gt 0$, hay una relación *directa*. Si $r \lt 0$, hay una relación inversa.

![[Correlación Lineal.png]]

## Variaciones

![[Desviaciones en la Correlación Lineal.png]]

Sea un punto particular $(X_i, Y_i)$ para el cual la *desviación total* es la distancia vertical $Y_i - \overline Y$ y la *variación total* es $VT = \sum (Y_i - \overline Y)^2$. Nótese que $frac{VT}{n} = S_y^2$, siendo $S_y^2$ la [[Medidas de Dispersión|variancia]] de $Y_i$.

La *desviación explicada* por el modelo de ajustamiento es la distancia vertical $\hat Y_i - \overline Y$, y la *variación explicada* es $VE = \sum (\hat Y_i - \overline Y)^2$, de la cual se deriva la *variación no explicada* $\overline {VE} = \sum (Y_i - \hat Y_i)^2$.

Las tres variaciones son positivas, de manera que $VT = VE + \overline{VE}$.

Recordando que $a_1' = \overline Y$ y $b_1' = b_1 = \frac{\sum x_y y_i}{\sum x_i^2}$, se multiplica y divide $b_1 \cdot b_2$ por $\sum x_i^2$. Se sabe que $\hat Y_i - \overline Y = b_1 x_i$.

$$r^2 = \frac{(\sum x_i y_i)^2 \sum x^2_i}{(\sum x^2_i)^2 \sum y_i^2} = \frac{b_1^2 \sum x^2}{\sum y_i^2} = \frac{\sum (\hat Y_i - \overline Y)^2}{\sum (Y_i - \overline Y)^2} = \frac{VE}{VT}$$

Donde $r^2$ es el *coeficiente de determinación*, que indica el porcentaje de la variación total explicada por el modelo lineal. Determina la **calidad del ajuste**. Se cumple que $0 \le r^2 \le 1$.

- $0.81  \le r^2 \le 1$ es muy bueno.
- $0.64  \le r^2 \le 0.81$ es bueno.
- $0.49  \le r^2 \le 0.64$ es regular.
