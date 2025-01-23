Recordando la [[Función de Transferencia]] $F(s)$ de un sistema $Y(s)=F(s)\cdot X(s)$, sea $x(t)=\delta(t)$ la *función impulso unitario*, tal que la respuesta del sistema está determinada por:

$$Y(s) = F(s)\cdot L[\delta (t)] = F(s)$$

Aplicando $L^{-1}$:

$$h(t) = L^{-1}[Y(s)] = L^{-1}[F(s)]$$

Donde $h(t)$ es la *respuesta al impulso* o *función de peso*. La [[Transformada de Laplace]] de la respuesta al impulso del sistema es su función de transferencia.

## Teorema del Valor Inicial

$$\lim_{t\rightarrow 0+} f(t) = f(0+) = \lim_{s\rightarrow \infty}s F(s)$$

## Teorema del Valor Final

$$\lim_{t\rightarrow \infty} f(t) = \lim_{s\rightarrow 0} s F(s)$$
