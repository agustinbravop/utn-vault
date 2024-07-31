Un **biestable** o *flip-flop* es un [[Circuitos Digitales|sistema lógico]] que permite mantener **dos estados estables**, son elementos de memoria capaces de **almacenar un bit** de información. Las entradas son impulsionales pero las salidas son niveles lógicos (siempre accesibles excepto durante los momentos de transición).

Fundamentalmente está constituido por dos circuitos NOT montados en oposición.

![[Principio de los Biestables.png]]

## Flip-Flop Set-Reset

Si $R = S = 0 \implies Q$ no cambia. Si $S = 1 \implies Q = 1$. Si $R = 1 \implies Q = 0$. Desde el diseño $R = S = 1$ es indeterminado.

![[Set-Reset.png]]

Tabla de verdad:

| R   | S   | Q(t) | Q(t+1) |
| --- | --- | ---- | ------ |
| 0   | 0   | 0    | 0      |
| 0   | 0   | 1    | 1      |
| 0   | 1   | 0    | 1      |
| 0   | 1   | 1    | 1      |
| 1   | 0   | 0    | 0      |
| 1   | 0   | 1    | 0      |
| 1   | 1   | 0    | ?      |
| 1   | 1   | 1    | ?      |

### Set-Reset Sincrónico

Se agrega una entrada $CK$ al circuito RS para que solo se pueda actuar sobre el estado del circuito cuando hay un pulso o señal de sincronismo. Si no hay un impulso clock no puede haber un impulso $S$ o $R$, y podemos considerar que la señal de $S$ dura lo mismo que el intervalo del clock.

## Flip-Flop JK

![[Flip-Flop JK.png]]

Es similar al RS pero define una funcionalidad para $J = K = 1$, que en lugar de indeterminado da el **complemento** del estado anterior. Esto requiere colocar dos compuertas AND en frente de un biestable RS (lo cual de todas maneras es necesario si el RS es sincrónico).

## Flip-Flop D

La entrada $D$ siempre sobre escribe su valor sin importar el estado previo. $Q_{siguiente} = D$. Es una versión de una sola entrada del RS.

![[Flip-Flop D.png]]

## Flip-Flop T

La entrada $T$ (*toggle*) **conmuta** el estado. $Q_{siguiente} = Q \oplus T$. Si $T = 0 \implies Q$ se mantiene. Si $T = 1 \implies Q$ se complementa. Es una versión de una sola entrada del JK.

![[Flip-Flop T.png]]
