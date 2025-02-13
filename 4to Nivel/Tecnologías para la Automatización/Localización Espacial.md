En la [[Robótica]], un robot industrial necesita interactuar con el espacio que lo rodea. Para esto, es necesario posicionar la muñeca/garra de su brazo en un punto tridimensional, utilizando los grados de libertad del robot. La **localización espacial** resuelve este problema, mediante:

1. **Odómetro**: usar [[Sensores]] como _encoders_ en ruedas.
2. **GPS local**: usado en entornos exteriores, con no mucha precisión.
3. **LiDAR**: permite crear un mapa 3D del entorno.
4. **SLAM**: _Simultaneous Location and Mapping_.
5. **Visión por computadora**: usar cámaras que ven el entorno.

Alternativamente, la **cinemática de posición** hace una descripción analítica del movimiento espacial del robot como una función respecto del tiempo.

El **problema cinemático** se puede definir de dos maneras:

- **Directo**: conociendo los _parámetros geométricos_, se busca determinar la posición y orientación del extremo del robot con respecto a unas coordenadas de referencia.
- **Inverso**: dada una cierta _posición_ y _orientación_, se determina la configuración geométrica que debe adoptar el robot para alcanzarla.

![[Localización Espacial.png]]

Este problema se resuelve con [[Herramientas Matemáticas para la Localización Espacial]]. Esto tiene aplicaciones prácticas en:

1. Robots industriales.
2. Vehículos autónomos.
3. Robots de servicio.
4. Drones.

## Cinemática Directa

La **cinemática directa** (_Direct Kinematics_) estudia el movimiento de los componentes físicos del robot sin considerar las fuerzas que lo causan.

Se calcula la posición y orientación final del extremo de un robot a partir de sus parámetros arituclares. Modelos matemáticpos:

- Matrices de transformación homogénea.
- Parámetros de Denavit-Hartenberg (DH), que sirven para definir y traducir puntos y rotaciones.

## Cinemática Inversa

La **cinemática inversa** (_Inverse Kinematics_) es más difícil ya que las ecuaciones son no lineales, y surgen preguntas sobre la existencia de una solución o múltiples soluciones (¿Cuál es la óptima?).

Cuando no se puede lograr una solución analítica, se usan métodos numéricos.

Modelos de movimiento:

- Modelo diferencial.
- Jacobiano (una matriz que representa los cambios necesarios en el vector $X_0$ para llegar a $X_T$).

Control del movimiento:

1. **[[Controladores#Acción de Control PID|Controladores PID]]**: para mantener la precisión y [[Estabilidad]].
2. **Control predictivo**: usa modelos del sistema.
3. **Control de impedancia y admitancia**: para la interacción segura.
4. **Algoritmos de planificación de trayectorias**: como RRT o A\*.
