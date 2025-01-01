En [[Teoría de la Estadística]], las **medidas de posición** son valores representativos del conjunto de datos.

La fórmula empírica de Karl Pearson $\overline x - M_o = 3 (\overline x - M_e)$ relaciona las 3 medidas de posición más usadas.

## Promedios

Por excelencia, se usa la *media aritmética*, aunque también se puede usar la geométrica, armónica, o cuadrática. 

$$\overline x = \frac{\sum x}{n}$$

1. Para un conjunto definido, $\sum \overline x = n \overline x$ es constante.
2. $\sum (x_i - \overline x) = \sum x_i - \sum x_i = 0$.
3. $\sum (x_i - \overline x)^2$ es mínimo.
4. a) Sea $d_i = x_i \pm A \implies \overline d = \overline x \pm A$.
4. b) Sea $d_i = c \cdot x_i \implies \overline d = c \cdot \overline x$.
5. Sea $d_i = x_i \pm y_i \implies \overline d = \overline x \pm \overline y$.

La media aritmética se ve afectada por valores extremos (*outliers*).

## Mediana

La mediana es el valor que divide al conjunto de datos en dos partes iguales (50%). No se ve afectada por valores extremos.

$$\text{para datos agrupados: } M_e = VLI + c \cdot \frac{\frac{n}{2}-F_a}{f_m} \ ; \ \text{para no agrupados: } M_e = \frac{n+1}{2}$$

## Moda

Es el valor con la mayor frecuencia absoluta. 

$$M_o = VLI + c \cdot \frac{\Delta_1}{\Delta_1 + \Delta_2} \ ; \ \Delta_1 = f_\text{max} - f_\text{anterior} \ ; \ \Delta_2 = f_\text{max} - f_\text{posterior}$$

## Cuantiles

Los *cuantiles* son valores que dividen al conjunto ordenado en $k$ partes iguales. 

Los *cuartiles* lo dividen en 4 partes, donde $Q_1 = VLI + c \cdot \frac{\frac{n}{4}-F_a}{f_{q_1}}$, $Q_2 = M_e$, y $Q_3 = VLI + c \cdot \frac{\frac{3n}{4}-F_a}{f_{q_3}}$. Se utilizan en los *gráficos de caja*, que condensan muchas medidas de manera visual.

![[Gráfico de Caja.png]]

## Asimetría

La *asimetría* es el grado de desviación hacia la izquierda o derecha con respecto a la moda.

![[Asimetría.png]]

- Asimetría hacia la izquierda: $\overline x \lt M_e \lt M_o$.
- Simetría: $\overline x = M_e = M_o$.
- Asimetría hacia la derecha: $\overline x \gt M_e \gt M_o$.
