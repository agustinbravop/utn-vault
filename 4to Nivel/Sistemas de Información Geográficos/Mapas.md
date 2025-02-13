Los **mapas** son herramientas de comunicación visual que buscan comunicar [[Información Geográfica]]. 

Es importante saber quién será el usuario y para qué va a servir el mapa. Es el usuario quien dice si el mapa es útil o no.

Elementos fundamentales a elegir:

1. Elementos a representar.
2. Forma de representar.
3. [[Fundamentos Cartográficos y Geodésicos#Escala|Escala]] y [[Proyecciones Cartográficas|proyección cartográfica]]. Afecta la [[Generalización Cartográfica]] necesaria.
4. Tipo de mapa (¿Es más científico o más coloquial?).

El mapa utiliza un lenguaje visual con elementos básicos (símbolos) que siguen normas y esquemas para combinarse. Elementos del mapa:

5. Nombre o título.
6. Autor.
7. Otra información sobre el mapa.
8. Canevás.
9. Leyenda.
10. Norte.
11. Escala.
12. Localizador.
13. Mapas de detalle.

Hay dos tipos de **cartografías**:

- **Cartografía base**: o fundamental o [[Topología|topográfica]]. Busca recoger con precisión *qué* hay sobre la Tierra, documentando sus características físicas. Es de carácter general. Es el "mapa de fondo".
- **Cartografía temática**: representa un tema concreto de cualquier índole. Se apoya en la cartografía base para ubicar la información temática en un contexto, y facilitar su comprensión.

![[Cartografía Base y Temática.png]]

Los mapas aportan información sobre la localización espacial de elementos o fenómenos, pasando de la realidad (3D) a un plano (2D). Describen un fenómeno que puede ser:

- Puntual.
- Lineal.
- Superficial o zonal.
- Volumétrico: pueden ser tangibles o solo una construcción mental.

El diseño cartográfico logra la transmisión de la información combinando una serie de **variables visuales**.

## Variables Visuales

Las **variables visuales** son un conjunto de parámetros gráficos que definen el carácter de un símbolo. Son medios visuales que varían los símbolos del mapa o muestran relaciones entre ellos.

Variables visuales:

1. **Posición**: su uso es muy restringido y particular.
2. **Tamaño**: dimensión del símbolo.
3. **Color**: es la más importante. Componentes: *valor*, *tono*, y *saturación*.

![[Color.png]]

4. **Textura**: es el relleno de un símbolo mediante algún patrón.
5. **Forma**: perímetro exterior de un objeto. Se suele aplicar a símbolos puntuales.
6. **Orientación**: grado de inclinación o giro.

![[Variables Visuales.png]]

Tipos de símbolos puntuales según su forma:

- **Pictóricos**: iconos expresivos.
- **Geométricos**: formas junto a una leyenda.
- **Asociativos**: dibujos y símbolos minimalistas.

Propiedades de las variables visuales (aunque no todas presentan todas):

1. **Asociativa**: cuando al aplicarse no aumenta ni disminuye la visibilidad del elemento.
2. **Selectiva**: cuando al aplicarse generan distintas categorías de símbolos.
3. **Ordenada**: cuando permite representar un orden (comparar valores mayores y menores).
4. **Cuantitativa**: cuando puede mostrar cantidades o proporciones.

![[Propiedades de las Variables Visuales.png]]

Tipos de información y su representación:

$$\text{Variables} \begin{cases}\begin{rcases} \text{Alfanuméricas}\end{rcases} \text{Información cualitativa} \\ \text{Numéricas} \begin{rcases}\begin{cases}\text{Nominal} \\ \text{Ordinal} \\ \text{Intervalos} \\ \text{Razones} \end{cases}\end{rcases} \text{Información cuantitativa}\end{cases}$$

El tipo de variable condiciona las operaciones que pueden realizarse con la componente temática del dato geográfico. También condiciona la variable visual a utilizar para comunicar la información:

![[Información Cualitativa y Cuantitativa.png]]

## Clases

Se pueden agrupar los valores en *clases*, lo cual es útil para categorizar y asignar simbología por categoría (y no valores individuales). La creación de clases requiere dos parámetros:

1. Número de clases distintas a crear.
2. Criterios para definir sus límites.

Métodos para crear clases de forma sistemática:

1. **Intervalos iguales**: $n$ clases de misma amplitud igual a $\frac{\max - \min}{n}$.
2. **Intervalos o rupturas naturales**: clasificación de cortes naturales con el algoritmo de Jenks. Esto maximiza las diferencias entre clases.
3. **Intervalos por percentiles**: todas las clases contienen el mismo número de observaciones.

Distintos métodos crean clases distintas, lo que afecta a la interpretación del mapa.

![[Clases.png]]

## Tipos de Mapas Temáticos

1. **Mapa de símbolos graduados**: muestra variaciones en el tamaño de los símbolos. El punto puede ser en un lugar dado o en el centro de gravedad de una superficie. Conviene usar 5 rangos creados con rupturas naturales.

![[Mapa de Símbolos Graduados.png]]

2. **Mapa de puntos**: cada punto es igual a otro, lo que permite mostrar la distribución geográfica de la información. Representa muy bien la *densidad* de los datos.

![[Mapa de Puntos.png]]

3. Mapa de Flujos: representan *trayectorias lineales* con símbolos lineales. Se pueden usar flechas para señalar direcciones. Se usan para rutas, ríos, tráfico aéreo, etc.

![[Mapa de Flujo.png]]

4. **Mapa de Isolíneas**: usa símbolos lineales para representar magnitudes cuando la magnitud hace referencia a un volumen que se distribuye por toda la superficie. Cada línea une puntos de igual valor. Suele ser apropiado para *variables continuas* e intervalos iguales de datos.

![[Mapa de Isolíneas.png]]

5. **Mapa Coroplético, Dasimétrico, e Isoplético**:
	- **Coroplético**: las cantidades se asignan a polígonos predefinidos.
	- **Dasimétrico**: las cantidades definen el polígono.
	- **Isoplético**: es un mapa de isolíneas con símbolos zonales para resaltar umbrales.

6. **Cartograma**: la información cualitativa se transmite *distorsionando* las unidades de superficie para que su tamaño represente la *magnitud* de la variable en cuestión.

![[Cartograma.png]]
