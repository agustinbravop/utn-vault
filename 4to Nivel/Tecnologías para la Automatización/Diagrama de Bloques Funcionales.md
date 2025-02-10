Un **diagrama de bloques funcionales** sirve para modelar un [[Sistema de Control]]. El componente básico es un *bloque funcional*, donde $G(s) = \frac{Y(s)}{X(s)}$:

![[Bloque Funcional.png]]

Un *comparador*, o punto suma, suma algebraicamente las señales, tal que $Z(s)=X(s)-Y(s)$:

![[Comparador.png]]

Otros elementos:

- **Punto de separación**: bifurca una señal y la reproduce por igual para ambas ramas.
- **Trayectoria directa**: serie de elementos mediante los cuales la señal fluye de entrada a salida.
- **Trayectoria de realimentación**: trayecto desde la salida controlada al punto suma de la entrada.
- **Trayectoria de pre-alimentación**: los elementos a la izquierda del punto suma.
- **Señal de entrada**: señal externa aplicada al SC para generar una acción deseada.

En la [[Ingeniería de Control]], "simplificar" un sistema es aplicar [[Álgebra de Bloques]] para pasar de un sistema complejo a uno simple.
