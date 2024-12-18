En el [[Paradigma Orientado a Objetos]], son plantillas para crear objetos de manera predeterminada. Las clases son [[Tipos de Dato]]. En ellas se definen los métodos que tendrán sus objetos.

Una clase puede ser:

- **Concreta**: puede ser instanciada para crear objeto. Viceversa, todo objeto pertenece a una clase concreta.
- **Abstracta**: abstrae varios métodos y atributos que algunas clases concretas tengan en común, y los agrupan en una clase abstracta. No se pueden instanciar. Establecen *contratos* que sus clases hijas deben cumplir (implementar). 

## Relaciones entre Clases

![[Relaciones entre Clases.png]]

- **Agregación**: una clase contiene atributos de otras clases, con un sentimiento de *pertenece-a*.
- **Composición**: similar a la agregación pero con un acoplamiento mayor. Tienen el ciclo de vida ligado, y no existe parte sin el todo. Tampoco existe el todo si le faltan partes. Es *dueño-de*.
- **Asociación**: la clase $A$ conoce a $B$ pero no viceversa. Es relación *tiene-un*.
- **De Uso**: la clase usa un objeto de otra clase pero no como un atributo, sino como un parámetro de un método o como una simple llamada a un método de esa clase.
