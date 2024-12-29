Un **caso de uso** (CU) es una secuencia de *interacciones* entre un sistema y alguien o algo que usa alguno de sus servicios. Es una **operación** completa y abarcativa, realizada entre el actor y el sistema, que produce un resultado identificable y útil para un autor.

![[Caso de Uso del Sistema.png]]

Son iniciados por el actor y siempre se escriben desde el **punto de vista del actor**, descubriendo cómo el sistema debe comportarse externamente (como si fuera un [[Sistema de Caja Negra]]). Los casos de uso especifican *qué* hace el sistema sin especificar *cómo* debe hacerlo.

Un **actor** representa el rol que una persona o sistema realiza frente al sistema. Puede ser

- **Primario**: persigue un objetivo.
- **Secundario**: participa para mantener el sistema o ayuda al actor primario a lograr su objetivo.

Un **usuario** es una *instancia* concreta de un actor que interactúa con el sistema. Al usar el sistema, el usuario asume un rol específico.

Cada caso de uso describe un autor, un evento disparador, y una serie de interacciones narradas con voz activa. Cada caso de uso tiene:

1. **Nombre**: debe coincidir con el objetivo del actor primario.
2. **Precondición**: describe en qué situación se debe encontrar el sistema para iniciar el CU.
3. **Postcondición**: describe cómo debe quedar el sistema si el CU finaliza con éxito.
4. **Excepciones**: situaciones anómalas y cómo tratarlas. Nos pueden desviar del *happy path*.

Los casos de uso se pueden considerar *clases*, cuyas instancias son una secuencia específica de acciones llamadas **escenario**. Hay varios escenarios posibles: happy path, error, not found, etc. El conjunto de escenarios forma al caso de uso. 

El **camino principal** o *happy path* es el escenario estándar, cuando el final del caso de uso resulta exitoso. Cada paso del *escenario* principal puede ser una:

1. **Interacción**: entre el usuario y el sistema.
2. **Validación**: de una [[Caso de Uso del Negocio#Reglas de Negocio|regla de negocio]] o de un dato ingresado.
3. **Cambio de estado lógico**: es interno al sistema. Ej: cambiar la contraseña, actualizar el stock.
