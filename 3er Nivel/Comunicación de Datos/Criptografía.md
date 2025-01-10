La **protección de los datos susceptibles de revelar** es una preocupación constante de la humanidad, pero la proliferación de redes de datos y la [[Comunicación de Datos]] aumentó las necesidades de tener datos seguros. Para proteger datos, se realizan:

- **Controles de acceso**: autenticación y autorización.
- **Controles de integridad**: para evitar modificaciones inadvertidas.

![[Criptografía.png]]

La **criptografía** es un conjunto de técnicas que permiten volver incomprensible un mensaje de forma que solo alguien con la llave secreta pueda descifrarlo.

El _criptoanálisis_ es la ciencia de determinar la clave o descifrar un mensaje sin la clave. Busca romper la criptografía.

$$\text{Criptología} = \text{Criptoanálisis} + \text{Criptografía}$$

La _robustez_ de un sistema criptográfico viene dada por su protección frente a ataques:

1. De fuerza bruta.
2. Por texto plano escogido.
3. A partir de texto plano.
4. De análisis por frecuencias.
5. Etc.

Se busca garantizar la **privacidad**, **integridad**, **autenticación**, y **disponibilidad** de los datos.

## Sistemas Simétricos

En los **sistemas simétricos**, las claves de cifrado y descifrado son la misma, por lo que solo debe ser conocida por el emisor y el receptor.

![[Criptografía Simétrica.png]]

Son rápidos y fáciles de implementar, pero requieren que la clave se comparta por un canal seguro, lo que resulta más difícil de lo que parece. Ej: DES, 3DES, AES.

## Sistemas Asimétricos

En los **sistemas asimétricos**, la llave pública es distinta a la llave privada. Una se utiliza para el cifrado, y la otra para el descifrado.

![[Criptografía Asimétrica.png]]

Ej: RSA, criptografía con curvas elípticas.
