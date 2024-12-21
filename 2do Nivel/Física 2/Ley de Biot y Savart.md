La Ley de Biot y Savart es una ley magnética equivalente a la [[Ley de Coulomb]]. La ley enuncia que ante una corriente $I$ surge un campo [[Campo Magnético]] $\vec B$.

![[Ley de Biot y Savart.png]]

$$\vec {dB} = \frac{\mu_0}{4 \pi} \frac{I \vec{dl}\times \hat r}{r^2} \ ; \ |\vec {dB}| = \frac{\mu_0}{4 \pi} \frac{Idl \sin(\theta)}{r^2} \ ; \ \vec B = \frac{\mu_0 I}{4\pi} \int \frac{\vec {dl} \times \hat r}{r^2}$$

Donde $\mu_0 = 4 \pi \times 10 ^{-7} \frac{Tm}{A}$ es la *permeabilidad magnética del vacío*.

## Campo Magnético debido a una Corriente Rectilínea

![[Campo Magnético debido a una Corriente Rectilínea.png]]

$$\begin{align}
|\vec {dl}| = dx \ \land \ \begin{cases} \tan (\pi - \theta) = - \tan \theta = \frac{R}{x} \\ \sin \theta = \frac{R}{r} \end{cases} \implies x = - R \cot \theta &\implies dx = \frac{R}{\sin^2 \theta} d\theta \\
dB = \frac{\mu_0}{4 \pi} \frac{I dl \sin\theta}{r^2} = \frac{\mu_0}{4\pi}\frac{I \sin \theta}{\frac{R^{\cancel 2}}{\cancel {\sin^2 \theta}}}\frac{\cancel R}{\cancel {\sin^2 \theta}} d\theta &\implies dB = \frac{\mu_0}{4\pi} \frac{I}{R} \sin\theta d\theta \\
B = \int dB = \frac{\mu_0 I}{4 \pi R} \int_0^\pi \sin \theta d \theta = \frac{\mu_0 I}{4\pi R}(1 +1) &\implies B = \frac{\mu_0 I}{2 \pi R}
\end{align}$$

