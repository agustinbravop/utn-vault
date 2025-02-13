La respuesta de un [[Sistema de Control]] es:

- **Transitoria**: sucede primero, y se busca que sea mínima.
- **Estable**: es la deseada, se debe mantener a lo largo del tiempo.

![[Análisis de la Estabilidad y del Error en Estado Estable de un Sistema de Control.png]]

La **rapidez de respuesta** del SC está relacionada con la duración del estado transitorio.

Una característica importante de los SC en estado estable es el _error_ que presentan en régimen permanente. El error es una medida de la precisión de un SC: $E(s)=S_i(s)-S_o(s)$.

En un [[Modelos Matemáticos de Sistemas de Control#Lazo Abierto vs Lazo Cerrado|sistema de lazo abierto]], el error en estado estable es la diferencia entre el valor de salida deseado y el realmente obtenido.

$$\text{Si } T(s) = \frac{S_o(s)}{S_i(s)} \implies S_o = T(s) S_i(s) \ \land \ E(s) = S_i(s) - S_o (s) \implies E(s) = S_i(s) \cdot (1-T(s))$$

Por ende, el error en lazo abierto depende de la señal de entrada y de la [[Función de Transferencia]]. Para un sistema de lazo cerrado con retroalimentación unitaria:

$$\frac{S_o(s)}{S_i(s)} = \frac{T^*(s)}{1+T^*(s)} \implies E(s) = S_i(s) - S_i(s) \frac{T^*(s)}{1+T^*(s)} \implies E(s) = \frac{S_i(s)}{1+T^*(s)}$$

Para calcular el error en **estado estable** (cuando $t\longrightarrow \infty$) se asume que desaparecieron todos los efectos transitorios de la respuesta.

El [[Respuesta al Impulso#Teorema del Valor Final|teorema del valor final]] para la [[Transformada de Laplace]] dice que $\lim_{s\rightarrow 0} S * F(s) = \lim_{t\rightarrow \infty} f(t)$. El error en estado estable de un SC depende del valor de la siguiente expresión:

$$e_s = \lim_{s\rightarrow 0} S * E(s)$$

Analizando según el valor de la función transferencia en lazo abierto $T^*(s)$:

$$\text{Sea } T^* (s) = \frac{k(s^m+a_{m-1}s^{m-1}+\dots+a_1s+a_0)}{s^q(s^n+b_{n-1}s^{n-1}+\dots+b_1s+b_0)} \text{ con } a_0,b_0 \ne 0 \ \land \ k \text{ cte}\ \land \ m,q,n\in \Bbb Z$$

El _tipo de sistema_ es igual a la cantidad de términos $s$ independientes en el denominador de $T^*(s)$. El error depende del tipo de sistema. También influye la señal de entrada $S_i(s)$.

Por ejemplo, analizamos el error para una $T^*(s)$ de tipo uno cuando la entrada es una señal escalón: si $T^*(s)$ es de tipo uno $\implies q =1 \implies e_s = \lim_{s\rightarrow 0} s \frac{1}{1+T^*(s)} S_i(s) \underbrace{\implies}_{T^*(s)\rightarrow\infty} e_s = 0$. Por ende, no hay error en estado estable.

| Tipo de sistema | Escalón           | Rampa           | Parábola        |
| --------------- | ----------------- | --------------- | --------------- |
| $0$             | $\frac{1}{1+k_p}$ | $\infty$        | $\infty$        |
| $1$             | $0$               | $\frac{1}{k_p}$ | $\infty$        |
| $2$             | $0$               | $0$             | $\frac{1}{k_p}$ |
| $3$             | $0$               | $0$             | $0$             |

## Perturbaciones

Los sistemas reales también presentan perturbaciones que pueden ser _endógenas_ o _exógenas_.

$$
\begin{align}e_{s_i}(s)&: \text{error cuando } s_i(s)\ne 0 \ \land P(s) = 0 \\
e_{p}(s)&: \text{error cuando } s_i(s)= 0 \ \land P(s) \ne 0 \\
e_t(s) &= e_{s_i}(s) + e_p(s)\end{align}
$$

Por ejemplo:

![[Ejemplo para Perturbaciones.png]]

$$
\begin{align}e_s &= \lim_{s\rightarrow 0} S * E(s) = \lim_{s\rightarrow 0} S * \frac{S_i(s)}{1+T_1(s)T_2(s)} \\
e_p &= \lim_{s\rightarrow 0} S * E(s) = \lim_{s\rightarrow 0} S * \left(\frac{P(s)}{1+\frac{T_2(s)}{1+T_2(s)T_1(s)}}\right) \\
e_t(s) &= e_s(s) + e_p(s)
\end{align}
$$
