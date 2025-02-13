Las **ecuaciones de diferencias** son expresiones que denotan la relación entre las entradas y las salidas de un sistema discreto. Resolverlas implica hallar la respuesta de un [[Sistema de Control]] discreto en el campo de las señales discretas. Para esto se utiliza la **transformada Z**.

Las ecuaciones de diferencias se pueden representar con un [[Diagrama de Bloques Funcionales]]:

![[Ecuaciones de Diferencias.png]]

Sea una función $f^*(t)$ que describe una secuencia de impulsos $\partial (t)$ separados entre sí por un tiempo $T$, que se consideran muestras de una función escalón unitario:

$$f^*(t)=f(0)\partial(t)+f(1)\partial(t-1T)+\dots+f(k)\partial(t-kT)$$

Aplicamos la [[Transformada de Laplace]], recordando que $\mathcal L [\partial (t-T)]=e^{-Ts}$ :

$$
\begin{align} \mathcal L [f^*(t)]&=F*(s)=f(0)\cdot 1 + f(1)\cdot e^{-Ts} + \dots + f(k)\cdot e^{-kTs} \\
\mathcal L [f^*(t)]&=F*(s)= \sum_{k=0}^\infty f(k)\cdot e^{-kTs}
\end{align}
$$

Ahora, se hace un cambio de variable $z = e^{kTs}$ tal que $s = \frac{1}{T}\cdot\ln z$ :

$$Z[f^*(k)]=F(z)=f(0) \cdot 1 + f(1)\cdot z^{-1}+f(2)\cdot z^{-2}+\dots+f(k)\cdot z^{-k}$$

$F(z)$ se denomina **la transformada Z de la secuencia de impulsos**, donde cada período de retardo da como resultado un impulso multiplicado por $z^{-1}$.

## Propiedades Básicas de la Transformada Z

En estos casos, se supone que la entrada $x(t)$ tiene transformada Z $x(z)$ y que $x(t)=0 \ \forall \ t\lt0$:

1. **Linealidad**: si $y(kT) = \alpha \cdot f(kT)+\beta\cdot g(kT) \implies Z[y(kT)]=y(z)=\alpha \cdot f(z) + \beta \cdot g (z)$.
2. **Desplazamiento**: multiplicar por $z$ equivale a un adelanto $T$ en el tiempo de muestreo.
3. **Traslación real**: si $n \in \Bbb N \ \land \ n \gt 0 \implies Z[x(t-nT)] = z^n \cdot x(z)$.
4. **Traslación compleja**: $Z[e^{at} \cdot x(t)]=x(z\cdot e^{at})$.
5. **Valor final**: si $x(z)$ permanece finita, lo cual es la condición de [[Estabilidad]], entonces se cumple que $\lim_{k\rightarrow \infty} x(kT) = \lim_{z\rightarrow 1}(1-z^{-1})\cdot x(z)$.

## Transformada Z de Funciones Básicas

Sea la **función escalón unitario** $f^*(t)=1$:

![[Función Escalón Unitario.png]]

$$
\begin{align}F(z)&=f(0)+f(1)z^{-1}+\dots+f(k)z^{-k} \\
\text{Si el impulso es unitario: } \ F(z)&=1+z^{-1}\dots+z^{-k} \\
\text{Lo cual}& \text{ es una serie geométrica convergente a } \frac{1}{1-\frac{1}{z}} \\
F(z)&=\frac{1}{1-\frac{1}{z}} = \frac{z}{z-1} \text{ donde } |z| \gt 1
\end{align}
$$

Ahora, para la **función rampa muestreada** $f^*(t)=t$:

![[Función Rampa Muestreada.png]]

$$
\begin{align}F(z)&=0+Tz^{-1}+\dots+kTz^{-k} \\
\frac{zF(z)}{T} &= 1+2z^{-1}+3z^{-2}+\dots+k z^{-k-1} \\
&\text{Es una serie geométrica convergente a } \frac{1}{\left(1-\frac{1}{z}\right)^2} \\
F(z)&= \frac{1}{z\left(1-\frac{1}{z}\right)^2} = \frac{Tz}{(z-1)^2} \text{ donde } |z|\gt 1
\end{align}
$$

## Transformada Z Inversa

La **transformada Z inversa**, o antitransformada, de $x(z)$ da la secuencia de tiempo $x(kT)$. A partir de la aplicación de esta antitransformada, solo se obtiene la secuencia temporal de valores correspondientes a los instantes de muestreo del sistema.

Existen infinitas $x(t)$ que originan una secuencia $x(kT)$ que podrían existir en los instantes de tiempo no muestreados. Por esto, la antitransformada Z solo provee valores exactos de $x(t)$ en los instantes de muestreo $x = kT$.

Para calcular la antitransformada, existen diferentes métodos:

- Método de expansión en fracciones parciales.
- Método computacional.
- Método de la división directa.

Esto nos permite entrar y salir de sistemas de control discretos (que usan señales digitales).
