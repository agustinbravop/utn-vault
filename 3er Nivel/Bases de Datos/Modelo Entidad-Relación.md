En el [[Modelado de Datos]] de las [[Bases de Datos]], el modelo **entidad-relación** propone diseñar la base de datos como un conjunto de _entidades_ (objetos del mundo real con _atributos_) y _relaciones_ (vínculos entre dos o más entidades).

El diseño conceptual de una [[Arquitectura de un SGBD]] contiene descripciones de alto nivel sobre los datos a almacenar. El modelo DER es una representación de este diseño. Sin embargo, existen restricciones que no pueden representarse (por ejemplo, dependencias funcionales). Un DER es subjetivo y presenta muchas decisiones de diseño.

![[Modelo Entidad-Relación.png]]

Las relaciones pueden tener _atributos descriptivos_, que registran información sobre la relación en sí (y no sobre alguna entidad particular).

Cada relación debe identificarse de manera unívoca por sus entidades participantes, sin necesitar referenciar sus atributos descriptivos. Cada entidad debe tener una _clave_ que la identifique unívocamente.

Cada _ejemplar_ de un conjunto de relaciones es un conjunto de relaciones en sí mismo. Se puede pensar en un ejemplar como una "instantánea" del conjunto de relaciones en un momento dado.

![[Ejemplar de un Conjunto de Relaciones.png]]

Las relaciones también pueden ser _ternarias_:

![[Conjunto de Relaciones Ternarias.png]]

Además, una misma entidad puede participar más de una vez en una relación si es que cumple papeles o _roles_ diferentes:

![[Conjunto de Relaciones con Roles.png]]

## Restricciones

Las **restricciones de clave** en las relaciones permiten limitar la _cardinalidad_ (1 a 1, 1 a $n$, o $n$ a $n$), de manera que cada instancia de una entidad pueda participar una sola vez en cierta relación. En el siguiente ejemplo: un Departamento solo puede ser dirigido por un solo Empleado.

Las **restricciones de participación** establecen si todas las instancias de una entidad deben participar o no de una relación. En el siguiente ejemplo: la participación del conjunto de entidades Departamento en el conjunto de relaciones Dirige es _total_ (todo Departamento es dirigido por un Empleado). Una participación que no es total se dice _parcial_.

Una restricción de clave se indica con una flecha punteada. Una participación total se indica con una línea gruesa.

![[Restricciones en el Modelo Entidad-Relación.png]]

Esto resulta en el siguiente ejemplar:

![[Ejemplar de Restricciones del Modelo Entidad-Relación.png]]

## Entidades Débiles

Cada _entidad débil_ solo se puede identificar de manera unívoca tomando en consideración alguno de sus atributos junto con la clave principal de otra entidad conocida como _propietaria identificadora_. Se debe cumplir que:

- Cada entidad propietaria se asocie con una o varias entidades débiles, pero que cada entidad débil solo tenga una propietaria.
- El conjunto de entidades débiles tenga participación total en el conjunto de entidades identificadoras.

Una entidad débil, y la _relación identificadora_ que la vincula con su entidad propietaria, se diagraman con borde grueso.

![[Entidades Débiles en el Modelo Entidad-Relación.png]]

En este ejemplo, cada entidad Beneficiario sólo se puede identificar de manera unívoca si se toma la clave "dni" de la entidad Empleados junto a la _clave parcial_ "nombrep".

## Jerarquías de Clases

Las entidades (subclases) pueden _heredar_ atributos de otras entidades (superclases).

![[Jerarquías de Clases en el Modelo Entidad-Relación.png]]

Se deben tener en cuenta dos restricciones:

- **Solapamiento**: ¿Puede "Empleado_temp" ser a la vez un "Empleado_fijo"?
- **Cobertura**: ¿Debe sí o sí todo "Empleado" pertenecer a una subclase? Es decir, ¿"Empleado" es una clase abstracta o concreta?

## Agregación

La _agregación_ indica que un conjunto de relaciones participa en otro conjunto de relaciones. Esto permite expresar _una relación entre relaciones_.

![[Agregación en el Modelo Entidad-Relación.png]]

## Símbolos

En resumen:

![[Símbolos del Modelo Entidad-Relación.png]]
