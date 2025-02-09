*Integrated Services* - ISA (IntServ) funciona junto al [[Protocolo]] RSVP para ofrecer [[Calidad de Servicio]] en la red. El usuario **solicita de antemano los recursos que necesita**, lo cual define un **flujo**.

| Servicio         | Características                                | Equivalencia en [[ATM]] |
| ---------------- | ---------------------------------------------- | ----------------------- |
| Garantizado      | Garantiza un caudal mínimo y un retardo máximo | CBR, VBR -rt            |
| Carga controlada | Bajo retardo pero sin garantías                | VBR -nrt                |
| Best effort      | Ninguna garantía                               | UBR, ABR                |

![[IntServ.png]]

Cada paquete se encola y procesa según su clase.

RSVP es un protocolo de señalización que arma un circuito virtual para que el receptor reserve los recursos de la sesión. El problema es la escalabilidad.
