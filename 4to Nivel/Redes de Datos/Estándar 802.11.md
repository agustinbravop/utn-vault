El **estándar 802.11** para redes inalámbricas opera en la capa física y en la [[Capa de Enlace]]. Es un [[Protocolo]] que aplica los mecanismos estudiados.

Modos básicos de operación:

1. **Ad-Hoc**: no se asocia a ningún *access point*.
2. **Infraestructura**: hay un access point que gestiona.
3. **Bridge**: extiende los servicios, funcionando como una especie de [[Puentes de Red|puente de red]].

**Las WLAN son una extensión de la red LAN cableada**, aunque pueden también ser un sustituto completo.

La configuración típica involucra varias estaciones y una base:

![[Estándar 802.11.png]]

Tipos de tramas:

1. **Datos**: tienen información del usuario.
2. **Control**: RTS, CTS, y ACK, necesarias para controlar el acceso al medio.
3. **Administración**: no se envían a capas superiores.

En la capa física, el estándar 802.11 define método de transmisión y sus frecuencias y velocidad asociadas. En la capa de enlace:

- La [[Subcapa de Control de Acceso al Medio]] implementa CSMA/CA basado en [[MACA y MACAW]].
- La subcapa LLC funciona igual a lo ya visto.

En modo Ad-Hoc, se usa DCF para que las estaciones coordinen entre sí usando un *Network Allocation Vector* (NAV). Dado que no se puede censar la tensión del cable, se hace un "censado virtual" del canal, basado en temporizadores y señales para evitar colisiones.

En modo infraestructura, implementa control PCF.

Servicios de un access point (AP) o base:

1. Asociación.
2. Desasociación.
3. Re-asociación.
4. Distribución.
5. Integración.

Servicios de una estación:

1. Autenticación.
2. De-autenticación.
3. Privacidad.
4. Transferencia de datos.
