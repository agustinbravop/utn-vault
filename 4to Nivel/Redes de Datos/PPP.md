**Point-to-Point Protocol** (PPP) es un [[Protocolo]] para la [[Capa de Enlace]], estandarizado por la IETF RFC 1661, 1662, 1663.

Es completamente _multiprotocolo_ y _multienlace_. Busca reemplazar LAPB y SLIP (otros dos protocolos derivados de [[HDLC]]). Tiene dos subprotocolos:

- Link Control Protocol (LCP).
- Network Control Protocol (NCP).

Características:

- No hace ni [[Control de Flujo]] ni direccionamiento.
- Sirve para establecer el circuito entre el cliente y el proveedor.
- Ofrece autenticación y compresión.
- Es sincrónico/asincrónico.
- Utiliza "números mágicos" para detectar bucles en los enlaces.
