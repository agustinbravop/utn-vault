En la [[Comunicación de Datos]], la **conmutación de paquetes** sirve para crear conexiones de datos con las que realizar la [[Transmisión de Datos]].

En una conexión típica de datos usuario-computador, la línea se encuentra desocupada la mayor parte del tiempo, por lo que utilizar la [[Conmutación de Circuitos]] resulta ineficaz.

En las **redes de conmutación de paquetes**, los datos se subdividen en _paquetes_. Cada _nodo_ recibe un paquete, lo almacena en una _cola_, y lo envía al nodo siguiente del camino.

Las colas permiten aceptar más demanda en la red a cambio de un mayor retardo, para construir redes _no bloqueantes_. También permiten priorizar paquetes.

## Técnicas de Conmutación

¿Cómo enviar varios paquetes secuencialmente? Hay dos maneras:

- **Datagramas**: se envían paquetes independientes que el nodo receptor debe reordenar. Cada paquete se enruta por separado, y por ende se pueden perder. Esto hace un **uso eficiente** de la red.
- **Circuitos virtuales**: se establece una llamada con el receptor y se fija el _camino_, que es estable pero inflexible. Así, el encaminamiento es el mismo para todos los paquetes, ofreciendo **fiabilidad**.

![[Conmutación de Paquetes.png]]

**Tamaño del paquete**: a mayor tamaño del paquete, se tiene menor paralelismo, y por ende un mayor tiempo de transmisión. Pero, si el tamaño es muy pequeño, la información de control de cada paquete comienza a ocupar una proporción mayor de la red.

## Encaminamiento

La _ruta_ depende de los requisitos: robustez, imparcialidad, optimización, etc. La **selección de la ruta** se basa en algún criterio de funcionamiento.

Se utiliza una _función de costo_ que a cada enlace le asocia un _costo_, para así **utilizar la ruta de menor costo**. El costo puede estar asociado a la capacidad, retardo, fiabilidad, etc.

La decisión se toma en cierto _instante_ (cuando el paquete llega o cuando se establece la sesión) y _lugar_ (el nodo que toma la decisión).

El tiempo de **actualización** de la información de la red depende de la [[Estrategia de Encaminamiento]] y la fuente de información, que puede ser local, de nodos adyacentes, o de toda la red.

A mayor cantidad de información y mayor frecuencia de actualización, si bien mejoran las decisiones de encaminamiento, también se consumen más recursos de la red.

## X.25

**X.25** es un protocolo estándar muy utilizado, aprobado en 1976. Especifica la interfaz entre una estación y una red de conmutación de paquetes. Se utiliza para interaccionar con redes de conmutación de paquetes.

Utiliza un modelo de [[Software de Redes]] de tres capas:

1. Física.
2. Enlace.
3. Paquetes.
