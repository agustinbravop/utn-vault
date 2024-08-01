A medida que aumenta el **costo** del [[Punto de Memoria]], se reduce el **tiempo de acceso** pero también se pierde **capacidad de almacenamiento**.

La CPU consulta primero al caché y luego a la RAM, pero no a otro nivel. Los caché se dividen en:

1. L1: pegados al núcleo específico.
2. L2: soporta al L1. Hay uno por cada núcleo.
3. L3: soporta al L2. Es compartido entre núcleos.

![[Jerarquía de Memorias.png]]

| Nivel | Memoria                 |
| ----- | ----------------------- |
| 0     | [[Registros]] de la CPU |
| 1     | Cache (SRam)            |
| 2     | Memoria principal (RAM) |
| 3     | Memoria Flash           |
| 4     | SSD/HDD/USB             |
| 5     | Discos ópticos          |
| 6     | Cintas magnéticas       |
