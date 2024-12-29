El modelado del dominio se realiza como parte del [[Modelado de los Sistemas]] luego de haber realizado el [[Modelado del Negocio]]. Consiste en un conjunto de *diagramas de clase* (de UML) que muestran *conceptos* del dominio del problema, y sus *atributos* y *relaciones* importantes.

![[Modelado del Dominio.png]]

Cada **concepto** es un objeto o *clase* del dominio, con relaciones con otras clases. Se establece un **vocabulario** a respetar para pensar formalmente sobre el problema.

Se requieren varias iteraciones para obtener un buen modelo del dominio, pero es, junto a la [[Especificación de Requisitos de Software]], el documento más importante para la etapa de diseño del [[Ciclo de Vida del Software]].

Existen **patrones de análisis** que sirven como solución probada de problemas recurrentes. Por ejemplo, se recomienda identificar los siguientes elementos:

1. **Actores y participantes**: se buscan actores y de qué manera participan.
2. **Lugares**: objetos que contienen otros objetos. Ej: ciudad-país, producto-caja.
3. **Ítems y descripciones**: buscar descripciones que se puedan aplicar a varios ítems.
4. **Transacciones**: algo que el sistema debe recordar. Suelen tener fecha, hora, y autor asociado.
5. **Generalización-especialización**: sucede cuando varios objetos comparten comportamiento.

Si $X$ no es un número, texto, o booleano, seguramente $X$ es un concepto y no un atributo. Hay que buscar evitar las relaciones que no aportan nada a los [[Requerimientos]], porque hacen ruido visual. Buscamos maximizar la utilidad que el modelo nos brinda, usando las mejores prácticas que conocemos.

Modelar es pensar con diagramas un modelo que se irá mejorando iterativamente.
