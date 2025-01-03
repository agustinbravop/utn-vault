El **modelo relacional** para el [[Modelado de Datos]] de las [[Bases de Datos]] es el modelo más utilizado actualmente. Propuesto por Edgar Codd en 1970, tiene una base matemática bien definida. Ofrece _independencia física y lógica_ (aunque no de manera perfecta).

Un _esquema de una relación_ especifica un _nombre_ para la relación y un nombre y tipo de dato para cada _campo_. Una _instancia_ es una tabla con filas y columnas. Ej:

```
Alumdos(_ide_: string, nombre: string, usuario: string NO NULO, edad: int, nota: real)
```

Terminología:

| Relación     | Tabla       | Archivo      |
| ------------ | ----------- | ------------ |
| Tupla        | Fila        | Registro     |
| Atributo     | Columna     | Campo        |
| Grado        | N° columnas | N° campos    |
| Cardinalidad | N° filas    | N° registros |

![[Ejemplar de una Relación en el Modelo Relacional.png]]

[[SQL]] es un lenguaje potente e intuitivo soportado por el modelo relacional.
