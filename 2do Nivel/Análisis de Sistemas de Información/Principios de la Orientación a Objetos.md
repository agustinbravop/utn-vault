El [[Paradigma Orientado a Objetos]] es un conjunto de teorías, o una forma de entender la realidad, o una manera de pensar. Las [[Metodología|metodologías]] orientadas a objetos ven a los sistemas como un conjunto de objetos que interactúan entre sí. Los objetos se analizan de particular a general (*bottom-up*). Ese análisis ascendente permite un refinamiento sucesivo.

El *contexto* del problema se ve como un conjunto de objetos que interactúan. Una *clase* describe un tipo de objeto del problema con atributos y comportamientos asociados.

$$\text{Orientación a Objetos} = \text{Objeto} + \text{Clasificación} + \text{Herencia} + \text{Comunicación}$$

Un *objeto* tiene:

1. **Estado**: compuesto por las variables de la instancia del objeto. Es *privado*.
2. **Comportamiento**: son los métodos o funcionalidades que tiene. Pueden manipular el estado.
3. **Identidad**: es única y distinta para cada objeto, independiente de sus atributos.

El comportamiento mueve al objeto de un estado a otro. Indica qué es lo que el objeto sabe hacer, es decir, determina sus **responsabilidades**.

La *implementación* es un conjunto de métodos que indica cómo el objeto responde a los mensajes que recibe, y es privada al objeto El conjunto de *mensajes* que el objeto sabe responder constituye su *protocolo*. El protocolo tiene 3 niveles de *interfaz*:

1. Pública.
2. Protegida.
3. Privada.

Siendo un *método* la implementación funcional de un mensaje, puede:

- Modificar el estado interno (*set*).
- Colaborar con otros objetos.
- Retornar atributos y terminar (*get*).

[[Herencia]]: una *subclase* puede heredar la estructura y los métodos de una superclase para reutilizar comportamiento. También puede tener métodos y datos propios. 

Una *operación*, según UML 2.0, especifica un servicio que se puede requerir de una clase. De esta forma, usando el mecanismo de herencia, puede haber varios métodos para la misma operación.

[[Polimorfismo]]: es un mecanismo que permite definir e invocar funciones con la misma interfaz pero con implementación diferente. Se logra en subclases con un ancestro común.

Una *clase abstracta* es una clase que no se puede instanciar, y se usa solo para definir subclases. Nos permite usar polimorfismo.

## Evolución de UML

UML fue impulsado por Grady Booch, James Rumbaugh, e Ivar Jacobson. Sus objetivos son:

- Establecer un lenguaje visual expresivo y sencillo para el [[Modelado de los Sistemas]].
- Mantener la independencia entre el modelado y los lenguajes de programación.
- Integrar las mejores prácticas.
- Imponer un estándar global.

UML nos ofrece una manera más natural o intuitiva de modelar. Gracias al encapsulamiento, facilita el mantenimiento y la extensión del software. Esto aumenta la productividad y la calidad.
