La **capa de acceso a datos** es la _capa_ (conjunto de entidades) de la aplicación encargada de la **persistencia** de los datos. Realiza consultas a [[Bases de Datos]] específicas en su lenguaje (suelen ser dialectos de [[SQL]]), pero devuelve **objetos del dominio** de la aplicación.

![[Data Access Layer.png]]

Así, el DAO (Data Access Object) abstrae la persistencia y el acceso a los datos. Esto permite que la aplicación pueda cambiar de motor de base de datos y solo modificar el DAO, es decir, el DAO _encapsula_ este comportamiento.

Objetos en Java para interactuar con una base de datos SQL:

1. `Connection`: se crea uno solo. Necesita la url de la base de datos.
2. `Statement`: representa una consulta de SQL.
3. `ResultSet`: es el resultado de una consulta. Con `.next()` se puede iterar sobre el cursor.

La capa de accesos a datos será consumida por la capa de servicios, que se encarga de encapsular la lógica de negocio de la aplicación.
