En la [[Transmisión de Datos]], si se dispone de dos dispositivos enlazados punto a punto, es deseable tener varias tramas pendientes de confirmación y evitar que el enlace sea un cuello de botella. La **multiplexación** permite compartir la [[Capacidad del Canal]] de datos.

![[Multiplexación.png]]

El *multiplexor* combina los datos de las líneas de entrada y los transmite. Luego, el *demultiplexor* acepta esa cadena, separa los datos conforme a cada canal correspondiente, y los distribuye a la salida.

La importancia de la multiplexación es que abarata costos de líneas de larga distancia, y el servicio es más costo-eficiente conforme aumenta la razón de datos.

## FDM

La **Multiplexación por División en Frecuencias** requiere que el [[Señales y Espectros|ancho de banda]] del medio sea mayor que el ancho de banda de la señal transmitida.

![[Multiplexación por División en Frecuencias.png]]

Cada señal se modula con una *frecuencia portadora* distinta, de manera que usa una porción particular del ancho de banda total, la cual se denomina *canal*. Para evitar interferencias, los canales se separan por una *banda de seguridad* que se mantiene sin usar.

La señal de ingreso se modula para ser desplazada a su banda de frecuencia apropiada. La señal transmitida es analógica.

## TDM Síncrona

La **Multiplexación por División en el Tiempo Síncrona** requiere que la razón de datos del medio sea mayor que la de las señales.

![[Multiplexación por División en el Tiempo Síncrona.png]]

Se multiplexan una serie de señales digitales en el mismo medio. Los datos de entrada se almacenan temporalmente en un buffer. Estos datos se organizan en tramas, cada trama conn un ciclo de subdivisiones. Una o más subdivisiones se dedican a una sola fuente, y una secuencia de trama en trama se denomina *canal*. Esas subdivisiones tienen la misma longitud que el buffer, que generalmente es 1 bit.

Esto se vuelve ineficiente cuando una fuente no manda datos por mucho tiempo, porque desaprovecha el ancho de banda al dejar tramas vacías.

- Control de flujo: no es necesario porque la razón de datos es fija.
- Control de errores: se aplica en cada canal de manera independiente a otros canales.
- Sincronización de tramas: se añade un bit de control a cada trama.

## TDM Asíncrona

La **Multiplexación por División en el Tiempo Asíncrona** o Estadística busca optimizar la TDM síncrona. En la TDM síncrona se desperdician muchas subdivisiones de las tramas por ir vacías. En la TDM estadística, las subdivisiones se asignarán dinámicamente bajo demanda.

En cada subdivisión, como no se sabe a qué fuente corresponde, se agregan unos bits de dirección. Si además hay varias fuentes por trama, se agregan bits de longitud.

Esta técnica permite que la razón de datos del medio pueda ser menor a la suma de las entradas. Para cuando hayan picos de demanda del multiplexor, se usan memorias temporales que guarden esos bits que no entraron en las tramas, con un sistema de colas. Un problema es que esa espera, si se acumula, puede colapsar la memoria temporal de los dispositivos.

## Línea de Abonado Digital Asimétrica

¿Qué sucede si el receptor también quiere enviar datos? **ADSL** permite la subida y descarga de datos digitales a alta velocidad a través del cable telefónico convencional, lo que es una multiplexación FDM. Es apropiada para la transmisión en internet.

ADSL presenta cierta **asimetría**, donde le da mayor capacidad al enlace descendente y menor capacidad al enlace ascendente (ya que normalmente un usuario descarga más de lo que sube).

**XDSL**: esquemas alternativos a ADSL. Ejemplos: HDSL, SDSL, VDSL.
