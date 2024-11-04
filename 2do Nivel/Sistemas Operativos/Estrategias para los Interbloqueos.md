Existen varias estrategias para tratar los [[Interbloqueos]].

## Ignorar

Se utiliza cuando la probabilidad de que ocurra un deadlock es baja. Esta es la estrategia que Linux implementa.

## Prevenir

Impone restricciones a los procesos limitando el uso de los recursos. Basta con asegurar que una de las cuatro condiciones necesarias no ocurra nunca. Se puede imponer un orden lineal de ejecución para imposibilitar la espera circular, o expropiar los recursos de un proceso, o que liberen sus recursos antes de solicitar más.

## Detectar

Cada cierto tiempo se ejecuta un algoritmo para detectar la existencia o no de un estado de deadlock. Se permiten las tres primeras condiciones necesarias y se detecta la espera circular. Si la hay, entonces se inicia un procedimiento de recuperación. El [[Sistema Operativo]] puede terminar todos los procesos, terminar hasta que no haya deadlock, expropiar un proceso, etc.

## Evitar

No se asignan recursos si hay posibilidad de deadlock. Para esto, es necesario conocer el estado del sistema (asignación actual de recursos).

El **algoritmo del banquero** permite evitar los interbloqueos. Cuando un proceso entra al sistema declara sus necesidades máximas para cada tipo de recurso. Requiere una matriz de solicitudes, asignaciones, y necesidades de recursos.
