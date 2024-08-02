El modelo de Wilkes propone un secuenciador [[Microprogramación|micro-programado]] que define una **memoria de control** con **palabras de control**. La palabra se divide en dos partes (las dos columnas de cables del diagrama). La primer parte es la micro-instrucción, y la segunda parte es la siguiente micro-instrucción a ejecutar. El campo $CO$ del registro $I$ indica la primer micro-instrucción a ejecutar. 

![[Modelo de Wilkes.png]]

Cada micro-instrucción ejecutada dispara ciertas [[Señales de Gobierno]] que controlan la ejecución de la instrucción indicada por el campo $CO$.
