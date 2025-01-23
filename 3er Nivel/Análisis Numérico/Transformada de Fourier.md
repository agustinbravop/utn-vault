La **transformada de Fourier** permite pasar una señal en el dominio del tiempo al dominio de la frecuencia y viceversa (es *reversible*), para así obtener información que no es evidente en el dominio temporal. Aprovechan el concepto de la [[Serie de Fourier]].

$$\mathcal{F}(f(t)) = F(\omega) = \int_{-\infty}^\infty f(t) \cdot e^{-j\omega t} dt$$

Esto es útil para las comunicaciones, la detección de compuestos, y el tratamiento digital de imágenes. También sirve para resolver ecuaciones diferenciales, por lo que se usa en el diseño de controladores clásicos de sistemas realimentados.

Ejemplo para $f(t) \begin{cases}e^{-t} & t\gt 0 \\ 0 & t\lt 0\end{cases}$:

$$F(\omega) = \int_{-\infty}^\infty e^{-t}e^{-j\omega t}dt = \int_{0}^\infty e^{-(1+j\omega)t}dt = -\frac{1}{1+j\omega} \left[e^{-(1+j\omega)t}\right]_0^\infty = \frac{1}{1+jw}$$
