En la [[Conmutación de Paquetes]], existen varias **estrategias** para el **encaminamiento**: la manera de decidir la mejor ruta.

## Estático

Se elige una ruta fija para cada par de nodos fuente-destino en la red, y solo se cambia cuando cambia la *topología* de la red. Tiene una *matriz* de encaminamiento central en un centro de control. Luego, cada nodo almacena una *tabla* de encaminamiento, que, dado un nodo destino al que debe llegar el paquete, indica el nodo siguiente al que enviar el paquete.
