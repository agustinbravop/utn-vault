En la computación cuántica se descubrió un algoritmo que factoriza números primos en un tiempo polinomial, lo cual rompe todos los sistemas asimétricos de la [[Criptografía]] actual. Si bien todavía no existe una implementación de la computación cuántica, ya existe la **criptografía cuántica**.

Si Alicia envía a Bruno unos _qubits_ para generar una clave, y un atacante intercepta el mensaje, al leer los qubits el atacante **introduce errores** por observar información cuántica. Luego, si Bruno detecta errores en el mensaje, solicita una nueva clave privada a Alicia.

Cada bit que Alicia desea enviar, lo codifica en un qubit usando al azar uno de dos alfabetos. Luego, Bruno lee los bits probando con un alfabeto al azar. La mitad de las veces va a leer bien el bit y la otra mitad los va a leer mal.

![[Criptografía Cuántica.png]]

Luego, Bruno le responde a Alicia los bits que detectó, y ambos descartan los que se detectaron usando el alfabeto incorrecto. Repiten el proceso hasta que todos los bits anteriormente incorrectos sean correctos.

Este esquema de criptografía cuántica permite que Alicia y Bruno puedan **detectar** si los están espiando, y así se soluciona el problema de los sistemas simétricos de compartir la clave secreta.

Una vez establecida la clave secreta, se realiza la [[Transmisión de Datos]] por el canal clásico utilizando un algoritmo criptográfico simétrico clásico.
