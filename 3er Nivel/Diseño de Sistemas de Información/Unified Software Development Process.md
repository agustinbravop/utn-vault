El [[Proceso Unificado de Desarrollo de Software]] (PUDS), o simplemente Unified Process (UP), fue propuesto por Jacobson-Booch-Rumbaugh en 1999.

- Es un framework de procesos ([[Metodologías de Desarrollo]]),
- Con un marco genérico, adaptable, y extendible,
- Basado en _componentes_ reutilizables,
- Que usa [[UML]] sin estar acoplado a él.

Tiene 3 **aspectos** fundamentales:

1. **Dirigido por casos de uso**: los CU guían el análisis, diseño, implementación, y prueba.
2. **Centrado en la arquitectura**: la cual es el conjunto de decisiones significativas acerca de la organización del sistema.
3. **Iterativo e incremental**: cada iteración resulta en un incremento.

Un proceso iterativo e incremental reduce riesgos atacando los riesgos más importantes primero. Muestra resultados a corto plazo y es más realista. Aún así, el UP es bastante tradicional: si no fuera iterativo e incremental, sería muy similar al modelo en cascada.

![[Modelos del UP.png]]

## Ciclo de Vida

La vida del sistema se divide en _ciclos_. Al final de cada ciclo, se hace una _product release_ en la que entrega una nueva versión del sistema.

Cada ciclo se compone de 4 _fases_ que terminan en un _hito_ (o _milestone_) al pasar a la siguiente:

1. **Concepción**: define el producto, negocio, objetivos, riesgos, viabilidad. Hito: objetivos y ciclo de vida. Artefactos: casos de uso principales, boceto de la arquitectura, y plan de iteraciones.
2. **Elaboración**: comprender el problema y eliminar riesgos. Hito: arquitectura del ciclo de vida. Artefactos: línea base de la arquitectura, 80% de los casos de uso, plan detallado de iteraciones.
3. **Construcción**: desarrollar el producto. Hito: capacidad operativa inicial (versión beta). Artefactos: software, manual de usuario.
4. **Transición**: puesta en producción de la versión beta y correcciones. Hito: lanzamiento del producto. Artefactos: los mismos que en la fase de construcción.

![[Iteraciones del UP.png]]

Cada fase se subdivide en _iteraciones_, controladas con selección y planificación. Cada iteración tiene sus flujos de trabajo principales, y termina en un _incremento_ o release interna.

Un _flujo de trabajo_ es una secuencia de actividades que produce artefactos. Un _artefacto_ es una pieza de información producida. Los [[Flujos de Trabajo del Unified Process]] son:

1. Requerimientos.
2. Análisis.
3. Diseño.
4. Implementación.
5. Testing.

![[Flujos de Trabajo del UP.png]]

Se puede ver cómo todos los flujos de trabajo están en todas las fases, pero con distintos niveles de protagonismo dependiendo de la fase.

Se dice que UP es _bidimensional_ (contenido y fases), mientras que el modelo en cascada, al no tener fases, tiene solo una dimensión: el contenido.
