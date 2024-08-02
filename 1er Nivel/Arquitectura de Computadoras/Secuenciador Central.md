El **secuenciador central** en la [[Arquitectura ABACUS]] es el órgano que **genera las** [[Señales de Gobierno]] desde la [[Unidad de Control]] en base al **registro de instrucción** $I$ y el **estado de la máquina**. El estado de la máquina es un conjunto de 4 indicadores o [[Biestables]]:

1. **D/M**: **detención** o marcha de la máquina.
2. **I**: un flip-flop RS que indica si actualmente estamos en un **ciclo instrucción**.
3. **O**: otro flip-flop RS que indica si actualmente estamos en un **ciclo operando**.
4. **S**: el **bit de signo** del registro AC.

![[Entorno del Secuenciador.png]]

A cada operación se le asocia un código ([[Codificación de las Instrucciones]]), el cual va en el campo $CO$ del registro $I$, registro que luego se decodifica para activar el circuito correspondiente del secuenciador.

![[Decodificación de la Instrucción.png]]

El objetivo es generar todas las micro-órdenes necesarias para ejecutar una instrucción, distanciadas en el tiempo por retardos apropiados. Esta sincronización se facilita al usar un **distribuidor de fases** que da señales temporales **regularmente espaciadas** y provenientes de un mismo **reloj**.

![[Distribuidor de Fases.png]]

Esas señales temporales regularmente espaciadas generan un **cronograma de base** para la arquitectura.

![[Cronograma del Distribuidor de Fases.png]]
