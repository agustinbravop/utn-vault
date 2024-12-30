> La mayor causa de fracaso es malas decisiones. - Brooks, 1975. _The Mythical Manmonth_

Estimar es hacer una estimación, **predicción** o **adivinación** de cuanto va a **durar** o **costar** un proyecto. Puede cambiar. Sí o sí una de las tres variables del triángulo de hierro debe ser verdaderamente variable y **poder cambiarse**.

Para **planificar** hay que **conocer**:

1. Qué vamos a hacer.
2. El tamaño.
3. El **tiempo ideal**: mínimo tiempo necesario para lograr el objetivo si todo sale bien.
4. El **tiempo real**: se le suma tiempo al ideal para considerar variables fuera de nuestro control.

## Métodos

Para estimar la **duración** y **costo** de un proyecto de desarrollo de software se pueden usar varios **métodos**, clasificados en dos ramas.

### Métodos Paramétricos

Asociados a la [[Teoría Clásica]], son **fórmulas** que requieren identificar **parámetros** para aplicarlos a **funciones matemáticas** para estimar los tiempos y costos de persona por hora. Se estima la cantidad de **líneas de código**, ajustable por lenguaje.

1. _Cocomo 2_: estimar cantidad de líneas de código necesarias.
2. _Punto función_: estimar cantidad de funciones necesarias.
3. _Punto caso de uso_.

### Métodos Heurísticos

Basados en la **experiencia propia**, requieren confiar en la **opinión** de alguien.

1. _Juicio del experto_: confiamos en la opinión del experto de la empresa. El problema es que solo él tiene el conocimiento, y si no está o se va entonces no se puede estimar.
2. _Técnica de Delphi_: similar al experto pero con conocimiento compartido por un grupo. El problema es que sigo dependiendo de gente que no está en el equipo de desarrollo.
3. _Estimación por analogía_: se estima en base a un SW similar que haya desarrollado previamente. El problema es que no se puede definir esa similitud y además requiere que en el proyecto anterior se haya hecho el seguimiento de la planificación (poco común en la práctica).

## Estimación Ágil

La [[Agilidad]] propone que el **equipo de trabajo** se encargue de la [[Estimación]].

Se consideran dos **variables**:

- **Tamaño**: complejidad asociada a la funcionalidad.
- **Velocidad**: es la **capacidad de trabajo** del equipo.

Se usan herramientas como el [[Punto Historia]] para estimar las [[4to Nivel/Ingeniería y Calidad de Software/Historias de Usuario|Historias de Usuario]] en prácticas como la [[Planning Poker]]. A la larga un [[Equipo Ágil]] estabiliza su [[Velocidad]] por iteración, facilitando la estimación de qué pueden lograr en cada iteración.
