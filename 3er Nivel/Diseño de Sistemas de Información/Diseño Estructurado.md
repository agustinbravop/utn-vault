El **diseño estructurado**, propuesto por Yourdon y Constantine en 1978, es una [[Metodologías de Desarrollo|metodología de desarrollo]] o enfoque anterior a los [[Métodos Orientados a Objetos]]. Si bien ya quedó obsoleto, algunas de sus propuestas siguen siendo relevantes.

El diseño estructurado surge como consecuencia de la programación estructurada, y está orientado a las funciones y datos. Se centra en buscar la mejor solución dentro de las limitaciones dadas.

> El diseño estructurado es el proceso de decidir qué componentes interconectados de qué manera solucionarán un problema bien especificado.

El objetivo es **crear software de mayor calidad a menor costo**, lo cual significa alcanzar la:

1. **Eficiencia**: el uso inteligente de los recursos.
2. **Mantenibilidad**: $\text{mantenibilidad} = \text{confiabilidad} / (\text{confiabilidad} + \text{reparabilidad})$.
3. **Modificabilidad**: capacidad de extender el sistema.
4. **Flexibilidad**: capacidad de tener muchas variaciones del mismo sistema.
5. **Generalidad**: alcance sobre una temática. Es importante para sistemas de propósito general.
6. **Utilidad**: facilidad de uso. Noción temprana de la [[Usabilidad]].

Estos objetivos conforman la **calidad objetiva** de un sistema.

Principios:

1. Abstracción y ocultamiento de la información.
2. Refinamiento sucesivo.
3. Modularidad: factorización en base al principio de "divide y vencerás".
4. Arquitectura del software: diseñar la estructura de datos y la estructura del programa (o jerarquía de control).
5. Procedimientos del software.

## Conceptos

### Cajas negras

Conviene usar módulos con entradas y salidas definidas, "sin mirar adentro".

## Costo

Sea $M(P)$ la medida del tamaño de un problema y $C(P)$ el costo de programar una solución. Sea $Q$ un problema distinto a $P$:

$$
\begin{align}
\text{Si } M(P) \gt M(Q) &\implies C(P) \gt C(Q) \\
&\implies M(P+Q) \gt M(P) + M(Q) \\
&\implies C(P+Q) \gt C(P)+C(Q) \\
&\implies C(P) \gt C\left(\frac{1}{2} P\right) + C\left(\frac{1}{2} P\right)
\end{align}
$$

Se deduce el Teorema Fundamental de la Ingeniería de Software: **es más barato resolver un problema por partes**.

### Regla de Miller

> Las personas mantienen en su cabeza $7 \pm 2$ conceptos a la vez.

![[Regla de Miller.png]]

La regla de Miller nos dice que los errores se reducen al reducir la complejidad del sistema. Subdividir un sistema en módulos reduce su complejidad, lo cual reduce la cantidad de errores, lo cual reduce el costo de programación (de manera asintótica hasta cierto límite). Subdividir demasiado también genera problemas, así que se busca un punto óptimo.

Se busca alta [[Cohesión]] y bajo [[Acoplamiento]].

### Complejidad de las Interfaces

La **complejidad de las interfaces** (las firmas de las funciones) está dada por la cantidad, accesibilidad, y estructura de la información.

## Estructura del Programa

Un _módulo_ es una secuencia de sentencias lexicográficamente continua, limitada por elementos de frontera, con un identificador agregado. Por ejemplo: una función o un método.

Las _conexiones_ a un módulo pueden ser:

- **Normales**: a través de una interfaz definida formalmente. Ej: `call <fn>`.
- **Patológicas**: van directo a un elemento interno del módulo invocado. Esto es muy difícil que suceda en la actualidad, pero era común durante la transición de la programación imperativa no estructurada a la programación estructurada. Ej: `goto <tag>`.

### Morfología

Un _diagrama de estructura_ muestra la **jerarquía de control** del software:

![[Diagrama Estruturado del Diseño Estructurado.png]]

En este tipo de diagramas, se pueden ver los distintos tipos de _flujo de datos_ y _flujo de control_:

1. **Flujo aferente**: la información sube (de sub-módulos hacia super-módulos).
2. **Flujo eferente**: la información baja (de super-módulos hacia sub-módulos).
3. **Transformación**: la información baja al sub-módulo y luego vuelve a subir, transformada.
4. **Coordinación**: la información sube al super-módulo y luego es enviada a otro sub-módulo.

Con el concepto de flujos se pueden identificar _estructuras desbalanceadas_, las cuales pueden ser:

- **Input-driven**: o predominantemente eferentes. Las entradas se leen primero y luego el código decide cómo tratarlas.
- **Output-driven**: o predominantemente aferentes. Se activan los módulos aferentes (bajos) antes de obtener una primera entrada.

Es preferible un **sistema balanceado** o _centrado en la transformación_ porque las ramas aferentes y eferentes están balanceadas. Este tipo de sistemas suelen estar muy factorizados. Se cree que una _morfología centrada en la transformación_ crea sistemas más baratos.

![[Estructuras Desbalanceadas en el Diseño Estructurado.png]]

Los sistemas no triviales tienen un razonamiento detrás de su morfología, dado que un diseñador decidió centrar el sistema en un aspecto que él considera importante. Esta decisión se debe tomar de manera racional (utilizando heurísticas) y no de manera intuitiva.

## Heurísticas de Diseño

Las **heurísticas de diseño** son trucos que nos permiten incrementar la modularidad del sistema:

1. **Tamaño de módulo**: un módulo grande se puede simplificar identificando y extrayendo subfunciones, o descomponiéndolo en funciones.
2. **Fan-out**: la amplitud de control o ancho de salida es el número de subordinados inmediatos de un módulo. Conviene mantenerlo en $7 \pm 2$.
3. **Fan-in**: el ancho de entrada es el número de módulos que invocan a este módulo. Siempre que sea posible, se desea maximizarlo.
4. **Alcance de control**: el módulo mismo y todos sus subordinados.
5. **Alcance de efecto**: todos los módulos cuya invocación está condicionada por un condicional. para un condicional dado, debe ser un subconjunto del alcance de control del módulo.

## Análisis de Transformación

El **análisis de transformación** es una estrategia para derivar diseños estructurados modulares que solo requieren una pequeña reestructuración para ser finales. Es un modelo del flujo de información realizado desde un punto de vista _top-down_.

Pasos;

1. Obtener el _diagrama de flujo de datos_ del problema.
2. Identificar los elementos de datos aferentes y eferentes.
3. Factorización del primer nivel.
4. Factorización de los flujos aferentes, eferentes. y de transformación.
