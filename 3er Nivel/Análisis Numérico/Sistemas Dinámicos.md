Los sistemas dinámicos son modelados por [[Sistemas de Ecuaciones Diferenciales Lineales]] (o no lineales). Debido a la dificultad de obtener sus soluciones explícitas, suele ser más importante estudiar su comportamiento.

De estos sistemas es interesante, para el tiempo tendiendo a infinito, conocer la [[Estabilidad]] de cada [[Punto Crítico]] del sistema.

Sea $X'=\varphi(X)$ con $\varphi=(\varphi_1,\dots,\varphi_n):\Omega \subseteq \Bbb R^n \rightarrow \Bbb R$ un sistema autónomo. Los sistemas autónomos cumplen que si $x(t)$ es una solución, también lo es $x(t+c)$ para cualquier constante $c$.

## Plano de Fase

Sea $\begin{cases}\frac{dx}{dt}=F(x,y) \\ \frac{dy}{dt} = G(x,y)\end{cases}$ un sistema autónomo plano donde cada solución es un par de funciones $x(t)$ e $y(t)$ que definen una _curva_ en el plano $xy$.

En cada punto $(x,y)$ de la curva u órbita, el vector $(F(x,y),G(x,y))$ es un vector tangente a dicha órbita, y el conjunto de esos vectores es el _campo de direcciones_ del sistema.
