En este taller de integración, se configura un esquema global de conectividad que involucra a los protocolos [[BGPv4]], [[RIP]], [[OSPF]], y servidores [[DNS]], [[DHCP]], y web. El objetivo es explorar cómo configurar estos protocolos y servicios en una red conectada a internet.

![[Esquema Global de Conectividad.png]]

1. **Tier 1**: proveedor global de nivel superior.
2. **Tier 2**: proveedor regional/nacional de nivel intermedio.
3. **Tier 3**: proveedor local/regional de nivel inferior.

Cada [[Enrutadores|router]] de este esquema se **configura** por consola de comandos. Primero se configuran las direcciones de todas las interfaces de los routers.

Luego, se deben activar los protocolos de ruteo según el contexto de cada router. En los tier  1, tier 2, y tier 3, se configura BGP.

Se configura OSPF en el lado derecho de la imagen, y se configura RIP en el lado izquierdo de la imagen.

Los dos tier 3 de esta topología son *routers de frontera* que se encargan de redistribuir las rutas para compartir información de enrutamiento entre protocolos (o dominios) de enrutamiento diferentes.

Luego se configuran los servidores DHCP, DNS, y web.

Finalmente, para validar que hay **conectividad**, se puede usar el comando `ping` desde un router apuntando a las direcciones IP de otros routers. Repetir esto en varios routers da mayor seguridad.
