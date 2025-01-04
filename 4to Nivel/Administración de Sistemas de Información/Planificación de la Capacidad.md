La **capacidad** es la **productividad máxima** (throughput máximo) del sistema.

La **planificación** de la capacidad es un proceso del subsistema de [[Aplicación de SI y TI]] que observa las **necesidades de negocio** que se deben satisfacer, entendiendo y analizando la [[Carga de Trabajo]] que se va a ejecutar y el servicio (**tiempo de respuesta**) que se quiere dar, y detalla los recursos físicos (**capacidad**) necesarios.

Es el proceso de **identificar la** **configuración** de un sistema para suministrar el [[Rendimiento de un SI]] satisfactorio para las [[Prestaciones de un SI]] determinadas. El objetivo fundamental es:

- Resolver conflictos de **capacidad limitada,** y
- Mantener una **equilibrada utilización** de los equipos.

A futuro, también es el proceso de **predecir** cuándo los niveles de la carga futura saturarán el sistema y determinar el modo más efectivo (en costos) de **retrasar esa saturación**. Esto es la [[Predicción de la Capacidad]].

## Metodología

Una metodología básica y sencilla sigue estos pasos:

1. Dotar de **instrumentación** al sistema.
2. **Monitorizar la utilización** del sistema.
3. **Caracterizar la carga**.
4. **Predecir el rendimiento** bajo diferentes alternativas.
5. **Seleccionar la alternativa** con el menor costo y/o mayor rendimiento.

Una buena planificación de la capacidad, puede al menos minimizar el ajuste de rendimiento en un sistema. Dependen de una correcta [[Caracterización de la Carga]].

## Capacidad Adecuada

La **capacidad adecuada** para dar soporte a la operación de una instalación del sistema es función de tres elementos:

1. Los **[[Acuerdos de Nivel de Servicio]]** o **SLAs**. Son umbrales de productividad, rendimiento y de disponibilidad exigidos y pactados que se deben garantizar. La **calidad de servicio** o **_QoS_** se puede cuantificar mediante la deficiencia de la calidad: $$\text{Desviación del QoS}=\frac{\text{QoS Conseguida} - \text{QoS Deseada}}{\text{QoS Deseada}}$$
2. La **arquitectura del sistema**: se puede cumplir los niveles usando dispositivos y subsistemas distintos. Esto depende de las exigencias del aplicativo, de la experiencia en la explotación, de la facilidad de administración u otros motivos no necesariamente relacionados al rendimiento.
3. El **presupuesto**: los costos restringen la capacidad de la que se puede disponer. Hay costos de **arranque** (compra, instalación, formación inicial) y de **operación** (mantenimiento, ambientales).

Se dice que un SI tiene una **capacidad adecuada** si los niveles de servicio se cumplen continuamente y si los servicios se suministran dentro de los límites de costo acordados.

## Niveles de Planificación

Las organizaciones comienzan de manera simple y **gradualmente van sofisticando** la gestión y planificación de la capacidad. En la actualidad hay una tendencia hacia la **gestión automatizada**. Hay varios niveles: 0. **Nivel 0**: no hay programa de gestión de la capacidad, y se realiza **ocasionalmente**.

1. **Nivel 1**: se usan **medidas de tendencia** y predicción en períodos pico.
2. **Nivel 2**: se conoce la **utilización exacta** de cada recurso debido.
3. **Nivel 3**: existe un sistema automático de **análisis y predicción** de la carga de trabajo.
4. **Nivel 4**: se predicen automáticamente los **niveles de servicio** según predicciones de capacidad.
5. **Nivel 5**: se utilizan los **criterios de las aplicaciones de negocio** a través de un modelo que sirve para predecir los niveles de servicio.
