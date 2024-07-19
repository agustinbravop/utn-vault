La **recursividad** es una técnica matemática y computacional en la cual la solución se basa en que el [[Algoritmo]] se llama a sí mismo dentro del proceso. Es una forma de repetición distinto a usar [[Estructuras de Código#Iterativas|estructuras iterativas]] mediante bucles.

```
FUNCIÓN factorial(n: entero): entero ES
	SI n = 0 O n = 1 ENTONCES
		factorial := 1
	CONTRARIO
		factorial := n * factorial(n - 1)
	FIN_SI
FIN_FUNCIÓN
```

El **caso base** devuelve sin llamarse a sí mismo, sirve como un **final** de la recursión. El **caso recursivo** es donde la función **se invoca a sí misma** con diferentes parámetros hasta llegar al caso base.

La recursividad supone una **reducción de la complejidad** del problema (donde `f(n - 1)` es menos complejo que `f(n)`) hasta que se llega al caso base, el más simple de todos. Sirve para **simplificar el código** o cuando la estructura de datos es recursiva (por ejemplo un [[Árbol]]), pero es ineficiente para largas repeticiones porque la recursividad es **lenta y cara**.

Las llamadas a la función se van apilando en en *callstack* hasta que se llega al caso base y las funciones comienzan a retornar: el *callstack* comienza a desapilarse.

Tipos de recursividad:

1. **Mutua**: cuando una `f(n)` llama a `g(n)` la cual lama a `f(n)` y etc...
2. **Múltiple**: la función presenta más de una llamada a sí misma.
3. **Anidada**: presenta varias llamadas en la misma línea (por ejemplo la serie de fibonacci).
4. **De cabeza**: se llama a sí misma al inicio del cuerpo (primera instrucción).
4. **De cola**: se llama a sí misma al final del cuerpo (última instrucción).
5. **Intermedia**: se llama a sí misma en el medio del cuerpo.

Para resolver problemas de manera recursiva:

1. Definir el **caso base**.
2. Organizar un **cambio de estado** que nos lleve hacia el caso base.
3. Establecer la **llamada recursiva**.