El **secuenciador central** en la [[Arquitectura ABACUS]] es el órgano que **genera las** [[Señales de Gobierno]] desde la [[Unidad de Control]] en base al **registro de instrucción** $I$ y el **estado de la máquina**. El estado de la máquina es un conjunto de 4 indicadores o [[Biestables]]:

1. **D/M**: **detención** o marcha de la máquina.
2. **I**: un flip-flop RS que indica si actualmente estamos en un **ciclo instrucción**. Se le asocian dos micro-órdenes $RI$ (reset de $I$) y $SI$ (set de $I$). 
3. **O**: otro flip-flop RS que indica si actualmente estamos en un **ciclo operando**. Se le asocian dos micro-órdenes $RO$ (reset de $O$) y $SO$ (set de $O$).
4. **S**: el **bit de signo** del registro AC.

![[Entorno del Secuenciador.png]]

A cada operación se le asocia un código ([[Codificación de las Instrucciones]]), el cual va en el campo $CO$ del registro $I$, registro que luego se decodifica para activar el circuito correspondiente del secuenciador.

![[Decodificación de la Instrucción.png]]

El objetivo es generar todas las micro-órdenes necesarias para ejecutar una instrucción, distanciadas en el tiempo por retardos apropiados. Esta sincronización se facilita al usar un **distribuidor de fases** que da señales temporales **regularmente espaciadas** y provenientes de un mismo **reloj**.

![[Distribuidor de Fases.png]]

Esas señales temporales regularmente espaciadas generan un [[Cronograma en ABACUS]] **de base** para la arquitectura. En particular, ABACUS tiene un distribuidor de dos fases, lo que genera un cronograma con $\theta_0$, $\Theta_0$, $\theta_1$ y $\Theta_1$ . $\theta$ indica que es impulsional, y $\Theta$ indica que es de nivel.

![[Cronograma del Distribuidor de Fases.png]]

## Expresiones Lógicas

Tomando cada micro-orden que aparece en cada cronograma, se deducen todos los casos (instantes de tiempo en el cronograma de dos fases de ABACUS) en los que debe estar activada, y se los junta en una **expresión lógica** que toma como variables binarias de entrada el estado de la máquina.
$$ 
\begin{aligned} 
ENS &= \theta_0 \\
ICM &= \theta_0 \\
PACM &= \theta_0 \\
LEC &= I + O + \overline{alm} + (\overline{O} \cdot \overline{I}) \\
ESC &= O \cdot alm \\
SRM &= \Theta_0 \cdot I + O \cdot \overline{alm} + IND \cdot \Theta_1 \cdot \overline{I} \cdot \overline{O} \\
TMS &= IND \cdot \Theta_1 \cdot \overline{I} \cdot \overline{O} \\
ENI &= \theta_1 \cdot I \\
SRD &= \Theta_1 \cdot I \cdot (sum + sus + and + or + alm + sal + sap \cdot AP) \\
SRP &= \Theta_1 \cdot I \cdot (pac + sap \cdot AN) + \Theta_1 \cdot O \\
INCP &= \theta_1 \cdot I \\
ENP &= \theta_0 \cdot (saal + sap \cdot AP) \\
SUM &= sum \cdot O \\
SUS &= sus \cdot O \\
AND &= and \cdot O \\
OR &= or \cdot O \\
ENA &= O \cdot \overline{alm} \\
EAC &= O \cdot \theta_0 \cdot \overline{alm} \\
PAC &= pac \cdot \theta_0 \\
SAC &= \Theta_0 \cdot O \cdot alm \\
EM &= \theta_1 \cdot O \cdot alm \\
SI &= \theta_0 \cdot O \\
RI &= \theta_0 \cdot I \cdot (sum + sus + or + and + alm) \\
SO &= \overline{IND} \cdot \theta_0 \cdot I \cdot (sum + sus + and + or + alm) + IND \cdot \theta_0 \cdot \overline{I} \cdot \overline{O} \\
RO &= \theta_0 \cdot O \\
\end{aligned}
$$

## Secuenciamiento de Operadores Aritméticos

Los [[Operadores Aritméticos de ABACUS]] de tipo secuencial necesitan un secuenciamiento que implemente el algoritmo de la operación. Necesitan principalmente los batidos del reloj central.

Ejemplo para la multiplicación en serie:

![[Secuenciador para la Multiplicación.png]]
