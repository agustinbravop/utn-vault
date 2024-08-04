La representación de números con coma flotante sacrifica precisión para poder representar un mayor rango de valores numéricos. Surge de la notación científica $S * M * base ^E$, donde:

- **Signo** (S): positivo o negativo.
- **Mantisa** ($M$).
- **Exponente** ($E$): representa la ubicación de la coma.

El [[Registros|registro]] se configura como `[S][E...][M...]` de manera que el signo es el bit de mayor peso, similar a las representaciones de los [[Números Binarios con Signo]].

## Cálculos entre Números de Coma Flotante

Se dice que un número en coma flotante está **normalizado** si el valor del signo es opuesto al valor del bit de mayor peso de la mantisa. Un número normalizado puede usarse en cálculos con números representados mediante coma flotante.

Para realizar cálculos entre dos números de coma flotante $A$ y $B$:

1. **Alinear mantisas**: $A$ y $B$ deben tener el mismo exponente, es decir tener la coma en el mismo lugar. Sea $E_A \lt E_B \implies$ se incrementa $E_A$ en uno y se desplaza $M_A$ uno a la derecha hasta que $E_A = E_B$. Ídem para $E_A \gt E_B$.
2. **Ajustar signos**: si la operación es $M_A - M_B \land M_A < M_B \implies$ hacer la operación $M_B - M_A = R$ (al revés) y luego complementar el signo de $R$. Esto asegura que la resta da positivo y luego se complementa el signo del resultado.
3. **Normalizar resultado**: el resultando puede no estar normalizado si hubo:
   - **Suma y desbordamiento** $\implies$ DESD $M \land E++$ una sola vez. Hace que $S = 1$.
   - **Resta y ceros a la izquierda** $\implies$ DESI $M \land E--$ hasta que el bit de mayor peso de $M$ sea 1. Esto solo sucede cuando $M_A > M_B$ y por ende $S = 0$.
