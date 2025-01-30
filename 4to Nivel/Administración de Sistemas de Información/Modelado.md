El **modelado** es la técnica que se debe usar en la [[Evaluación de las Prestaciones]] cuando algún elemento (de HW o SW) del sistema **no está instalado**. El objetivo es **estimar el tiempo** que un trabajo tarda en ser procesado. La dificultad reside en la **obtención de datos** precisos para ejecutar un modelo y obtener resultados con un **grado de aproximación** aceptable.

En general, sus técnicas se fundamentan en la **teoría de colas**, que pueden ser individuales o formar redes abiertas o cerradas. Se dividen en dos grupos:

- **Técnicas de [[Simulación]]**: para construir un programa que **reproduce el comportamiento** temporal del sistema, basándose en sus estados y transiciones. Son **caros** en tiempo de cálculo y esfuerzo de puesta a punto.
- **Técnicas analíticas**: **resolución mediante fórmulas** y algoritmos de ecuaciones matemáticas que representan un equilibro entre eventos del sistema. Son más **limitados**, incapaces de tratar ciertos comportamientos y estructuras que existen en los SI.

Una técnica analítica es el [[Análisis Operacional]].
