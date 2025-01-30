A lo largo de una [[Simulación]] de un sistema discreto, las variables de estado cambian sólo en instantes discretos de tiempo.

## Organización Temporal del Proceso

Conforme avanza el tiempo de la simulación, ocurren *eventos* que provocan un **cambio de estado** en el sistema. La historia secuencial de estados de un modelo se puede realizar al determinar la aparición de eventos a lo largo del tiempo.

Avance del tiempo:

- **Evento a evento**: se avanza la simulación hasta encontrar el siguiente evento. [[Simulación con Metodología Evento a Evento]].
- **Intervalos constantes**: los eventos se consideran cada cierto *delta de tiempo*, y deben ser desplazados a "ocurrir" o ser tratados en ese momento. A menor delta de tiempo, más preciso es el tiempo de ocurrencia del evento, pero más lenta la simulación. [[Simulación con Avance del Tiempo Constante]].

Para cada simulación dada, se elige la metodología más conveniente.

## Elección de los Estados Inicial y Final

La simulación de un sistema discreto solo estudia un lapso de tiempo determinado de la operación del [[Modelo]]. Dependiendo del objetivo, restricciones, comportamiento, etc, se debe establecer un *estado inicial* de arranque de la simulación y un *estado final* en el cual se pueda terminar.

Definir el estado inicial es definir los valores iniciales de las variables del modelo.

Existe un *período transitorio* mientras el sistema pasa del estado inicial a un estado operativo estable.

## Determinación de la Cantidad de réplicas

A mayor cantidad de réplicas (corridas de la simulación), se logra reducir el delta del [[Intervalo de Confianza]] de los resultados de la simulación, aunque con rendimientos decrecientes. 

Con que el intervalo de confianza sea lo suficientemente pequeño para poder tomar una decisión, sin reducir el nivel de aceptación $(1-\alpha)$, se considera que es una cantidad de réplicas suficiente.

Como resultado de una simulación con $n$ réplicas se tiene una cantidad $n$ de valores $x_i$ de una variable $x$. Para sacar conclusiones, hay que verificar si ese conjunto sigue una [[Distribución Normal]] y si son independientes entre sí.
