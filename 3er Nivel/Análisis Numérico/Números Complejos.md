![[index 2025-01-22 15.40.35.excalidraw.svg]]

Los números complejos se describen de forma binomial como:

$$z = a+ bi$$

Con su parte real $\text {Re}(z) = a$ y su parte imaginaria $\text{Im}(z)=b$. Se definen:

1. **Suma**: $z_1 + z_2 = (a_1 + a_2) + (b_1 + b_2)i$.
2. **Multiplicación**: $z_1 \cdot z_2 = (a_1 \cdot a_2 - b_1 \cdot b_2) + (a_1 \cdot b_2 + b_1 \cdot a_2)$.
3. **Conjugado**: si $z=(a;b) \implies \overline z = (a;-b)$.
4. **Módulo**: si $z=a+bi \implies |z| = \sqrt {a^2 + b^2}$.
5. **División**: $\frac{z_1}{z_2} = \frac{a_1+b_1 i}{a_2+b_2i} \frac{a_2-b_2i}{a_2-b_2i} = \frac{(a_1a_2+b_1b_2)+(b_1a_2-a_1b_2)i}{a_2^2+b_2^2}$.
6. **Argumento**: si $z=(a;b) \implies \theta = \arctan \frac{b}{a}$.
7. **Raíces**: $\sqrt[n]{z} = z^{\frac{1}{n}} = |z^{\frac{1}{n}}| \cdot\text{cis}(\frac{\theta+2k\pi}{n})$,  con $o\le k \lt n$.
8. **Potencias**: $z^n = |z|^n \cdot \text{cis}(n\theta)$.

Otras formas de definir un número complejo:

- Forma Trigonométrica: $z = |z| (\cos \theta + i \sin \theta)$.
- Forma Polar: $z = |z|_\theta = (|z|;\theta)$.

Se cumple que:

- $z=|z|\cdot e^{i\theta}$.
- $e^{i\theta}=\cos \theta + i \sin \theta$.
- $\frac{e^{i\theta}-e^{-i\theta}}{2i}=\sin\theta$.
- $\frac{e^{i\theta}-e^{i\theta}}{2}=\cos\theta$.

Identidades trigonométricas útiles:

- $\sin(x+y) = \sin(x)\cos(y) + \cos(x)\sin(y)$.
- $\cos(x+y) = \cos(x)\cos(y) - \sin(x)\sin(y)$.
- $\sin(x-y) = \sin(x)\cos(y) - \cos(x)\sin(y)$.
- $\cos(x-y) = \cos(x)\cos(y) + \sin(x)\sin(y)$.
- $\sin(2x)=2\sin(x)\cos(x)$.
- $\cos(2x)=\cos^2(x)-\sin^2(x)$.
