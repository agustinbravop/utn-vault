El _inventario_ es la cantidad de artículos que son almacenados y se mantienen inactivos en un instante de tiempo dado. Comprenden materias primas, productos, repuestos, recursos, etc. Hay 3 tipos de inventario:

- Materia prima.
- Productos en proceso.
- Productos terminados.

Todo lo inventariado conlleva un **valor económico**. El objetivo de los **modelos de inventarios** es definir el _nivel de inventario_ que minimiza los costos del sistema sujetos a la restricción de satisfacer la demanda, haciendo un uso óptimo de la capacidad productiva.

Costos involucrados en un problema de inventario:

1. **De fabricación**: por producir el producto. Es una función $C(Z)$ directamente proporcional a la cantidad $Z$ producida.
2. **De mantenimiento**: por almacenar el producto.
3. **De penalización**: por no satisfacer la demanda.
4. **Rendimientos**: ingresos. Importan cuando no se controla el precio de venta.
5. **De recuperación**: o _salvamento_, es el valor de desecho. Es menor al valor de venta.
6. **Tasa de descuento**: tiene en cuenta el valor del dinero en el tiempo.

Estos costos determinan la _rentabilidad del negocio_.

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

La _demanda_ es el número de unidades de un producto que se deberá extraer del inventario en un período de tiempo dado. También puede ser determinística o probabilística.

### Modelo de Wilson

El modelo de Wilson, o el modelo simple sin agotamiento, es el más básico. Supone una demanda constante.

![[Modelo de Wilson sin Agotamiento.png]]

- $K$: costo de preparación o de emisión de la orden de compra. Es independiente de la cantidad ordenada.
- $b$: costo del producto. Es el costo unitario de la cantidad comprada.
- $c_1$: costo de almacenamiento. Representa almacenar una unidad de un ítem durante una unidad de tiempo.
- $I$: es la tasa de mantenimiento, tal que $I\cdot b = c_1$.
- $c_2$: costo de escasez o agotamiento.
- $D$: demanda anual fraccionada en $n$ lotes de tamaño $q$, tal que $D = n\cdot q$.
- $T$: tiempo total fraccionado en $n$ períodos iguales, tal que $T = n \cdot T_i$.

Si $n=\frac{D}{q}$ es el número de órdenes emitidas en el período $T$, entonces $n\cdot K = \frac{D}{q}K$ es el costo de preparación. El costo propio del producto es $b\cdot D$. En este modelo, es constante y conocido. El _costo total esperado_ resulta:

$$\text{CTE} = \frac{D}{q}K + \frac{Q}{2}Tc_1$$

Y $\text{CTE}$ será mínimo cuando $\frac{d\text{CTE}}{dq} = -\frac{DK}{q^2_0}+\frac{Tc_1}{2}=0$ y $\frac{d^2\text{CTE}}{dq^2} = \frac{2DK}{q^3_0}\gt0 \implies q_0\gt 0$. Así, el _lote óptimo_ $q_0$ resulta:

$$q_0 = \sqrt{\frac{2DK}{Tc_1}} \implies \text{CTE}_0 = \sqrt{2KDTc_1}$$

Si $\sqrt{\frac{2KD}{Tc_1}}\ge D$, entonces $q_0 =D$.

### Modelo de Demanda Constante con Stock de Protección

Se agrega al modelo de Wilson un **inventario de contingencia**, reconociendo los eventuales errores de estimación o cálculo que pueden ocurrir en la realidad. Dado que el stock mínimo es $s_p \ne 0$, se añade el costo de mantener el stock de protección: $s_p T c_1$.

![[Modelo de Demanda Constante con Stock de Protección.png]]

El lote óptimo es idéntico al modelo de Wilson: $q_0 = \sqrt{\frac{2KD}{Tc_1}}$ y $T_0 = \sqrt{\frac{2KT}{c_1D}}$. El $\text{CTE}_0$:

$$\text{CTE}_0 = \sqrt{2KTDc_1} + s_pTc_1$$

### Modelo de Demanda Constante con Agotamiento

Se asume un agotamiento simple con escasez, es decir, en este modelo pueden ocurrir **faltantes**. Se agrega un costo de preparación $\frac{D}{q}\cdot K$.

![[Modelo de Demanda Constante con Agotamiento.png]]

El costo de almacenamiento para un período será $\frac{1}{2}sT_{i_1}c_1 = \frac{1}{2}s^2\frac{T_i}{q}c_1$. Considerando además que $T_i = \frac{T}{n}=\frac{Tq}{D}$, se llega a $\frac{1}{2}s^2\frac{T}{D}c_1$. Por semejanza de triángulos: $\frac{T_{i_1}}{s}=\frac{T_i}{q} \implies T_{i_1}=\frac{T_i s}{q}$. El costo para todo el tiempo adoptado será: $\frac{1}{2}s^2\frac{T}{\cancel D}c_1\frac{\cancel D}{q}=\frac{1}{2}s^2\frac{T}{q}c_1$.

El costo de agotamiento para un período será $\frac{1}{2} T_{i_2} (q-s)c_2 \implies \frac{1}{2}\frac{T_i(q-s)^2}{q}c_2 \implies \frac{1}{2}\frac{T}{D}(q-s)^2c_2$.

