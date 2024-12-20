**Ley de las Corrientes**: la suma algebraica de las intensidades de corriente en cualquier unión o nodo de un circuito es igual a cero. Las corrientes entrantes son positivas y las salientes son negativas. Esto es análogo a la ley de conservación de las cargas.

**Ley de las Mallas**: la suma algebraica de las diferencias de potencial que se encuentran al recorrer cualquier malla es igual a cero. Esto es análogo al principio de conservación de la energía.

Las dos **Leyes de Kirchhoff** sirven para obtener la [[Corriente Eléctrica]] de un circuito. Dado un circuito, primero se le debe asignar un *sentido* arbitrario para la corriente, y establecer un sentido horario o antihorario para recorrer las mallas del circuito. Se debe respetar que:

- Si al recorrer el circuito atravesamos una [[Fuentes de Fuerza Electromotriz|fem]], se la considera positiva si lo hacemos de menor a mayor [[Potencial Eléctrico]] (de $-$ a $+$).
- Si al atravesar una [[Resistencia Eléctrica]] lo hacemos en el sentido de la corriente, la caída del potencial es negativa (se resta).

## Circuitos RC

![[Leyes de Kirchhoff en un Circuito RC.png]]

### Carga de un Capacitor

Al inicio de la carga de un [[Capacitor]], en $t = 0$ y con la llave $S$ abierta, el capacitor está descargado de manera que $Q(t =0)=0$. Cuando $S$ se cierra se establece una corriente $I$, por lo que $\Delta V$ en el capacitor $C$ aumenta hasta que $\Delta V = \varepsilon$.


$$
\begin{align}
\varepsilon = IR + \frac{Q}{C} \ \land \ I = \frac{dQ}{dt} &\implies \\
\varepsilon = R\frac{dQ}{dt} + \frac{Q}{C} &\implies  \\ 
\frac{dQ}{C\varepsilon - Q} = \frac{dt}{RC} &\implies \\
\int_0^Q \frac{dQ}{C\varepsilon - Q} = \frac{1}{RC} \int_0^tdt &\implies \\
- \ln(C\varepsilon - Q) + \ln (C\varepsilon) = \frac{t}{RC} &\implies \\
\ln (1 - \frac{Q}{C\varepsilon}) = -\frac{t}{RC} &\implies \\
1-\frac{Q}{C\varepsilon} = e^{-\frac{t}{RC}} &\implies \\
Q = C \varepsilon (1-e^{-\frac{t}{RC}}) &\implies V_c = \varepsilon (1 - e ^{-\frac{t}{RC}})
\end{align}
$$

De donde se deduce que $Q_{max} = C\varepsilon$ y $V_{c_{max}} = \varepsilon$. Se define una *constante de tiempo* $\tau = RC$ que representa el tiempo requerido para que el capacitor llegue al 63% de su carga y su $V_{c_{max}}$.

### Descarga de un Capacitor

Cuando la llave $S$ se cierra, y no hay una *fem* presente, se establece una corriente $I$ que empieza a descargar al capacitor $C$. La resistencia $R$ va disipando energía eléctrica hasta que $I = 0$.

$$
\begin{align}
IR = \frac{Q}{C} \ \land \ I = - \frac{dQ}{dt} &\implies \\
-\frac{dQ}{dt}R = \frac{Q}{C} &\implies \\
\frac{dQ}{Q} = -\frac{dt}{RC} &\implies \\
\int_{Q_0}^Q \frac{dQ}{Q} = \int_0^t \frac{dt}{RC} &\implies \\
\ln \frac{Q}{Q_0} = \frac{t}{RC}  &\implies \\
Q = Q_0 e^{-\frac{t}{RC}} &\implies V_c = V_0 e ^{-\frac{t}{RC}}
\end{align}
$$

Recordando que $C= cte$, se puede considerar $V_0 = \frac{Q_0}{C}$. También se utiliza una *constante de tiempo* $\tau = RC$ que indica cuándo la carga en el capacitor, el voltaje a través de él, y la corriente de la resistencia, disminuyen al 37% de su valor original.
