El **diagrama de Nyquist**, o **diagrama polar**, busca representar la misma información que un [[Diagrama de Bode]] en un solo gráfico. El diagrama es una _traza polar_ de la [[Respuesta en Frecuencia]] del [[Sistema de Control]].

Hay cuatro puntos clave a representar:

- $w=0$: inicio de la traza.
- $w=\infty$: fin de la traza.
- $\phi = 0\degree \ \lor \ \phi = \pm 180\degree$: donde la traza cruza el eje real.
- $\phi = \pm 90\degree$: donde la traza cruza el eje imaginario.

## Criterio de Estabilidad de Nyquist

El **criterio de estabilidad de Nyquist** es un método gráfico-numérico para determinar la [[Estabilidad de los Sistemas de Control]] mediante un diagrama de Nyquist.

El lugar geométrico $G(jw)H(jw)$ con $-\infty \le w \le \infty$ encierra $N$ veces con un giro completo al punto $-1+0j$.

Se considera que $N$ es positivo si los giros son en sentido horario. Sea $P$ el número de polos en el semiplano derecho de la [[Función de Transferencia]] de lazo abierto.

$$\text{Sea } Z=N+P: \text{ el sistema es estable} \iff z = 0 \implies N = -P$$

En un sistema [[Estabilidad|estable]], $G(jw)H(jw)$ debe encerrar $P$ veces a $-1+0j$ en sentido antihorario.

![[Diagrama de Nyquist.png]]

Para que el sistema sea estable, tanto el margen de ganancia (MG) como el margen de fase (MF) deben ser positivos.

Si $\frac{1}{\text{MG}} \gt 1 \implies \text{MG}\lt 1 \implies MG$ es negativo. Si se tiene $G(jw)H(jw)\lt-180\degree\implies$ MF es negativo. Si MG y/o MF es negativo, el sistema es inestable.
