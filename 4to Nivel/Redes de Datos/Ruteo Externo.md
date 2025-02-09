En las [[Redes de Datos]], hay inconvenientes que el paradigma de ruteo interno (como el [[Ruteo IP]]) no puede resolver cuando la escala es global.

El internet original (ARPANET) tenía [[Enrutadores]] núcleo y no núcleo. El problema es que las rutas por defecto no existían, lo que produce un loop infinito de ruteo por enviar paquetes a una ruta desconocida por los routers.

![[Ruteo Externo ARPANET.png]]

¿Y si tenemos varios backbones? Seguimos con el problema de la ruta por defecto.

![[Ruteo Externo con Varios Backbones.png]]

Luego aparece el problema de las redes ocultas. En el siguiente ejemplo, ¿Cómo hacer que los paquetes lleguen a la red 4?

![[Redes Ocultas en el Ruteo Externo.png]]

La solución es pasar de un núcleo hacia un [[Autonomous Systems|AS]] (*Autonomous System*, Sistema Autónomo). [[BGPv4]] es una solución para el ruteo externo.
