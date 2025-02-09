La **seguridad informática** es toda una especialidad en sí, con varias normativas. El primer paso es definir [[Políticas]], teniendo en cuenta los activos a resguardar y las imposiciones legales.

La seguridad de la información es la protección de la información contra todo tipo de amenazas en pos de asegurar la continuidad del negocio. Nosotros hacemos foco en la **ciberseguridad**.

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

Una función unidireccional *hashing* permite que $P \longrightarrow \text{MD}(P)$ sea fácil pero $\text{MD}(P) \longrightarrow P$ sea imposible. Se produce una *colisión* cuando $\exists P, P' / \text{MD}(P) = \text{MD}(P')$. La longitud de la clave debe ser mayor a 128 bits para disminuir la facilidad de producir colisiones. Se usa en firmas digitales para la autenticidad, el no repudio, y la integridad.

Pocos cambios en $P$ deben provocar grandes cambios en $\text{MD}(P)$. Se puede usar con la  clave pública o la clave privada.

Algoritmos de cifrado asimétrico:

1. **RSA**: propuesto en 1977, se seleccionan dos números primos grandes $p$ y $q$ que se mantienen en secreto para generar las dos claves. La fortaleza reside en la imposibilidad práctica de factorizar un número grande.

El problema de *Man In The Middle* (MITM). Un atacante suplanta la identidad de una persona/sistema y genera un par de claves auténticas en su nombre. Para solucionarlo, se introduce una *Certification Authority* (CA) que emita **certificados** firmados con la clave privada del receptor, para asegurar que la clave pública del receptor es válida.

Varias CA forman parte de una *Public Key Infrastructure* (PKI). Existe una **cadena de confianza** entre las CAs, que forman una jerarquía descentralizada.
