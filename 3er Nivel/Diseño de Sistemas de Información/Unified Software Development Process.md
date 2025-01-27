El [[Proceso Unificado de Desarrollo de Software]] (PUDS), o simplemente Unified Process (UP), fue propuesto por Jacobson-Booch-Rumbaugh en 1999.

- Es un proceso ([[Metodologías de Desarrollo]]),
- Con un maro genérico, adaptable, y extendible,
- Basado en *componentes* reutilizables,
- Que usa [[UML]] sin estar acoplado a él.

Tiene 3 **aspectos** fundamentales:

1. **Dirigido por casos de uso**: los CU guían el análisis, diseño, implementación, y prueba.
2. **Centrado en la arquitectura**: la cual es el conjunto de decisiones significativas acerca de la organización del sistema.
3. **Iterativo e incremental**: cada iteración resulta en un incremento.

Un proceso iterativo e incremental reduce riesgos atacando los riesgos más importantes primero. Muestra resultados a corto plazo y es más realista. Aún así, el UP es bastante tradicional: si no fuera iterativo e incremental, sería muy similar al modelo en cascada.

## Ciclo de Vida

La vida del sistema se divide en *ciclos*. Al final de cada ciclo, se hace una *product release* en la que entrega una nueva versión del sistema.

Cada ciclo se compone de 4 *fases* que terminan en un *hito* (o *milestone*) al pasar a la siguiente:

1. **Concepción**: define el producto, negocio, objetivos, riesgos, viabilidad. Hito: objetivos y ciclo de vida. Artefactos: casos de uso principales, boceto de la arquitectura, y plan de iteraciones.
2. **Elaboración**: comprender el problema y eliminar riesgos. Hito: arquitectura del ciclo de vida. Artefactos: línea base de la arquitectura, 80% de los casos de uso, plan detallado de iteraciones.
3. **Construcción**: desarrollar el producto. Hito: capacidad operativa inicial (versión beta). Artefactos: software, manual de usuario.
4. **Transición**: puesta en producción de la versión beta y correcciones. Hito: lanzamiento del producto. Artefactos: los mismos que en la fase de construcción.

Cada fase se subdivide en *iteraciones*, controladas con selección y planificación. Cada iteración tiene sus flujos de trabajo principales, y termina en un *incremento* o release interna.

Un *flujo de trabajo* es una secuencia de actividades que produce artefactos. Un *artefacto* es una pieza de información producida. Los [[Flujos de Trabajo de UP]] son:

1. Requerimientos.
2. Análisis.
3. Diseño.
4. Implementación.
5. Testing.

![[Unified Software Development Process.png]]

Se puede ver cómo todos los flujos de trabajo están en todas las fases, pero con distintos niveles de protagonismo dependiendo de la fase.

Se dice que UP es *bidimensional* (contenido y fases), mientras que el modelo en cascada, al no tener fases, tiene solo una dimensión: el contenido.
