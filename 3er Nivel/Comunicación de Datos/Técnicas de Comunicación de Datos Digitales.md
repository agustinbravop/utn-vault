La [[Señales y Espectros|señal]] se transmite en un único camino de a un elemento de señal a la vez. En la [[Comunicación de Datos]] se debe resolver la _temporización_: el receptor debe conocer el instante de llegada y la duración de cada bit para muestrearlo correctamente. Si esto no se resuelve, sucede la _desincronización_.

La [[Transmisión de Datos]] puede ser:

- **Asíncrona**: se evita la temporización al enviar caracter por caracter, tal que el receptor puede _resincronizarse_ al inicio de cada caracter. Cada caracter va acompañado por un 20% de información de control.
- **Síncrona**: se transmiten bloques de bits sin utilizar [[Códigos]] de comienzo o parada. Se deben sincronizar los relojes del emisor y del receptor.

## Configuraciones de la Línea

Al configurar un enlace, interesa la _topología_: la distribución física de las estaciones de la red en el medio de transmisión. Se define si un _enlace_ es **punto a punto** o **multipunto**. También interesa si la transmisión es **full-duplex** (dos sentidos en simultáneo) o **semi-duplex** (dos sentidos alternos).

Las _interfaces_ tienen características:

1. **Mecánicas**: cables.
2. **Eléctricas**: niveles de tensión.
3. **Funcionales**: circuitos de intercambio.
4. **De procedimiento**: conexión DTE-DCE.
   - DTE: Data Terminal Equipment. Usan el medio de transmisión a través del DCE.
   - DCE: Data Circuit-Terminating Equipment. Equipo de red.
