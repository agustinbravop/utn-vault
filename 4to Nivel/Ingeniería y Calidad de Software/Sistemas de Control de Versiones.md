Combinan herramientas y procedimientos para gestionar versiones de los [[Gestión de la Configuración#Elemento de configuración|ECs]] cuando son creados y modificados. La implementación estándar en la industria de un sistema de control de versiones es [[Git]].

Algunas definiciones:

- **Repositorio:** es el conjunto de archivos o elementos de configuración que se están controlando.
- **Check out**: es buscar y acceder a un artefacto del repositorio.
- **Check in:** es guardar una nueva versión del artefacto. Es importante describir las modificaciones realizadas.
- **Trunk:** o main, o master. Es la rama (o historia) principal del repositorio.
- **Head:** referencia a la última versión (último commit) de la rama.
- **[[Estrategias de Branch y Merge]]**: es para incorporar cambios de ramas al trunk.
- **Delta de cambios:** conjunto de cambios que nos llevan de una versión a la otra (diff).

![[Control de la Configuración 2024-04-28 00.12.11.excalidraw.svg]]

Es importante que los _delta changes_ se hagan cada plazos cortos así son pocos los cambios, y la integración del código se vuelve frecuente. Esos cambios deben estar justificados y sería ideal que su descripción tenga un link al ticket de cambio asociado. Por ejemplo, que un commit de GitHub tenga un link a la historia de usuario o tarea de Jira.

## Repositorios

Se clasifican en:

- **Centralizados:** hay una sola línea base con todos los cambios guardados que se encuentra en el servidor central. Fueron los primeros pero se dejaron de usar porque ocurrían bloqueos entre desarrolladores y no escalaban de manera eficiente.
- **Distribuidos:** surgen desde la comunidad de OSS (Open Source Software) y proponen que cada persona o servidor tenga su propia linea base. Igual conviene tener un repositorio remoto central para la integración continua del código.

Para mantenerse lo más sincronizado posible, se hace _pull_ al comenzar a trabajar y antes de cada _push_. Mantener el delta de cambios pequeño ayuda a disminuir la probabilidad de que haya conflictos.
