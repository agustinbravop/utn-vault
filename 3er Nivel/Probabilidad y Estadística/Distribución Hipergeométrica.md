La [[Distribuciones de Probabilidad de Variable Discreta|distribución]] **hipergeométrica** se basa en $n$ realizaciones sin reposición de un experimento, siendo los sucesos _condicionales entre sí_. Tiene una deducción similar a la [[Distribución Binomial]], con secuencias excluyentes pero esta vez con eventos dependientes.

Sea un total de $N$ items, de los cuales $X$ tienen la característica $A$:

$$P(\text{en $n$ realizaciones, $x$ apariciones}) = \frac{\left( X \atop x \right) \left( N - X \atop n - x \right)}{\left( N \atop x \right)}$$

Se cumplen $N \gt 0; \ 0 \ge X \ge N; \ 1 \ge n \ge N; \ 0 \ge x \ge n; \ x \le X$.

![[Distribución Hipergeométrica.png]]

## Condición de Cierre

Partiendo del binomio de Newton para $(1+x)^{m+n}$:

$$
\begin{align}
(1+x)^{m+n} &= (1+x)^m (1+x)^n \\
&= 1 + \left( m+n \atop 1 \right) x + \left( m+n \atop 2 \right) x^2 + \dots \\
&= \left[ 1 + \left( m \atop 1 \right) x + \dots \right] \cdot \left[ 1 + \left( n \atop 1 \right) x + \dots \right] \\
\left( m+n \atop r \right) &= \sum_{s=0}^r \left( n \atop s \right) \left( m \atop r-s \right) \\
\left( N \atop n \right) &= \sum_{x=0}^n \left( X \atop x \right) \left( N-X \atop n-x \right) \\
1 &= \sum_{x=0}^n \frac{\left( X \atop x \right) \left( N-X \atop n-x \right)}{\left( N \atop n \right)} \\
\end{align}
$$

## Esperanza

Se define un lema 1:

$$\left( a \atop b \right) = \frac{a}{b} \left( a-1 \atop b-1 \right)$$

Para aplicarlo:

$$
\begin{align}
E(x) &= \sum_{x=1}^{n} x \frac{\left( X \atop x \right) \left( N-X \atop n-x \right)}{\left( N \atop n \right)} = \sum_{x=1}^n \cancel x \frac{\frac{X}{\cancel x} \left( X-1 \atop x-1 \right) \left( N-X \atop n-x \right)}{\frac{N}{n} \left( N-1 \atop n-1 \right)} = n \frac{X}{N} \underbrace{\cancel{\sum_{x=0}^m \frac{\left( Z \atop z \right) \left( M-Z \atop m-z \right)}{\left( M \atop m \right)}}}_\text{=1 (condición de cierre)} = n \frac{X}{N} = np \\
E(x) &= np
\end{align}
$$

## Varianza

$$V(x) = npq \frac{N-n}{N-1}$$

Donde $\frac{N-n}{N-1}$ se denomina _factor de corrección_.
