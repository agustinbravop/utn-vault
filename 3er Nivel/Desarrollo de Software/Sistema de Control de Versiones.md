Un **sistema de control de versiones** registra los cambios realizados sobre un conjunto de archivos a lo largo del tiempo, de manera que es posible recuperar versiones específicas.

Un SCV facilita el trabajo cooperativo. Ej: _git_, _cvs_, _subversion_.

Un SCV puede ser:

1. **Local**: almacena las versiones en una base de datos. No existe una manera eficiente de compartir código con otros desarrolladores.
2. **Centralizado**: se almacenan las versiones en un servidor al cual los usuarios se sincronizan para subir y bajar cambios.
3. **Distribuido**: cada desarrollador tiene una copia local del proyecto para trabajar de manera aislada, con un mecanismo de resolución de conflictos que permite integrar los cambios.

Ejemplos de SCVs distribuidos:

1. **CVS**: arquitectura cliente-servidor con un servidor central. Hacemos copias locales y luego las subimos (solo si están en la última versión). Licencia GNU.
2. **SVN**: subversion surgió en el 2000 para solucionar problemas de CVS. Tiene commits atómicos, manejo de archivos binarios, y solo envía los cambios (no el archivo completo). Estructura: `TRUNK` tiene la versión principal, mientras que las `TAGS` almacenan versiones de release.
3. **GIT**: surge en 2005 como alternativa open-source de _bitkeeper_. Es rápido, sencillo, eficiente, y distribuido. Introdujo el área de _staging_.
