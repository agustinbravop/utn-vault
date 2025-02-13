En la [[Capa de Enlace]], el **entramado** consiste en armar la trama a enviar y entender la trama recibida. El [[Protocolo]] utiliza la información de control de la trama para identificarla. La transmisión puede estar orientada a _bits_ o a _bloques_.

Estrategias:

- **Conteo de caracteres**: es una estrategia sencilla que agrega un dato de control que indica la cantidad de campos a contar para armar la trama. No se usa porque el mismo conteo puede tener un error.
- **Secuencias de bits**: caracteres _bandera_ que indican el comienzo y fin de las tramas. Deberían ser _transparentes_ (los datos no se tocan), tal que la capa de enlace los pone y los quita. Si la bandera aparece como dato, se inserta un _caracter de escape_. La bandera debería aparecer por única vez para delimitar la trama. Si hay un error en la inserción, se pierde esa trama pero solo esa trama.
  - **Inserción de bit**: si `01111110` es bandera y se quiere enviar seis `1` de dato, cada cincos `1` de dato se añade un `0` de control para desambiguar.
- **Violaciones del código**: son condiciones anormales de la transmisión. Por ejemplo, la [[Codificación de Datos#Datos Digitales en Señales Digitales|codificación Manchester]] establece transiciones alto-bajo o bajo-alto, pudiendo usar transiciones bajo-bajo o alto-alto para el entramado.
