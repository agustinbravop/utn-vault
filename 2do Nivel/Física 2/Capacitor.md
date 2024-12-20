Un **condensador** o **capacitor** es un dispositivo que proporciona un **almacenamiento temporal** de [[Energía Potencial Eléctrica]] y de [[Carga Eléctrica]] para ser utilizada en circuitos.

![[Capacitor.png]]

Un condensador puede ser cargado conectando sus placas a los terminales de una batería.

## Capacidad Eléctrica

La **capacidad eléctrica** es la propiedad que caracteriza las posibilidades de almacenamiento de carga de un capacitor. Por convenio siempre es positiva. Se mide en Faradios $F$, aunque como suele tener valores muy grandes es conveniente usar microfaradios:

$$C = \frac{Q}{\Delta V} \ ; \ \frac{[\text{Coulomb } C]}{[\text{Volt } V]} = [\text{Faradio } F]$$

![[Capacidad Eléctrica de Dos Placas.png]]

La capacidad $C$ de un capacitor de placas plano-paralelas se calcula de la siguiente manera:

$$E = \frac{|\sigma|}{\varepsilon_0} = \frac{Q}{\varepsilon_0 A} \ \land \ \Delta V = E d = \frac{Q d}{\varepsilon_0 A} \implies C = \frac{Q}{\Delta V} = \frac{\cancel{Q}}{\frac{\cancel{Q} d}{\varepsilon_0 A}} = \frac{\varepsilon_0 A}{d}$$

Se deduce que la capacidad aumenta al aumentar el área o al disminuir la distancia.

## Clasificación

![[Capacitores en Serie y en Paralelo.png]]

- **Condensadores en Serie**: usan la misma corriente. $V = V_1 + V_2$.
- **Condensadores en Paralelo**: la corriente se divide. $V = V_1 = V_2$.

La **capacidad equivalente** de un conjunto de condensadores conectados entre sí es la capacidad de un único condensador que cuando sustituye al conjunto produce el mismo efecto exterior.

### En Serie

![[Capacitores en Serie.png]]

Se tiene $\Delta V = \Delta V_1 + \Delta V_2 \ ; \ Q = Q_1 = Q_2$. Entonces:

$$C_{eq} = \frac{Q}{\Delta V} \implies \Delta V = \frac{Q}{C_{eq}} \implies \frac{Q}{C_{eq}} = \frac{Q}{C_1} = \frac{Q}{C_2} \implies \frac{1}{C_{eq}} = \frac{1}{C_1} + \frac{1}{C_2} \implies C_{eq} = \frac{C_1 C_2}{C_1 + C_2}$$

Para $n$ condensadores en serie: $\frac{1}{C_{eq}} = \frac{1}{C_1} + \frac{1}{C_2} + \dots + \frac{1}{C_n} = \sum_{i = 1}^n \frac{1}{C_i}$.

### En Paralelo

![[Capacitores en Paralelo.png]]

$\Delta V = \Delta V_1 = \Delta V_2 \ ; \ Q = Q_1 + Q_2$. Entonces: $C_{eq} = \frac{Q}{\Delta V} \implies C_{eq} = C_1 + C_2 \ ; \ C_{eq} = \sum_{n=1}^n C_i$.

Para resolver un problema de circuitos, conviene ir de atrás hacia la fuente, simplificando primero los condensadores en paralelos y luego los condensadores en serie.

![[Capacitor Equivalente.png]]

## Energía Eléctrica

Un capacitor cargado almacena **energía eléctrica**. La energía almacenada es igual al trabajo para cargarlo. El trabajo necesario para añadir una cantidad de carga $dq$ es $dW = V dq$. La energía almacenada en un capacitor es $U$, para calcularla:

$$dW = Vdq \ \land \ V = \frac{q}{C} \implies W = \int_0^Q V \ dq = \frac{1}{C} \int_0^Q q \ dq \implies U = \frac{1}{2} \frac{Q^2}{C} = \frac{1}{2} C V^2 = \frac{1}{2} Q V$$

La **potencia** $P$ se define como $P = \frac{U}{t} \ ; \ [\text{Watt } W] = \frac{[\text{Joule } J]}{[seg]}$.

Dado un condensador de placas planas paralelas, con placas de área $A$ con una distancia $d$ entre ellas, se halla la densidad de energía $\mu$ de su campo eléctrico $E$:

$$
\begin{gather}
C = \frac{\varepsilon_0 A}{d} \ \land \ V = E \times d \implies U = \frac{1}{2}CV^2 = \frac{1}{2} \frac{\varepsilon_0 A}{\cancel{d}} E^2 d^\cancel{2} = \frac{1}{2} \varepsilon_0 E^2 A d \\
\mu = \frac{U}{\text{Vol}_\text{entre placas}} = \frac{1}{2} \varepsilon_0 E^2
\end{gather}$$

Se deduce que la energía eléctrica $U$ almacenada por unidad de volumen es proporcional al cuadrado del campo eléctrico $E$ en la región.
