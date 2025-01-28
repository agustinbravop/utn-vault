En las [[Metodologías de Desarrollo]], existen métodos inspirados en el [[Paradigma Orientado a Objetos]] que nos otorgan ciertas ventajas:

- Reusabilidad del software.
- Mejor mantenibilidad del software.
- Disminuir el _gap semántico_ entre el analista y el diseñador.
- Ayuda a resolver problemas complejos.

Es importante distinguir entre objetos y atributos, clases y objetos, el todo y sus partes.

Un **sistema orientado a objetos** está formado por objetos con cierta responsabilidad que interactúan entre sí enviando y recibiendo mensajes. Un **programa orientado a objetos** es una _red colaborativa_ de objetos.

Un **objeto** puede representar algo físico o abstracto, del problema o la solución, etc.

![[Métodos Orientados a Objetos 2025-01-24 19.41.03.excalidraw.svg]]

Tipos de _mensajes_:

1. Sincrónico.
2. Asincrónico.
3. De tiempo límite (tienen un _timeout_).

Una _responsabilidad_ es el contrato u obligación de un objeto, cosas que hace y conoce.

Una _colaboración_ ocurre cuando dos o más objetos interactúan entre sí para realizar una tarea. Cuando un objeto no sabe hacer algo por fuera de su responsabilidad, delega a otro objeto mediante mensajes.

Pilares:

1. **Abstracción**: nos enfocamos en la interfaz del objeto y no en su implementación.
2. **Encapsulamiento**: permite ocultar los detalles de implementación. Mejora la mantenibilidad.
3. [[Herencia]]: reutilización del código y la estructura.
4. [[Polimorfismo]]: cada objeto puede resolver un mismo mensaje de distinta manera. Se logra mediante interfaces, sobrecarga de métodos, sobreescritura de métodos, etc.

El **diseño orientado a objetos** abarca un proceso de descomposición orientada a objetos y una notación para representar modelos lógicos o físicos y estáticos o dinámicos. Pasos:

1. Identificar clases.
2. Identificar responsabilidades.
3. Asignar responsabilidades a clases.
4. Identificar colaboraciones.
