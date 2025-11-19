Estos sistemas de [[Inteligencia Artificial]] trabajan en entornos de incertidumbre. Aprovechan el [[Teorema de Bayes]] o teorema de las causas:

$$P(E_k/A) = \frac{P(E_k) P(A/E_k)}{P(A)} = \frac{P(E_k)P(A/E_k)}{\sum P(E_i)P(A/E_i)}$$

El modelo basado en [[Probabilidad]] será, para $i=1,\dots,n$:

$$p(e_i | s_1,\dots,s_m) = \frac{p(e_i) \cdot p(s_1,\dots,s_m | e_i)}{\sum p(e_j) \cdot p(s_1,\dots,s_m | e_j)}$$

Y se aplica una *simplificación* del cálculo que sacrifica exactitud pero mantiene proporcionalidad:

$$
p(e_i | s_1,\dots,s_m) \propto p(e_i) \cdot \prod p(s_j|e_i)
$$

Donde $p(s_j | e_i)$ es la **verosimilitud**, que representa el conocimiento.

¿Qué pasa si no se puede contar? Por ejemplo, si los atributos son continuos. En estos casos se utiliza alguna de las [[Distribuciones de Probabilidad de Variable Continua]]. Por ejemplo, usando la [[Distribución Normal]]:

$$f(x)=\frac{1}{\sigma\sqrt{2\pi}} e ^{\frac{(x-\mu)^2}{2\sigma^2}}$$

Donde la **media** es $\mu = \frac{1}{N}\sum_{i=1}^N x_i$ y el **desvío** es $\sqrt \sigma^2=\sqrt{\frac{\sigma(x_i-\mu)^2}{N}}$.

El modelo basado en probabilidades más simple es el **Naive Bayes**.

## Naive Bayes

Una vez obtenidas las probabilidades a priori y las verosimilitudes:

$$V_{NB} = \underset{v_j \in V} {\text{argmax}} [P(V_j) \prod_i P(a_i | v_j)$$

Se obtiene una distribución normal **por cada par clase-dimensión**, considerando que las clases son exhaustivas y mutuamente excluyentes. Cada distribución permite calcular $P(a_i=x|v_j)$ dado un valor $x$ perteneciente a la dimensión $a_i$ y usando la distribución normal para $a_i$ y $v_j$.

Finalmente se obtiene $p(e_i|s_1,\dots,s_m)$ para $i=1,\dots,n$. De estos valores se elegirá el mayor para clasificar al nuevo dato en la clase $e_k$ cuyo $p(e_k|s_1,\dots,s_m)$ sea el mayor. Esto es así gracias a que la simplificación del cálculo mantiene la **proporcionalidad** entre las probabilidades, de manera que el ranking no se ve afectado. Se puede obtener la **probabilidad real** haciendo:

$$\frac{p(e_k|s_1,\dots,s_m)}{\sum p(e_i|s_1,\dots,s_m)}$$

gracias a la condición de cierre.

### Naive Bayes para Histogramas

No todos los problemas tienen dimensiones que siguen la distribución normal. Existen muchas otras distribuciones que se pueden usar.

También se puede **particionar** el atributo continuo en intervalos discretos para evitar usar una distribución de probabilidad. A mayor cantidad de intervalos (**bins**) es mayor la *resolución* y por ende mejora la precisión del modelo. Esto se denomina Naive Bayes para **histogramas**. El enfoque de histogramas es bueno cuando los datos no siguen una distribución clara.

Los bins no necesitan ser del mismo tamaño, y une exceso de bins puede empeorar la precisión del modelo.
