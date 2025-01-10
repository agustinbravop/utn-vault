En la [[Teoría de la Codificación]], Nyquist propone una _frecuencia de muestreo_ igual o mayor al doble de la frecuencia natural de entrada, y sostiene que al usar un muestreo con una frecuencia superior al doble de la de entrada, la información recuperada es **redundante**.

Siendo $F_N=2f$, se establece que $F_N \le 2 \Delta F$ cuando los canales son _sin ruido_ y las señales binarias tienen una _transmisión mononivel_ (supuesto que es físicamente inalcanzable).

Es posible superar ese máximo usando transmisión multinivel, mandando mensajes de dos o más bits. Siendo $BPS$ los bits por segundo: $BPS \le 2 \Delta F \log_2 m$, siendo $m$ los niveles de modulación (cables).

**Límite de Nyquist**: $BPS=2\Delta F H$ es la máxima velocidad binaria alcanzable en canales sin ruido.

Luego, Shannon considera los canales [[Ruido|ruidosos]] y su relación entre la cantidad máxima de niveles y la _razón señal a ruido_ del canal, estableciendo el **límite de Shannon**.

$$m_\text{max} = \left( 1 + \frac{S}{N}\right)^{\frac{1}{2}} \implies BPS = 2\Delta F \log_2 m_\text{max} \implies BPS = \Delta F \log_2 \left(1+\frac{S}{N}\right)$$
