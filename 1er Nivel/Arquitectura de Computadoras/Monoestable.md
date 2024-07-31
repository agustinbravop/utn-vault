El **monoestable** es un [[Circuitos Digitales|sistema lógico]] basado en los [[Biestables]]. Trabaja con dos estados pero una sola posición estable (siempre se estabiliza en la misma posición).

![[Monoestable.png]]

$\theta$ determina un **período de tiempo** que el monoestable tarda en estabilizarse. $R$ es el **impulso** que estabiliza al monoestable. El estado estable es 0 (por eso es un flip-flop RS que se estabiliza cuando $R = 1$). Ante un impulso en $S$ el estado pasa a 1 hasta que el temporizador $\theta$ manda un 1 por $R$.

Siempre que la duración del impulso $S$ sea menor a $\theta$, no habrá indeterminación por $S = R = 1$.
