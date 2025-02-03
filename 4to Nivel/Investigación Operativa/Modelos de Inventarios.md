El *inventario* es la cantidad de artículos que son almacenados y se mantienen inactivos en un instante de tiempo dado. Comprenden materias primas, productos, repuestos, recursos, etc. Hay 3 tipos de inventario:

- Materia prima.
- Productos en proceso.
- Productos terminados.

Todo lo inventariado conlleva un **valor económico**. El objetivo de los **modelos de inventarios** es definir el *nivel de inventario* que minimiza los costos del sistema sujetos a la restricción de satisfacer la demanda, haciendo un uso óptimo de la capacidad productiva.

Costos involucrados en un problema de inventario:

1. **De fabricación**: por producir el producto. Es una función $C(Z)$ directamente proporcional a la cantidad $Z$ producida.
2. **De mantenimiento**: por almacenar el producto.
3. **De penalización**: por no satisfacer la demanda.
4. **Rendimientos**: ingresos. Importan cuando no se controla el precio de venta.
5. **De recuperación**: o *salvamento*, es el valor de desecho. Es menor al valor de venta.
6. **Tasa de descuento**: tiene en cuenta el valor del dinero en el tiempo.

Estos costos determinan la *rentabilidad del negocio*.

La [[Investigación Operativa]] puede mejorar las políticas de inventario, que determinan cuándo y cuánto reabastecer. Pasos:

1. Formular un modelo matemático que describa el comportamiento del inventario.
2. Elaborar una **política de stock óptima**, a partir de ese modelo.
3. Utilizar un sistema de información para mantener registros de los niveles de inventario.
4. A partir de estos registros, usar la política óptima de stock para saber cuándo y cuánto reabastecer.

Principios para la administración de un depósito:

1. Todo ítem debe estar codificado y localizado.
2. Todo movimiento de inventario debe estar documentado.
3. Diferenciar (con colores) los lugares y documentos de entrada de los de salida.
4. En una auditoría, todo ítem es contado 3 veces por personas diferentes.
5. Los ítems de mayor peso se ubican en niveles inferiores.
6. Al cerrar el día, hay que verificar los saldos de los ítems que tuvieron movimientos.
7. Nadie del personal se va antes de cuadrar el movimiento de los ítems.
8. Si es posible, marcar lo contado e inventariado.
9. Los ítems de un mismo código se almacenan en un mismo lugar.

La **clasificación ABC**, según el volumen monetario (alto, medio, bajo), sirve para optimizar el stock de ítems de alta rotación (que se venden mucho), los cuales conviene que tengan un inventario bajo.

## Modelos Matemáticos Determinísticos

Existe una variedad de modelos matemáticos que resuelven los problemas de inventario. Según su capacidad de **predecir** la demanda, los modelos pueden ser determinísticos o probabilísticos. Veremos en detalle algunos modelos determinísticos.

La *demanda* es el número de unidades de un producto que se deberá extraer del inventario en un período de tiempo dado. También puede ser determinística o probabilística.

s