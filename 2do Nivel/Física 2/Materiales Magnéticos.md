De acuerdo con sus propiedades, los **materiales magnéticos** se clasifican en:

1. **Paramagnéticos**: débilmente atraídos por [[Campo Magnético|campos magnéticos]] intensos.
2. **Diamagnéticos**: débilmente repelidos por campos magnéticos intensos.
3. **Ferromagnéticos**: fuertemente atraídos por campos magnéticos intensos. Presentan fenómenos de histéresis y dominios magnéticos.

Las sustancias pueden clasificarse en términos de su permeabilidad magnética $\mu$ al compararla con la permeabilidad del espacio libre $\mu_0$.

$$\mu = \mu_0 (1+\chi_m) \begin{cases} 
\mu \gt \mu_0 \ \text{ sustancia paramagnética } \\
\mu \lt \mu_0 \ \text{ sustancia diamagnética }
\end{cases}$$

Debido a que $\chi_m$ es muy pequeño para sustancias paramagnéticas y diamagnéticas, en estas sustancias se observa que $\mu \approx \mu_0$. En sustancias ferromagnéticas, $\mu$ suele ser cientos de veces más grande que $\mu_0$.

## Paramagnetismo

$0 \lt \chi_m \le 1$: la susceptibilidad es pequeña, como resultado de la presencia de átomos o iones que tienen un momento magnético permanente. Se halló experimentalmente la Ley de Curie:

$$M = C \frac{B_0}{T}$$

Donde $C$ es la *constante de Curie*, una constante positiva específica para cada material, y $T$ depende de la temperatura. Por debajo de la *temperatura de Curie* $T_c$, los momentos magnéticos están alineados y la sustancia se vuelve ferromagnética.

![[Magnetización en Función de la Temperatura Absoluta.png]]

## Diamagnetismo

La susceptibilidad magnética $\chi_m \lt 0$ es negativa e independiente de la temperatura. Al aplicarle a estos materiales un campo magnético externo, un débil momento magnético en dirección opuesta al campo es inducido. Esto causa una débil repulsión por [[Imanes]].

El diamagnetismo está presente en todas las sustancias, pero la ser tan débiles sus efectos, solo se evidencia en ausencia del paramagnetismo y ferromagnetismo.

## Ferromagnetismo

La susceptibilidad $\chi_m \gt 0$ es grande. Existen interacciones entre los *spins* de los electrones. En ausencia de campo magnético existen dominios magnéticos con magnetización no nula. Estos dominios se comportan como pequeños imanes orientados al azar.

![[Dominios Magnéticos.png]]

Al aplicar un campo magnético $B_0$ externo, los momentos se alinean dando lugar a una [[Magnetización]] neta $M$.

### Curva de Histéresis

![[Curva de Histéresis.png]]

1. En $O$: $B_m = 0$ con dominios orientados al azar.
2. En $a$ y $d$: puntos de saturación donde $M = M_\text{sat}$.
3. En $b$ y $e$: el campo $B = B_m$ es igual al campo remanente.
4. En $c$ y $f$: el material está desmagnetizado debido a $M = 0$.

![[Ciclos de Histéresis.png]]

La curva de histéresis permite determinar si cierta sustancia es un material ferromagnético duro (que forma un buen imán permanente) o un material ferromagnético blando (que sin un campo externo, pierde fácilmente la magnetización).
