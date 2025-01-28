En la vista de estados de [[UML]], el **diagrama de máquina de estados** está compuesto por _estados_ y _transiciones_.

![[Diagrama de Máquina de Estado.png]]

Una transición puede ser externa (dentro del mismo nodo), interna, o de finalización (cuando termina la actividad). Las transiciones tienen:

1. Un estado origen y un estado destino.
2. Un _evento_ disparador y una acción/efecto de _entry_/_exit_/_on_.
3. Una condición de guarda.

Los eventos son instantáneos y ocurren en cierto tiempo y espacio. Pueden ser:

1. De **cambio** (una expresión booleana).
2. De **llamada** (una petición sincrónica).
3. De **señal** (una interrupción asíncrona).
4. De **tiempo** (definen un _timeout_ o _interval_).

Los estados pueden ser simples o _compuestos_. Un estado compuesto puede ser _ortogonal_ (en paralelo a otros estados mutuamente excluyentes) o _no ortogonal_.
