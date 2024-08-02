De las [[Técnicas de Direccionamiento]], el direccionamiento **indirecto** permite usar direcciones que entran en la palabra de memoria pero no entran en la zona de dirección $D$ del [[Registros|registro]] de instrucción $I$. $D$ contiene la dirección en memoria de un [[Puntero]] (otra dirección de memoria). En total, requiere **dos ciclos de memoria**, porque recorre la [[Unidad de Memoria]] dos veces.

![[Direccionamiento Indirecto.png]]

En el primer ciclo de memoria busca la palabra que contiene la dirección del operando. En el segundo ciclo, busca el operando en la dirección indicada por el contenido de la palabra de memoria previamente encontrada.
