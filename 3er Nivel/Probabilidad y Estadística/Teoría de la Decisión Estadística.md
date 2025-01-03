En [[Estadística]], la **teoría de la decisión estadística** constituye la parte de la **inferencia** estadística que permite decidir, sobre una base de [[Teoría de las Muestras|resultados muestrales]], la validez de algún supuesto del valor de un parámetro.

En esta teoría no se sabe el valor de un parámetro, pero en lugar de estimarlo (como en la [[Teoría de la Estimación Estadística]]), se supone su valor y luego se prueba su validez. Las **pruebas de hipótesis** permiten probar la validez de estos valores supuestos.

**Hipótesis Estadística**: es un supuesto formulado respecto del valor de algún parámetro de una [[Población]]. Existen dos tipos:

- **Hipótesis nula** ($H_0$): se supone un valor determinado y luego se busca rechazarlo.
- **Hipótesis alternativa** ($H_1$): cualquier hipótesis diferente a la nula. Puede adoptar una de 3 formas:
	1. $\mu \gt \mu_0$: prueba *unilateral a la derecha*.
	2. $\mu \lt \mu_0$: prueba *unilateral a la izquierda*.
	3. $\mu \ne \mu_0$: prueba *bilateral*.

## Pasos Operativos

1. **Formulación de la hipótesis nula**: se formula $H_0) \ \mu = \mu_0$.
2. **Formulación de la hipótesis alternativa**: se adopta solo una de las 3 formas.

| Si se desea probar     | Parámetro desconocido | Parámetro conocido |
| ---------------------- | --------------------- | ------------------ |
| Aumento de producción  | $\mu \gt \mu_0$       | $\mu \lt \mu_0$    |
| Disminución de tiempos | $\mu \lt \mu_0$       | $\mu \gt \mu_0$    |

3. **Determinación de valores muestrales**: se realiza la investigación muestral y el [[Cálculo del Tamaño de la Muestra]]. Se obtienen $\overline x$, $S^2_x$, y $S_x$.
4. **Elemento de comparación**: se compara la media poblacional $\mu_0$ con la media muestral $\overline x$. Para esto se estandariza a $z$ cuando $n \lt 30$ o $t$ cuando $n \le 30$.

$$\text{Para la media: } z=\frac{\overline x - \mu_0}{\frac{S_x}{\sqrt n}} \ , \ t = \frac{\overline x - \mu_0}{\frac{S_x}{\sqrt {n-1}}}. \text{ Para la varianza: } z=\frac{S_x - \sigma_x}{\frac{\sigma_x}{\sqrt {2n}}} \ , \ \chi^2_1 = \frac{nS^2_x}{\sigma^2_x}$$

5. **Criterio objetivo**: se determina objetivamente un *valor límite*, usando una probabilidad cercana a cero (dada por el *nivel de significación* $\alpha$). Luego, se encuentra en la tabla correspondiente el *valor crítico* de la variable ($z_c$ o $t_c$), tal que $P(z_c) = 1 - \alpha$. Este valor crítico divide a las zonas de rechazo y no rechazo.

![[Teoría de la Decisión Estadística (Criterio Objetivo).png]]

6. **Regla de decisión**: suponiendo $H_0) \ \mu=\mu_0$: si $|z| \ge |z_c| \implies$ las diferencias entre $\overline x$ y $<'mu_0$ son significativas, por ende se rechaza la hipótesis nula. En cambio, si $|z| \lt |z_c| \implies$ no se rechaza la hipótesis nula. Se utiliza la $t$ de Student cuando $n \lt 30$.

### Análisis del nivel de significación

Estos resultados obtenidos siempre tienen el riesgo del **error**. 

Un *error de tipo I* ($e_I$) es un **falso negativo** que surge cuando se rechaza una hipótesis nula verdadera. El nivel de significancia $\alpha$ es exactamente la probabilidad de cometer este error. 

Un *error de tipo II* ($e_{II}$) es un **falso positivo** ocurre cuando se acepta como verdadera una hipótesis falsa. Su probabilidad de cometerse es $\beta$ y no es anticipable.
