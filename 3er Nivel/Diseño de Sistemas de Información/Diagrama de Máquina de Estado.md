En la vista de estados de [[UML]], el **diagrama de máquina de estados** está compuesto por *estados* y *transiciones*.

![[Diagrama de Máquina de Estado.png]]

Una transición puede ser externa (dentro del mismo nodo), interna, o de finalización (cuando termina la actividad). Las transiciones tienen:

1. Un estado origen y un estado destino.
2. Un *evento* disparador y una acción/efecto de *entry*/*exit*/*on*.
3. Una condición de guarda.

Los eventos son instantáneos y ocurren en cierto tiempo y espacio. Pueden ser:

1. De **cambio** (una expresión booleana).
2. De **llamada** (una petición sincrónica).
3. De **señal** (una interrupción asíncrona).
4. De **tiempo** (definen un *timeout* o *interval*).

Los estados pueden ser simples o *compuestos*. Un estado compuesto puede ser *ortogonal* (en paralelo a otros estados mutuamente excluyentes) o *no ortogonal*.
