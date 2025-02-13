La **geodesia** es la ciencia que estudia la forma y dimensiones de la Tierra. Tiene varias ramas:

- **Geométrica**: analiza el aspecto geométrico de la Tierra.
- **Física**: estudia el campo gravitatorio y sus variaciones.
- **Astronómica**: medir los astros para determinar coordenadas terrestres.

La **cartografía** es un conjunto de operaciones y procesos que intervienen en la creación, edición, y análisis de [[Mapas]]. Se basa en la premisa de **modelar la realidad** de manera que comunique información espacial de manera efectiva.

![[Fundamentos Cartográficos y Geodésicos.png]]

Problemas que ataca:

1. **Edición**: definir el objetivo del mapa y definir los rasgos a representar.
2. **Proyección**: representar el área del objeto en una superficie plana.
3. **Generalización**: eliminar características del objeto que no son relevantes.
4. **Diseño**: organizar los elementos del mapa para una comunicación efectiva.

## Escala

La *escala* es la relación matemática entre las dimensiones reales y las representadas. Puede ser:

- **Natural**: 1 a 1.
- **De reducción**: el plano es menor a la realidad. Ej: 1 a 10.000.
- **De ampliación**: el plano es mayor a la realidad. Ej: 2 a 1.

Representaciones de la escala:

1. **Escala numérica**: 1:100.
2. **Unidad por unidad**: 1 cm = 4 km.
3. **Escala gráfica**: 

![[Escala Gráfica.png]]

## Forma de la Tierra

La Tierra no es plana, y su forma no se puede ignorar al estudiar terrenos extensos. Pero, tampoco es una esfera perfecta. Una aproximación a su forma es el *geoide*.

> El **geoide** es la superficie equipotencial del campo gravitatorio que mejor se ajusta, al nivel medio del mar.

El campo gravitatorio depende de la densidad y la gravedad, la cual cambia con la altura. El geoide es una superficie irregular, similar a una esfera, pero con altos y bajos menores a 100 m.

El ***elipsoide*** es una elipse aproximada al geoide, pero fácil para cálculos matemáticos. Tiene 3 parámetros:

1. **Semieje ecuatorial**: $a$. Va desde el centro de masas hasta la superficie.
2. **Semieje polar**: $b$. La elipse base rota alrededor de este eje.
3. **Factor de achatamiento**: $f=1-\frac{b}{a}$.

![[Forma de la Tierra.png]]

Los parámetros $a$, $b$ y $f$ se miden con distintos valores en distintos modelos a lo largo de los años:

1. Elipsoide Hayford: $a = 6\ 378\ 388 \text{ metros}$ y $f = \frac{1}{297}$.
2. Elipsoide WGS84: $a = 6\ 378\ 137 \text{ metros}$ y $f = \frac{1}{298,257223563}$.
3. Elipsoide GRS80: $a = 6\ 378\ 137 \text{ metros}$ y $f = \frac{1}{298,257222101}$.
