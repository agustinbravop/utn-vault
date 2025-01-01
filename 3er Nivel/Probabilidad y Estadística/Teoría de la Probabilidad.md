Para construir un modelo probabilístico que describa un fenómeno aleatorio, se necesita conocer todos los resultados posibles y asignarle a cada uno un grado de posibilidad.

El *espacio muestral* $\Omega$ es el conjunto de todos los posibles resultados de un fenómeno aleatorio. Por ejemplo, si lanzamos dos monedas, el espacio muestral es $\Omega = \set{ (C, C), (C, X), (X, C), (X,X)}$. Si lanzamos un dado de seis caras, el espacio muestral es $\Omega = \set{ 1, 2, 3, 4, 5, 6}$.

Todo resultado de un $\Omega$ debe ser **mutuamente excluyente** respecto de los demás, y en conjunto deben ser **colectivamente exhaustivos**. El espacio muestral puede ser **discreto** (enumerable) o continuo (un intervalo de números reales).

Un *evento* o *suceso* $A$ es un conjunto de resultados posibles contenidos en el espacio muestral, de forma que $A \subseteq \Omega$. Bajo esta definición, el espacio muestral $\Omega$ y el conjunto vacío $\phi$ son eventos.

Sea un fenómeno aleatorio que puede dar lugar al suceso $A$ de $h$ formas diferentes, las cuales le favorecen de un total de $n$ formas posibles de ocurrencia del fenómeno. Se define a la *probabilidad* de ocurrencia de $A$ como:

$$n \le 1 \ \land \ 0 \le h \le n \implies 0 \le P(A) \le 1 \ \land \ P(A) = \frac{h}{n}$$

Si $h = 0$, entonces $A$ es un suceso imposible. Si $h = 1$, entonces $A$ es un suceso seguro y cierto.
