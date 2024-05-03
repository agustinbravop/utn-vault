La **Software Configuration Management** es un conjunto de actividades que se desarrollaron para administrar el cambio a lo largo del [[Modelos del Proceso|ciclo de vida]] del software. Es clave para la [[Ingeniería de Software|ingeniería]] (the multiperson development of multiversion software).

> Es el arte de identificar, organizar, revisar y controlar las modificaciones que sufre el software que construye un equipo de desarrollo. - Babich

**SCM NO es mantenimiento**, sino que se realiza desde el inicio del desarrollo.

Las actividades de la SCM la caracterizan como una **disciplina de soporte**. Ellas son:

- Identificación.
- [[Control de la Configuración|Control]].
- Auditoría.
- Contabilidad del estado.

## Artefactos de Software

Se hace SCM sobre todos los artefactos de software del ciclo de vida:

- **Programas:** código fuente y ejecutables.
- **Documentos:** modelos y requerimientos.
- **Datos**
- **Infraestructura:** categoría nueva gracias a la _Infrastructure as Code_.

Existen estándares y normas de SCM pero no son comunes en la industria. Utilizan las siguientes definiciones.

### Version

instancia de un artefacto de software. Puede ser una:

- **Revisión:** versión que busca reemplazar versiones anteriores.
- **Variante:** versión que se añade sin reemplazar las anteriores.
- **Entrega:** (release) versión que se distribuye a los clientes.

### Elemento de configuración

Es cualquier parte de un producto de trabajo con un nombre y atributos, sobre el cual se quiere gestionar su configuración. Es la **unidad atómica gestionable**. Los **ECs** son versionados.

### Configuración

es una selección de una versión por cada artefacto del sistema. Es el estado completo del sistema en cierto instante.

### Línea Base

Una línea base o de referencia es una especificación revisada formalmente que sirve como base para un desarrollo posterior y solo puede cambiarse con métodos formales de control de cambios.

### Traza

Es una relación entre dos elementos de configuración. Con la SCM se busca la **trazabilidad** para poder seguir la historia del sistema y conocer qué cambios fueron introducidos en qué momentos y quiénes fueron los participantes involucrados.
