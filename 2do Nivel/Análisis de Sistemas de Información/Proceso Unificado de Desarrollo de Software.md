Los sistemas de software son cada vez más grandes, complejos, y distribuidos. La demanda del mercado es **cada vez más software de mejor calidad en menor tiempo de manera predecible**. Un _proceso_ permite repetir las prácticas exitosas y mejorar o evitar las ineficientes.

El proceso de desarrollo de software es el conjunto de actividades necesarias para transformar los [[Requerimientos]] de usuario en un sistema de software. El **proceso unificado** (UP) es un proceso de desarrollo de software, construido a partir de los aportes de 3 autores:

1. Rumbaugh: aporta los modelos de objetos de dominio del problema.
2. Jacobson: aporta la producción orientada al usuario.
3. Booch: aporta modelos de diseño orientados a objetos.

Toda [[Metodología]] tiene:

1. **Paradigma**: un enfoque o forma de ver las cosas. En este caso, tiene [[Principios de la Orientación a Objetos]].
2. **Actividades, Acciones, y Tareas**: determinan qué hacer.
3. **Flujo de Trabajo**: determina la secuencia lógica de cuándo hacer cada cosa.
4. **Herramientas**: técnicas que ayudan a realizar las cosas.
5. **Tipo**: si es prescriptivo o adaptativo. En este caso, es **prescriptivo**.

El _Unified Process_ (UP) es un conjunto de artefactos, actividades, y roles, basados en las mejores prácticas, promoviendo una visión y cultura de trabajo común. Reduce los riesgos y hace que el proyecto sea más predecible (y medible). Los objetivos de usar un proceso son:

1. Lograr un desarrollo más rápido, reduciendo el _time-to-market_.
2. Mejorar la calidad y disminuir el [[2do Nivel/Análisis de Sistemas de Información/Riesgo|Riesgo]].
3. Disminuir los costos.

![[Proceso de Desarrollo de Software.png]]

UP ofrece 6 mejores prácticas:

1. Desarrollar iterativamente.
2. Administrar requerimientos.
3. Usar una arquitectura de componentes.
4. Modelar visualmente.
5. Verificar la calidad.
6. Controlar los cambios.

Teniendo en cuenta los [[Flujos de Trabajo]], el PU es **iterativo** e **incremental**:

1. Logra la integración continua.
2. Logra el aprendizaje temprano.
3. Es más barato equivocarse.
4. Hay flexibilidad mediante la retroalimentación y la adaptación.
5. Hay consistencia gracias a las iteraciones cortas y fijas.

![[Desarrollo Incremental e Iterativo.png]]

## Componente de Software

Un _componente_ es un elemento de software que ofrece un conjunto de funcionalidades. Permite crear nuevas funciones reutilizando o ensamblando componentes. Un componente es:

1. **Reutilizable**.
2. **Intercambiable** (de bajo acoplamiento).
3. **Cohesivo** (hace una sola cosa y la hace bien).
4. Con **interfaces bien definidas**.

## Arquitectura de Software

Mientras que los [[Caso de Uso del Sistema|casos de uso]] conducen el desarrollo de la _arquitectura_, la arquitectura indica qué casos de uso pueden realizarse. Da la **forma** del sistema, y debe soportar su mantenimiento y extensión.

Las 4+1 vistas de la arquitectura según Kruchten:

![[4+1 Vistas de Kruchten.png]]

La arquitectura se ve influenciada por la plataforma, sistemas legacy, requisitos no funcionales, restricciones de diseño, etc.

## Ciclo de Vida del Software

El [[Ciclo de Vida del Software]] en el Proceso Unificado tiene varios _ciclos_ de desarrollo que concluyen con un producto evolucionado. Cada _fase_ se subdivide en varias _iteraciones_. En cada fase hay un _hito_ o entrega de ejecutables, código fuente, y/o documentos.

![[Ciclo de Vida del Software en el Proceso Unificado.png]]

Cada hito es un punto de control. Tras cada ciclo, se entrega una nueva versión del producto.

Flujos de trabajo o _disciplinas_ en el PU:

1. Requisitos ([[Captura de Requisitos en el PU]]).
2. Análisis ([[Flujo de Análisis en el PU]]).
3. Diseño.
4. Implementación.
5. Pruebas.
6. De Soporte: gestión de cambios, de configuración, etc.

![[Disciplinas del Proceso Unificado.png]]

El Proceso Unificado es un marco de trabajo flexible y extensible, con la libertad de ser adaptado a cada contexto de cada [[Proyecto de Software]]. Cada equipo de desarrollo aplica su propio PU personalizado a sus necesidades específicas.
