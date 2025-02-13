_Internet Control Message Protocol_ (ICMP) es un [[Protocolo]] con **paquetes de control**, que se puede encapsular en [[IP]] con un header de 8 bytes y datos de tamaño variable.

![[Encapsulamiento de ICMP.png]]

La sección de datos la usan los mensajes de error para incluir todos los IP de cabecera, junto con los primeros 8 bytes de datos del paquete.

![[Encabezado ICMP-1.png]]

La suma de verificación es necesaria porque IP solo controla errores en el encabezado, pero ICMP se encapsula en el área de datos.

Hay varios tipos de ICMP, para distintos usos. El ICMP de tipo 4, _source quench_, permite avisar a un emisor que disminuya su tasa de peticiones para evitar saturar el buffer del [[Enrutadores|router]] o host. Varios otros tipos se utilizan, aunque algunos están deprecados.
