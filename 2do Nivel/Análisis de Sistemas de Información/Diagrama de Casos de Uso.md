Un **diagrama de casos de uso** muestras las relaciones entre los actores y los [[Caso de Uso del Sistema]] (o [[Caso de Uso del Negocio]]). Modela a actores y sus casos de uso. Se lo diagrama desde el punto de vista del usuario y tiene un alto nivel de abstracción.

Un _actor_ es una persona o sistema que asume un rol al _interactuar_ con el sistema.

Un _caso de uso_ es una secuencia de transacciones realizadas por el sistema para brindar valor a un actor del sistema.

![[Relaciones en un Diagrama de Casos de Uso.png]]

Estos diagramas son una buena imagen general del sistema y sus usuarios, pero son malos para representar restricciones de diseño o [[Requisitos de Software]] no funcionales.

```mermaid
flowchart LR;
1[Identificar<br/>roles<br/>relevantes] --> 2[Identificar<br/>objetivos de<br/>cada rol] --> 3[Crear un<br/>caso de uso<br/>por objetivo] --> 4[Estructurar<br/>los casos<br/>de uso] --> 5[Revisar y<br/>validar con<br/>el usuario]
```

El caso de uso debe describir de forma clara el comportamiento externo observable del software. No se deben mencionar interfaces del sistema o situaciones externas al alcance del sistema. Se debe identificar claramente al actor y usar la voz activa en forma de acción-reacción. El caso de uso responde de forma completa al objetivo de un actor, y tiene sentido para el actor.

Un diagrama de CU no debe mostrar más de 15 casos, sino que debería particionarse en varios _paquetes_. Es conveniente agrupar las funcionalidades en módulos por actor. Hay que comprobar que los CU incluyan toda la funcionalidad del sistema.

## Tipos de Caso de Uso

Según el nivel de detalle de su descripción:

1. Breve.
2. Informal.
3. Expandido.

Para considerar la granularidad apropiada de un caso de uso, hay que tener en cuenta los objetivos de los actores.

Según si corresponde con un proceso de negocio o no:

- Primario.
- Secundario.
