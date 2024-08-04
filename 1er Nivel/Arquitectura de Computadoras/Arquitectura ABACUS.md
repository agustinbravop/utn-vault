ABACUS es una [[Arquitectura de Computadoras]] simple y con propósitos educativos propuesta por Meinadier. Es una máquina sincrónica con 3 unidades y 2 [[Buses]].

Unidades:

- [[Unidad Aritmético-Lógica]].
- [[Unidad de Control]].
- [[Unidad de Memoria]].

![[Esquema General de ABACUS.png]]

- **Bus M**: de instrucciones y operandos (datos).
- **Bus S**: de direcciones de memoria de los operandos.
- **AC**: acumulador temporal de la UAL.
- **P**: [[Registros|registro]] que almacena la dirección de la próxima instrucción (es el _instruction pointer_).
- **I**: registro de instrucción subdividido en CO (código operación) y D (dato u operando).
- **M**: registro con el contenido leído de la ubicación de memoria accedida.
- **S**: registro para buscar una ubicación en la memoria.

Sus partes se activan según las [[Señales de Gobierno]] activadas en cada momento.
