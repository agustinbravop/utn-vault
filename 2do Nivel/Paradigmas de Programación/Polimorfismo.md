En el [[Paradigma Orientado a Objetos]], el **polimorfismo** permite ejecutar los métodos de distintos objetos que pertenezcan a la misma clase en común. Se lo logra de varias maneras.

## Sobrecarga

En la [[Sistemas de Tipos#Sobrecarga|sobrecarga]] se crean varios métodos con el mismo identificador pero con distinta cantidad de parámetros o parámetros de distinto tipo. Esto asegura que la *firma* del método siga siendo única. Este polimorfismo es estático y se resuelve al compilar.

## Polimorfismo Paramétrico

El polimorfismo paramétrico permite generalizar una[[Clases|clase]] "wrapper" a cualquier clase. Mediante esa interfaz genérica, podemos reutilizar su funcionalidad. Se basa en los [[Sistemas de Tipos#Tipos Parametrizados|tipos parametrizados]] de los lenguajes estáticos, lo que se suele denominar *generics*. En los lenguajes dinámicos, todo es *generics*, pero sin la *type safety* de los lenguajes dinámicos.

## Polimorfismo de Inclusión

El polimorfismo de inclusión da gracias a la [[Herencia]] y a la redefinición de métodos. Mediante la misma interfaz, cada subclase de una clase padre en común ejecuta su propio método personalizado. 

Esto facilita expandir la base de código agregando y quitando subclases, sin tener que tocar el código que las usa.
