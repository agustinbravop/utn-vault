El **acoplamiento**, considerado por primera vez en el [[Diseño Estructurado]], es una medida cualitativa del **grado de interdependencia** entre los módulos de un sistema. Se ve influenciado por:

1. **Tipo de conexión entre módulos**: módulos mínimamente conectados.
2. **Complejidad de la interfaz**: dada por la cantidad, accesibilidad y estructura de la información.
3. **Tipo de flujo de información**: determina si el acoplamiento es por datos o por control.
4. **Tiempo de ligado**: al programar, compilar, linkear, o ejecutar.

El _acoplamiento por entorno común_ se da cuando dos o más módulos acceden a un entorno de datos público, por ejemplo una variable global.

El _desacoplamiento_ se puede lograr de varias maneras:

- Rompiendo dependencias.
- Localizando variables.
- Usando conexiones normales.
- Usando buffers para elementos comunicados.

Siempre se busca desarrollar sistemas con **bajo acoplamiento** y alta [[Cohesión]]:

![[Acoplamiento y Cohesión.png]]
