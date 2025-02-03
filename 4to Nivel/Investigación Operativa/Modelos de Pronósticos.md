Un _pronóstico_ es una estimación cuantitativa o cualitativa de uno o varios factores (variables) que conforman un evento futuro, en base a información actual o del pasado.

Los **modelos de pronósticos** son utilizados en la [[Investigación Operativa]] para estimar o predecir valores futuros o tendencias basándose en datos históricos y análisis estadísticos de la variable a pronosticar.

Estos modelos se aplican para:

1. Pronosticar la demanda de un producto.
2. Predecir el rendimiento de un proceso de producción.

Los métodos de predicción pueden ser:

- **Cuantitativos**: utilizan datos numéricos y técnicas estadísticas, basadas en modelos matemáticos y en datos históricos.
- **Cualitativos**: son subjetivos, basados en opiniones de expertos, intuición, y experiencia. Son útiles cuando no hay datos históricos disponibles. Ej: método Delphi, juicio experto, focus groups, redacción de escenario.

## Método de Series Temporales

Una _observación_ indica el valor $X_i$ tomado en el instante de tiempo $i$ de una variable aleatoria de interés. Una _serie de tiempo_ es una serie de observaciones $\set{X_1,X_2,\dots,X_t}$ a lo largo del tiempo $i=1,2,\dots,t$.

Una serie de tiempo describe el pasado, a partir del cual un modelo matemático extrapola los datos para generar pronósticos futuros. Suelen tener algunos patrones típicos, como por ejemplo:

![[Modelos de Pronósticos.png]]

Algunos modelos comunes son:

1. **Medias:** obtiene el promedio de todas las observaciones.
2. **Medias móviles**: toma el promedio de las _n_ observaciones recientes.
3. **Suavizado exponencial**: da más peso a las observaciones recientes para reflejar mejor las tendencias actuales de la variable bajo estudio.
4. **Modelo ARIMA** (_Autoregressive Integrated Moving Average_): combinan componentes regresivos, promedios móviles y diferenciación para pronosticar series temporales complejas.

## Método de Regresión

El método de predicción-causa, o el modelo causal o de regresión, consiste en analizar las relaciones causales entre una variable dependiente y una o más variables independientes, para predecir la variable de interés en base a las variables que la afectan. El [[Ajustamiento Lineal]] mediante el [[Método de los Mínimos Cuadrados]] es un ejemplo de este enfoque.
