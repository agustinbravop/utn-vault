El _Global Positioning System_ (GPS) es el _Global Navigation Satellite System_ (GNSS) más conocido. Un GNSS permite determinar una ubicación en la Tierra comparando los tiempos de señales transmitidas por satélites.

Constelaciones actuales: GPS (USA), GLONASS (Rusia), Galileo (EU), Beidou (China).

Hay 3 segmentos:

1. **Segmento Espacial**: compuesto por **32 satélites** en 6 [[Órbitas]] de 4 satélites cada una, separadas entre sí por 60°. Hay al menos 8 satélites visibles en cualquier punto y momento.
2. **Segmento de Control**: **6 estaciones de monitoreo** dedicadas a monitorear el sistema. Actualizan relojes y efemérides de los satélites. Existe una estación de control maestro (MCS) y otra alternativa.
3. **Segmento de Usuario**: hay **equipos profesionales y de recreación**. Requieren una antena, procesador, display, y reloj medianamente preciso.

![[Segmentos de GPS.png]]

Los satélites viajan en órbitas bien definidas. Con sus **parámetros orbitales**, podemos transformar su posición a una en un [[Sistema de Referencia de Coordenadas]].

Para los **receptores**, se puede usar el método gráfico de _trilateración_ que requiere la distancia a 3 satélites para formar la intersección de 3 esferas.

Existe otro método matemático que resuelve un sistema de ecuaciones de 4 incógnitas: $X_p$, $Y_p$, $Z_p$, y $\Delta t$. Con 4 satélites se puede encontrar una única solución:

$$
\begin{align}c\cdot (t_1+\Delta t) = \sqrt{(X_{s_1} - X_p)^2 + (Y_{s_1} - Y_p)^2 + (Z_{s_1} - Z_p)^2} \\
c\cdot (t_2+\Delta t) = \sqrt{(X_{s_2} - X_p)^2 + (Y_{s_2} - Y_p)^2 + (Z_{s_2} - Z_p)^2} \\
c\cdot (t_3+\Delta t) = \sqrt{(X_{s_3} - X_p)^2 + (Y_{s_3} - Y_p)^2 + (Z_{s_3} - Z_p)^2} \\
c\cdot (t_4+\Delta t) = \sqrt{(X_{s_4} - X_p)^2 + (Y_{s_4} - Y_p)^2 + (Z_{s_4} - Z_p)^2} \\
\end{align}
$$

![[GPS.png]]

Cada satélite transmite un código diferente. El receptor genera el mismo código de manera simultánea, y lo compara con el código recibido para determinar el desfasaje:

![[Resolución de Distancias en GPS.png]]

Hay dos **mensajes de navegación**:

- Almanaque: brinda la posición aproximada de toda la constelación.
- Efemérides: da la posición precisa de cada satélite individual en función del tiempo.

Fuentes de errores:

1. Errores en la posición de los satélites.
2. Errores por el rebote de la señal en otros elementos.
3. Errores derivados del paso de la señal por la atmósfera.
4. Errores en la precisión de los relojes.
5. _Dilution of Precision_ (DOP), que depende de la geometría de los satélites.

El **GPS diferencial** contempla la corrección de errores.
