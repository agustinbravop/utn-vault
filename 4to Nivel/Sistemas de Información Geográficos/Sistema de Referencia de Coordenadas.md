Un _sistema de coordenadas geográficas_ define dos ángulos medidos desde el centro de la Tierra para **expresar posiciones** en su superficie.

- **Latitud**: mide el ángulo entre cualquier punto de la superficie y el Ecuador.
- **Longitud**: mide el ángulo a lo largo del Ecuador partiendo del meridiano de Greenwich.

![[Sistema de Coordenadas Geográficas.png]]

Los **sistemas de referencia de coordenadas** dan el soporte matemático necesario para **asignar coordenadas** a puntos medidos sobre la superficie terrestre.

Parten de definiciones basadas en mediciones y son necesarios para establecer la posición de puntos que respondan a un sistema de coordenadas con un origen.

Un _sistema local_ se puede definir con un punto Datum de origen donde coinciden la normal al [[Fundamentos Cartográficos y Geodésicos#Forma de la Tierra|elipsoide]] y al geoide. Es _planimétrico_, sin alturas asociadas.

Un _sistema global_ tiene su origen coincidente con el _geocentro_ (el centro de masa de la Tierra). Define los siguientes ejes:

1. Eje $Z$: paralelo a la dirección del polo (para una época dada).
2. Eje $X$: coincidente con el plano meridiano de Greenwich (para una época dada).
3. Eje $Y$: situado en el plano ecuatorial. Es perpendicular al plano $XZ$.

Para pasar a coordenadas geográficas (latitud, longitud), se aplica una _transformación_ tal que $(X,Y,Z)\longrightarrow (\text{lat}, \text{long}, \text{altura})$. Algo similar se hace para cambiar entre [[Proyecciones Cartográficas]].

## Marcos de Referencia

Un **marco de referencia** es la materialización de un sistema de referencia constituido por las coordenadas de una **red de puntos** que lo definen.

![[Marcos de Referencia.png]]

Las coordenadas de los puntos son consistentes entre sí para una época dada. Las medidas de los puntos se realizan con mojones, estaciones, etc.

No existe una única manera de **referenciar geográficamente** un objeto. Por ende, el EPSG crea el _EPSG Geodetic Dataset_: un repositorio de datos para identificar coordenadas tal que describan posiciones sin ambigüedades.

Por ejemplo, el código EPSG:4326 identifica al elipsoide WGS84 utilizando coordenadas en grados con el meridiano de Greenwich como meridiano central (de longitud 0).

En Argentina, la proyección oficial es la Gauss-Kruger. El ente responsable es el IGN, y el marco actual es el POSGAR 07, que materializa al WGS84.

Gauss-Kruger divide al país en 7 _fajas_ de 3° cada una. El Chaco está entre la 4 y la 5. Los códigos EPSG correspondientes son 2217X, siendo X la faja (de 1 a 7).

![[POSGAR 07.png]]
