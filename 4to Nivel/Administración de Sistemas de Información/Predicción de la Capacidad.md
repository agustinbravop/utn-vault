Parte de la [[Planificación de la Capacidad]] es el proceso de **predecir** cuándo los niveles de la carga futura saturarán el sistema y determinar el modo más efectivo (en costos) de **retrasar esa saturación**. La **capacidad** es la **productividad máxima** (throughput máximo) del sistema.

## Patrones de Datos Históricos (Modelos de Comportamiento)

Estos modelos de comportamiento o **patrones de datos históricos** marcan la tendencia histórica y a futuro de la carga, diferenciados por su fluctuación y periodicidad:

- **Tendencia**: refleja una carga de trabajo que **tiende** a aumentar o disminuir claramente.
- **Cíclicos**: fluctuaciones con una **periodicidad frecuente** y consistente. Por ejemplo: PedidosYa se usa más para la cena que para el desayuno.
- **Estacional**: fluctuaciones con una **periodicidad ligada al ambiente** de uso del sistema. Por ejemplo, el SYSACAD no se usa nunca en enero, y se usa mucho en marzo.
- **Estacionario**: no muestra ningún signo de variación sistemática, presenta una **media constante**.

![[Patrones de datos históricos de la carga.png]]

## Métodos de Predicción

Se dividen en cuantitativos y cualitativos:

- **Métodos cuantitativos**: usan **técnicas estadísticas** sobre los patrones de **datos históricos** para **estimar valores futuros** de los parámetros de la carga de trabajo (el rendimiento).
- **Métodos cualitativos**: proceso subjetivo de **análisis e intuición** sobre un mercado considerado. Utiliza opiniones de expertos, planes de negocio y cualquier **información** relevante al espacio tecnológico del sistema.

Los valores obtenidos con métodos cuantitativos se **ajustan** a los obtenidos o con los métodos cualitativos, o con otras [[Técnicas de Evaluación de un SI]] cuantitativas como la monitorización y el benchmarking.

Los **factores** a considerar para seleccionar la técnica de predicción cuantitativa **adecuada** son:

- La disponibilidad y fiabilidad de **datos históricos**.
- La exactitud y el **horizonte** de planificación.
- El **patrón** encontrado en los datos históricos.

### Técnicas Cuantitativas

1. **Regresión lineal**: estima el valor de una variable dependiente como **función lineal** de otras variables independientes. Apropiada para trabajar con **datos no estacionales** que muestran una tendencia.
   Siendo la línea de regresión: $y = a + b * x$, se puede usar el método de **_cuadrados mínimos_**:
   $$b=\frac{\sum^{n}_{i=1} x_iy_i-n\overline{x}\overline{y}}{\sum_{i=1}^{n}x^2_i-n\overline{x}^2} \ , \ a = \overline{y}-b\overline{x}$$
2. **Medias móviles**: predicción simple cuyo valor predecido es la **media de observaciones previas**. Muy útil para predicciones a **corto plazo** de **datos casi estacionarios**. Siendo $y_i$ el conjunto de observaciones, el valor predicho es:
   $$f_{t+1}= \frac{y_t+y_{t-1}+ \ ... + \ y_{t-n+1}}{n}$$
3. **Suavizado exponencial**: similar a las medias móviles pero con más peso en las **observaciones recientes** para dar una mejor indicación del futuro cercano. Se asigna un **peso** $\alpha$ con $0 < \alpha < 1$ al valor observado más reciente:
   $$f_{t+1}= (1 - \alpha) f_t + \alpha \ y_{t-n+1}$$

### Unidades de Predicción Natural

Una _Natural Forecast Unit_ o **NFU** o **UPN** es una **variable de negocio** cuyo valor está **directamente relacionado a los recursos consumidos** por las aplicaciones. Por ejemplo: aumentar la cantidad de empleados aumenta la cantidad de transacciones mensuales de nómina de salarios. Por ende, una predicción de esa variable de negocio permite estimar la utilización de recursos futura.

Los **componentes esenciales** para caracterizar la carga usando NFUs son:

- Medidas del trabajo solicitado al sistema usando NFUs como **métricas**.
- Las relaciones que muestren el **número de transacciones** para cada NFU en el período dado.
- Las relaciones que indiquen los **recursos** del sistema que consume cada transacción.
