Un **proceso** es un programa en ejecución sobre un [[Sistema Operativo]]. Sus elementos típicos son:

- **Datos**.
- **Instrucciones**.
- **Pila** del sistema.
- **Bloque de control del proceso**.

Un proceso puede ser de:

- **Kernel**: corre en modo sistema o privilegiado. Son rutinas del SO.
- **Usuario**: corre en modo usuario.

## Bloque de Control de Proceso

El **BCP** es una estructura de datos que manifiesta la existencia de un proceso. Se almacena en la memoria del sistema operativo. Almacena:

- El identificador del proceso.
- La información del estado del CPU.
- La información de control del proceso (privilegios, propiedad de recursos, etc).

Se utiliza un modelo de 7 estados para los estados de un proceso. Si el proceso está *suspendido*, se encuentra en memoria secundaria (serializado al disco). Si está en *ready*, *running*, o *blocked*, entonces está en memoria principal.

![[Modelo de 7 Estados de un Proceso.png]]

Cuando pasa de *running* a *blocked*, sucede un **cambio de contexto** en el cual se debe salvar el estado de la CPU.
