Los **General Responsibility Assignment Software Patterns** son un conjunto de 9 principios de alto nivel para el desarrollo de software, similares a los [[Principios SOLID]]. Fueron reunidos en el libro "Applying [[UML]] and Patterns" de Craig Larman, y están pensados para los [[Métodos Orientados a Objetos]].

1. **Alta [[Cohesión]]**: aumentar el nivel en el que los elementos de un módulo corresponden juntos. De peor a mejor, los niveles son: **casual $\rightarrow$ lógica $\rightarrow$ temporal $\rightarrow$ procedural $\rightarrow$ de información $\rightarrow$ secuencial $\rightarrow$ funcional**.
2. **Bajo [[Acoplamiento]]**: reducir el nivel de interdependencia entre módulos para facilitar el mantenimiento.
3. **Controlador**: intermediario entre la UI y la lógica de negocio para desacoplarlos. Intenta ser una abstracción liviana. MVC es una implementación de este patrón.
4. **Creador**: la clase `B` tiene la responsabilidad de crear una instancia de la clase `A` si es que `B` contiene a `A`, guarda a `A`, usa cercanamente a `A`, o tiene sus datos.
5. **Experto en Información**: la responsabilidad de instanciar un objeto cae en la clase que tiene los datos necesarios para instanciarlo.
6. **[[Polimorfismo]]**: usar polimorfismo para evitar la lógica condicional en base al tipo de un objeto o dato.
7. **Fabricación Pura**: introducir clases que no tienen correspondencia con el dominio (osea, solo existen en la solución), pero que mejoran el diseño del sistema.
8. **Indirección**: asignar a una clase intermedia la responsabilidad de mediar entre dos clases para limitar la propagación de cambios (romper dependencias).
9. **Variaciones Protegidas**: el principio fundamental de protegerse frente al cambio.

Los patrones GRASP son de alto nivel, y se solapan entre ellos y también con SOLID. No son exhaustivos, y conviene considerarlos más como buenas prácticas que como leyes obligatorias.
