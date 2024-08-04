Con 4 bits se puede representar $2^4 = 16$ números, osea un dígito hexadecimal, utilizando el código **_binary coded decimal_**. Hay varias versiones:

1. **Natural**: pesos 8421.
2. **Exceso 3**: cada número tiene un 3 sumado.
3. **Aiken**: pesos 2421 para una simetría entre 4 y 5, 3 y 6, 0 y 9, etc.
4. **5421**.
5. **Gray**: en cada salto cambia un solo bit, tiene un patrón cíclico al incrementar de a uno.

| Decimal | BCD natural | BCD exceso 3 | BCD Aiken | BCD 5421 | BCD Gray |
| ------- | ----------- | ------------ | --------- | -------- | -------- |
| 0       | 0000        | 0011         | 0000      | 0000     | 0000     |
| 1       | 0001        | 0100         | 0001      | 0001     | 0001     |
| 2       | 0010        | 0101         | 0010      | 0010     | 0011     |
| 3       | 0011        | 0110         | 0011      | 0011     | 0010     |
| 4       | 0100        | 0111         | 0100      | 0100     | 0110     |
| 5       | 0101        | 1000         | 1011      | 1000     | 0111     |
| 6       | 0110        | 1001         | 1100      | 1001     | 0101     |
| 7       | 0111        | 1010         | 1101      | 1010     | 0100     |
| 8       | 1000        | 1011         | 1110      | 1011     | 1100     |
| 9       | 1001        | 1100         | 1111      | 1100     | 1101     |
