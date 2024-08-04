La microprogramación en una [[Arquitectura de Computadoras]] consiste en reemplazar el [[Secuenciador Central]] cableado por un **secuenciador programado**. A cada instrucción de la [[Computadora]] le corresponde un **micro-programa** almacenado en una **memoria de control**, cuya ejecución genera las [[Señales de Gobierno]] que gobiernan la ejecución de la instrucción.

Se llama **micro-instrucciones** a las instrucciones del micro-programa. Ejecutar una micro-instrucción genera micro-órdenes.

La microprogramación permite tener _ordenadores de código de instrucción variable_, es decir que es posible modificar fácilmente el conjunto de instrucciones de una computadora micro-programada. Abre un campo entre hardware y software denominado **_firmware_**.

Los fundamentos de la microprogramación se definieron en el [[Modelo de Wilkes]] en 1951.

## Codificación de las Micro-instrucciones

- **Por campos**: se dividen las micro-ordenes en grupos indepppendientes para que sea imposible que en cada grupo se den micro-órdenes simultáneas. Además, para la comodidad del programador, cada grupo corresponde a un tipo de función (apertura de puertas de [[Registros]] a [[Buses]], gobierno de una unidad funcional, etc). Genera micro-instrucciones largas pero ofrece una decodificación más directa.
- **Por tipo de instrucción**: se le da a la micro-instrucción una estructura similar a la de una instrucción, con código de operación y dirección de operando. Su decodificación es compleja pero logra una longitud pequeña.

## Direccionamiento de las Micro-instrucciones

- **Secuencial**: la próxima micro-instrucción es la de la dirección siguiente. Es simple y no alarga a la micro-instrucción. Requiere micro-instrucciones de salto.
- **Explícito**: similar al modelo de Wilkes, cada micro-instrucción tiene en sus bits de menor peso el formato `[A..][..I..][..B]` y se calcula la siguiente micro-instrucción de esta manera:
  - Si $I = 0 \implies$ siguiente micro-instrucción $= (A) + (B)$.
  - Si $I = 1 \implies$ siguiente micro-instrucción $= (A) + (C)$.

![[Direccionamiento de las Micro-instrucciones.png]]

## Acompasamiento de las Micro-instrucciones

- **Ritmo fijo**: se suele usar en microprogramación por campo.
- **Ritmo variable**: se suele usar en microprogramación por tipo de instrucción. Cada micro-instrucción define el ritmo que desea.

![[Acompasamiento de las Micro-instrucciones.png]]
