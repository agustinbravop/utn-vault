La representación como **espacio de estados** forma la base de muchos métodos de [[Inteligencia Artificial]]. Su estructura se corresponde con la estructura de la resolución de un problema por dos razones:

1. Permite definir formalmente el problema.
2. Permite definir el proceso de resolución del problema.

La descripción formal de un problema especifica:

1. Un espacio de estados.
2. Estados iniciales (situaciones en las que comienza la resolución del problema).
3. Estados objetivos.
4. Operadores (reglas que describen acciones).

Para utilizar búsqueda, el problema debe poder resolverse usando reglas en combinación con una **estrategia de control** para trasladarse en el espacio del problema desde el estado inicial hasta el estado objetivo. Requisitos de una buena estrategia de control:

- Causar algún cambio de estado (sino, nunca alcanzaría la solución).
- Ser sistemática, por una necesidad de cambio local y global.

## Métodos Sistemáticos de Búsqueda

Estos métodos exploran exhaustivamente el espacio de estados para encontrar una solución. Si el camino de solución existe, estos métodos lo van a encontrar.

### Primero en Amplitud

Este algoritmo encuentra la solución mínima (óptima).

```text
Algoritmo
	Crear una variable ListaNodos y asignarle el estado inicial.
	Hasta que ListaNodos esté vacía o encontrar un estado, hacer:
		Eliminar el primer item de ListaNodos y llamarlo E.
		Si ListaNodos está vacía, terminar.
		Para que cada regla se empareje con el estado en E, hacer:
			Aplicar la regla para generar un nuevo estado.
			Si el nuevo estado es un estado objetivo, devolver ese estado.
			Caso contrario, añadir el nuevo estado al final de ListaNodos.
```

### Primero en Profundidad

Con un poco de suerte este algoritmo puede evitar examinar gran parte del espacio.

```text
Algoritmo
	Si el estado inicial es un estado objetivo, terminar con éxito.
	Caso contrario, hacer:
		Generar un sucesor E del estado inicial. Si no hay, marcar fracaso.
		Llamar a la búsqueda con E como estado inicial.
		Si devuelve un éxito, marcar éxito. Caso contrario, continuar el ciclo.
```

Estos métodos pueden ser más eficientes si se usan heurísticas.

## Métodos de Búsqueda Heurística

La **heurística** aumenta la eficiencia de una búsqueda, aunque agrega complejidad al algoritmo. Existen heurística de propósito general y heurísticas de dominio específico.

Hay soluciones:

- **Absolutas**: cuando el estado objetivo es único.
- **Relativas**: cuando hay varios estados objetivos. Cuidado con la localidad y con quedar atrapado en un máximo o mínimo local y no lograr la solución óptima.

### Escalada Simple

Este algoritmo consiste en usar una **función de evaluación** que **introduce [[5to Nivel/Inteligencia Artificial/Conocimiento|Conocimiento]]** en el proceso de control para hacer **estimaciones**. Es muy simple: aplica operadores al estado actual hasta encontrar un nuevo estado que sea mejor, y luego repite el proceso tomando ese nuevo estado como estado actual.

```
Algoritmo
	Evaluar el estado inicial.
		Si es el estado objetivo, devolverlo.
		Caso contrario, hacerlo el estado actual.
	Repetir hasta encontrar una solución o que no queden operadores
		por aplicar al estado actual:
		Seleccionar un nuevo operador y aplicarlo al estado actual
			para generar un nuevo estado.
		Evaluar el nuevo estado:                       # Función de evaluación
			Si es un estado objetivo, devolverlo.
			Si es mejor que el actual, convertirlo en el actual.
			Si no es mejor que el actual, continuar con el bucle.
```

Este algoritmo puede quedar atrapado en máximos/mínimos locales, por lo que no siempre logra la solución óptima.

### Escalada por Máxima Pendiente

Este algoritmo primero genera todos los sucesores del estado actual y luego elige el mejor (el más prometedor). Esto evita continuar por un estado que sea mejor al estado actual pero que no sea el mejor sucesor.

```text
Algoritmo
	Evaluar el estado inicial.
		Si es el objetivo, devolverlo.
		Caso contrario, continuar con el inicial como actual.
	Repetir hasta encontrar una solución o hasta que una iteración completa
		no produzca un cambio en el estado actual:
		Sea SUCC un estado peor que algún posible sucesor del actual.
		Por cada operador aplicado al actual hacer:
			Aplicar el operador y generar un nuevo estado.
			Evaluar el nuevo estado:
				Si es objetivo, devolverlo.
				Sino, compararlo con SUCC:
					Si es mejor que SUCC, asignarlo a SUCC.
			Si SUCC es mejor que el estado actual, hacerlo el estado actual.
```

### Primero el Mejor

Este algoritmo vuelve a nodos anteriores si son más prometedores que los sucesores actuales. Es un balance entre la búsqueda primero en amplitud y la búsqueda primero en profundidad.

```text
Algoritmo
	Comenzar con ABIERTOS conteniendo solo el estado inicial.
	Hasta llegar a un objetivo o que no queden nodos en ABIERTOS hacer:
		Tomar el mejor nodo de ABIERTOS.
		Generar sus sucesores.
		Para cada sucesor hacer:
			Si no se generó antes:
				Evaluarlo, añadirlo a ABIERTOS y almacenar a su padre.
			Si ya se generó antes:
				Si el nuevo camino es mejor, cambiar al padre. En este caso
					se actualiza el costo de alcanzar al nodo y sus sucesores.
```

### A\*

El algoritmo A\* adapta la búsqueda primero el mejor para poder usarse en grafos. Este algoritmo mantiene una lista CERRADOS de nodos explorados y con sucesores generados. Si un sucesor ya se encontraba en CERRADOS pero se encontró un mejor camino, se debe propagar esa mejora al nodo viejo, lo cual es delicado de implementar. Su implementación es más sofisticada.

En estos métodos se define una **función heurística** $f'=g+h'$ que hace una estimación del mérito de cada nodo. Esta función $f'$ se trata de una aproximación a la función $f$ que es la que tendría la verdadera evaluación de cada nodo. La función $g$ es una medida del costo de ir desde el estado inicial hasta el actual, y por ende se lo conoce exactamente. La función $h'$ es una estimación del costo de alcanzar el estado objetivo a partir del estado actual, y se considera una aproximación a $h$.

- Si $g=0 \implies$ se elige siempre el nodo más prometedor.
- Si $h'=0 \implies$ $g$ controla la búsqueda.
- Si $h'=0 \land g=\text{cte}\implies$ la búsqueda es igual a primero en amplitud.

#### Criterio de Admisibilidad de A\*

> El criterio de admisibilidad dice que A\* encuentra la mejor solución si $h'$ no sobrestima a $h$.

Supongamos un camino óptimo con valor $V_\text{opt}$ y que el nodo $n_j$ forma parte del camino no óptimo porque $h'(n_j)$ sobrestima $h(n_j)$:

$$f'(n_j) = g(n_j) + h'(n_j)\gt V_\text{opt}$$

Supongamos otro nodo $n_i$ que sí forma parte del camino óptimo. Si $h'(n_i)$ no sobrestima a $h(n_i)$:

$$f'(n_i) = g(n_i) + h'(n_i) \le V_\text{opt}$$

Por lo cual:

$$f'(n_i)\le V_\text{opt} \lt f'(n_j)$$
