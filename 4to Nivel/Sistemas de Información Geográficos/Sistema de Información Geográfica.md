Un [[4to Nivel/Administración de Sistemas de Información/Sistemas de Información|Sistema de Información]] **geográfica** (SIG) es una **integración organizada** de HW, SW, y datos geográficos, diseñada para tratar información geográficamente referenciada para resolver problemas complejos de **planificación y gestión**.

En el sentido más genérico, son herramientas que permiten analizar [[Información Geográfica]], editar mapas, y presentar los resultados.

![[Sistema de Información Geográfica.png]]

Un SIG debe poder responder:

1. Dónde está el objeto $A$?
2. ¿Dónde está $A$ con relación a $B$?
3. ¿Cuántas ocurrencias de $A$ hay en una distancia $D$ de $B$?
4. ¿Cuál es la dimensión de $B$?
5. ¿Camino más corto entre $P$ y $Q$?
6. Etc...

Las tres funcionalidades principales son:

1. **Consulta**: responder preguntas.
2. **Análisis**: buscar patrones y tendencias. Elaborar escenarios potenciales.
3. **Representación**: visualizar la información.

Un SIG es un modelo informatizado del mundo real, descrito en un sistema de referencia ligado a la Tierra, establecido para satisfacer unas necesidades de información específicas.

El esquema clásico define 5 componentes:

![[Esquema Clásico de un SIG.png]]

El HW incluye una serie de periféricos para tareas concretas, como GPS o tabletas digitalizadoras. Los datos son lo más importante, difícil, y caro de obtener: o se relevan, o se compran. Los métodos definen reglas de implementación y reglas de negocio.

Olaya redefine los componentes, proponiendo una evolución del esquema clásico:

1. **Datos**.
2. **Análisis**.
3. **Visualización**.
4. **Factor organizativo**.
5. **Tecnología** (SW y HW).

## Áreas de Aplicación

Los SIG son adaptables a distintos entornos. Cada situación prioriza una u otra capacidad del SIG, según sus necesidades particulares.

Factores de clasificación:

1. Procesos de interés.
2. Tipo de datos.
3. Volumen de variables y datos.
4. Precisión de trabajo necesaria.
5. Tipo de usuarios esperados.
6. Complejidad de las operaciones.
7. Medida en que los SIG responden a necesidades existentes.

Así se puede definir grupos comunes de actividad existentes en torno al SIG, así como el papel que el SIG juega en esa disciplina.

Papeles que el SIG desempeña:

1. Herramienta modelizadora.
2. Herramienta para la toma de decisiones.
3. Herramienta para difusión de información geográfica.
4. Herramienta centralizadora ([[Bases de Datos Espaciales]]).

Áreas de aplicación:

5. **Gestión de recursos naturales**: son los SIG más antiguos. Hacen análisis y gestión de datos.
6. **Gestión de riesgos**: para usuarios avanzados.
7. **Ecología**: conocer el estado y comportamiento de poblaciones.
8. **Negocios y marketing**: para el análisis de mercado.
9. **Ciencias sociales**: requieren un gran componente espacial.
10. **Planificación**: el SIG sirve para la toma de decisiones, ofreciendo una visión global.
11. **Militar**: las fuerzas armadas usan SIG hace mucho. Los ejércitos son creadores de cartografía.

## Revisión Histórica

En la historia de los SIG confluyen dos factores que se retroalimentan:

```mermaid
flowchart LR;
1[Necesidad de información geográfica] ---> 2[Aparición de las primeras computadoras]
2 ---> 1
```

12. **1854**: se da una epidemia en Soho, Londres. John Snow mapea las víctimas y relaciona sus ubicaciones con las ubicaciones de las bombas de agua de la ciudad.
13. **1964**: Canadá desarrolla el primer SIG. Lo importante es la codificación y almacenamiento de la información geográfica.
14. **1967**: DIME es un primer intento de resolución de los problemas que el CGIS de Canadá tenía.
15. **1968**: aparece el programa SYMAP para realizar cartografía computacional. Permitía la entrada de información vectorial.
16. **1969**: se desarrolla GRID en la Universidad de Harvard con datos raster (imágenes).
17. **1970s**: más investigación y desarrollo pero sin uso masivo.

![[Revisión Histórica de los SIG.png]]

Evolución de:

- Los SIG como **disciplina**: surgieron de los cartógrafos.
- La **tecnología**: del HW y SW.
- Los **datos**: su generación y almacenamiento.
- Las **técnicas y formulaciones**: nuevos enfoques y conceptos.

Tendencias actuales:

- Los SIG pasan de ser sistemas completos a ser _plataformas adaptables_.
- Se convierten en herramientas base para las disciplinas beneficiarias.
- Pasan a ser elementos de consumo diario con _presencia social_.
- Han pasado de un concepto a una _ciencia_.
