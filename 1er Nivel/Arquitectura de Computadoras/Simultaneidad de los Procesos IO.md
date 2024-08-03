
Hay un problema fundamental que una [[Arquitectura de Computadoras]] debe solucionar en la diferencia de velocidad entre la rápida ejecución de las instrucciones del programa en la [[Unidad Aritmético-Lógica]] y los lentos ritmos de transferencia de los [[Canales]]. La simultaneidad entre procesamientos y entradas-salidas tiene una historia de avances y enfoques.

1. **Modo bloqueado**: en cada instrucción de entrada-salida **se espera** hasta que el periférico esté disponible. Es muy simple pero muy ineficiente, el computador se queda esperando mucho tiempo.
2. **Modo por prueba de estado**: se agrega una instrucción `PRE` que **consulta el estado del periférico** y, si está disponible, realiza la transferencia elemental. Esto permite no tener que esperar tanto pero es una **responsabilidad del programador** incómoda.
3. **Modo por interrupción de programa**: ahora el periférico **interrumpe** al programa en curso para avisarle al computador que está libre y que puede continuar la transferencia.
4. **Modo automático o canal**: se usa una instrucción especial de canal la cual se envía al **canal** y él la resuelve: `[cant palabras][dir 1er palabra][dir periférico][condición de fin]`. Mientras el programa en curso continúa, el canal le **roba ciclos** al procesador al ritmo del periférico, y luego avisa la finalización.
5. **Encadenamiento automático de transferencias**: la CPU genera un programa canal en la [[Unidad de Memoria]], que permite encadenar varias transferencias y tratarlas como si fueran una sola. Esto permite fragmentar el espacio en memoria al que se transfiere la información.

![[Simultanedidad de los Procesos IO.png]]
