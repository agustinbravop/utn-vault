En la [[Capa de Enlace]], el **control de flujo** es un mecanismo para **evitar que un emisor rápido sature a un receptor lento**. El enlace debe controlar el flujo.

El *tiempo de propagación* $T_\text{prop} = \frac{d}{V}$ es una limitación física por la distancia que un bit viaja. El *tiempo de transmisión* $T_\text{trans} = \frac{L}{R}$ depende de la velocidad del transmisor.

$$\frac{T_\text{prop}}{T_\text{trans}} = a \longrightarrow \text{ si } a \gt 1 \implies \frac{d}{V} \gt \frac{L}{R}. \ \text{Si } a \lt 1 \implies \frac{d}{V}\lt\frac{L}{R}$$

El receptor debe comunicar al transmisor si está saturado o no. Hay dos estrategias:

- **Parada y espera**: por cada trama enviada, el transmisor espera hasta recibir una señal del receptor para enviar la trama siguiente. Resulta ineficiente cuando el tamaño de la trama es pequeño.
- Ventanas deslizantes: la *ventana* es la cantidad de tramas que se pueden enviar. Se espera la señal de recepción por ventana, no por trama. Esta estrategia es más eficiente.

El receptor devuelve un *acuse de recibo* (ACK) que le indica al transmisor que está listo para recibir otro mensaje.
