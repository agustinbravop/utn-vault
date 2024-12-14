Los [[Archivo|archivos]] son un mecanismo de abstracción del [[Sistema Operativo]] que proporciona una manera de **almacenar y leer información** en el disco. Son **unidades lógicas** de información creadas por un [[Proceso]] con información asociada (nombre, permisos, formato, etc).

Desde la visión física del sistema operativo, un archivo entero puede estar dividido en varios **bloques** de la unidad de disco.

![[Bloques de la Unidad de Disco.png]]

**Extensiones**: en algunos sistemas (UNIX), las extensiones de archivos son solo convenciones. En otros (Windows), la extensión determina qué aplicación lo abre por defecto.

**Atributos**: están asociados al [[Sistema de Archivos]]. Ej: tamaño actual, tamaño máximo, banderas, contraseña, creador, hora de creación.

**Directorios**: archivos especiales que pueden contener otros archivos.

**Operaciones sobre archivos**:

1. Create.
2. Delete.
3. Open.
4. Close.
5. Read.
6. Write.
7. Append.
8. Seek.
9. Get attributes.
10. Set attributes.
11. Rename.
