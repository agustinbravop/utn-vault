De las [[Técnicas de Direccionamiento]], el direccionamiento inmediato es la más sencilla. Implica ignorar la [[Unidad de Memoria]] y simplemente enviar a la [[Unidad Aritmético-Lógica]] el contenido de $D$, que contiene el operando a procesar. No consume ciclos de memoria.

![[Direccionamiento Inmediato.png]]

En ABACUS, esto requiere que el [[Registros|registro]] $I$ (conformado por $CO$, $CD$ y $D$) esté conectado al [[Buses|bus]] M.

En realidad, no es propiamente un direccionamiento, debido a que ya se dispone del operando.
