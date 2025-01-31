Para la [[Simulación]] de [[Sistemas Discretos]] con la metodología de avance del tiempo constante, se concentra la información a instantes de períodos constante entre ellos. Se define un $\Delta t$ constante, y una cantidad o demanda variable.

## Modelo de Sistema de Almacenamiento

Sea una cantidad de pedido fija, con un momento de pedido variable. El objetivo es minimizar el costo total de funcionamiento de depósito. Datos:

1. $\text{VD}$: función de distribución de probabilidad de la demanda diaria.
2. $\text{DE}$: función de distribución de probabilidad de la demora del proveedor en la entrega.
3. $\text{CALM } \alpha_1 = \$/\text{tiempo}$: costo de almacenamiento.
4. $\text{CVP } \alpha_2 = \$/\text{unidad}$: costo de ventas perdidas.
5. $\text{CEP } \alpha_3 = \$/\text{pedido}$: costo de emisión de pedido.
6. $\text{TF}$: tiempo final o período considerado.

- **Variables de control**: punto de emisión de pedido $\text{SR}$ (stock de reposición) y tamaño del pedido $\text{TP}$.
- **Variables de estado**: stock $\text{ST}$ y pedido realizado $\text{IP}$ (valor booleano).

![[Avance del Tiempo Constante (Sistema de Almacenamiento).png]]

## Modelo de Almacenamiento Alternativo

En este modelo alternativo, se supone una cantidad de pedido variable y un momento de pedido fijo, lo que nos permite considerar perturbaciones e _inercia_. Esto se puede aplicar a, por ejemplo, los comercios cuyo proveedor o repositor viene siempre el mismo día. Cuando viene, se repone según lo vendido o demandado.

**Variables de control**: capacidad del almacén $\text{CA}$ y frecuencia de pedido fija $\text{FP}$.

El diagrama es muy similar al del modelo anterior (cantidad fija, momento variable).

![[Avance del Tiempo Constante (Almacenamiento Alternativo).png]]

Un _ciclo_ es el período de tiempo entre la llegada de dos pedidos. En un ciclo, se pueden acumular _ventas atrasadas_, suponiendo que el cliente compra ni bien se repone el producto.

En la submetodología de tamaño de pedido variable, se prevén _perturbaciones aleatorias externas_. Si en el [[Modelo de Simulación]] del sistema bajo estudio no hay perturbaciones aleatorias externas o se las conoce con exactitud, entonces conviene utilizar la submetodología de tamaño de pedido constante.

En lugar de considerar una capacidad de almacén máxima a rellenar, se puede tener en cuenta _situaciones anteriores_ (inercia) para el cálculo del $\text{TP}$ variable.
