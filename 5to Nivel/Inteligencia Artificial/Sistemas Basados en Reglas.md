Estos modelos de [[Inteligencia Artificial]] tienen tres partes relevantes:

1. **Base de Conocimiento**: almacena información permanente y estática (un conjunto de reglas).
2. **Motor de Inferencia**: obtiene nuevas conclusiones o hechos.
3. **Memoria de Trabajo**: almacena los datos.

Hay dos elementos fundamentales:

- [[Datos]]: hechos conocidos sobre un problema particular. Es dinámico.
- [[5to Nivel/Inteligencia Artificial/Conocimiento|Conocimiento]]: relaciones entre los objetos dentro del dominio del problema.

Una **regla** es una afirmación lógica que relaciona dos o más objetos:

$$\text{(premisa) } \ A \longrightarrow B \ \text{ (conclusión)}$$

El motor de inferencia usa datos y conocimientos para obtener conclusiones. Las _conclusiones simples_ derivan de _reglas simples_ (no vemos reglas compuestas). El MI solo acepta operadores $\land$ (and) y $\lnot$ (not).

Reglas de inferencia que se pueden usar:

- **Modus Ponens**: si la premisa es cierta, la conclusión pasa a ser conocimiento. Propaga hacia adelante.
- **Modus Tollens**: si la conclusión es falsa, la remisa también es falsa. Propaga hacia atrás, lo que equivale a expandir la base de conocimiento.

Estas reglas de inferencia permiten obtener **conclusiones simples**.

![[Modus Ponens y Modus Tollens.png]]

Estos modelos son determinísticos, y por ende no muy inteligentes. El [[Modelo de Reglas de Asociación]] introduce incertidumbre a las reglas, y es más potente.

## Estrategias de Inferencia

La estrategia de inferencia que usamos es el **encadenamiento de reglas**, donde los hechos conocidos dan lugar a _hechos inferidos_. Pasos:

1. Asignar a los objetos sus valores conocidos.
2. Ejecutar cada regla de la base de conocimiento y concluir nuevos hechos si es posible.
3. Repetir la etapa 2 hasta que no se pueda obtener nuevos hechos.

Si durante el encadenamiento encontramos una _contradicción_, eso se debe a un hecho conocido erróneo. El motor de inferencia hace **rollback** y descarta la máquina de trabajo hasta ese punto.

## Control de la Coherencia

El control de la coherencia es necesario por si la base de conocimiento es inconsistente.

**Un conjunto de reglas es _coherente_ si existe al menos un conjunto de valores de todos los objetos que producen conclusiones no contradictorias**. Con uno es suficiente.

Un valor $a$ para el objeto $A$ NO es factible si las conclusiones al hacer $A=a$ contradicen cualquier combinación de valores del resto de objetos. Los valores no factibles deben ser prohibidos.
