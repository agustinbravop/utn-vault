Existen varios **medios** posibles para la [[Transmisión de Datos]]. Normalmente se clasifican en dos:

- Medios guiados.
- Medios no guiados.

## Medios Guiados

En estos medios de transmisión, la [[Capacidad del Canal]] depende drásticamente del medio y la distancia.

![[Medios de Transmisión Guiados.png]]

1. **Par Trenzado**: es muy utilizado, económico, y sencillo. Dos cables de cobre de 1 milímetro entrecruzados (para reducir la _diafonía_ o interferencia electromagnética) van embutidos en un aislante. Tiene las menores prestaciones en cuanto a distancia y velocidad.
2. **Cable Coaxial**: es un conductor cilíndrico externo que rodea a un cable conductor. El diámetro varía entre 1 y 2,5 centímetros. Es mucho menos susceptible a la diafonía y puede cubrir mayores distancias que un par trenzado.
3. **Fibra Óptica**: es un medio flexible y extremadamente fino, de entre 2 y 125 micrómetros. Se construye con diversos vidrios y plásticos. Ofrece mayor ancho de banda y mayor separación entre repetidores, con menor tamaño, menor peso, y menor atenuación.

## Medios No Guiados

Una **antena** es un conductor eléctrico que capta o irradia energía electromagnética. A mayor frecuencia, las antenas son más baratas, pero existe una mayor atenuación y ofrecen una menor distancia.

La _ganancia_ de una antena es la [[Potencia Efectiva]] de salida en una dirección dada. Es una medida de su _direccionalidad_. **Ecuación de transmisión de Friis** entre una antena receptora y otra antena transmisora:

$$\frac{P_r}{P_t} = G_t \cdot G_r \cdot \left( \frac{\lambda}{4\pi R}\right)^2$$

Para los medios de transmisión no guiados se utilizan distintos _rangos de frecuencias_ del [[Señales y Espectros|espectro electromagnético]], cada uno con distintas propiedades:

1. **Microondas terrestres**: son altamente direccionales. Una antena parabólica de 3 metros de diámetro se fija y alinea con la antena receptora. Si no hay obstáculos intermedios, se pueden alcanzar distancias de decenas de kilómetros. El ancho de banda está entre 2 y 40 GHz. Nos permiten transmitir a largas distancias. La principal pérdida se debe a la _atenuación_.
2. **Microondas por satélite**: un satélite de comunicaciones es una estación que retransmite microondas, actuando como enlace entre otras dos estaciones. En particular, los _satélites geoestacionarios_ mantienen su posición respecto de la Tierra (son los más eficientes). En la órbita geoestacionaria hay 360, uno por cada grado sexagesimal. El rango óptimo es 1-10 GHz.
3. **Ondas de radio**: son omnidireccionales, por lo que no se requiere ni alinear antenas ni que sean parabólicas. Van entre 3 KHz y 300 GHz. Sufren una atenuación menor que las microondas.
4. **Infrarrojos**: no pueden atravesar paredes, lo que limita sus aplicaciones pero aumenta su seguridad, por lo que sufren menor interferencia. Esta banda no requiere permisos de organismos reguladores. Requieren _line of sight_.
5. **Ondas de luz**: ofrecen _señalización unidireccional_: un _láser_ para enviar datos y un _fotodetector_ para recibir datos. Requieren line of sight. Ofrecen un ancho de banda alto a un costo barato, pero el canal se ve afectado por niebla densa, lluvia, corrientes de aire generadas por calor, obstáculos, etc.
