En la [[Teoría de la Estimación Estadística]], el **cálculo del tamaño de la muestra** permite determinar el tamaño aceptable que debe tener una muestra para un muestreo de calidad. La [[Teoría de las Muestras]] dice que una sola muestra es suficiente para realizar una investigación estadística, siempre y cuando su tamaño $n$ sea aceptable.

## En Muestreo con Reposición

Se sabe que $\overline x \ne \mu_x$ pr lo que se puede definir una tolerancia $d =\overline x - \mu_x$ tal que:

$$\frac{d}{\sigma_\overline x}=\frac{\overline X - \mu_x}{\sigma_\overline x}=z_I \ \land \ \sigma_\overline x = \frac{\sigma_x}{\sqrt n} \implies z_I = \frac{d}{\frac{\sigma_x}{\sqrt n}} \implies n = \frac{z_I^2 \ \sigma_x^2}{d^2}$$

Vemos que el tamaño de la muestra depende de:

1. $\sigma^2_x$: a mayor variabilidad de la variable, mayor tamaño de la muestra.
2. $z_I^2$: indica el grado de confianza exigido en la estimación. A mayor muestra, mayor confianza. La confianza será $z^2_I = 1$ cuando $n \rightarrow \infty$.
3. $d^2$: a menor margen de error tolerado, mayor tamaño de la muestra. Si $d=0$, entonces $n=N$.

## En Muestreo sin Reposición

Es un caso similar al anterior pero con algunos factores de corrección.

$$d = \overline X - \mu_x \implies \frac{d}{\sigma_\overline X} = \frac{d}{\frac{\sigma_x}{\sqrt n}\frac{\sqrt{N-n}}{\sqrt {N-1}}} = z_I \implies n = \frac{z^2_I \sigma_x^2 N}{d^2(N-1)+z_I^2\ \sigma_x^2}$$

Se puede validar que $\lim_{N\rightarrow\infty} n= \frac{z_I \sigma^2_x}{d^2}$, por ende se obtiene la ecuación del caso con reposición.

Nota: el valor de $n$ siempre se redondea hacia arriba.
