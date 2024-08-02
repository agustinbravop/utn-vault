Las [[Técnicas de Direccionamiento]] relativas hacen un direccionamiento relativo con respecto a una **dirección de referencia**. Se suele emplear cuando la longitud de la palabra de memoria es insuficiente para direccionar toda la memoria. Hay varios tipos.

## Por Base y Desplazamiento

Un [[Registros|registro]] **base** tiene la dirección de referencia. Adempas, la zona de dirección $D$ del registro de instrucción $I$ tiene el desplazamiento a la base. La dirección **efectiva** es $(BASE) + (D)$.

![[Direccionamiento por Base y Desplazamiento.png]]

Este direccionamiento permite a los programas **abstraerse** de absolutamente toda la memoria. Requiere que exista una [[Codificación de las Instrucciones|instrucción]] para establecer el valor de la base.

## Por Referencia al Programa

Se toma al **contador del programa** como referencia.

![[Direccionamiento por Referencia al Programa.png]]

Esto sirve para bifurcaciones del código, donde se accede con un *if* o con un *else* según un *offset* positivo o negativo.

## Por Página o Yuxtaposición

Este direccionamiento permite tener **sistemas operativos multitarea** (con varios programas a la vez).

![[Direccionamiento por Página o Yuxtaposición.png]]

Si $A$ está cerrado hay direccionamiento en la página cero, y si está abierto hay direccionamiento en la página de la instrucción.

## Indexado

El direccionamiento indexado es útil en la programación de programas para tratar datos almacenados vectorialmente, o como registros de conveniencia.

![[Direccionamiento Indexado.png]]

Los registros de índice $X_1$, $X_2$ y $X_3$ suman la dirección que ellos contienen a $D$. La dirección efectiva es $(X_i) + (D)$. Es similar a un direccionamiento por base y desplazamiento pero con varios registros base disponibles.
