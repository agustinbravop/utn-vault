La [[Planificación]] de un [[Proyecto]] se puede realizar con **software de gestión de proyectos**, como Microsoft Project.

Microsoft Project visualiza el proyecto con un **diagrama de Gantt**. Este software logra incorporar en la [[Representación de un Proyecto]] los faltantes del método de los potenciales:

- Duración de cada tarea.
- Recursos asignados a cada tarea.
- Fechas de inicio y fin.

El software calcula automáticamente:

- La duración de cada tarea y del proyecto.
- El costo de cada tarea, de cada tarea resumen, y del proyecto.
- Tareas pertenecientes al [[Camino Crítico]].

![[Microsoft Project.png]]

Conceptos de Microsoft Project (MSP):

1. **Información del proyecto**: se ingresa nombre, fecha de inicio, y fecha de fin.
2. **Tareas**: se cargan las tareas y MSP determina el diagrama de Gantt.
3. **Tareas resumen**: agrupan un conjunto de subtareas relacionadas. Permiten dividir al proyecto en etapas para controlar y priorizar por etapas.
4. **Calendario**: dependiendo del tipo de proyecto se muestra en días, semanas, o meses.
5. **Hitos**: puntos de control representados con un ◆. Representan el fin de una etapa o tarea resumen. Son tareas de duración cero y costo cero, como simplemente firmar un reporte.
6. **Vinculación de tareas**: se puede dar de cuatro maneras.
   - **Fin a comienzo**: `A` termina para que `B` comience. Es secuencial.
   - **Comienzo a comienzo**: `A` y `B` comienzan juntas.
   - **Fin a fin**: `A` y `B` finalizan juntas.
   - **Comienzo a fin**: `B` termina solamente si `A` ya comenzó.
7. **Asignación de recursos**: primero se cargan en la _hoja de recursos_ y luego se asignan.
   - **Grupo**: identifica si el trabajador es contratado, de planta, directivo, etc.
   - **Capacidad máxima**: 100% = 8 horas por día = 1 día laboral.
   - **Tasa estándar hora**: es el valor por hora de trabajo que cobra el recurso humano.
   - **Tasa hora extra**: es el valor de hora extra que cobra (generalmente un 50%).
   - **Costo por uso**: costo por servicio realizado, o el costo de recursos materiales consumidos.
   - **Calendario base**: es el calendario de 8 horas diarias que dice cuándo trabajar.
8. **Asignación de tiempos**: la unidad de tiempo a usar depende del tipo de proyecto.
   - **Estimación única**: se usa en actividades convencionales de tiempo normalizado dado que son conocidas.
   - **Estimación por ponderación**: es aplicable a proyectos en desarrollo con _tiempos inciertos_.

$$T_\text{esperado} = \frac{T_\text{optimista} + 4 \times T_\text{medio} + T_\text{pesimista}}{6}$$
