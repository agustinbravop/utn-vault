Los sistemas transaccionales son [[Sistemas de Referencia]] en los cuales los usuarios acceden desde terminales remotos para interactuar con un conjunto determinado de programas. Cada interacción es una **transacción**. La planificación no recibe ayuda humana externa, y cada usuario se siente **dueño absoluto** del sistema. Ejemplo: comprar por Mercado Libre, inscribirse a materias en el SYSACAD.

![[Pasted image 20240506002636.png]]

## Índices Característicos

Es definido por el flujo de transacciones que le llega:

- **Tiempo de respuesta**: es la suma de: - Tiempo de **reacción**: desde la petición hasta que comienza su ejecución. - Tiempo de **ejecución**: desde la ejecución hasta su finalización. - Tiempo de **retorno**: desde la finalización hasta que se le responde al usuario.
  $$\text{Tiempo de Respuesta} = \text{Reacción} + \text{Ejecución} + \text{Retorno}$$
