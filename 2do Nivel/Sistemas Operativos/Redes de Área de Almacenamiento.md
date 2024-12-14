Una **SAN** (Storage Area Network) es una red privada que utiliza **protocolos de almacenamiento** en lugar de protocolos de red (a diferencia del [[Almacenamiento Conectado a la Red]]). Se encarga de conectar los servers con los storage.

Una SAN permite flexibilidad y **escalabilidad** sin perder velocidad o control, pero las implementaciones son de software propietario, por lo que gestionar la red se vuelve costoso.

## RAID

Un **Redundant Array of Independent Disks** es un conjunto de discos que trabajan juntos en un sistema. Para el [[Sistema Operativo]] un RAID es un solo disco. Se clasifican en varios niveles, que se pueden combinar:

0. Distribución de bandas a nivel bloque sin redundancia (*stripping*). Esto mejora la **velocidad**.
1. Mirroring ofrece redundancia que mejora la **confiabilidad**.
2. Código de corrección de errores mediante paridad.
3. Paridad con entrelazado de bits.
4. Paridad con entrelazado de bloques.
5. Paridad distribuida con entrelazado de bloques.
6. Información de redundancia para protegerse del fallo de 2 discos. Esto ya es **muy robusto**.
