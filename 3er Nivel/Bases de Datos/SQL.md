**Structured Query Language** (SQL) es un lenguaje desarrollado por IBM en los 70s para interactuar con los [[Sistema de Gestión de Bases de Datos]]. Está basado en el [[Modelo Relacional]]. Se divide en 4 sublenguajes:

1. **DDL**: Data Definition Language. `CREATE`, `ALTER`, `DROP`, `TRUNCATE`. Crea el [[Modelado de Datos|modelo conceptual]].
2. **DML**: Data Manipulation Language. `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `MERGE`.
3. **DCL**: Data Control Language. `GRANT`, `REVOKE`.
4. **TCL**: Transaction Control Language. `COMMIT`, `ROLLBACK`.

## Restricciones de Integridad

Las restricciones de integridad (RIs) son condiciones que deben cumplirse para toda instancia (fila) de una entidad (tabla). Se especifican al definir el esquema y se validan al alterar relaciones.

Una instancia _legal_ cumple todas las RIs. Los SGBD no deben permitir instancias ilegales. Con esto, se busca **evitar inconsistencias** y aumentar la confiabilidad de los datos.

```sql
PRIMARY KEY _  /* define la clave primaria */
UNIQUE _       /* define las otras claves candidatas */
/* campo que referencia la clave primaria de otra relación */
FOREIGN KEY _ REFERENCES _
```

Las **clases de dominio** son los tipos de datos (`date`, `integer`, `varchar`, etc).

La **integridad referencial** define qué hacer si se borra una tupla referenciada por _foreign keys_:

- `NO ACTION`: por defecto, se rechaza.
- `CASCADE`: borra tuplas referenciadas por la tupla borrada. Esto es ideal para [[Modelo Entidad-Relación#Entidades Débiles|entidades débiles]].
- `SET NULL`: modifica la foreign key a un valor nulo.
- `DEFAULT`: modifica la foreign key a un valor por defecto.

Las **transacciones** son una secuencia atómica de operaciones que deben cumplir con los principios ACID. O se ejecutan todas las operaciones de la transacción, o se cancelan todas. Ciclo de vida de una transacción:

![[Transacciones en SQL.png]]

Dentro de una transacción, se puede utilizar `DEFERRED` para diferir el control de las restricciones de integridad al final de la transacción. Por defecto, se usa `IMMEDIATE` para hacer el control al terminar cada instrucción particular.

Los **asertos** son predicados que expresan una condición que la base de datos debería satisfacer. Sirven para validaciones complejas o que involucren a más de dos relaciones. Ej: un vínculo con doble restricción de participación, "saldoTotal mayor a préstamoTotal", etc.

```sql
CREATE ASSERTION nombre CHECK (predicado)
```

Los disparadores o **triggers** son instrucciones que el SGBD ejecuta solo cuando sucede un evento disparador.

```sql
CREATE TRIGGER nombre ON tabla [BEFORE|AFTER] [INSERT|UPDATE|DELETE] ...
```
