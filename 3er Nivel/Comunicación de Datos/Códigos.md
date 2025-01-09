Sea *alfabeto* un conjunto de letras o *símbolos* que forman *palabras* al encadenarse entre sí. Un **código** es un subconjunto de palabras del alfabeto.

Si $C$ es un código sobre $A$ y $A$ tiene $q$ elementos $\implies$ $C$ es un código $q$-ario.

Si todas las palabras del código tienen la misma longitud, se lo considera un *código de bloques*. Si $C$ es de longitud $n$ y tiene $m$ palabras, es un $(n,m)$-código.

Sea una *función de codificación* $F$ con una aplicación biyectiva (por ende *descifrable*) $f: A\rightarrow C$. Por ejemplo: el código Morse $f: \set{a,b,\dots,z} \rightarrow \set{., \_, \ }$ no tiene longitud fija, y las letras más comunes tienen as codificaciones más cortas, lo que aumenta su **eficiencia**.

 En la [[Detección de Errores]], los **códigos detectores de errores** asumen que el canal de la [[Comunicación de Datos]] es ruidoso y entonces buscan maximizar la [[Teoría de la Codificación|cantidad de información]] transmitida sin perder demasiada confiabilidad.

$P(a_j \ \text{recibido} | a_i \ \text{enviado})$ es la probabilidad de enviar un símbolo y recibir otro. En la práctica, el canal perfecto no existe, y las probabilidades de transición sí existen.

Se considera que el [[Ruido]] se distribuye **aleatoriamente** y que el canal es *sin memoria*, por ende una transmisión con error no afecta a las siguientes transmisiones. Para detectar errores, se necesita añadir *redundancia* de manera que se pueda validar que las palabras recibidas son erróneas. Sea la *tasa de información* $R = \frac{1}{n}\log_q m$ para la **relación dato-redundancia**.

Ej: el código $C = \set {000000, 010101,1 101010, 111111}$ presenta una repetición por tres. Si nos llega una palabra que no es del código, la aproximamos a la que [[Distancia de Hamming|dista]] 1 del código, suponiendo que solo hay un error. Aplicando la tasa de información: $R = \frac{1}{6} \log_2 4 = \frac{1}{3}$ se demuestra que solo un tercio del mensaje es información.

## Decodificación

Se considera el código $C \subseteq A^n$ y $u \rightarrow w$. Para *decodificar*, se utiliza una aplicación $f(w) = u$ llamada *regla de decisión*. Si $f: A^n \rightarrow C$ verifica $P(w | f(w)) = \max P(w|v)$ entonces $f(w)$ tiene la mayor probabilidad de coincidir con la palabra enviada. Se dice que $f$ es una regla de decisión de *probabilidad máxima*.

Sea un Binary Simmetric Channel (BSC) en el cual $p$ es la probabilidad del error. Bo se conoce el valor de $1-p$ y no se calculan probabilidades, sino que se ve cuál es la palabra del código más próxima a la palabra recibida.

![[BSC.png]]

En un BSC, este método coincide con una regla de decisión de probabilidad máxima.

Dado un BSC con $0 \le p \le \frac{1}{2}$, la probabilidad de tener $k$ errores en $k$ posiciones de manera que la $w$ recibida difiera de la $v$ enviada en $k$ lugares es: $P(w|v) = p^k \cdot (1-p)^k$.

Se dice que la decodificación es *completa* si solo hay una palabra con distancia mínima. Es *incompleta* cuando se produce un error por haber más de una palabra posible.
