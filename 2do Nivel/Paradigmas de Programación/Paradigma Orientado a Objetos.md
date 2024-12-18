El [[Paradigma de Programación]] orientado a **objetos** establece varios conceptos básicos.

**Objetos**: son entidades que representan cosas o conceptos, sirven para modelar. Un objeto tiene _atributos_, _comportamiento_, e _identidad_. Son **dinámicos**: viven y mueren.

**[[Clases]]**: son plantillas para crear objetos de cierta manera predeterminada. Las clases son [[Tipos de Dato]]. En la clase se definen los métodos que tendrán los objetos de esta clase.

## Comportamiento

**Mensajes**: un objeto cliente (o usuario) le envía un mensaje a otro objeto para que ejecute un método. Así se logra el comportamiento del programa. Ej: un mensaje `doble(5)` a un objeto de la clase `Multiplicador` solicita que el objeto multiplicador ejecute el método `doble`, y luego retorne el resultado.

Hay dos métodos especiales:

- **Constructor**: se ejecuta al instanciar un objeto para establecer atributos.
- **Destructor**: se ejecuta al eliminar un objeto para controlar la memoria.

## Atributos

Los **atributos** de los objetos son variables [[Variables#Enlace|enlazadas]] a algún valor (que puede ser otro objeto) y viven en el [[Variables#Ámbito|ambiente]] del objeto (`this, self`). Pueden ser:

- **De Instancia**: es una zona de memoria propia al objeto, distinta para cada instancia.
- **De Clase**: es una sola zona de memoria para la clase compartida por todas las instancias. Si una instancia $A$ modifica un atributo de clase, otra instancia $B$ de la misma clase verá el cambio.

Conviene que los atributos sean privados para que solo los objetos de la clase misma puedan cambiar su estado interno. Luego, los métodos públicos se encargan de manipular el estado privado. Este **encapsulamiento** asegura que los objetos siempre estén en un **estado válido**.
