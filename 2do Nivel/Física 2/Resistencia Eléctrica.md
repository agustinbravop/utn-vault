La **resistencia eléctrica** $R = \frac{L \rho}{A}$ se deriva de la [[Ley de Ohm]]. Es una propiedad extensiva (porque depende de la cantidad de material de un cuerpo). Se define como:

$$R = \frac{V}{I} \ ; \ [\text{Ohm } \Omega] = \frac{[\text{Volt } V]}{[\text{Ampere } A]}$$

Los resistores utilizados en circuitos usualmente llevan su valor marcado en su superficie mediante un código de barras de colores.

![[Resistencia Eléctrica.png]]

Si $R = \frac{\rho L}{A} \implies \rho = \frac{RA}{L} = [\Omega m]$. La **resistividad** $\rho$ de un material es un valor tabulado (se busca en una tabla). Indica cuánto resiste el material al paso de [[Cargas Eléctricas]]. 

Por lo general, la resistividad varía respecto de la temperatura: $\rho (T) \approx \rho_0 [1 + \alpha (T-T_0)]$, donde $\alpha$ es un *coeficiente térmico de resistividad*.

![[Tabla de Resistividades.png]]

## Resistencias Equivalentes

Las formulas son inversas a las de un [[Capacitor]]. En serie:

![[Resistencia Eléctrica en Serie.png]]
$$V = V_1 + V_2 = I R_1 + I R_2 = I R_{eq} \implies R_{eq} = R_1 + R_2 = \sum_{i=1}^n R_i$$

En serie, se tiene que $R_{eq}$ es mayor que $R_1$ y mayor que $R_2$. Ahora, en paralelo:

![[Resistencia Eléctrica en Paralelo.png]]

$$I = I_1 + I_2 = \frac{V}{R_1} + \frac{V}{R_2} = \frac{V}{R_{eq}} \implies \frac{1}{R_eq} = \frac{1}{R_1} + \frac{1}{R_2} = \sum_{i=1}^n \frac{1}{R_i}$$

En paralelo, se tiene que $R_{eq}$ es menor que $R_1$ y menor que $R_2$.
