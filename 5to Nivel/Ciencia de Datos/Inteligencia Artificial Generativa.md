Los GPTs y LLMs son tan flexibles que volvieron a tener relevancia los [[Agentes]] de [[Inteligencia Artificial]] y representan un cambio de paradigma. Muchos de los patrones que los humanos siguen también pueden ser desempeñados por modelos fundacionales bien diseñados.

Propiedades:

- Entendimiento del lenguaje natural.
- Interacción con contexto.
- Generación de contenido estructurado.

Esto se debe a los ***transformers***, una arquitectura que puede calcular de manera recurrente y en paralelo las relaciones entre tokens (palabras). El concepto de **atención** (*attention is all you need*) es la intuición detrás del funcionamiento de transformers.

## Agentic Systems

Un "sistema agentico" (**agentic system**) es una funcionalidad que permite a un agente a ejecutarse efectivamente, incluyendo:

- Herramientas.
- Memoria.
- El modelo fundacional.
- Orquestración.
- Infraestructura de soporte.

La integración con *frameworks de orquestación* permite a los modelos interactuar con sistemas externos, ejecutar tareas prácticas, y coordinar múltiples agentes de IA. Las *herramientas* son las capacidades fundamentales que le permiten al agente desempeñar acciones específicas. La *memoria* permite a los agentes mantener el contexto y aprender de interacciones pasadas

Tipos de agentes:

1. **Reflex agents**: mapeo directo de input a acción. No hay razonamiento interno.
2. **ReAct agents**: varían entre razonamiento y acción, partiendo tareas en pasos.
3. **Planner-Executor agents**: definen dos fases diferentes.
4. **Query-Decomposition agents**: iterativamente dividen una pregunta en subpreguntas.
5. **Reflection agents**: ReAct + revisar pasos previos para aprender de los errores.
6. **Deep Research agents**: atacan investigaciones abiertas mediante la combinación de múltiples patrones y tipos de agentes.

Un agente más adaptativo y capaz suele implicar latencia y costos mayores.

## RAG

*Retrieval-Augmented Generation* (RAG) incorpora memoria en los agentic systems, permitiéndoles generar respuestas enriquecidas por el contexto y por ende con mayor información.

![[RAG.png]]

En proyectos del mundo real, es importante elegir entre un simple script de código, un workflow determinístico, un chatbot tradicional, un sistema RAG, o un agente autónomo completo.
