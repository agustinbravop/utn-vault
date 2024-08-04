La **UAL** o **ALU** (en inglés) es la encargada de ejecutar las instrucciones de cálculo en una [[Computadora]]. Para esto dispone de [[Operadores Aritméticos]] o unidades funcionales.

En ABACUS cada operación de la ALU, ejecutada por un operador, está gobernada por señales lógicas. El elemento de su ALU combina todos varios operadores aritméticos para ofrecer las siguientes operaciones que involucran al bus M y al registro acumulador:

1. **CAR**: carga del bus M al acumulador.
2. **CARC**: carga con complementación (complementa cada dígito y luego carga).
3. **SUM**: suma del contenido del bus M al AC.
4. **SUS**: sustracción.
5. **AND**: intersección lógica entre el contenido del bus M y el del AC.
6. **OR**: reunión lógica.
7. **ORX**: OR exclusivo.
8. **DESI**: desplazamiento a izquierda.
9. **DESD**: desplazamiento a derecha.

![[Elemento de la ALU.png]]

A esta ALU de ABACUS se le puede asociar los siguientes indicadores:

1. **DEB**: indicador de desbordamiento cableado en una suma (si se opera [[Números Binarios con Signo|en complemento a 2]]).
2. **S**: indicador de signo.
3. **CE**: indicador de cero.

El diseño de la ALU impacta en los ciclos de cálculo del computador, lo cual afecta la performance de la [[Arquitectura de Computadoras]].
