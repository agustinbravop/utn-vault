En la vista de gestión del modelo de [[UML]], un **diagrama de paquetes** muestra las _dependencias_ de nuestros paquetes, reflejando la arquitectura de alto nivel del sistema. Cada _paquete_ es una unidad de organización del modelo.

![[Diagrama de Gestión del Modelo.png]]

- **Modelo**: es un paquete que abarca una descripción cerrada del sistema. Representa un POV.
- **Subsistema**: es un paquete con piezas de especificación y realización. Representa una partición.

![[Diagrama de Gestión del Modelo 2.png]]

Una dependencia puede ser:

- **De acceso**: no modifica el _namespace_ del cliente, sino que solamente concede permiso para hacer referencias. Ej: `Productos::Producto.get()`.
- **De importación**: agrega nombres al namespace del cliente. Ej: `Precio.get()`.
