Se denomina **carga** (_workload_) a todas las **demandas** que realizan los **usuarios** a los servicios de un sistema informático durante un **intervalo de tiempo**. Esto implica un esfuerzo de las [[Prestaciones de un SI]] (los recursos de HW y SO).

Los usuarios o las necesidades de servicio exigen que un sistema informático deba cumplir una serie de requisitos o **especificaciones de ejecución** para considerar que su funcionamiento es aceptable.

![[Pasted image 20240505213856.png]]

En el subsistema de [[Aplicación de SI y TI]] es clave hacer una adecuada [[Caracterización de la Carga]].

## Carga de Prueba

Para la [[Evaluación de las Prestaciones]] se utiliza una **carga de prueba** que puede ser _real_ o _sintética_.

La **carga real** de un sistema informático **cambia continuamente** y las mediciones no pueden repetirse (excepto al trabajar en un entorno controlado de carga). Por esto para probar el sistema se suele usar un **modelo de carga** o **carga sintética** construida por un conjunto de programas que reproduce la carga real de manera compacta y repetible.

Son **cualidades deseables** de la carga de prueba:

- **Reproductibilidad**: poder probar varias veces.
- **Compacidad**: que reduzca el tiempo de ejecución respecto de la carga real.
- **Compatibilidad**: consistente con el uso de la carga.
- **[[Caracterización de la Carga#Representatividad de un Modelo de Carga|Representatividad]]**: el modelo retiene los aspectos de la carga real.
- **Flexibilidad**: que sea fácil adaptar el modelo.
- **Independencia del sistema**.
