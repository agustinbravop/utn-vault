El origen de los datos en un [[Sistema de Información Geográfica]] es muy variado y con **formatos distintos**. La metodología de la recolección condiciona la forma en la que los datos llegan a nosotros, su uso, y las operaciones con las que adaptarlos.

La recolección de [[Información Geográfica]] es un ámbito complejo con muchas alternativas que un SIG debe integrar.

Ventajas de los datos digitales frente a los analógicos:

1. Sencilla actualización.
2. Fácil distribución.
3. Análisis fácil y preciso.
4. Mantenimiento fácil.
5. Menor espacio de almacenamiento.

**Fuentes** de datos:

- **Primarios**: son aquellos que ya están en un formato que podemos emplear en un SIG.
- **Secundarios**: se deben adaptar, dado que en su forma original no son adecuados para usarse en un SIG.

![[Fuentes de la Información Geográfica.png]]

Vemos ahora algunas fuentes importantes.

## Teledetección

La **[[Teledetección]]** es una técnica de adquisición y tratamiento digital de imágenes para recopilar datos a usar en análisis de la superficie terrestre y el entorno.

No requiere contacto físico: mide las _perturbaciones_ que el objeto provoca en su entorno. Consiste en dos partes:

1. Adquisición de las imágenes mediante sensores.
2. Tratamiento de las imágenes adquiridas para identificar elementos.

## Topografía

La **topografía** es la ciencia que estudia el conjunto de procedimientos disponibles para **determinar la posición de un punto** sobre la superficie de la Tierra, tanto en planimetría como en altimetría, por lo general referido a un [[Sistema de Referencia de Coordenadas#Marcos de Referencia|marco de referencia]].

El **levantamiento topográfico** es un estudio técnico y descriptivo de un terreno, para representarlo _topográficamente_.

![[Levantamiento Topográfico.png]]

Antiguamente se usaban reglas trigonométricas para medir distancias. Hoy en día se utilizan dispositivos electrónicos.

## Cartografía Impresa

Antiguamente la cartografía impresa era la única fuente que se tenía. Es una fuente secundaria, aunque sigue siendo básica para trabajar con un SIG porque hay mucha información que sigue sin estar digitalizada.

Los [[Mapas]] o planos tienen varias variables en un único documento, las cuales conviene desagregar dependiendo de su uso. Una fotografía aérea puede servir como una [[Capa de Información Geográfica]] con [[Representación Raster]], o para identificar elementos discretos con [[Representación Vectorial]].

La **digitalización** de la cartografía impresa puede ser:

- **Manual**: requiere un operador que defina explícitamente los elementos a crear. Solo da un resultado vectorial.
- **Automática**: el sistema genera los datos digitales. Escaneo para datos raster, semiautomático para datos vectoriales.

En lo posible, se debe mantener la calidad original, pero esto no siempre es posible. Causas de errores:

1. Precisión del equipo utilizado.
2. Habilidad y experiencia del operario.
3. Fuentes originales con errores.
4. Errores derivados del proceso.

Los SIG tienen funcionalidades de edición para evitar estos errores al digitalizar. Por ejemplo, snapping.

### Digitalización Manual

Es una forma sencilla de crear una capa vectorial. Se puede hacer de dos maneras:

- **Heads-down**: usar un equipo especializado en digitalización, con una tableta digitalizadora.
- **Heads-up**: usar las funciones de edición de un SIG (digitalización en pantalla).

![[Digitalización Manual Heads-down.png]]

Ventajas:

1. Menor coste.
2. Posibilidad de dividir el trabajo.
3. Posibilidad de ampliación (zoom).
4. Mayor precisión.

### Digitalización Automática

El _escaneo_ consiste en utilizar un scanner que toma una imagen impresa y la convierte en una foto digital. Luego, a esta capa raster se le deben asignar coordenadas (_georreferenciación_).

La _vectorización_ se puede hacer:

- En base a una imagen digital, con un software de reconocimiento de imágenes.
- Con dispositivos específicos y un documento analógico.

![[Vectorización.png]]

Usualmente este proceso es menos preciso que la digitalización manual, por lo que se suelen aplicar correcciones posteriores.

La _rasterización_ es un proceso sencillo, pero supone una pérdida de exactitud.

![[Rasterización.png]]

## Geocodificación

La **geocodificación** es la digitalización directa de valores y coordenadas, sin necesidad de dispositivos especializados o elementos gráficos.

Se parte de una serie de datos espaciales expresados alfanuméricamente susceptible de convertirse en una capa. **Se asignan coordenadas a puntos de interés**.

La procedencia de los datos puede ser variada (por ejemplo, trabajos de campo). Si están en formato analógico, se pueden digitalizar. En formato digital, son archivos que un SIG lee para usar las coordenadas que contienen.

El objetivo suele ser crear una nueva capa de **puntos con coordenadas**.

## Fotogrametría

La **fotogrametría** es una técnica para estudiar y definir con precisión la forma, las dimensiones, y la posición en el espacio de un objeto, usando las medidas hechas sobre fotografías del objeto.

La fuente de información es la _fotografía_.

Fotogrametría vs topografía:

- Sustituir el trabajo de campo por trabajo de oficina.
- Permitir levantar zonas extensas o de difícil acceso.
- Levantamientos más homogéneos.

Secuencia de trabajo:

1. Realización del vuelo fotogramétrico.
2. Apoyo fotogramétrico del vuelo.
3. Restitución y rectificación fotogramétrica.

La _restitución_ es el proceso de conformar los _pares estereoscópicos_ (imágenes del mismo lugar tomadas desde distintos puntos de vista), y posterior procesamiento.

No existe una clara frontera entre fotogrametría y teledetección.

## Sistemas GNSS

El [[GPS]] (Sistema de Posicionamiento Global) es el más extendido de los **sistemas GNSS**. Permiten **posicionar objetos** sobre la superficie terrestre en términos absolutos, no solo en relación a otros.

Se pueden usar en todo el mundo bajo cualquier clima las 24 horas.

## Información Geográfica Voluntaria

La VGI (_Volunteered Geographical Information_) es el uso de internet para crear, gestionar, y difundir información geográfica aportada **voluntariamente** por **usuarios** de la propia red.

Son iniciativas en las que el usuario de a pie, sin formación como [[Fundamentos Cartográficos y Geodésicos|cartógrafo]], puede aportar sus datos voluntariamente. Es un **cambio social y filosófico** que redefine la creación del dato geográfico, y le abre las puertas a un amplio grupo de personas.

Surge gracias a los receptores GPS de bajo costo y a los conceptos participativos de la web 2.0.
