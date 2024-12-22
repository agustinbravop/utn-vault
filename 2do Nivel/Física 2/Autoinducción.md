Cuando una [[Corriente Eléctrica]] variable pasa a través de una bobina (o solenoide), dentro se produce un [[Flujo Magnético]] variable, el cual genera una [[FEM Inducida]] en esa misma bobina. Esta [[Fuentes de Fuerza Electromotriz|fem]] se opone al cambio en el flujo.

Sea $k$ una constante que depende de la forma y dimensiones del circuito. Aplicando la [[Ley de Faraday y Ley de Lenz]] para hallar la *fem autoinducida*:

$$\frac{d \phi_B}{dt} = k \frac{dI}{dt} \implies \varepsilon = -N \frac{d\phi_B}{dt} = -Nk\frac{dI}{dt} = -L \frac{dI}{dt}$$

Se define el *coeficiente de autoinducción* $L$:

$$L = Nk \ ; \ [\text{Henrio } Hy] = \frac{[\text{Volt V}] [\text{segundos}]}{[\text{Ampere } A]}$$

Donde 1 *Henrio* representa la autoinducción de una bobina en la que la variación de la corriente en 1 Ampere por segundo produce una fem autoinducida de 1 Volt.

$$si N \frac{d\phi_B}{dt} = L \frac{dI}{dt} \implies N\phi_B = LI \implies L \frac{N\phi_B}{I} = \frac{N}{I}BA = \frac{N}{\cancel I}\frac{\mu N \cancel I}{\text{long}} A \implies L = \frac{\mu N^2 A}{\text{long}}$$

Se deduce por $L=\frac{N \phi_B}{I}$ que $L$ depende del número de espiras, del flujo, y de la corriente. La magnitud de $L$ también depende de la geometría y de la presencia de un [[Materiales Magnéticos#Ferromagnetismo|material ferromagnético]].

## Inductancias en Serie

![[Inductancias en Serie.png]]

$$\begin{gather}\Delta V = V_a - V_b = L \frac{dI}{dt} \\ \begin{rcases} I = I_1 = I_2 = I_3 \\ V = V_1 + V_2 + V_3 \end{rcases} \implies L \frac{dI}{dt} = L_1 \frac{dI}{dt} + L_2 \frac{dI}{dt} + L_3 \frac{dI}{dt} \implies L = L_1 + L_2 + L_3  \implies L = \sum_{i=1}^{N}L_i
\end{gather}$$

## Inductancias en Paralelo

![[Inductancias en Paralelo.png]]

$$\begin{cases}
I = I_1 + I_2 + I_3 \\
\frac{dI}{dt} = \frac{dI_1}{dt} + \frac{dI_2}{dt} \frac{dI_3}{dt} \\
\frac{V}{L} = \frac{V}{L_1} + \frac{V}{L_2} + \frac{V}{L_3} \\
\frac{1}{L} = \frac{1}{L_1} + \frac{1}{L_2} + \frac{1}{L_3} \implies \frac{1}{L} = \sum_{i=1}^N \frac{1}{L_i}
\end{cases}$$
