Las **historias de usuario** (HU) son pedacitos de funcionalidad que establecen los [[Requerimientos]] del cliente. Es la alternativa a la [[Captura de Requisitos en el PU]] que las [[Metodologías Ágiles]] proponen. Se escriben con cierto formato:

```
Como <rol>
Quiero <funcionalidad>
Para <valor para el negocio>
+ <criterios de aceptación>
+ <prioridad>
+ <estimación>
+ <dependencias>
```

Se les suele agregar un ID, un título, y criterios de aceptación. De manera oportunista, se les puede ir agregando detalle al implementarlas.

Las 3 C orientan a las HUs hacia los resultados y no hacia la especificación:

- **Card**: se suele usar una tarjeta o post-it.
- **Conversation**: las HUs son una herramienta para generar diálogo y aclarar dudas.
- **Confirmation**: se deben establecer pruebas que determinen la completitud exitosa de la HU.

Los _criterios de aceptación_ se pueden definir:

- **Por comportamiento**: escritos en GHERKIN (`GIVEN ... WHEN ... THEN ...`).
- **Por escenarios**: se definen el camino feliz y los alternativos. Similar a un [[Caso de Uso del Sistema]].

Una buena HU sigue el acrónimo INVEST:

1. Independiente.
2. Negociable.
3. Valuable.
4. Estimable.
5. Small.
6. Testeable.

Una HU muy grande se la puede considerar un _tema_, que da una visión general de un subsistema del software. Este tema se puede subdividir en _épicas_, que agrupan funcionalidades. Cada una de estas funcionalidades sería una historia de usuario, que el equipo de desarrollo subdivide en _tareas_ al momento de implementarla.

## Estimación

Las HU se estiman con _story points_, un puntaje subjetivo que mide la _complejidad_ que el equipo de desarrollo considera que tiene la implementación de la HU. Este puntaje se puede asignar con varias técnicas, como la planning poker. Se pueden usar varias escalas, como los talles de remera (XS, S, M, ...) o la serie de Fibonacci (1, 2, 3, 5, 7, 13, ...).

La _velocidad_ es la cantidad de story points que se pueden lograr en un sprint.
