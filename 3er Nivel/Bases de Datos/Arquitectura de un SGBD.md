El enfoque de las [[Bases de Datos]] busca:

1. Separar los programas de los datos.
2. Soportar múltiples vistas de usuario.
3. Usar un catálogo para guardar el esquema de datos.

En la **arquitectura de tres niveles** de un [[Sistema de Gestión de Bases de Datos]]:

- Todos los usuarios deben poder acceder a los mismos datos.
- La vista de un usuario es independiente de las vistas de otros usuarios.
- El usuario no conoce cómo se almacenan o acceden los datos.

![[Niveles de Abstracción.png]]

Se busca tener **abstracción** (independencia de los datos) entre los siguientes niveles:

1. **Nivel Externo**: son las vistas a la que un usuario puede acceder. Distintos usuarios con distintos permisos tienen vistas diferentes.
2. **Nivel Conceptual**: es la capa lógica que describe qué datos se almacenarán, sus relaciones, atributos, y operaciones.
3. **Nivel Físico**: tiene un esquema físico que describe la estructura física de almacenamiento y los caminos de acceso.

Se busca la **independencia de datos**:

- **Lógica**: poder modificar el esquema conceptual sin alterar ni los esquemas externos ni los programas de aplicación. Ej: el esquema de las tablas en [[SQL]].
- **Física**: poder modificar el esquema interno sin alterar el conceptual. Ej: los índices.

Arquitectura de un SGBD basado en el modelo relacional de datos:

![[Arquitectura de un SGBD.png]]

Los **usuarios** pueden ser de varios tipos:

1. **Finales**: sin conocimiento técnico o con un poco de conocimiento informal.
2. **Programadores de apps**: en su código incrustan comandos SQL.
3. **Administradores de bases de datos**: son expertos que gestionan la base de datos.

Un administrador de bases de datos se encarga de definir esquemas, estructuras, permisos de acceso a datos, etc.
