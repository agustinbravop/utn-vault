Un **caso de uso del negocio** representa un proceso del [[Negocio Detrás del Sistema]], que puede ser *general* o *complejo*. Es un modelo, útil en el [[Modelado del Negocio]], que representa el conjunto de actividades a realizar para satisfacer una petición.

En un diagrama, representamos quién se beneficia de qué procesos. Un *actor* es cualquier persona o cosa externa a la organización que interactúa con ella. Se subdividen en:

- **Clientes**: son la razón de ser del negocio.
- **Socios**: son los dueños del negocio (inversionistas, sucursales, etc).

![[Actores.png]]

No hay secuencialidad, solo iniciadores. Ejemplo:

![[Ejemplo de Caso de Uso del Negocio.png]]

Las relaciones pueden ser:

- **De inclusión**: siempre que se realiza un caso de uso, también se realiza el caso de uso incluido. Sirve para reutilizar casos de uso, o para particionarlos en partes comunes.
- **De extensión**: se ejecuta solo si el actor lo desea (condicionalmente).
- **De generalización**: es un caso de uso especializado, que "hereda" de otro caso de uso.

![[Relaciones en un Caso de Uso del Negocio.png]]

## Reglas de Negocio

Los casos de uso de negocio nos permiten especificar las **reglas de negocio** existentes, que definen qué, cómo, cuándo, y porqué debe hacerse algo en una empresa. También pueden haber:

1. **Reglas de Restricción**: son condiciones a cumplir para ejecutar el proceso deseado. Pueden ser:
	- **De operaciones**: pueden ser de flujo o de estímulo-respuesta.
	- **De estructura**: pueden ser de dominio de datos (tipos y valores válidos) o de relación.
2. **Reglas de Derivación**: pueden ser:
	- **De inferencia**: establecen un hecho que se deriva de otro hecho.
	- **De cálculo**: establecen cómo se calcula un descuento, promedio, precio, etc.
