La suma en la [[Arquitectura ABACUS]] tiene 4 fases:

1. Buscar instrucción: $(P) \to S \ ; \ ((S)) \to M$.
2. Buscar operando: $(M) \to I \ ; \ (D) \to S \ ; \ ((S)) \to M$.
3. Operación suma: $(AC) + (M) \to AC$.
4. Preparar siguiente instrucción: $(P) + 1 \to P \ ; \ (P) \to S$.

Cada paso activa ciertas [[Señales de Gobierno]].

| Paso                | Señales de Gobierno              | Explicación                                                                                                    |
| ------------------- | -------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| $(P) \to S$         | $SRP, \ \vec{ENS}$               | Escribir el contenido de P en S.                                                                               |
| $((S)) \to M$       | $\vec{ICM}, \ \vec{PACM}, \ LEC$ | S tiene una dirección de memoria. El contenido del contenido de S es el contenido de esa dirección de memoria. |
| $(M) \to I$         | $SRM, \ \vec{ENI}$               | Escribir el contenido de M en I.                                                                               |
| $(D) \to S$         | $SRD, \ \vec{ENS}$               | Escribir el contenido de D en S.                                                                               |
| $((S)) \to M$       | $\vec{ICM}, \ \vec{PACM}, \ LEC$ | Buscar la dirección de S y copiar su contenido a M.                                                            |
| $(AC) + (M) \to AC$ | $SRM, \ ENA, \ SUM, \ \vec{EAC}$ | Sumar ese contenido al contenido del AC.                                                                       |
| $(P) + 1 \to P$     | $\vec{INCP}$                     | Incrementar en uno el _instruction pointer_.                                                                   |
| $(P) \to S$         | $SRP, \ \vec{ENS}$               | Escribir dirección de la sig. instrucción en S.                                                                |
