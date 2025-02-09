El uso de subredes o ***subnetting*** es una técnica para subdividir redes y **aprovechar las direcciones** disponibles de [[IP]] (el [[Protocolo]] de Internet).

![[Subnetting.png]]

Se ocupan unos bits del `hostID` de la dirección IP para usar un identificador de subnet que permita aprovechar el último octeto para varias subredes, lo cual consume una sola dirección IP. Ej:

```
11111111.11111111.11111111.111 00000
\________________________/ \_/ \___/
      porción de red     subred host
```

![[Subnetting para cada Clase.png]]

Con el **subnetting con VLSM** (*Variable Length Subnet Mask*), se puede dividir una subred en subredes más pequeñas con máscaras diferentes según los requerimientos que tengamos.

![[Subnetting con VLSM.png]]

CIDR (Classless Inter-Domain Routing) es la capacidad que tienen los protocolos de enrutamiento (en un [[Enrutadores|router]]) de enviar actualizaciones a todos sus vecinos de redes con VLSM y de sumarizar esas direcciones en una sola dirección.

La **sumarización de rutas** o supernetting es el proceso por el cual un router parte de un conjunto de direcciones de red (bloque CIDR) y obtiene una única dirección que contiene a las demás.

Mientras que el subnetting genera una máscara de red fija y cantidad de hosts uniforme en todas las subredes, el proceso de VLSM adapta las máscaras según la cantidad de hosts de cada subred. así, las máscaras se vuelven dinámicas para poder aprovechar más direcciones.
