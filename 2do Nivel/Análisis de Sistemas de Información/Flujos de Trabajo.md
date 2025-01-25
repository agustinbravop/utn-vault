Un **flujo de trabajo** o modelo de proceso establece una forma de trabajar durante el [[Ciclo de Vida del Software]].

## Modelo Prueba y Error

Sirve si la tarea es simple y unipersonal, pero no escala para sistemas grandes y complejos.

## Modelo en Cascada

Se definen etapas del desarrollo, y una comienza cuando termina la anterior, la cual como resultado le entrega un documento a la etapa siguiente. El beneficio de la documentación es que aumenta la visibilidad, pero también vuelve menos ágil al [[Proyecto de Software]].

![[En Cascada.png]]

En este flujo se producen bloqueos y retrasos. Además, como el testing se realiza al final, los errores son muy costosos.

## DRA

Adapta el modelo en cascada para dividir el desarrollo en varios módulos, y cada equipo se encarga de un módulo. Se basa en la reutilización de componentes.

![[DRA.png]]

Acelera el desarrollo pero requiere mucho esfuerzo.

## Modelo en V

Modifica el modelo en cascada para centrarse en el testing. Hay una fase de verificación y otra fase de validación, para testear lo antes posible.

![[Modelo en V.png]]

## Prototipos

Es un modelo experimental de un sistema o componentes con los suficientes elementos que permiten su uso, para que el usuario pruebe el [[Prototipos|prototipo]] y nos de su retroalimentación para mejorarlo.

![[Prototipos.png]]

Los prototipos pueden ser:

- **Evolutivos**: se refina el prototipo hasta ser la versión final. Esto requiere asentar una base sólida.
- **Desechables**: el prototipo se desecha luego de ser probado, por lo que se lo puede desarrollar rápidamente y sin calidad.

## Modelo Incremental

Cada secuencia produce un _incremento_ del software, y con cada incremento se entrega un producto totalmente operacional, a diferencia del prototipado evolutivo que simula algunas funcionalidades.

![[Modelo Incremental.png]]

## Modelo Iterativo

Cada _iteración_ refina las mismas funcionalidades que la iteración anterior, pero con mayor detalle y mejor desempeño. Las primeras iteraciones son bosquejos del sistema, y la última es el producto completamente terminado.

Complementa muy bien al modelo incremental.

## Modelo en Espiral

Es un antecedente del [[Proceso Unificado de Desarrollo de Software]], que adopta los principios del modelo incremental y del modelo iterativo para proponer un _modelo iterativo-incremental_.

![[2do Nivel/Análisis de Sistemas de Información/attachments/Modelo en Espiral.png]]
