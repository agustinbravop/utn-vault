La **administración de redes** es un conjunto de estándares, herramientas, y procedimientos para la **supervisión**, vigilancia, reparación, y mantenimiento de [[Redes de Datos]].

En **redes complejas** o grandes, es imprescindible contar con mecanismos de administración adecuados. Se puede hacer administración de:

1. Rendimiento.
2. Configuración.
3. Contabilidad.
4. Fallas.
5. Seguridad.

Componentes:

1. **Managed Object**: agente/servidor que recolecta datos del funcionamiento.
2. **Network Management System**: cliente que consulta y controla los dispositivos.
3. **Management Information Base**: base de datos que organiza la información.

La _Management Information Base_ (MIB) es una base de datos distribuida y jerárquica con estructura de [[Árbol]] que contiene objetos administrados. Cada dispositivo implementa una porción del árbol.

Los _atributos_ (objetos administrados) pueden ser escalares o tabulares. Se los representa con la notación ASN.1 (_Abstract Syntax Notation_). Por ejemplo, para acceder a estadísticas de [[IP]], se debe invocar su ruta completa: `iso.org.dod.internet.mgmt.mib.ip`.

_Structure Management Information_ (SMI), estandarizado en RFC 1155, establece un marco general para la definición y construcción de la MIB. Provee una forma estandarizada de representar información de administración.

**SNMPv1**, basado en SMI y definido en RFC 1157, define cuatro operaciones: `Get`, `GetNext`, `Set`, `Trap`. Es seguridad basada en _community_. Puede generar vulnerabilidades pero es ampliamente utilizado.

Luego surge **SNMPv2**, definido en RFC 1902, que agrega las operaciones `GetBulk` e `Inform`. Mejora los tipos de datos.

**SNMPv3**, definido en RFC 3411/3418, presenta una arquitectura modular para mejorar la [[Ciberseguridad]]. Agrega soporte para la encriptación y autenticación. El motor SNMP decide si permitir o no el acceso para cada operación. Es poco usado por ser inconveniente.

**RMON** permite el monitoreo remoto. Dispositivos específicos _sondean_ la red y centralizan la información de varios dispositivos. Esto evita sobrecargar todos los hosts.
