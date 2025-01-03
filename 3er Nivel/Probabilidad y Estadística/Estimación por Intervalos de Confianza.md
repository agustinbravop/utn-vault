En la [[Teoría de la Estimación Estadística]], la **estimación por intervalos** es un procedimiento que permite, a partir de un [[Estimación Puntual|estimador puntual]], obtener dos valores que limitan un *intervalo de confianza*, dentro del cual se encuentra el parámetro a estimar con una cierta probabilidad conocida, denominada *nivel de confianza*.

$$P(l\le\theta\le u) = NC = 1-\alpha$$

Donde $NC$ es el nivel de confianza, y $\alpha$ es el *nivel de significación*. Sin $NC = 0.95 \implies$ en 95 de cada 100 muestras el parámetro estará dentro del intervalo. Los niveles de confianza más comunes para utilizar son 0.99, 0.95, y 0.90.

## Para Muestras Grandes

Este caso tiene las siguientes condiciones:

1. $n \gt 30$.
2. Todas las estadísticas son variables, y por el [[Teorema Central del Límite]] tienden a tener una [[Distribución Normal]] cuando $n$ es grande.
3. Como $n$ es grande, no se necesita corregir el vicio del estimador $S^2_x$.

$$\overline x = \mu_\overline x = \mu_x \ \land \ \sigma_\overline x = \frac{\sigma_x}{\sqrt n} \text{ se estandariza con } z = \frac{\overline x - \mu_\overline x}{\sigma_\overline x} = \frac{\overline x - \mu_x}{\frac{\sigma_x}{\sqrt n}}$$

Los valores son simétricos de manera que:

$$P\left(-z_1 \le \frac{\overline x - \mu_x}{\frac{\sigma_x}{\sqrt n}}\le z_1\right) = P\left(\overline x + z_1 \frac{\sigma_x}{\sqrt n}\ge\mu_x\ge \overline x - z_1\frac{\sigma_x}{\sqrt n}\right)=NC$$

Ahora, también se estandariza la varianza:

$$z_i =  \frac{S_x-\mu_{S_x}}{\sigma_{S_x}} = \frac{S_x-\mu_x}{\frac{\sigma_x}{\sqrt{2n}}}$$

De manera que:

$$P\left(- z_1 \le\frac{S_x-\sigma_x}{\frac{\sigma_x}{\sqrt {2n}}} \le z_1\right) = P\left(S_x + z_1 \frac{S_x}{\sqrt {2n}}\ge\mu_x\ge S_x - z_1\frac{S_x}{\sqrt {2n}}\right) = NC$$

El nivel de confianza $NC$ es una [[Teoría de la Probabilidad|probabilidad]]. A mayor $NC$, hay mayor probabilidad de que el parámetro caiga en el intervalo pero hay menor precisión en la estimación (por ser un intervalo más grande). Si $N=1 \implies$ el intervalo va de $- \infty$ a $+ \infty$.

![[Intervalo de Confianza para Muestras Grandes.png]]

## Para Muestras Pequeñas

En este caso las condiciones son:

1. $n \le 30$.
2. Todas las estadísticas son variables y tienen una distribución que no necesariamente es normal.
3. Como $n$ es pequeño, es necesario corregir el vicio del estimador $S^2_x$.

Para la media poblacional usamos una [[Distribución t de Student]]:

$$t = \frac{\overline x - \mu_\overline x}{\sigma_\overline x} = \frac{\overline x - \mu_x}{\frac{S_x}{\sqrt{n-1}}} = \frac{\overline x - \mu_x}{\frac{S_c}{\sqrt n}} \ \text{ tal que } \ P(-t_1 \le t \le t_1) = NC$$

Ahora, reemplazando $t$:

$$P\left(-t_1 \le \frac{\overline x-\mu_x}{\frac{S_x}{\sqrt{n-1}}} \le t_1\right) = P\left(\overline x + t_1 \frac{S_x}{\sqrt{n-1}}\ge \mu_x \ge \overline x -  t_1\frac{S_x}{\sqrt{n-1}}\right) = NC$$

Para la varianza poblacional usamos una variable $\chi^2$ de la [[Distribución Chi-Cuadrado]] con $v$ grados de libertad:

$$\frac{nS^2_x}{\sigma^2_x}=\frac{\sum(x_i-\overline x)^2}{\sigma^2_x} = \chi^2_v \ \text{ tal que } \ P(\chi^2_1 \le \chi^2_v \le \chi^2_2) = NC$$

Ahora, reemplazando $\chi^2_v$:

$$P\left(\chi^2_1 \le \frac{nS^2_x}{\sigma^2_x}\le\chi^2_2\right) = P\left(\frac{nS^2_x}{\chi^2_1}\ge \sigma^2_x \ge \frac{nS^2_x}{\chi^2_2}\right) = NC$$

![[Intervalos de Confianza para Muestras Pequeñas.png]]
