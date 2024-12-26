Los átomos tienen un momento dipolar magnético debido a lmovimiento de los electrones. En general se cancelan, pero en presencia de un [[Campo Magnético]] $B$ externo los dipolos microscópicos se alinean a $B$. Dentro de un material [[Polarización de un Dieléctrico|polarizado]], los dipolos magnéticos crean un campo magnético paralelo a los vectores momento dipolar magnético.

## Vector Magnetización

El estado magnético de la sustancia se describe mediante el vector magnetización $\vec M$, igual al momento dipolar magnético por unidad de volumen, siendo $N$ el número de átomos por unidad de volumen y $<\vec\mu>$ el momento dipolar magnético medio de los átomos:

$$\vec M = N <\vec \mu>$$

Sea una barra de longitud $L$ y sección $A$ magnetizada:

![[Vector Magnetización.png]]

$$B_m = \mu_0 I_m \ \land \ \mu = I_m A = \frac{B_m L A}{\mu_0} \text{ pero } \mu = \int M dV = MLA = \frac{B_mLA}{\mu_0} \implies \vec B_m = \mu_0 \vec M$$

Donde $\vec B_m$ es el **campo magnético inducido** por la magnetización $M$. El $\vec B$ total en un punto interior de la sustancia es $\vec B = \vec B_0 + \vec B_m = \vec B_0 + \mu \vec M$.

## Intensidad Magnética

Sea un solenoide de longitud $L$, con $n$ espiras por unidad de longitud, lleno de un material con momento magnético $M$ por unidad de volumen y por el que circula una corriente $i$. Aplicando la [[Ley de Ampere]]:

![[Intensidad Magnética.png]]

$$\oint \vec B \vec {dl} = \oint (\vec B_0 + \mu_0 \vec M) \vec {dl} = \mu_0 I \ \overset{\text{ por Ampere }}\implies \oint \left(\frac{\vec B}{\mu_0}-\vec M\right)\vec{dl} = I$$

Se define la _intensidad magnética_ $\vec H = \frac{\vec B}{\mu_0} - \vec M$ para simplificar el análisis: $\oint \vec H \cdot \vec {dl} = I$. La circulación de la intensidad magnética $H$ es igual a la [[Corriente Eléctrica]] a debida a las [[Cargas Eléctricas]] libres que atraviesan el área definida por el camino de integración.

También se definen la _permeabilidad magnética relativa_ $\mu_r = \frac{\mu}{\mu_0} = \left( 1 + \frac{M}{H} \right)$ y la _susceptibilidad magnética_ $\chi_m = \frac{M}{H}$, que indica el grado de sensibilidad a la magnetización de un material influenciado por un campo magnético.
