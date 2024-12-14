Un **archivo** es el conjunto de [[Registro|registros]] **homogéneos** referidos a objetos de la misma naturaleza o del mismo tipo, almacenados en un soporte externo, que presenta entre sí una relación lógica y que pueden ser consultados individualmente de forma iterativa o sistemática.

Un archivo está **almacenado en memoria externa**, pero es **procesado en memoria interna**. La información almacenada es permanente. Aseguran una independencia de los datos respecto de los algoritmos que los utilizan.

Todo [[Algoritmo]] intercambia datos con el archivo: la unidad básica de entrada/salida es el registro.

Según su **utilidad**, pueden ser:

1. De **entrada**.
2. De **salida**.
3. **Históricos**.
4. De **movimiento**.
5. **Temporales**.

Según los datos almacenados, son **ASCII** (comprensible para humanos) o **binarios** (comprensibles para computadoras).

## Propiedades

- **Consistencia**: verifica la validez del dato almacenado con su definición en el **ambiente**.
- **Congruencia**: verifica la validez de los datos **entre sí**.
  - **Fina**: validación entre datos en archivos distintos (un mismo DNI en ALUMNOS validado contra PADRON).
  - **Gruesa**: validación entre datos en un mismo registro.

Por ejemplo, dado un formato "día/mes/año", el registro "13/13/2019" sería consistente pero no congruente.

## Soportes

Son los **medios físicos** donde se almacenan los datos. Para tratar archivos, se usan:

- **Secuenciales**: los registro están escritos uno a continuación del otro.
- **Direccionables**: los registros se localizan por su dirección, pero necesitan un campo clave.

## Organización

La organización se define al momento de creación del archivo y es permanente.

1. **Secuencial**: sucesión de registros almacenados consecutivamente (**continuidad física**). Para acceder a un registro $n$ hay que pasar por los $n-1$ registros anteriores.
2. **Directa**: posee una **continuidad lógica** y se accede a ellos mediante su posición, con cada registro teniendo un campo clave. Usa un soporte direccionable.
   - **Indexada**: incluye índices en el almacenamiento de los registros para buscar un registro sin recorrer todo el archivo. Implica la colocación de un listado al inicio del archivo que debe actualizarse cada vez que se actualice el archivo. Divide al archivo en un área de datos y un **área de índices**.
