La **ingeniería de control** aplica la [[Teoría de Control]] para analizar, diseñar, desarrollar, e implementar un [[Sistema de Control]].

Los proyectos de sistemas de control (SC) involucran equipos interdisciplinarios con profesionales de varias ingenierías: ingenieros en sistemas de información, electrónica, industrial, mecánica, etc.

El ingeniero debe diseñar la arquitectura de la [[Bases de Datos|base de datos]] asociada al SC, debe seleccionar el lenguaje de programación más apropiado para el SC, define la arquitectura de [[Redes de Datos]] y los componentes priorizando [[Eficiencia y Eficacia]].

Algunas definiciones:

1. **Planta**: cualquier objeto físico que se desea controlar.
2. **Proceso**: cualquier operación que deba controlarse.
3. **Sistema**: combinación de componentes con un objetivo.
4. **Perturbación**: aparta a la variable controlada del valor de referencia.
5. **Control retroalimentado**: reduce la diferencia entre la variable y la referencia.
6. **Sistema de control retroalimentado**: mantiene una relación entre salida y referencia.
7. **Servomecanismo**: es el SC retroalimentado donde la salida es mecánica.
8. **Sistema de regulación automática**: SC retroalimentado cuya salida varía lentamente.
9. **Sistema de control de procesos**: SC de regulación automática que regula procesos.
10. **Sistema de control adaptable**: es capaz de detectar cambios en sus componentes internos.
11. **Sistema de control de aprendizaje**: el controlador "aprende" como un ser humano.

Los tiempos de SC también son importantes de considerar. Un SC da una respuesta:

1. **Transitoria**: es una salida errática cercana a $t=0$. Dura $T_s$.
2. **Estacionaria**: salida convergente lejos de $t=0$ que dura indefinidamente.

![[Tiempos del Sistema de Control.png]]

La estabilidad absoluta se clasifica en:

- **Estable**: la respuesta converge a un valor deseado.
- **Marginalmente estable**: salida con oscilaciones aceptables, amortiguadas.
- **Inestable**: diverge a valores muy grandes.

![[4to Nivel/Tecnologías para la Automatización/attachments/Estabilidad.png]]

La **estabilidad relativa** son los márgenes de estabilidad (máximo y mínimo) dentro de los cuales es aceptable que oscile la salida del sistema. La tensión entre la velocidad de respuesta y la precisión en la estabilidad es un problema de diseño.

El diseño de sistemas de control debe tener en cuenta estos factores para diseñar un sistema y luego resolverlo. "Resolver un sistema" es hallar la relación matemática entre sus entradas y salidas. Se puede usar un [[Diagrama de Bloques Funcionales]].
