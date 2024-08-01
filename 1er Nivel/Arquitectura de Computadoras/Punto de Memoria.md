El **punto de memoria** es el **soporte físico** que permite almacenar un bit de información. Hay varios tipos:

1. **RAM**: Random Access Memory. Lectura y escritura **volátil**. Borra y escribe eléctricamente por palabra.
2. **ROM**: Read Only Memory. **Solo lectura**. Se escribe mediante máscaras a **nivel físico**. No borra.
3. **PROM**: Programmable ROM. Solo lectura. Se escribe **eléctricamente**. No borra.
4. **EEPROM**: Erasable PROM. Principalmente de lectura. Se puede borrar el **chip entero** mediante luz ultravioleta.
5. **EEPROM**: Electrically Erasable PROM. Principalmente de lectura. Se puede borrar eléctricamente **por bloques**.
6. **Flash**: Principalmente de lectura. Se puede borrar eléctricamente **por palabras**. Ejemplo: USB, MicroSD.

## Ram Estática

Las posiciones en la memoria se escriben o leen en cualquier orden (*random access*). Cada bit en una SRAM se almacena en 4 transistores que forman 1 [[Biestables|biestable]]. Otros 2 transistores más controlan el acceso.

![[SRAM.png]]

Utiliza 6 MOSFETs para almacenar un bit de información. $WL$ es un bus de control que controla el acceso (y usa los transistores $M_5$ y $M_6$). Los 4 transistores $M_1$-$M_4$ forman un biestable. Es veloz pero también caro, grande, y consume mucha velocidad.

## RAM Dinámica

Se desarrolló en IBM y usa solo un condensador y un transistor. Se estructuran los puntos en una matriz. Las columnas se **pre-cargan** a un voltaje igual a la mitad del voltaje que representa el 1 lógico. Una fila se energiza por medio del decodificador de filas. Esto requiere constantes ciclos de regeneración para mantener esa pre-carga.

![[DRAM.png]]

Una DRAM es más barata y pequeña que una SRAM, pero también es menos veloz.
