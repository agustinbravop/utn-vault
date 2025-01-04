El **_benchmarking_** es el proceso de **comparar** sistemas obteniendo medidas.
$$\text{Benchmarking} \ne \text{Medición}$$

Es un método frecuente de comparar SIs frente a una **carga característica** de una instalación concreta. Es la [[Evaluación de las Prestaciones]] sobre un **prototipo**, y las variantes de este método sirven para **evaluar la potencia relativa** de un sistema a lo largo de su ciclo de vida (compararse con versiones anteriores de sí mismo), **contrastar monitores** y **validar modelos**. Las dificultades son:

- ¿Cómo determinar esa carga característica? [[Caracterización de la Carga]].
- ¿Cómo valorar el aprovechamiento que hacen los programas de las peculiaridades de los distintos sistemas?

En el proceso de _benchmarking_ se utiliza un [[Benchmark]] como herramienta.

## Pasos

1. Determinar **objetivos**: qué se quiere estudiar y porqué.
2. Seleccionar el **benchmark adecuado**: tener en cuenta la [[Caracterización de la Carga#Representatividad de un Modelo de Carga|representatividad]] de la carga.
3. Determinar los **aspectos del sistema** que influyen en el **rendimiento**: se debe asegurar la **comparabilidad** entre experimentos.
4. Ejecutar el **benchmark**.
5. Analizar los **resultados** para estudiar la **causa** de la variación.

## Factores que Influyen

1. El tipo y versión del **SO**.
2. El **compilador** usado en la prueba.
3. El **lenguajes** de programación.
4. El sistema de **librerías** de ejecución.
5. El tamaño de la memoria **cache**.

## Errores Comunes

1. Representar solo los comportamientos medios: olvidar la **varianza**.
2. Controlar inadecuadamente el **nivel de carga**.
3. Ignorar los efectos de la cache: ignorar el **orden de las peticiones**.
4. Ignorar el **overhead del monitor**.
5. No validar las **medidas**: errores de medición.
6. No asegurar las **mismas condiciones iniciales**: experimentos no repetibles.
7. No medir las prestaciones del **estado transitorio**.
8. Comparar las prestaciones con las utilizaciones de recursos.
9. Recoger muchos datos pero analizarlos muy poco.
