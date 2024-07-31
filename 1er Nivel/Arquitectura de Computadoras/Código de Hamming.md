El [[Códigos Redundantes|código redundante]] de Hamming puede **detectar y corregir** errores de **un solo bit** (aunque se lo puede escalar). Se usa cuando hay una baja probabilidad de error.

Embebe $p$ bits de [[Paridad]] entre $i$ bits de información para formar un mensaje de $i + p = n$ bits, de manera que siempre se cumpla la relación $2^p \ge i + p + 1$. Así, tener $p$ bits de paridad nos permite transmitir hasta $2^p - p - 1 \ge i$ bits de información.

Por conveniencia, se ubican los bits de paridad en las posiciones del mensaje que son potencias de 2.

## Ejemplo

Información: $1 \ 0 \ 1 \ 0  \to 1 \ 0 \ 1 \ 0 \ 0 \ 1 \ 0$ (codificado).

| Posiciones | 7     | 6     | 5     | 4     | 3     | 2     | 1     |
| ---------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| Bits       | $i_3$ | $i_2$ | $i_1$ | $p_2$ | $i_0$ | $p_1$ | $p_0$ |
| Valores    | 1     | 0     | 1     | 0     | 0     | 1     | 0     |

Cada $p$ de paridad reduce a la mitad el conjunto de bits que puede tener el error. Con $p_0 \to \frac{7}{2} = 4$, con $p_1 \to \frac{4}{2} = 2$, finalmente con $p_2 \to \frac{2}{2} = 1$ logramos ubicar el bit con un valor erróneo.
