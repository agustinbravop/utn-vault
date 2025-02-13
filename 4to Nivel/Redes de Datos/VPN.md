Una _Virtual Private Network_ (VPN) conecta [[Redes de Datos]] de la misma organización ubicadas en distintos lugares, usando la internet pública. Sobre la infraestructura pública de internet, se monta una infraestructura privada.

La performance, costo, y disponibilidad, dependen del ISP seleccionado.

En términos de [[Ciberseguridad]], el tráfico VPN debe ser encriptado extremo-a-extremo, y deben estar autenticadas bajo el paradigma cliente-servidor. No puede alterarse la VPN una vez establecida.

Tipos de VPN, a nivel de:

1. [[Capa de Enlace]]: L2TP, PPTP (más sencillo). Son gateway a gateway.
2. [[Capa de Red]]: [[IPSec]], [[BGPv4]] con MPLS. Son extremo a extremo.
3. [[Capa de Transporte]]: SSL. Es aplicación a aplicación.

El tipo de VPN a utilizar depende del problema a resolver. Se pueden usar las VPNs junto con un mecanismo de direcciones privadas (NAT).
