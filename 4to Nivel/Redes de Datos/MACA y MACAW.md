En la [[Subcapa de Control de Acceso al Medio]] (capa MAC), surgen complicaciones cuando no todas las estaciones están al alcance de las demás. Esto no nos permite usar ni CSMA ni CDMA. Hay dos problemas:

- **Problema del nodo oculto**: $A$ cree que el canal está libre porque no oye a $B$ usándolo.
- **Problema del nodo expuesto**: $A$ cree que el canal está ocupado, pero $B$ no interferiría.

## MACA

Multiple Access Collision Avoidance (de 1990). Usa y ajusta temporizadores.

Hay dos operaciones importantes para resolver problemas: Request to Send (RTS) y Clear to Send (CTS). 

![[Protocolos Inalámbricos.png]]

### MACAW

MACA Wireless (MACAW, de 1994) agrega un acuse de recibo (ACK) y agrega información de control que mejora el rendimiento.
