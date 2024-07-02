Las **técnicas** de [[Evaluación de las Prestaciones]] son métodos y herramientas que permiten **obtener los índices de prestaciones de un sistema** que está ejecutando una [[Carga de Trabajo]] dada y con unos valores determinados de los **parámetros** del sistema.

Las técnicas se clasifican en tres tipos:

- [[Monitorización]].
- [[Modelado]].
- [[Benchmarking]].

## Modelado

Es una herramienta que se debe usar cuando se evalúa el comportamiento de un sistema con algún **elemento no instalado** (de software o hardware). La dificultad reside en la **obtención de datos** precisos para ejecutar un modelo y obtener resultados con un **grado de aproximación** aceptable. Se puede utilizar:

- **Técnicas de simulación**: para construir un programa que **reproduce el comportamiento** temporal del sistema, basándose en sus estados y transiciones. Son **caros** en tiempo de cálculo y esfuerzo de puesta a punto.
- **Técnicas analíticas**: **resolución mediante fórmulas** y algoritmos de ecuaciones matemáticas que representan un equilibro entre eventos del sistema. Son incapaces de tratar ciertos comportamientos y estructuras que existen en los SI. Son más **limitados**.

## _Benchmarking_

Es un método frecuente de comparar SIs frente a una **carga característica** de una instalación concreta. Es la medición del comportamiento sobre un **prototipo**, y las variantes de este método sirven para **evaluar la potencia relativa** de un sistema a lo largo de su ciclo de vida (compararse con versiones anteriores de sí mismo), **contrastar monitores** y **validar modelos**. Las dificultades son:

- ¿Cómo determinar esa carga característica? [[Caracterización de la Carga]].
- ¿Cómo valorar el aprovechamiento que hacen los programas de las peculiaridades de los distintos sistemas?
