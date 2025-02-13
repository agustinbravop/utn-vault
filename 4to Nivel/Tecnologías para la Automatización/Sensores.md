Los **sensores** de un [[Sistema de Control]] son dispositivos que recogen información del mundo real que miden magnitudes físicas y las transforman a señales eléctricas útiles para el SC.

En la actualidad hay varios tipos de sensores para la automatización:

1. **Sensores ultrasónicos**: emiten pulsos, viajan por el aire, y detectan un objeto que los refleja.
2. **Sensores fotoeléctricos**: generan una señal eléctrica en función de la luz recibida.
3. **Sensores de proximidad inductivos**: genera un campo electromagnético que detecta metales.
4. **Sensores de proximidad capacitivos**: cuenta con dos electrodos. Detecta cualquier material.

Un _potenciómetro_ es un dispositivo con valor de resistencia variable que permite controlar la intensidad de corriente. Su salida en volts, siendo $K$ la sensibilidad y $P_p$ la posición, es la siguiente:

$$V_s = K \cdot P_p$$

Un _detector de temperatura_ usa la propiedad de cambio de la [[Resistencia Eléctrica]] de los metales o semiconductores en función de la temperatura.

$$V_s = K_t \cdot T$$

Un _tacómetro eléctrico_ mide las revoluciones de un dispositivo que gira. Por ejemplo, un volante. Su salida, donde $K$ es una constante de proporcionalidad y $w$ es la velocidad angular, es:

$$V(t) = K \cdot \frac{d\phi}{dt} = K \cdot w$$
