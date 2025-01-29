La _cantidad de información_ $I$ es una medida de la disminución de incertidumbre de un suceso. La cantidad de información que se obtiene al conocer un hecho es directamente proporcional al número posible de estados previos, y proporcional a la [[Probabilidad]]. Según Shannon:

$$I = \log_2 \left(\frac{1}{p}\right)$$

La $I$ de los mensajes es su cantidad de bits en binario: la cantidad de símbolos posibles que representan el mensaje.

La _entropía_ $H$ de Shannon es la suma ponderada de todas las cantidades de información de todos los posibles estados de una variable aleatoria $v$:

$$H(v) = \sum_{i=1}^n \ P(x_i) \cdot \log_2\left(\frac{1}{P(x_i)}\right)$$

Si $P(x_i)=1 \implies H(v)=0$, por lo que si el suceso es seguro o cierto entonces desaparece la _incertidumbre_. $H(v)$ es proporcional a la longitud media de los mensajes, por lo que, dado un alfabeto cualquiera, es conveniente codificar en mensajes cortos los símbolos más comunes.

Un _bit_ mide la cantidad de información asociada al suceso con dos posibilidades equiprobables. Ej: se requiere 1 bit para el resultado de tirar una moneda, y 4 bits para almacenar los dígitos decimales.

Dentro de un **sistema de transmisión**, la entropía es la cantidad de información media de sus mensajes, tal que $H = I_\text{med}$.

Si un conjunto de mensajes $N$ todos son equiprobables, la entropía total es $H = \log_2 N$. La entropía indica la _cantidad de bits necesarios_ para representar un mensaje.

**Teorema de Disminución de la Entropía**: la entropía de una variable $X$ condicionada por otra $Y$ es menor o igual a la entropía de $X$: $H(X/Y)\le H(X)$. Si fueran iguales, entonces $X$ e $Y$ serían independientes.

Shannon propone $I(X,Y) = H(Y) - H(Y/X)$ como la _cantidad de información que $X$ contiene sobre $Y$_. Se cumple que $I(X,Y)\ge 0$ y $(X,Y)=I(Y,X)$. Esto significa que la $I$ que aporta conocer $X$ al medir $H(Y)$ es igual a la disminución de entropía que este conocimiento conlleva.
