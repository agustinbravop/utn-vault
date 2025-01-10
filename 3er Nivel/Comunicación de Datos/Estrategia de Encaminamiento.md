En la [[Conmutación de Paquetes]], existen varias **estrategias** para el **encaminamiento**: la manera de decidir la mejor ruta para hacer llegar un paquete al nodo destino.

## Estático

![[Estrategia de Encaminamiento Estático.png]]

Se elige una ruta fija para cada par de nodos fuente-destino en la red, y solo se cambia cuando cambia la _topología_ de la red. Tiene una _matriz_ de encaminamiento central en un centro de control. Luego, cada nodo almacena una _tabla_ de encaminamiento, que, dado un nodo destino al que debe llegar el paquete, indica el nodo siguiente al que enviar el paquete.

## Inundaciones

![[Estrategia de Encaminamiento por Inundaciones.png]]

Un nodo envía un paquete a todos sus nodos vecinos, excepto por la línea por la que llegó el paquete. Este modo necesita una manera de cesar las retransmisiones.

## Aleatorio

Se eligen líneas de manera alternada. Se busca alcanzar la robustez de las inundaciones pero con un costo menor en los recursos de la red.

## Adaptable

Las decisiones de encaminamiento cambian a medida que las condiciones de la red cambian.

El encaminamiento adaptable reacciona a los fallos y a la congestión de la red, pero requiere que los nodos intercambien información acerca del estado de la red. A mayor información, mejor la decisión de encaminamiento, pero también aumentan los recursos de la red gastados en el control.

Esta estrategia es compleja pero es la más utilizada debido a su [[Control de Congestión]].
