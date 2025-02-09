En el [[Estándar 802.11]], dado que el medio es **no guiado**, se necesita encriptar para tener confidencialidad.

Un primer intento fue **WEP**, que usaba el [[Seguridad y Criptografía#Cifrado Simétrico|cifrado simétrico]]. Su implementación defectuosa y esquema vulnerable hace que no se utilice más.

Nace el **estándar 802.11i** y el [[Protocolo]] **WPA**. En entornos no críticos se usa WPA, un compromiso entre WEP y la totalidad del estándar 802.11i.

WPA usa el protocolo **TKIP** (*Temporal Key Integrity Protocol*), variando la clave de cifrado con cada paquete de datos para mejorar el cifrado.

![[TKIP.png]]

WPA asegura la integridad de datos al usar un código de autenticación de mensajes (MIC) que previene la modificación o inyección de paquetes.

WPA2 es una versión mejorada que usa un protocolo CCMP (*Counter with CBC-MAC Mode Protocol*) para el cifrado, basado en [[Seguridad y Criptografía#Cifrado Simétrico|AES]] y por ende más robusto que TKIP, el cual está basado en RC4.

![[CCMP.png]]

WPA3, que surge en 2018, introduce SAE (*Simultaneous Authentication of Equals*) para una autenticación más segura. Requiere hardware más avanzado o moderno.

## WPA

Proceso general de conexión:

1. Negociación inicial.
2. Autenticación.
3. Intercambio de claves.
4. Cifrado de datos.
5. Protección contra ataques.

El **proceso de autenticación** en WPA con EAPOL (*Extensible Authentication Protocol*) se describe como un *handshake* de 4 vías. Es un proceso de intercambio de 4 paquetes entre un punto de acceso y un cliente inalámbrico para **generar claves de cifrado** a utilizar.

![[Proceso de Autenticación WPA.png]]
