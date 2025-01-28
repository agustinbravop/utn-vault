En la vista de diseño de [[UML]], un **diagrama de componentes** detalla las relaciones entre componentes del sistema.

Un _artefacto_ es la manifestación física (en código, hipertexto, etc) de un modelo. Un **componente** es una pieza modular que (en UML 2.0) se ha separado del concepto físico de _artefacto_, es decir que puede o no implementarse.

![[Diagrama de Componentes.png]]

Un _puerto_ es un punto de interacción con una interfaz bien definida. Cada puerto tiene un conjunto de interfaces provistas y/o requeridas. Se utilizan en clasificadores encapsulados, ya que permiten modificar la estructura interna de un clasificador sin afectar clientes externos que dependan de él.

Un puerto puede ser:

- **De comportamiento**: implementa comportamiento.
- **De delegación**: deriva a otro puerto interno.

No hay suposiciones sobre cómo implementar puertos. Pueden ser un objeto real o tan solo un concepto del modelado.

Un componente se expone solamente a través de interfaces, y solo requiere de interfaces (mediante sus _puertos_). Se busca que su implementación sea fácil de reemplazar.

La distinción entre clase estructurada ([[Diagrama de Estructura Compuesta]]) y componente es vaga.
