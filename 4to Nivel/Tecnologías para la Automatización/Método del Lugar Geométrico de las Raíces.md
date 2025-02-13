El **método del lugar de las raíces** es un enfoque práctico para graficar el Lugar _Geométrico de las Raíces_ (LGR).

Este método sirve para conocer cómo varían las raíces del denominador de la [[Función de Transferencia]] dentro del plano [[Números Complejos|complejo]], lo que permite estudiar la [[Estabilidad de los Sistemas de Control]].

Para ello, se generan curvas que muestran el desplazamiento de las raíces conforme cambiamos los valores de funcionamiento. Estos gráficos son el _lugar geométrico de las raíces_ (LGR): un conjunto de curvas que se grafican en el plano complejo.

El método del LGR permite determinar la posición de los polos de la función de transferencia de lazo cerrado para valores de ganancia $k \in [0,\infty]$ a partir de la función de transferencia de lazo abierto.

$$\text{Sea } \frac{C(s)}{R(s)} = \frac{bs+k}{ms^2+bs+k} \longrightarrow ms^2+bs+k=0 \implies \text{ es difícil visualizar } s(m,b,k)$$

Se transforma la expresión para que sea más cómoda de trabajar:

$$\frac{C(s)}{R(s)} = \frac{G(s)}{1+G(s)H(s)} \Longrightarrow \text{Ecuación característica: } 1 + G(s)H(s) = 0$$

La ecuación característica $1 + G(s)H(s) = 0$ se puede expresar de varias maneras:

$$
\begin{align}1 + G(s)H(s) &= 0\\
G(s)H(s) &= -1\\
1 + K\frac{P(s)}{Q(s)} &= 0\\
1 + K\frac{(s+z_1)(s+z_2)\dots(s+z_m)}{(s+p_1)(s+p_2)\dots(s+p_n)}&=0\end{align}
$$

De la expresión $G(s)H(s)=-1$ surgen dos condiciones:

- **Condición de magnitud de la parte real**: $|G(s)H(ss)|=1$.
- **Condición de argumento de la parte compleja**: $\angle(G(s)H(s))=0j$.

El procedimiento del método del LGR es el siguiente:

1. **Hallar los polos y ceros de lazo abierto**: partiendo de $G(s)H(s)$.

El diagrama del LGR tiene tantas ramas como polos de lazo cerrado existan. Los polos siempre son o reales, o complejos conjugados.

2. **Determinar el LGR sobre el eje real**: un punto pertenece al LGR sobre el eje real si el número de polos y ceros de lazo abierto a su izquierda es impar.

Un segmento del LGR sobre el eje real va desde un polo o cero hasta otro polo, o cero, o en el infinito.

3. **Determinar las asíntotas**: las ramas del LGR tocan a las asíntotas en el infinito.

El _ángulo de las asíntotas_ en sentido antihorario es $\alpha = \frac{180°(2k+1)}{n-m}$, tal que hay $n-m$ asíntotas distintas. El _punto de partida de las asíntotas_, que determina la distancia al origen en la que todas las asíntotas cruzan el eje real, es $\sigma_a = \frac{\sum \text{polos finitos} - \sum \text{ceros finitos}}{n-m}$.

4. **Hallar los _puntos de ruptura_**: donde nacen o mueren ramas del LGR.

Los puntos de ruptura están o sobre el eje real, o son pares complejos conjugados. Hay por lo menos un punto de ruptura en todo segmento del LGR entre dos polos de lazo abierto sobre el eje real adyacente, o entre dos ceros de lazo abierto adyacentes aunque uno de ellos esté en el infinito.

Para hallar los puntos de ruptura, se hace $1+G(s)H(s)=0 \longrightarrow B(s)+KA(s)=0$, tal que:

$$\frac{dK}{ds} = \frac{B'(s)A(s)-B(s)A'(s)}{A^2(s)} = 0$$

Si una raíz de $\frac{dK}{ds}=0$ es real, para ser punto de ruptura debe caer en el LGR del eje real.

Si dos raíces son complejos conjugados, $s$ es un punto de ruptura solo si $K(s)$ da un valor positivo real al colocar el valor de dichas dos raíces.

5. **Determinar los puntos en los que el LGR cruza el eje imaginario**.

El eje imaginario implica que la parte real de $s$ es nula, por lo que se puede hacer $s = jw$ en la ecuación característica: $G(jw)H(jw)$. Se obtiene un conjunto de dos ecuaciones (una de la parte real, y otra de la parte imaginaria). Se resuelve el sistema de dos ecuaciones para dos incógnitas:

- $w$: frecuencia en el punto de corte del eje imaginario.
- $k$: valor de la ganancia en ese punto.

6. **Dibujar el LGR**: consiste en inferir visualmente el diagrama.

Ejemplo, dada la siguiente ecuación característica:

$$1+\frac{k(s^3+s^2-s+15)}{s^4+2s^3-3s^2-58s-104}=0$$

![[Método del Lugar Geométrico de las Raíces.png]]
