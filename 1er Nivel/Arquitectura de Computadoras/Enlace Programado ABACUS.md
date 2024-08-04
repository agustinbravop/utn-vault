Dentro de los [[Canales]], el enlace programado es más bien un **medio de acceso** controlado por el **programa en curso** (es decir que la responsabilidad cae en el programador). Usa el **modo bloqueado** y el **modo interrupción de programa** de la [[Simultaneidad de los Procesos IO]].

Transfiere solo una palabra y hace prueba de estado. Aprovecha cuatro instrucciones:

1. `PRE`: prueba de estado.
2. `GBP`: gobierno de periférico.
3. `ENT`: entrada.
4. `SAL`: salida.

![[Enlace Programado ABACUS.png]]

Una instrucción de salida de informacón tendría el siguiente intercambio de señales (gracias a la [[Interfaz del Canal]]):

![[Intercambio de Salida para el Enlace Programado.png]]
