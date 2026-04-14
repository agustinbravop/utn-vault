En [[Data Warehouse]], el modelo multidimensional almacena hechos, dimensiones, jerarquías y métricas. Su gráfico es similar al DER de [[Bases de Datos]] pero la filosofía tiene algunas diferencias. Definiciones:

- **Dimensión**: un nivel, una o más jerarquías.
- **Jerarquía**: conjunto de niveles relacionados.
- **Nivel**: un tipo de entidad.
- **Miembro**: una instancia en un nivel.

Un *hecho* relaciona *métricas* (atributos de las tablas de hechos) con los niveles *hoja* de las dimensiones involucradas.

Se lo puede pensar como un DER limitado sin relaciones muchos-a-muchos y con la menor cantidad de relaciones opcionales posibles. Lo ideal es usar **jerarquías estrictas** (relaciones N:1). Si la realidad no lo permite, hay que tener en cuenta algunos cuidados:

- **Jerarquías balanceadas**: ideales para el diseño estrella o copo de nieve (snowflake).
- **Jerarquías recursivas**: generalmente requieren una consulta recursiva.
- **Jerarquías ragged**:
![[Jerarquía Ragged.png]]
- **Jerarquías No Estrictas**: tienen al menos una relación M:N. Implica un grafo en la instancia, lo cual introduce el *problema del doble conteo*. Lo mejor es evitar ese problema, aunque hay algunas soluciones posibles:
	- Usar un factor de distribución.
	- Elegir un miembro padre como primario e ignorar el resto.
	- Dividir la jerarquía (implica modificar el esquema, suele ser lo ideal).
	- Formar grupos.

Pasos a seguir:

1. Identificar tabla de hechos.
2. Identificar medidas de la tabla de hechos.
3. Identificar dimensiones.
4. Identificar jerarquías y atributos de las dimensiones.
5. Revisar las consultas y verificar que el modelo las resuelve.

**MDX** (MultiDimensional eXpressions) es el lenguaje de consulta multidimensional. A diferencia de SQL, MDX no especifica las relaciones (joins) pero es posicional y referenciado.

Microsoft propone un *modelo tabular* alternativo al multidimensional donde los datos se procesan en memoria, no en disco. Usa un almacenamiento basado en columnas y algoritmos de compresión sofisticados para ofrecer tiempos de consulta muy rápidos.
