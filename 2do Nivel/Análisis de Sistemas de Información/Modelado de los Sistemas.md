Un **modelo** es una representación o *proyección facilitada* de la realidad. Es una *descripción analógica* (similar pero no alternativa).

El **modelado** es una acción de *proceso intelectual* por el cual un sujeto representa cierta características de un objeto a través de un modelo (una abstracción mental). Conocer es el acto en el que aprendemos características del objeto. No se puede modelar sin conocer, por esto es primero necesario el trabajo del [[Analista de Sistemas]] en la [[Ingeniería de Requisitos]].

En el modelado se usan 3 conceptos:

1. **Abstracción**: nos centramos en ciertos aspectos, y dejamos otros de lado.
2. **Conceptualización**: formamos un *concepto*, un conjunto de propiedades, que describe las propiedades comunes de un grupo de objetos. Tiene nombre, propósito, y miembros.
3. **Simbolización**: proceso mediante el cual *simbolizamos* el concepto para poder comunicarlo.

El modelado facilita:

- Comunicar ideas evitando ambigüedades.
- Evaluar alternativas.
- Aproximarnos gradualmente al producto.
- Visualizar el producto.

El modelado depende de la complejidad y del uso que se le dará al modelo. Un modelo se realiza con un *propósito determinado* y con un *público específico*. 

Al analista de sistemas, modelar le sirve para:

- Concentrarse en ciertos aspectos importantes y dejar otros indiferentes de lado.
- Discutir cambios y correcciones ([[Gestión de Requisitos]]).
- Validar el entendimiento del [[Negocio Detrás del Sistema]] y de las necesidades.

Las **herramientas** de modelado de sistemas deben ofrecer:

- Gráficas con detalles textuales de apoyo.
- Visualización en segmentos de forma descendente.
- Redundancia mínima.
- Transparencia.
- Visualización sencilla (fácil de entender).

Los modelos del **sistema existente** (actual) sirven como una *representación* durante la ingeniería de requisitos para entender sus funcionalidades, debilidades, y fortalezas. Luego, los modelos del **sistema nuevo** son una *construcción* que sirve para explicar los requisitos.

Los modelos sirven a lo largo de todo el [[Ciclo de Vida del Software]]:

![[Modelado de los Sistemas.png]]

## Software

$$\text{Software} = \text{Programa}+\text{Datos}+\text{Documentación}$$

En el modelado de software, se analiza y diseña el software antes de codificarlo. Ayudan a especificar [[Requisitos de Software]], estructuras de datos, etc. Son importantes para la calidad del software.

Un modelo puede ser de:

1. **Alto nivel**: es temprano, se lo muestra a stakeholders para explorar conceptualmente el problema. Nos centramos en el *qué* y no en el *cómo*.
2. **Medio nivel**: sirven para entender distintos módulos de la solución.
3. **Bajo nivel**: código fuente.

Hay modelos o herramientas específicas:

- Para el análisis estructurado: DFD, EP, DER, DD, DTE.
- Para el análisis orientado a objetos: diagramas de actividad, caso de uso, secuencia, clase, estado, etc. Se engloban en el *Unified Modeling Language* (UML), que ofrece 4 **perspectivas** del sistema:
	1. **Externa**: se modela el entorno o contexto del sistema.
	2. **Interacción**: se modelan las interacciones entre componentes o con el entorno.
	3. **Estructural**: se modela la organización, estructuras de datos, etc.
	4. **Comportamiento**: se modela cómo responde el sistema (dinámico) ante ciertos eventos.
