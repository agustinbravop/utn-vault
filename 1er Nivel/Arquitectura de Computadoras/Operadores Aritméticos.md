Dentro del contexto de la [[Unidad Aritmético-Lógica]], un **operador elemental** es un componente lógico con entradas y salidas que permite realizar un cálculo sobre dos bits del mismo peso de dos cadenas de bits.

Los operadores cableados son más performantes, mientras que los operadores microprogramados son más baratos. La [[Arquitectura ABACUS]] cablea unas pocas operaciones básicas ([[Operadores Aritméticos de ABACUS]]) y desarrolla esquemas para implementar operaciones más complejas como la división, multiplicación o el manejo de números con [[Coma Flotante]].

## Clasificación

Según la operación:

- **En serie**: es más lento pero más barato. Para operaciones más complejas.
- **En paralelo**: es más rápido pero requiere más cableado. Para operaciones simples.

Según su naturaleza:

- **Combinacional**: realizan todos sus cálculos en un solo _clock_ de tiempo. Son rápidos pero grandes y caros.
- **[[Circuitos Secuenciales|Secuencial]]**: necesitan saber si usa el **AC** como entrada y/o como salida (puede ser una fuente y/o un destino). Son simples y baratos pero más lentos que los combinacionales.

## Indicadores

Los indicadores (_flags_) de un operador aritmético informan de distintos eventos que puedan haber ocurrido al ejecutar la operación. Sirven para detectar errores, hacer saltos condicionales, etc. Algunos son:

1. Última operación.
2. Error de desbordamiento.
3. Error de desborde de capacidad.
4. Error de división por cero.
5. Estado del acumulador positivo.
6. Estado del acumulador negativo.
7. Estado del acumulador igual a cero.
