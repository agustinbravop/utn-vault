La [[Termodinámica]] estudia las transformaciones e intercambios de energía que tienen lugar en la materia, particularmente las transformaciones de trabajo en **calor** y de calor en trabajo.

**Energía Interna**: es toda energía de un sistema que está asociada con sus componentes microscópicos, átomos, y moléculas, cuando se ve desde un sistema de referencia en reposo con respecto al centro de masa del sistema.

El **calor** se define como la transferencia de energía a través de la frontera de un sistema debido a la diferencia de temperatura entre el sistema y su entorno. El trabajo y el calor no son energía, son formas de transferencia de energía.

El calor se mide en **calorías**: 1 caloría es la cantidad necesaria de energía para elevar la temperatura de 1 gramo de agua de 14,5° C a 15,5° C a presión normal. $1 \text{ cal} = 4.186 \text{ J}$.

La **capacidad calorífica** $C$ de una masa $m$ es la energía necesaria para elevarla $1\degree  \text C$, considerando volumen constante o presión constante a veces:

$$C = \frac{Q}{\Delta T} \implies Q = C\Delta T$$

El **calor específico** $c$ es la capacidad calorífica $C$ por unidad de masa $m$:

$$c = \frac{C}{m} = \frac{Q}{m\Delta T} \implies Q = c m \Delta T$$

## Calorimetría

La **calorimetría** es la medición del calor. Sea un recipiente con una cantidad de agua $M$ y con un [[Principio Cero de la Termodinámica#Termómetro|termómetro]] que actualmente indica la temperatura $t_0$. Se le introduce un objeto de masa $m$ con una temperatura mayor a la del agua, por lo que el termómetro marca $t_s$. Eventualmente, ambos sistemas equilibran sus temperaturas, y el termómetro marca $t_e$.

![[Calorimetría.png]]

$$\begin{align}Q_\text{absorbido} &= - Q _\text{cedido} \\
Q_s &= - c_s m_s (t_e - t_s) \\
Q_a &= c_\text{agua} M (t_e-t_0) + [c_\text{termómetro} m_\text{termometro} + c_\text{recipiente} m] (t_e - t_0) \\
C_s &= \frac{(M c_\text{agua} + k)(t_e - t_0)}{m_s (t_s - t_e)}
\end{align}$$

En un *cambio de fase* la energía entregada a la sustancia se usa para cambiar su estructura interna, **sin cambio en su temperatura**. La cantidad de energía necesaria depende de su masa.

El **calor latente** $L$ depende de la sustancia y del cambio de fase:

$$L = \frac{Q}{m} \implies Q = Lm$$
