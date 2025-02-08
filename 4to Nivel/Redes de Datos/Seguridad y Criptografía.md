Conceptos:

1. Confidencialidad.
2. Autenticación.
3. Integridad.
4. No repudio (que no se pueda rechazar la autenticidad del emisor).
5. Disponibilidad.

La **criptografía** estudia los mecanismos para mantener oculto el contenido de un mensaje.

![[Seguridad y Criptografía.png]]

Lo importante es que $D_k(E_k(P))=P$, para que se pueda recuperar el mensaje.

Existen varios métodos de cifrado.

En el **cifrado XOR** se aplica XOR al mensaje con una clave de misma longitud. Es inexpugnable pero es frágil e impráctico. Es muy vulnerable por sí solo, pero forma parte de cifrados más complejos.

## Cifrado Simétrico

En el **cifrado en bloque simétrico** se cifra la entrada en bloques de $k$ bits (siendo $k$ una potencia de 2). La misma clave cifra y descifra. Algunos métodos simétricos:

1. **DES**: este método cifra bloques de 64 bits con una clave de 56 bits y 19 etapas. Es vulnerable a claves débiles y se lo considera obsoleto.

![[DES.png]]

2. **3DES**: es compatible con el DES de clave única cuando $k_1=k_2$. Es más eficiente con tres claves $k_1$, $k_2$, y $k_3$, pero igual se considera roto, porque se conocen esquemas de computación paralela que lo pueden romper en muy poco tiempo.

![[3DES.png]]

3. **AES**: también es un proceso reversible de una sola clave. Es mucho más robusto que los anteriores, y se considera confiable.

En general, la seguridad de los esquemas simétricos depende del secreto de la llave. Son más veloces que los esquemas asimétricos, y se pueden implementar en hardware.

## Cifrado Asimétrico

La criptografía asimétrica estudia algoritmos que tienen una clave privada y otra pública. Se basan en funciones matemáticas unidireccionales (funciones *hash*), tal que el cifrado $f(M)=C$ es fácil, pero el descifrado $f^{-1}(C)=N$ es computacionalmente imposible si no se tiene la llave.

1. **RSA**: propuesto en 1977, se seleccionan dos números primos grandes $p$ y $q$ que se mantienen en secreto para generar las dos claves. La fortaleza reside en la imposibilidad práctica de factorizar un número grande.
