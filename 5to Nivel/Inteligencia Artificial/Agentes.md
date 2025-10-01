Un **agente** es todo aquello que percibe su ambiente mediante sensores y que responde o actúa en ese ambiente mediante actuadores.

> "Un **agente** es un sistema informático encapsulado, situado en un ambiente, que actúa de forma [[Inteligencia Artificial|autónoma y flexible]] para lograr su objetivo." - Woolbridge

Deben tener:

1. **Proactividad**: orientación a objetivos.
2. **Reactividad**: percibir el ambiente y responder.
3. **Sociabilidad**: interactuar con otros agentes.

Para construir un agente inteligente, la clave es lograr un balance entre el comportamiento reactivo y la orientación a objetivos.

- Estados del ambiente: $S = \set{s_1, s_2, \dots}$.
- Acciones del agente: $A=\set{a_1,a_2,\dots}$.
- Agente: definido como $\text action : S^* \rightarrow A$.

El entorno del agente se puede clasificar en:

- Accesible (información completa) vs inaccesible (información parcial).
- Determinístico vs no determinístico (incertidumbre).
- Episódico vs no episódico.
- Estático vs dinámico.
- Discreto vs continuo.

## Agentes Puramente Reactivos

Los **agentes puramente reactivos** deciden qué hacer sin considerar su historial.

$$
\begin{align}
\text {see} &: S \rightarrow P \ \ \ \ \ \text{ donde $P$ es el conjunto no vacío de percepciones} \\
\text {action} &: P \rightarrow A
\end{align}
$$

Dos estados diferentes $s \in S$ y $s'\in S$ son **equivalentes** $\iff$ $\text {see}(s) = \text {see}(s')$.

## Agentes con Estado

Los **agentes con estado** tienen una representación interna de lo que creen que sucede en el ambiente.

$$
\begin{rcases}
\text {see} &: S \rightarrow P \\
\text {action} &: I \rightarrow A \\
\text {next} &: I \times  P \rightarrow I
\end{rcases}  \ \text { action}(\text{next}(i_0,\text{see}(s)))
$$

## Arquitecturas Concretas

- [[Agentes Basados en Lógica]].
- [[Agentes Reactivos]].
- [[Agentes BDI]].

### Modelo de Capas

Una arquitectura de capas implica crear subsistemas en una jerarquía, descomponiendo un agente en subsistemas donde algunos se encargan del comportamiento reactivo y otros del comportamiento proactivo.

![[Modelo de Capas (Agentes).png]]

El flujo de información y de control se puede dar de varias maneras:

- **Capas horizontales**: cada capa actúa como un agente. Es un enfoque simple pero el problema es que las capas compiten entre sí por la acción del agente, por lo que su comportamiento puede ser incoherente.
- **Capas verticales de un paso**: el flujo de control y el flujo de información es el mismo.
- **Capas verticales de dos pasos**: la información sube por la arquitectura y luego baja el control. Esto es similar a la jerarquía de una organización tradicional donde el nivel operativo captura datos para el directorio y ejecuta decisiones tomadas por el directorio.

## IA Agentiva

La [[Inteligencia Artificial]] agentiva es una forma de IA centrada en la toma de decisiones y la acción autónoma.

Esta tecnología se basa en la **percepción** del entorno y el [[Razonamiento]] con LLMs. El agente formula distintas soluciones, lo que implica **planificación, acción, y reflexión** (es decir que aprende de los resultados).
