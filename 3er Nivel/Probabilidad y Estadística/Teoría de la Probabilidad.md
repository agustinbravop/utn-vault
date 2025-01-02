Para construir un modelo probabilístico que describa un fenómeno aleatorio, se necesita conocer todos los resultados posibles y asignarle a cada uno un grado de posibilidad.

El *espacio muestral* $\Omega$ es el conjunto de todos los posibles resultados de un fenómeno aleatorio. Por ejemplo, si lanzamos dos monedas, el espacio muestral es $\Omega = \set{ (C, C), (C, X), (X, C), (X,X)}$. Si lanzamos un dado de seis caras, el espacio muestral es $\Omega = \set{ 1, 2, 3, 4, 5, 6}$.

Todo resultado de un $\Omega$ debe ser **mutuamente excluyente** respecto de los demás, y en conjunto deben ser **colectivamente exhaustivos**. El espacio muestral puede ser **discreto** (enumerable) o continuo (un intervalo de números reales).

Un *evento* o *suceso* $A$ es un conjunto de resultados posibles contenidos en el espacio muestral, de forma que $A \subseteq \Omega$. Bajo esta definición, el espacio muestral $\Omega$ y el conjunto vacío $\phi$ son eventos.

Sea un fenómeno aleatorio que puede dar lugar al suceso $A$ de $h$ formas diferentes, las cuales le favorecen de un total de $n$ formas posibles de ocurrencia del fenómeno. Se define a la *probabilidad* de ocurrencia de $A$ como:

$$n \le 1 \ \land \ 0 \le h \le n \implies 0 \le P(A) \le 1 \ \land \ P(A) = \frac{h}{n}$$

Si $h = 0$, entonces $A$ es un suceso imposible. Si $h = 1$, entonces $A$ es un suceso seguro y cierto.

## Probabilidad de Sucesos Opuestos

Sea $\overline A$ el conjunto de sucesos que no son el suceso $A$. Si $h$ casos favorecen a $A$, entonces $(n-h)$ casos favorecen a $\overline A$, de manera que $P(\overline A) = \frac{n-h}{n}$.

$$P(A) + P(\overline A) = \frac{h}{n} + \frac{n-h}{n} =  \cancel {\frac{h}{n}} + 1 - \cancel {\frac{h}{n}} = 1 \implies P(A) + P(\overline A) = 1$$

![[Probabilidad de Sucesos Opuestos.png]]

## Probabilidad de Sucesos Mutuamente Excluyentes

Sean $A$ y $B$ *incompatibles* de forma que $P(A \cap B) = 0$.

![[Probabilidad de Sucesos Mutuamente Excluyentes.png]]

## Regla de la Suma

Sean $A$ y $B$ mutuamente excluyentes tal que la probabilidad de $A\cup B$ es:

$$P(A \cup B) = \frac{h_A+h_B}{n} = \frac{h_A}{n} + \frac{h_B}{n} = P(A) + P(B) \implies P(A \cup \overline A) = P(A) + P(\overline A) = 1$$

Ahora, si $A$ y $B$ fueran *compatibles*:

$$P(A\cup B) = P(A) + P(B) - P(A\cap B)$$

Se resta la parte que se sumó dos veces.

![[Regla de la Suma.png]]

## Probabilidad Condicional

Sea $P(B /A)$ la *probabilidad condicional* de $B$ dado $A$, es decir la probabilidad de que ocurra $B$ habiendo ya ocurrido $A$.

Si se cumple que $P(B/A) = P(B) \implies$ $A$ y $B$ son *sucesos independientes*.

## Regla de la Multiplicación

Siendo $A$ y $B$ sucesos independientes, se cumple que:

$$P(A/B) = \frac{P(A\cap B)}{P(B)}$$

![[Regla de la Multiplicación.png]]

La cual es la probabilidad de que un "dardo" que cayó en $B$ también caiga en $A\cap B$.
