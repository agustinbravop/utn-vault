Un [[Proyecto]] tiene dos tipos de **costos**: costos directos y costos indirectos.

Los **costos directos** se pueden identificar y asignar directamente a una tarea o actividad. También se llaman _variables_ dado que dependen del volumen de trabajo. Surgen de la hoja de recursos del [[Planificación con Software de Gestión de Proyectos|Microsoft Project]] (MSP), de los recursos asignados a las tareas.

Los **costos indirectos** no se pueden asignar directamente a una tarea particular. También se llaman _fijos_ o estructurales porque se deben afrontar aún cuando no se realiza ninguna actividad.

Algunos costos se pueden considerar _semi-fijos_ cuando varían con respecto a los volúmenes de actividad pero siguen sin ser asignables a una tarea específica.

La **tabla de costos** es calculada por el MSP:

- **Costo fijo**: el total de costos indirectos del proyecto.
- **Costo previsto**: costo del proyecto planificado una vez guardado como línea de base.
- **Costo total**: lo que realmente costó el proyecto. $C_\text{total} = C_\text{real} + C_\text{restante}$.
- **Costo real**: costo de las tareas ejecutadas. Surge cuando hacemos el seguimiento.
- **Costo restante**: costo de las tareas todavía no ejecutadas.
- **Variación**: la diferencia entre el costo total y el costo previsto. Indica las ganancias o pérdidas.

Una vez calculados los costos, se guarda el proyecto en MSP como línea de base. Esto significa que el proyecto ya está planificado, y se puede proceder al [[Seguimiento]] una vez el proyecto inicie.

## Importancia de los Costos

Analizar los costos dentro de una empresa ayuda a la **toma de decisiones**. Por ejemplo:

| Costos     | Nivel 1 | Nivel 2 | Nivel 3 | Nivel 4 |
| ---------- | ------- | ------- | ------- | ------- |
| Fijos      | $1.200  | $12.000 | $12.000 | $12.000 |
| Variables  | $0      | $13.500 | $22.500 | $31.500 |
| Total      | $12.000 | $25.500 | $24.500 | $43.500 |
| Producción | $0      | $15.000 | $25.000 | $35.000 |

Observando el ejemplo, podemos decir que:

- Los costos directos por unidad se mantienen constantes al variar el volumen de producción.
- Los costos unitarios disminuyen al incrementar la producción, debido a que la incidencia de los costos fijos disminuye.
- La empresa debe afrontar los costos fijos cualquiera sea su nivel de producción.

## Costos de los Insumos

$$\text{Costo material} = \text{Costo de adquisición} + \text{Costo de tenencia}$$

Los **costos de adquisición** son todos los costos que incurre la empresa hasta que el material entra a la empresa y es controlado en su almacén.

$$\text{Costo de adquisición} = \underbrace{\text{Importe} - \text{Descuento} + \text{Flete}}_\text{costos directos} + \underbrace{\text{Proporcional a departamentos}}_\text{costos indirectos}$$

Los **costos de tenencia** son todos los costos que surgen de tener el material en la empresa.

$$\text{Costo de tenencia} = \text{Proporcional a departamentos} + \text{Seguros} + \text{Obsolescencia} + \dots$$

Todos estos costos son indirectos y se necesita un _sistema de imputación_ para asignarlos.

$$\text{Tasa de tenencia} = \frac{\text{Costo de tenencia}}{\text{Costo de adquisición}} \times 100$$

Para reducir los costos de tenencia se pueden utilizar varias técnicas, entre ellas:

1. **Análisis de la estructura de stocks**: se clasifica el stock según su costo de reposición, lo cual ayuda a saber qué inventario cuidar y priorizar más. Ejemplo:

| Tipo de stock | Porcentaje del valor | Porcentaje de unidades |
| ------------- | -------------------- | ---------------------- |
| Estratégico   | 20 %                 | 8 %                    |
| Importado     | 28 %                 | 4 %                    |
| Alto valor    | 32 %                 | 9 %                    |
| Escaso valor  | 20 %                 | 79 %                   |
| **Total**     | 100 %                | 100 %                  |

2. **Punto de pedido**: consiste en establecer el momento preciso en el que proveerse para evitar el exceso de inventario. Hay dos puntos de pedido:
   - $PP_{\text{mínimo}}=\text{Días de demora}\times \text{Consumo diario}$.
   - $PP_{\text{seguro}}=(\text{Días de demora}+\text{Márgen})\times \text{Consumo diario}$.
3. **Lote óptimo de compra**: responde a la pregunta de cuándo comprar.

$$Q = \sqrt{\frac{\text{Consumo anual} \times \text{Costo de recepción} \times 200}{\text{Tasa de tenencia} \times \text{Precio de plaza}}}$$

4. **Filosofía just in time (JIT)**: en este enfoque se produce y provee bajo demanda. Es una filosofía que surge en Toyota (Japón) en los 70s y está fundamentada en el desperdicio cero.

### Sistemas de Imputación de Costos Indirectos

Los **sistemas de imputación de costos indirectos** determinan una metodología para cargarlos al producto o servicio realizado. Se pueden usar varios sistemas, entre ellos:

- Sistema tradicional.
- Sistema ABC.

El **sistema tradicional** distribuye los costos indirectos entre los departamentos que intervienen en la elaboración del producto. La base de distribución hace referencia al alquiler, gastos de mantenimiento, etc, de cada departamento.

Según las horas máquina que cada departamento usó para fabricar el producto, se le asigna una mayor cantidad de costos indirectos. Así, se asignan los costos en función al volumen de producción.

El **sistema ABC** de _Costeo Basado en Actividades_ define los siguientes pasos:

1. Determinar actividades generadoras de costos indirectos.
2. Determinar el motivo o causal de los costos en la actividad.
3. Afectar a cada producto en la parte proporcional a dicha actividad.
4. Determinar los costos unitarios de cada producto.

El sistema ABC trata de identificar los costos indirectos con cada producto de la manera más certera posible. Es similar a la asignación de costos directos.

## Costos de la Mano de Obra

La **mano de obra directa** es la mano de obra identificada directamente con el producto final o servicio, y se compone por todos los recursos humanos que hacen tareas en el proceso productivo.

La mano de obra **indirecta** no se asigna directamente al producto ya que cumple una función de apoyo. Ej: secretarios, conserjes, etc.

La mano de obra es un tipo distinto de recurso porque las personas tienen objetivos individuales, enfermedades, accidentes, oportunidades, etc. Esa _impredecibilidad_ influye en la correcta ejecución de las tareas, en el rendimiento, y en el ausentismo.
