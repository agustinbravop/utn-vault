Los números pseudoaleatorios nos permiten generar valores de [[Variables Aleatorias]] de manera **determinística**, lo que resulta útil en una [[Simulación]].

Dado un conjunto de números aleatorios generados determinísticamente, se los debe validar con un conjunto de [[Pruebas Estadísticas para Números Aleatorios]] para comprobar que cumplan con las características de los números aleatorios.

Características de los números pseudoaleatorios:

1. Están **uniformemente distribuidos** (evitar _weighted dice_).
2. Ser **estadísticamente independientes** (que uno no dependa del otro).
3. Ser **reproducibles**.
4. A efectos prácticos para su uso (aunque son problemas antiguos ya solucionados):
   - Tener un período largo sin repetición.
   - Ser generados por un método largo.
   - Que no requieran mucho almacenamiento.

## Métodos de Generación

Hay muchas maneras de obtener números pseudoaleatorios: listados, métodos físicos, con computadoras, con relaciones de recurrencia, etc.

Hoy en día, los números pseudoaleatorios son fáciles de generar automáticamente por computadora, por lo que su generación es trivial.

Los métodos de generación no garantizan que los números generados cumplan todos los requisitos de un número aleatorio, por lo que es importante probarlos estadísticamente.

### Método Congruencial Mixto

Se plantea la _relación de recurrencia_:

$$X_{n+1} = (AX_n+c) \mod m$$

Con estos _parámetros_:

- $X_0 \gt 0$: semilla.
- $a \gt 0$: multiplicador.
- $c \gt 0$: constante aditiva.
- $m \gt x_0, m \gt a, m \gt c$: módulo.

### Método Congruencial Multiplicativo

Se plantea una relación de recurrencia más simple:

$$X_{n+1} = aX_n \mod m$$

Ejemplo:, siendo $X_{n+1} = 3X_n \mod 100 \ \land \ X_0 = 17$:

| $n$ | $X_n$ |
| --- | ----- |
| 1   | 51    |
| 2   | 53    |
| 3   | 59    |
| 4   | 77    |
| 5   | 31    |