$$CTE = f(s,q) = \frac{KD}{q}+\frac{1}{2}s^2\frac{T}{q}c_1 + \frac{1}{2}\frac{T}{q}(q-s)^2c_2$$

El costo total esperado $\text{CTE}$ resulta mínimo en $\frac{\partial \text{CTE}}{\partial s}=\frac{\partial\text{CTE}}{\partial q}=0$.

$$
\begin{align}\frac{\partial \text{CTE}}{\partial s} = s \frac{\cancel T}{q} c_1 - \cancel T c_2 + \frac{\cancel T}{q}s \ c_2 = 0 \implies s_0 = \frac{c_2 q_0}{c_1 + c_2} &= \sqrt{\frac{2KD}{Tc_1}} \cdot \sqrt{\frac{c_2}{c_1+c_2}} \\
\frac{\partial \text{CTE}}{\partial q} = -2KD - s^2_0T(c_1+c_2)q^2Tc_2=0 \implies \dots \implies q_0 &= \sqrt{\frac{2KD}{Tc_1}} \cdot \sqrt{\frac{c_1+c_2}{c_2}}
\end{align}
$$

Reemplazando, siendo $\frac{c_2}{c_1+c_2}\lt 1$ la _tasa de deficiencia_, nos queda:

$$
\begin{align}
\text{CTE}_0 = \sqrt{2KDTc_1} \cdot \sqrt{\frac{c_2}{c_1+c_2}} \\
T_0 = \sqrt{\frac{2KT}{Dc_1}} \cdot \sqrt{{\frac{c_1+c_2}{c_2}}}
\end{align}
$$

### Modelo Triangular (Reposición No Instantánea)

En el modelo triangular, se supone la reposición no instantánea para considerar las demoras que puedan existir. Se define la _velocidad de producción_ $p$, tal que se debe cumplir $p \gt d$ para satisfacer la demanda.

Se utiliza una función stock $S(t)=P(t)-\delta (t)$ que es igual a lo producido menos lo demandado.

![[Modelo Triangular (Reposición No Instantánea).png]]

Entre $t=0$ y $t=t_p$, se cumple que $p = \frac{q}{t_p}$. Si $t = t_p$, entonces:

$$
\begin{align}S(t_p)&=P(t_p)-\delta (t_p)  \\
&= p \cdot t_p - d \cdot t_p\\
&= t_p(p-d)=S_m\end{align}
$$

Donde $S_m$ es el stock máximo, que ocurre cuando $t = t_p$. El costo de almacenamiento $\text{CA}$ es:

$$\text{CA} = c_1 \int_0^{t_1} S(t)dt = \frac{1}{2} c_1 S_m t_1 = \dots = \frac{1}{2}c_1 q \left(1 - \frac{d}{p}\right) t_1$$

Si todos los períodos son iguales:

$$\text{CTE} = \underbrace{\frac{D}{q}K}_\text{preparación} + \underbrace{b \cdot D}_\text{producto} + \underbrace{\frac{1}{2}q \ Tc_1\left(1-\frac{d}{p}\right)}_\text{almcenamiento}$$

Resulta:

$$q_0 = \sqrt{\frac{2KD}{T\left(1-\frac{d}{p}\right)c_1}}=\sqrt \frac{2Kdp}{(p-d)c_1}$$

### Modelo con Descuento por Cantidad

Este modelo es simple y sin agotamiento pero con un costo de compra variable. El costo unitario no crece de forma lineal, sino que crece de a intervalos de la siguiente manera:

![[Modelo con Descuento por Cantidad.png]]

Esto sucede cuando un proveedor nos da una tabla con franjas de precio, dependiendo de cuántas unidades le pidamos.

- $b_i$ es el costo del $i$-ésimo producto.
- $P$ es el porcentaje de interés que se produciría con el dinero inmovilizado.
- $c_i'$ es el costo efectivo de almacenamiento, de manera que $c_i = P \cdot b_i + c'_i$.

$$
\begin{align}\text{CTE}(q, b_i) &= \underbrace{\frac{D}{q} K}_\text{preparación} + \underbrace{b_i \cdot D}_\text{producto} + \underbrace{\frac{1}{2}q\ T (P\cdot b_i + c'_i)}_\text{almacenamiento}\\
q_{0_i} &= \sqrt \frac{2KD}{T(P\cdot b_i + c_i')}
\end{align}
$$

### Modelos con Restricciones

Estos modelos se utilizan cuando existe una restricción del tipo $S \ge \sum_{i=1}^n q_i \cdot s_i$.

- Limitación del número de órdenes: $\text{NO} \ge \sum \frac{S_i}{q_i} \implies \dots \implies q_i = \sqrt \frac{2\lambda D_i}{b_i T}$.
- Limitación del dinero inmovilizado en stock: $\text{TI} \le \sum T_i = \sum \frac{1}{2} q_i b_i \implies \dots \implies q_i = \sqrt \frac{2D_i}{\lambda b_i}$.

En ambos modelos, $\lambda$ es un multiplicador de Lagrange asociado a la restricción. Dado $q_i$ en función de $\lambda$, se lo reemplaza en la restricción original (que contiene a $q_i$) y se despeja a $\lambda$ para encontrar su valor.
