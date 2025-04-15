Para el profesional que desarrolla un nuevo [[Proyecto]] de un sistema, los ingresos a cobrar dependen de los [[Costos de un Proyecto]] de hacer dicho sistema.

El **flujo de fondos netos** o **presupuesto de caja** nos permite calcular los beneficios que recuperarán la inversión y obtendrán la ganancia. Por ejemplo:

|                       | Año 0       | Años 1 a 5  | Total       |
| --------------------- | ----------- | ----------- | ----------- |
| Inversión inicial     |             |             | $-3.900.000 |
| Ingrresos anuales     | $-3.900.000 | $4.320.000  | $21.600.000 |
| Egresos anuales       |             | $-1.320.000 | $-6.600.000 |
| Flujo de fondos netos | $-3.900.000 | $3.000.000  | $11.100.000 |

El cuadro sugiere que invertimos $3.900.000 y recuperamos $11.100.000 a los 5 años, pero en realidad $11.100.000 no es la ganancia verdadera porque los ingresos y egresos suceden en años distintos, lo cual no considera la **inflación**.

Se deben traer esos flujos anuales al presente para determinar cuánto representan al _momento cero_ de la inversión. Para esto se usa el concepto de **valor futuro** ($V_f$).

$$V_f = V_p \cdot (1+i)^n \implies V_p = \frac{V_f}{(1+i)^n}$$

Donde $i$ es el _interés_ durante los $n$ períodos. $(1+i)^n$ es el _factor de capitalización_ y su inversa es el _factor de actualización_.

El **valor actual neto** es la sumatoria de los flujos de fondos netos expresados al momento cero menos la inversión inicial:

$$\text{VAN} = \frac{Y_1 - E_1}{1+i} +  + \dots + \frac{Y_n - E_n}{(1+i)^n} - I_0$$

Se analiza el $\text{VAN}$ de tres maneras:

- $\text{VAN}=0$: el empresario recupera la inversión pero no gana ni pierde.
- $\text{VAN}\lt0$: el empresario pierde dinero, por lo que el proyecto debe rechazarse.
- $\text{VAN}\gt0$: el empresario gana el dinero del $\text{VAN}$.

El $\text{VAN}$ es un indicador de rentabilidad importante para contextos de inflación.

La **tasa interna de retorno** ($\text{TIR}$) es la tasa de interés $i$ que hace que el $\text{VAN}$ del proyecto sea igual a cero. Es muy importante comparar la $\text{TIR}$ con la tasa de inflación del país. Si la $\text{TIR}$ fuera mayor a la inflación, el proyecto podría aceptarse. Caso contrario, el proyecto ni siquiera cubre la pérdida del valor adquisitivo de la moneda.
