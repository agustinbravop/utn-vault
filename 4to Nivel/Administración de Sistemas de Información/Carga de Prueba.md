Para la [[Evaluación de las Prestaciones]] se utiliza una **carga de prueba** que puede ser _real_ o _sintética_.

La [[Carga de Trabajo]] **real** de un sistema informático **cambia continuamente** y las mediciones no pueden repetirse (excepto al trabajar en un entorno controlado de carga). Por esto para probar el sistema se suele usar un **modelo de carga** o **carga sintética** construida por un conjunto de programas que reproduce la carga real de manera compacta y repetible.

Son **cualidades deseables** de la carga de prueba:

- **Reproductibilidad**: poder probar varias veces.
- **Compacidad**: que reduzca el tiempo de ejecución respecto de la carga real.
- **Compatibilidad**: consistente con el uso de la carga.
- **[[Caracterización de la Carga#Representatividad de un Modelo de Carga|Representatividad]]**: el modelo retiene los aspectos de la carga real.
- **Flexibilidad**: que sea fácil adaptar el modelo.
- **Independencia del sistema**.

## Implementación

Las **fases de implementación** de un modelo de carga son:

1. **Especificación**: se definen los **componentes básicos** de la carga real y el conjunto de **parámetros** para describirlos en base al **nivel de detalle** del modelo.
2. **Construcción**: cuatro operaciones básicas:
   1. Análisis de los **parámetros**: mediante técnicas estadísticas.
   2. Extracción de **valores representativos**: mediante variedad de técnicas.
   3. Asignación de valores a los **componentes** del modelo.
   4. Reconstrucción de **mezclas de componentes** significativos: secuencias de peticiones que reproduzcan en el modelo **situaciones similares** a las de la carga real.
3. **Validación**: se evalúa el **criterio** de [[Caracterización de la Carga#Representatividad de un Modelo de Carga|representatividad]] del modelo (y su nivel). Se **compara** su comportamiento con el de la carga real en **puntos conocidos**. Un modelo de carga puede **calibrarse** modificando los valores de sus parámetros.
