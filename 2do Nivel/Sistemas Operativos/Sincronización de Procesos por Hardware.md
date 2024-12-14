Soluciones por hardware para la [[Comunicación entre Procesos]].

## Inhabilitación de Interrupciones

![[Diagrama de Inhabilitación de Interrupciones.png]]

- Válido solo para monoprocesadores.
- Bajo rendimiento por no poder intercalar procesos (es muy enfoque que bloquea mucho).

## Test and Set Lock

![[Diagrama de Test and Set Lock.png]]

Instrucción de hardware, específica a cada [[Arquitectura de Computadoras]], que compara y fija la bandera de manera **atómica**.

## Intercambiar

![[Diagrama de Intercambiar.png]]

Instrucción de hardware, específica a cada arquitectura, que intercambia dos valores de manera **atómica**, evitando por hardware las [[Comunicación entre Procesos#Condiciones de Competencia|condiciones de competencia]].
