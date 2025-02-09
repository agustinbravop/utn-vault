Los **puertos** son una abstracción a nivel de [[Capa de Transporte]] de las conexiones lógicas de procesos con la red.

Se dividen en *clientes* y *servidores*. Son gestionados por el [[Sistema Operativo]]. Identifican unívocamente un proceso (de [[TCP]] o [[UDP]]) en una máquina (con interfaz [[IP]]).

Se asignan mediante *sockets*, identificados por la tupla $(p,\ IP_o,\ P_o,\ IP_d,\ P_d)$. Se clasifican en tres rangos de puertos:

1. 0-1023: Well-Known Ports.
2. 1023-49151: puertos registrados.
3. 49152-65535: puertos dinámicos o privados.
