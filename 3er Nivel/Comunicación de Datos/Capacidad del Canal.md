La **capacidad del canal** es la velocidad a la que se pueden [[Transmisión de Datos|transmitir los datos]]. Para un **ancho de banda** dado, se busca la mayor velocidad de datos sin superar la tasa de errores permitida. El mayor inconveniente será el [[Ruido]].

Según, Nyquist, para un BSC sin ruido y con ancho de banda $W$ (Hertz), la velocidad es $2 \cdot W \text{ bps}$, siendo $\text{bps}$ bits por segundo. Para señales multinivel, la fórmula es:

$$C = 2 W \cdot \log_2 M$$

Shannon considera el ruido térmico, y propone:

$$C=W\cdot \log_2\left(1+\frac{S}{N}\right)$$

Donde $C$ está medido en $\text{bps}$. Esto se considera un máximo teórico, inalcanzable en la práctica.

**Cociente $E_b/N_0$**:

$$\frac{E_b}{N_0} \text{ donde } E_b = S \cdot T_b = \frac{S}{R}$$
