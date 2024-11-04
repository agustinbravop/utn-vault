Un conjunto de [[Proceso|procesos]] está en estado de **interbloqueo** o **deadlock** cuando todos los procesos están esperando un evento que solo puede ser causado por otro proceso del conjunto.

![[Interbloqueos 2024-11-03 18.03.38.excalidraw.svg]]

Un deadlock **deteriora el funcionamiento** del [[Sistema Operativo]]. El problema es de naturaleza lógica y no tiene una solución eficiente. Existen [[Estrategias para los Interbloqueos]].

Para usar un recurso, los procesos deben **solicitar, usar, y liberar** el recurso. La solicitud y la liberación se realizan mediante [[Llamadas al Sistema]].

**Condiciones necesarias** (de Coffman) para un deadlock:

1. Exclusión mutua.
2. Retener y esperar.
3. Sin expropiación.
4. Espera circular.
