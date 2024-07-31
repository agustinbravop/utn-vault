Los caracteres de información se agrupan en una matriz. Para cada fila y columna se agrega y calcula un bit de [[Paridad]]. Luego se calcula un bit de paridad cruzada a partir de los bits de paridad agregados. La **paridad cruzada** permite detectar y corregir más de un error.

Una matriz de $n$ filas y $m$ columnas necesita $n + m + 1$ bits de control. Esto es **caro** porque consume más ancho de banda.

## Ejemplo

| 0   | 1   | 0   | 1   | *0* |
| --- | --- | --- | --- | --- |
| 1   | 1   | 0   | 0   | *0* |
| 0   | 0   | 0   | 1   | *1* |
| *1* | *0* | *0* | *0* | *0* |

$$3 * 4 = 12 \ \text{bits de información}. 
3 + 4 + 1 = 8 \ \text{bits de control}.$$

Por cada 20 bits enviados, solo 12 transmiten información.
