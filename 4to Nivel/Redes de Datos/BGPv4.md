*Border Gateway Protocol v4* (BGPv4) es un [[Protocolo]] para el [[Ruteo Externo]] que permite la comunicación entre [[Autonomous Systems]].

![[BGPv4.png]]

Se propaga **información de accesibilidad** (políticas) en lugar de costos (métricas). No se usan los mecanismos de [[Enrutadores#Ruteo Dinámico por Vector Distancia|Vector Distancia]] ni [[Enrutadores#Ruteo Dinámico por Estado de Enlace|Estado de Enlace]]: se usa **Vector Camino**, que es un *coloreado* de rutas accesibles. 

Se basa en la **accesibilidad administrativa**: el tránsito entre ASs es electivo, por lo que hay tráfico permitido y tráfico prohibido.

BGPv4 define una sola ruta para cada prefijo que aprende. Si un paso de la ruta se cae, se pierde la conectividad. Existen sitios online con información sobre el estado de BGP.

BGPv4 usa el puerto 179 de [[TCP]], y también tiene soporte de CIDR ([[Subnetting]]).

Mensajes de BGPv4:

1. `OPEN`: iniciar sesión.
2. `UPDATE`: actualización (anunciar o eliminar rutas).
3. `NOTIFICACION`: errores. Sirven para cerrar la sesión BGP y la conexión TCP.
4. `KEEPALIVE`: mantener la conexión. Sirve como respuesta a un `OPEN`.

Encabezado común a todos los mensajes:

![[Encabezado BGPv4.png]]

El campo *marker* es un valor acordado por ambos lados para marcar el inicio de un mensaje. El campo *length* está medido en bytes.

En el siguiente ejemplo, vemos cómo se debe considerar la **información desde la perspectiva del receptor**:

![[Información desde la Perspectiva del Receptor en BGPv4.png]]

El router $R_2$ corre el protocolo BGP y reporta información desde la perspectiva de la persona ajena, no desde su propia tabla. $R_2$ le habla a BGP en nombre del AS. Informa la accesibilidad a las redes desde una **perspectiva exterior**.

Como BGP solo propaga información de accesibilidad, un receptor puede implementar restricciones administrativas pero no puede seleccionar una ruta de menor costo, dado que no se comunican métricas.

Un emisor solo anuncia los caminos que debe seguir el tráfico. 

Restricciones de BGP:

- No soporta rutas múltiples.
- No soporta balanceo de cargas.
- No garantiza consistencia global (los AS deben acordar un esquema consistente).

Un *router arbiter* es una base de datos depurada, autenticada, y replicada, de información de accesibilidad para incrementar la consistencia global de BGP. Previene la propagación de información incorrecta por el backbone global. Mantiene información positiva y negativa de rutas.

Los **pares** proveen tránsito entre sus clientes, pero no proveen tránsito entre pares. En el siguiente ejemplo, el peer 1 no puede comunicarse directamente con el peer 3.

![[Relación entre Pares BGPv4.png]]

**Estructura de la internet global**:

1. **Tier 1**: vende tráfico pero no lo compra.
2. **Tier 2**: compra tráfico del Tier 1 y lo vende.
3. **Tier 3**: compra pero no vende mucho tráfico BGP. Son ISPs, data centers, etc.

![[Estructura de la Internet Global.png]]
