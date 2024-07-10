La **monitorización** es una [[Técnicas de Evaluación de un SI]] para **supervisar**, analizar y evaluar el comportamiento y [[Rendimiento de un SI]] **en funcionamiento**. Permite **observar** la actividad de un sistema mientras es usado por usuarios.

La monitorización es implementada por un [[Monitor]] como herramienta de monitoreo.

Sirve para:

1. Conocer la utilización de recursos (identificar [[Cuellos de Botella]]).
2. Encontrar segmentos de código más utilizados (_profiling_).
3. Realizar la [[Caracterización de la Carga]] y crear una [[Carga de Prueba]].
4. La adaptación dinámica del propio sistema según su carga (_auto-scaling_).

Una **medida** permite tratar fenómenos cuantitativamente, son observaciones mediante las cuales se efectúa el **seguimiento** del sistema. No se habla de medición dada la dificultad de repetir las mismas condiciones de carga y tiempo. Por esto se habla de monitorización y seguimiento.

## Tipos de Técnicas

1. **Detección de acontecimientos**: por eventos que cambian el estado del sistema. Requiere insertar _traps_ en en lugares determinados del SO para detectar esos eventos.
2. **Períodos de tiempo**: por muestreo a intervalos de tiempo fijos o aleatorios mediante interrupciones de reloj.

## Presentación de los Resultados

La forma de presentar los resultados facilita su interpretación. Existen gráficos, tablas, etc. Las variables presentadas pueden ser:

- **Cualitativas**: un conjunto de categorías mutuamente excluyentes. Suelen ser palabras.
- **Cuantitativas**: se expresan numéricamente y pueden ser **discretas** o **continuas**.
