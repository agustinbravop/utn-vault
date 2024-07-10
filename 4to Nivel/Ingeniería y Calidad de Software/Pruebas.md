Las **pruebas** apuntan a **destruir** el software construido $\implies$ mentalidad opuesta a la de desarrollo. El ingeniero debe descartar ideas preconcebidas y superar conflictos de interés frente a errores encontrados en el software.

Premisa principal: **todo software tiene errores** y debemos **encontrar la mayoría posible**. Dado un presupuesto, buscamos encontrar la mejor manera de **detectar la mayor cantidad de errores**.

Incluye el diseño de los [[Casos de Prueba]]. Se pueden **automatizar** con la [[Automatización de Pruebas]]. Se organiza mediante [[Estrategias de Prueba]].

En los [[Proyectos Ágiles]] las pruebas no son una etapa del proyecto, sino que el tester es un **miembro del equipo** siempre presente. Las [[Pruebas]] son una **disciplina y actividad**, no un paso o fase del proyecto.

## Principios

1. A las pruebas se les puede hacer un **seguimiento** hasta los **requisitos** del cliente.
2. Las pruebas deberían **planificarse** mucho antes de que empiecen.
3. Se puede aplicar **Pareto** (el 80% de los bugs aparecen en el 20% del sistema).
4. Las pruebas deberían empezar por lo pequeño e ir hacia lo grande (**bottom-up**).
5. No son posibles las pruebas exhaustivas.
6. Para ser eficaces, debe testear un **equipo independiente**.

## Facilidad de Prueba

La **facilidad de prueba** es la facilidad con la que se puede probar un sistema. Es el resultado de un **buen diseño**.

Características de un software fácil de probar:

1. **Operatividad** (software funcional)
2. **Observabilidad** (poder ver el resultado de la prueba)
3. **Controlabilidad** (poder configurar el software y sus variables)
4. **Capacidad de descomposición** (cohesión y acoplamiento)
5. **Simplicidad** (funcional, estructural y del código)
6. **Estabilidad**
7. **Facilidad de comprensión** (del código)
