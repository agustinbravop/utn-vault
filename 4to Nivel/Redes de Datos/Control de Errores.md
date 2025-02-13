En la [[Capa de Enlace]], un _error_ es la pérdida o deterioro de una trama o acuse. Hay varias técnicas para el **control de errores**:

1. Detección de errores.
2. Confirmación positiva (ACK).
3. Temporizador de retransmisión.
4. Confirmación negativa (NAK) y retransmisión.

Estas técnicas permiten aplicar _Automatic Repeat Request_ (ARQ), que tiene varias estrategias:

- **Con parada y espera**: el emisor espera un ACK por cada trama. Si llega al _timeout_ sin recibir un ACK, reenvía la trama. El receptor descarta tramas duplicadas.
- **Con go-back-n**: se usan ventanas de $m$ tramas cada una. Si el emisor envía las tramas 4, 5 y 6, pero sucede un error en la 5, el receptor pide retransmisión desde la trama 5. El emisor busca las 5 y 6 en su _buffer_ y las retransmite.
- **Con selective repeat**: es un poco más sofisticado. El receptor indica las tramas exactas en las que hubo errores y el transmisor solo retransmite esas. Evita descartar tramas innecesariamente.
  - **Solapamiento de ventanas**: este problema ocurre cuando, si el tamaño de la ventana es igual a la cantidad de números de secuencia del [[Protocolo]], y se pierde el acuse de recibo y por ende el transmisor reenvía la misma ventana, el receptor va a pensar que es una ventana nueva siguiente. Se soluciona con $W\le2^{k-1}$ y $W \le \frac{\text{MAX\_SEQ}+1}{2}$.
