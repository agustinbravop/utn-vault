_IPSec_ es un [[Protocolo]] para la [[Ciberseguridad]] de [[IP]], es decir, seguridad en la [[Capa de Red]]. Brinda servicios de:

1. Autenticación.
2. Autenticación + encriptación.
3. Distribución de claves.

Se establece una **asociación de seguridad** (SA) unidireccional entre ambos extremos. Los extremos finales pueden ser hosts o intermediarios ([[Enrutadores]], [[Firewalls]], etc). Puede operar en:

- **Modo Túnel**: se arma un datagrama que encapsula al IPSec original.
- **Modo Transporte**: se agrega una cabecera de seguridad al datagrama original.

Una _Security Parameter Index_ (SPI) es negociado entre ambas partes. Este SPI agrupa los atributos de seguridad usados: el algoritmo de cifrado, longitud de la clave, duración de la SA, etc.

Si bien IPSec se puede configurar manualmente en cada router, se necesita un mecanismo escalable y flexible. RFC 2409 propone IKE, que integra ISAKMP y OAKLEY, aunque se puede usar cualquier otro esquema (como PKI).
