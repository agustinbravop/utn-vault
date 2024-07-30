Los códigos redundantes en una [[Codificación]] agregan **bits de control** a la información para **detectar errores y corregirlos**, asegurando la **integridad** de la información transmitida (recibida). Permiten detectar alteraciones de la información debido al ruido del canal en el que viaja el mensaje.

La **paridad** par e impar de ceros y unos de una cadena binaria resulta útil. La paridad se controla con un XOR:

| A   | B   | A XOR B = P |
| --- | --- | ----------- |
| 0   | 0   | 0           |
| 0   | 1   | 1           |
| 1   | 0   | 1           |
| 1   | 1   | 0           |

- [[Código Entrelazado]].
- [[Control Dos entre Tres]].
- [[Código de Hamming]].
