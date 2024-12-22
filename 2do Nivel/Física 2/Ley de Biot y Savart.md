La Ley de Biot y Savart es una ley magnética equivalente a la [[Ley de Coulomb]]. La ley enuncia que ante una [[Corriente Eléctrica]] $I$ surge un campo [[Campo Magnético]] $\vec B$.

![[Ley de Biot y Savart.png]]

$$\vec {dB} = \frac{\mu_0}{4 \pi} \frac{I \vec{dl}\times \hat r}{r^2} \ ; \ |\vec {dB}| = \frac{\mu_0}{4 \pi} \frac{Idl \sin(\theta)}{r^2} \ ; \ \vec B = \frac{\mu_0 I}{4\pi} \int \frac{\vec {dl} \times \hat r}{r^2}$$

Donde $\mu_0 = 4 \pi \times 10 ^{-7} \frac{Tm}{A}$ es la *permeabilidad magnética del vacío*.

## Campo Magnético Debido a una Corriente Rectilínea

![[Campo Magnético debido a una Corriente Rectilínea.png]]

$$\begin{align}
|\vec {dl}| = dx \ \land \ \begin{cases} \tan (\pi - \theta) = - \tan \theta = \frac{R}{x} \\ \sin \theta = \frac{R}{r} \end{cases} \implies x = - R \cot \theta &\implies dx = \frac{R}{\sin^2 \theta} d\theta \\
dB = \frac{\mu_0}{4 \pi} \frac{I dl \sin\theta}{r^2} = \frac{\mu_0}{4\pi}\frac{I \sin \theta}{\frac{R^{\cancel 2}}{\cancel {\sin^2 \theta}}}\frac{\cancel R}{\cancel {\sin^2 \theta}} d\theta &\implies dB = \frac{\mu_0}{4\pi} \frac{I}{R} \sin\theta d\theta \\
B = \int dB = \frac{\mu_0 I}{4 \pi R} \int_0^\pi \sin \theta d \theta = \frac{\mu_0 I}{4\pi R}(1 +1) &\implies B = \frac{\mu_0 I}{2 \pi R}
\end{align}$$

La intensidad del campo magnético $B$ en el punto $P$ depende de la corriente eléctrica y de la distancia al punto.

## Campo Magnético Debido a una Corriente Circular

![[Campo Magnético Debido a una Corriente Circular.png]]

Por simetría en el punto $P$, se cancelan las $\vec {dB}_y$. Las $\vec {dB}_x = dB \cos(\theta) \ ; \ r = \sqrt{R^2 + x^2}$. Para hallar el campo a lo largo del eje de la espira:

$$\begin{align}
\cos \theta = \frac{R}{r} = \frac{R}{\sqrt{R^2 + x^2}} &\implies dB_x = dB\cos\theta = \frac{\mu_0 I}{4\pi}\frac{dl}{\sqrt{R^2+x^2}^2}\frac{R}{\sqrt{R^2+x^2}}=\frac{\mu_0 I}{4 \pi}\frac{R}{(R^2+x^2)^{\frac{3}{2}}}dl \\
&\implies \int dB_x = B_x = \frac{\mu_0I}{2} \frac{R^2}{(R^2+x^2)^{\frac3 2}}
\end{align}$$

Donde el campo en el centro de la espira, cuando $x = 0$, es $B_x = \frac{\mu_0 I}{2R}$.

## Fuerzas entre Corrientes

![[Fuerzas entre Corrientes.png]]

Si dos cables están suficientemente cerca, cada uno interactúa con el campo magnético del otro. Dado $\vec F = I \vec d \times \vec B \ \land \ B = \frac{\mu_0 I}{2 \pi R}$ se cumple que:

$$
\begin{rcases} 
F_1 = I_1lB_2  \frac{\mu_0 I_1 I_2}{2 \pi a} l \\
F_1 = I_2lB_1  \frac{\mu_0 I_2 I_1}{2 \pi a} l
\end{rcases} \implies \vec F_1 = - \vec F_2
$$

Si las corrientes eléctricas tienen el mismo sentido, los conductores se atraen. Si las corrientes tienen sentido opuesto, los conductores se repelen.

![[Fuerzas entre Corrientes de Sentido Igual y Contrario.png]]
