La _población_ $N$ es el conjunto de elementos que responden a una característica en común.

La _muestra_ $n$ es el subconjunto de elementos de una población, que se estudiarán de manera referida a toda la población, para ahorrar tiempo y costo. Debe ser una muestra _representativa_ de la población. Por ende, a mayor variabilidad en la población, mayor debe ser la muestra.

![[Población.png]]

Una _variable_ es una característica concreta de los elementos de una población. Puede ser:

- **Cualitativa**: describe al elemento. Es **ordinal** si hay una jerarquía (ej: bueno, medio, malo) o **nominal** si es una lista desordenada (ej: ciudades del mundo).
- **Cuantitativa**: es un valor numérico. Es **continua** si están asociadas a la medición, o **discreta** si está asociada al conteo. En las de **razón**, el 0 indica la no existencia. En las de **intervalo**, el 0 divide el intervalo.

A veces se usa una _muestra piloto_ $n_h$ tal que si $n_h \lt n \implies$ se obtiene una nueva muestra, y en cambio si $n_h \ge n \implies$ se mantiene $n_h$.

El _muestreo_ es el método estadístico que permite seleccionar una muestra de una población. Puede ser un muestreo:

1. **Simple al Azar**: sirve para cuando se puede listar todos los elementos de una población de características homogéneos (de baja variabilidad).
2. **Estratificado**: cuando la población tiene una variabilidad importante, conviene dividirla en $h$ estratos heterogéneos entre sí pero internamente homogéneos, tal que $n = \sum_{i=1}^h n_i$.
3. **Sistemático**: es conveniente cuando la población está ordenada en una secuencia en la que el atributo a analizar es aleatorio.

El _rango_ $R$ es la diferencia entre el valor máximo $x_M$ y el valor mínimo $x_m$ de la muestra:

$$R = x_M - x_m$$

Los datos de la muestra se dividen en [[Intervalos de Clase]] para su tratamiento y análisis. Las [[Medidas de Posición]] son valores representativos del conjunto de datos.
