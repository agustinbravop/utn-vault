En [[UML]], un diagrama de [[Clases]] pertenece a la vista estructural del modelo del sistema. Permite visualizar las clases del programa y sus relaciones.

![[Diagrama de Clases.png]]

La _visibilidad_ de los atributos puede ser _privada_ solo para la clase, _pública_ para todos, _protegida_ a solamente la clase y sus subclases, o _interna_ al paquete. Un atributo o método es _estático_ si pertenece a la clase y es compartido por todos los objetos, en lugar de haber uno para cada objeto.

Relaciones:

1. Asociación.
2. Agregación.
3. Composición.
4. Generalización.
5. Dependencia (uso).

Un **clasificador** es un concepto discreto que tiene identidad, estado, comportamiento, y relaciones. Suele ser todo lo que sea instanciable. Ej: una clase, interfaz, caso de uso, actor, tipo de dato, etc.

Una **interfaz** es un clasificador que declara un conjunto de métodos. De esos métodos, solamente se especifica su _firma_, no su implementación. Así, las interfaces establecen un contrato que deben cumplir las clases que las implementen, lo que desacopla el código. Se las considera más flexibles y "livianas" que las clases abstractas.

![[Interfaz.png]]

Una **dependencia** existe entre dos elementos si cambios en la definición de un elemento pueden provocar cambios en el otro. Toda asociación implica una dependencia, debido a la relación proveedor-cliente.

Los **estereotipos** que existen son:

1. **Entidad**: `<<entity>>`.
2. **Interfaz**: `<<boundary>>`.
3. **Control**: `<<controller>>`.

![[Estereotipos de UML.png]]

UML 2.0 introduce una diferencia entre _ownership_ (cuando una clase es dueña de la asociación) y _navegabilidad_ (cuando una clase solamente conoce a la otra clase de la asociación).
