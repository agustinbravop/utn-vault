Un sistema es **estable** si responde en forma limitada a una excitación limitada. Se analizan los polos de la [[Función de Transferencia]] $F(s)$, suponiendo que son [[Números Complejos]]:

- Si todos los polos están en la mitad izquierda del plano $s$ (de manera que su parte real es negativa), entonces es un sistema *estable*.
- Si se tiene un polo en el eje imaginario, el sistema es *marginalmente estable*.
- Si se tiene un polo en la mitad derecha, el sistema es *inestable*.

![[Estabilidad.png]]

La **estabilidad** es una propiedad del sistema y no depende de la función de entrada que se le aplique. Un sistema estable, con el tiempo, vuelve a las condiciones iniciales. Un sistema inestable es difícil de controlar. Dado que $F(s)$ caracteriza al sistema, se la puede usar para especificar condiciones de estabilidad.

Una función de transferencia caracteriza al comportamiento del sistema sin proporcionar información sobre su estructura física interna, de manera que dos sistemas físicamente distintos pueden tener la misma función de transferencia.

$F(s)$ nos permite predecir la forma de las señales sin necesidad de resolver la ecuación diferencial que describe al sistema. Además, si no se tiene esa ecuación diferencial, aún se puede obtener su función de transferencia de manera experimental, estimulando al sistema y estudiando su respuesta.
