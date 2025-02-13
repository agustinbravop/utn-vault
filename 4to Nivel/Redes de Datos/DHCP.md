_Dynamic Host Configuration Protocol_ (DHCP) es un [[Protocolo]] que funciona sobre [[UDP]].

Es una extensión del protocolo BOOTP que da flexibilidad al administrar direcciones IP. Se usa para **configurar dinámicamente los parámetros** [[TCP]]/[[IP]] de una red.

Tiene dos elementos:

1. Un mecanismo para asignar direcciones IP y parámetros TCP/IP.
2. Un protocolo para negociar y transmitir información de host.

Funcionamiento de DHCP:

1. **Descubrimiento**: se envía un mensaje "Discover" buscando servidores DHCP disponibles.
2. **Oferta**: el servidor responde con una dirección IP disponible (y otros parámetros).
3. **Solicitud**: el dispositivo confirma una de las ofertas recibidas.
4. **Confirmación**: el servidor responde con un ACK, y reserva los recursos ofrecidos.
5. **Renovación**: para que el dispositivo siga reservando sus recursos.
6. **Liberación**: el dispositivo envía un "Release", para dejar de usar sus recursos.
