La **cohesión**, considerada en el [[Diseño Estructurado]], es una medida cualitativa de la **relación funcional** de los elementos de un módulo.

Los niveles de cohesión son:

$$\underbrace{\text{Funcional} \gt \text{Secuencial} \gt \text{De comunicación}}_{\text{unidos por los datos (generalmente aceptables)}} \gt \underbrace{\text{Procedural} \gt \text{Temporal}}_{\text{unidos por el flujo de control}} \gt \underbrace{\text{Lógica}\gt \text{Casual}}_{\text{ nada (inaceptable)}}$$

![[Cohesión.png]]

Un módulo puede tener elementos asociados por distintos principios, mezclando los niveles de cohesión. En este caso, se dice que el módulo tiene el nivel de cohesión aproximado al nivel más alto de cohesión que sea aplicable a TODOS sus elementos.

Se busca que el software que estamos desarrollando tenga alta cohesión y bajo [[Acoplamiento]]:

![[Acoplamiento y Cohesión.png]]
