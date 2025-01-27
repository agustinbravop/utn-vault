*Unified Modelling Language* (UML) es un lenguaje de de [[Modelado de los Sistemas|modelado]] para **visualizar**, **especificar**, **construir**, y **documentar**, artefactos de un software.

![[UML 2025-01-24 19.54.00.excalidraw.svg]]

Como lenguaje, tiene una sintaxis y semántica particular. Es flexible y aplicable en distintos métodos, dominios, procesos.

En UML, un **modelo** es la representación en algún medio que captura los aspectos importantes (abstracción) de un sistema. Dependiendo del punto de vista que se tenga, se modela de una u otra manera.

Una **vista** es un subconjunto de construcciones de modelado que se enfocan en un aspecto particular del sistema. 

En UML, se clasifican las vistas en 4 **áreas**:

1. **Estructural**: describe elementos del sistema y sus relaciones. Vistas:
	- **Estática**: modelo incremental que captura la estructura de los objetos. [[Diagrama de Clases]].
	- **Diseño**: incorporada en UML 2.0, es más próxima a la implementación que las demás, y descompone al sistema en unidades modulares. [[Diagrama de Estructura Compuesta]], [[Diagrama de Componentes]], y [[Diagrama de Colaboración]].
	- **Casos de Uso**: captura los requerimientos funcionales del sistema, y describe cómo usar el sistema desde el exterior. [[Diagrama de Casos de Uso]].
2. **Comportamiento Dinámico**: funcionamiento del sistema a través del tiempo. Vistas:
	- **Interacción**: muestra el intercambio de mensajes entre objetos (colaboraciones) para lograr un objetivo dado. [[Diagrama de Secuencia]] y [[Diagrama de Comunicación]].
	- **Máquina de Estados**: se modelan objetos con comportamiento estado-dependiente, representando el ciclo de vida de cada clase. [[Diagrama de Máquina de Estado]].
	- **Actividades**: variante de la máquina de estados para modelar flujos de trabajo. Es similar a un diagrama de flujo o *flowchart*. [[Diagrama de Actividad]].
3. **Física**: recursos computacionales del sistema y los artefactos desplegados en ellos. Vistas:
	- **Despliegue**: surge en UML 2.0, reemplazando las vistas físicas de UML 1.x. [[Diagrama de Despliegue]].
4. **Gestión del Modelo**: ayuda a organizar el resto de modelos con paquetes. Vistas:
	- **Gestión del Modelo**: divide al sistema en unidades más pequeñas para facilitar su gestión. [[Diagrama de Paquetes]].
