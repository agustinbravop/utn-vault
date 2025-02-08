**High-Level Data Link Control** (HDLC) es un [[Protocolo]] punto a punto de [[Capa de Enlace]]. 

Define 3 tipos de estaciones, 2 configuraciones del enlace, y 3 modos de operación. 

Se usaba antes para *topologías centralizadas* (arquitecturas maestro/esclavo). Cumplía con todas las funciones de la capa de enlace, lo que lo hace un protocolo pesado: uno no siempre necesita todos los campos de control que HDLC define.

Eventualmente surgieron protocolos hijos que solo utilizan ciertas partes de HDLC:

- **LAPB**: no ofrece direccionamiento para así ahorrar bits de control en la trama.
- **SLIP**: solo ofrece [[Entramado]]. Sirve para redes de internet en los hogares.
