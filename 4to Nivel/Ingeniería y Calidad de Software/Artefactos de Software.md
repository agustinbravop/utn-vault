Se hace [[Gestión de la Configuración]] sobre todos los artefactos de software del ciclo de vida:

- **Programas:** código fuente y ejecutables.
- **Documentos:** modelos y requerimientos.
- **Datos**.
- **Infraestructura:** categoría nueva gracias a la _Infrastructure as Code_.

Existen estándares y normas de SCM pero no son comunes en la industria. Utilizan las siguientes definiciones.

## Versión

Una **versión** es una instancia de un artefacto de software. Puede ser una:

- **Revisión:** versión que busca reemplazar versiones anteriores.
- **Variante:** versión que se añade sin reemplazar las anteriores.
- **Entrega:** (release) versión que se distribuye a los clientes.

## Elemento de configuración

Es cualquier parte de un producto de trabajo con un nombre y atributos, sobre el cual se quiere gestionar su configuración. Es la **unidad atómica gestionable**. Los **ECs** son versionados.

## Configuración

Una **configuración** es una selección de una versión por cada artefacto del sistema. Es el **estado completo** **del sistema en cierto instante**.

## Línea Base

Una **línea base** o de referencia es una especificación revisada formalmente que sirve como base para un desarrollo posterior y solo puede cambiarse con métodos formales de control de cambios.

## Traza

Una **traza** es una relación entre dos elementos de configuración. Con la SCM se busca la **trazabilidad** para poder seguir la **historia del sistema** y conocer qué cambios fueron introducidos en qué momentos y quiénes fueron los participantes involucrados.
