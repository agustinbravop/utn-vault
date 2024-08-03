Cuando no es posible guardar toda la transferencia de información en una zona contigua de memoria, se la particiona en varias zonas que apuntan a la siguiente. El encadenamiento de datos consiste en efectuar esta operación de carga bajo control del [[Canales|canal]] sin tener que implicar a la unidad central.

![[Encadenamiento de Datos.png]]

Para lograr esto se debe agregar información extra en un registro doble:

- $DEC$: dirección de la siguiente zona de palabras transferidas.
- $CDP$: cantidad de palabras de la zona.
- $IT$: bandera de interrupción.
- $ED$: bandera de encadenamiento.
