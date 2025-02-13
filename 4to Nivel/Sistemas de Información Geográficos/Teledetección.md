La **teledetección** es la ciencia y arte de obtener información de un objeto, al medir _perturbaciones_, a través del análisis de los datos adquiridos mediante algún dispositivo que no está en contacto físico con el objeto. Es una de las [[Fuentes de la Información Geográfica]].

Se divide en dos partes:

1. Adquirir las imágenes mediante sensores.
2. Procesar, interpretar, y tratar las imágenes.

![[Teledetección.png]]

El resultado será una [[Capa de Información Geográfica]] con [[Representación Raster]].

Elementos del proceso de teledetección:

1. **Fuente de radiación**: puede ser natural o artificial. El terreno perturba la radiación.
2. **Objetos**: que emiten o interactúan con la radiación.
3. **Atmósfera**: por la cual se desplaza la radiación.
4. **Receptor**: que recoge la radiación perturbada o emitida.

![[Elementos en la Teledetección.png]]

Los píxeles de la imagen final contienen un valor que indica la intensidad de la radiación, para cierta parcela y en cierta banda del [[Señales y Espectros|espectro electromagnético]].

El _nivel digital_ es el valor entero que indica el nivel de radiación dentro de una escala definida. Suele ir del 1 al 256. Asociado a cada píxel de la imagen, hay un nivel digital (_Digital Number_, DN) que mide la radiancia promedio correspondiente al área de ese píxel.

La _radiación electromagnética_ es producto de las alteraciones en el campo electromagnético, el cual es un fenómeno ondulatorio. Tiene un período $T$ y una longitud de onda $\lambda$.

El _espectro electromagnético_ es la **distribución energética** de las [[Ondas Electromagnéticas]]. Una imagen con varias bandas contiene información sobre la intensidad de la radiación reflejada en distintas partes del espectro.

![[Espectro Electromagnético.png]]

La **_firma espectral_** es la respuesta característica de un tipo de objeto dentro del espectro electromagnético. Depende de las características físicas y químicas del objeto, las cuales varían según su longitud de onda.

## Plataformas

La _plataforma_ es el medio en el que se sitúa el sensor y desde el cual se observa. Es un elemento tecnológico del sistema de teledetección. Tipos:

- Dentro de la atmósfera: en su mayoría **aviones**.
- Fuera de la atmósfera: principalmente **satélites**.

![[Plataformas para la Teledetección.png]]

Las plataformas condicionan las mediciones efectuadas por el sensor, ya que establecen la distancia entre el sensor y el elemento registrado en la superficie terrestre:

- **Aviones**: son las plataformas clásicas. Ofrecen mayor disponibilidad, pero dependen del clima y no abarcan superficies muy amplias.
- **Satélites**: no pueden dirigirse a voluntad debido a su [[Órbitas|órbita]], la cual está definida por parámetros orbitales, pero cubren grandes zonas de terreno.

## Sensores

El _sensor_ es el elemento tecnológico del sistema de teledetección que capta la radiación y registra su intensidad. Hay de dos tipos:

- **Activos**: transmiten sus propieas emanaciones electromagnéticas. Pueden trabajar bajo cualquier condición atmosférica. La variable que se mide es el tiempo que la radiación tarda en volver. Del tiempo se deduce la _distancia_, y de ella se deduce el _relieve_ del terreno. Ejemplos:
  - **RADAR**: _Radio Detection and Ranging_.
  - **LiDAR**: _Light Detection and Ranging_.
- **Pasivos**: aprovechan fuentes de radiación naturales (el sol). Esto incluye la mayoría de satélites que manejan bandas del espectro visible.

## Resolución

La **resolución** es la habilidad de un sensor de discriminar información de detalle. Hay cuatro tipos:

1. **Resolución espacial**: son las dimensiones registradas en la mínima unidad de información incluida en la imagen, denominada **_píxel_**. Existen compañías que suministran imágenes satelitales de alta resolución. De acuerdo a la resolución espacial, cambia el uso que se le puede dar a la imagen.

![[Resolución Espacial.png]]

2. **Resolución espectral**: es el **número y anchura de las bandas espectrales** que puede discriminar el sensor. Hay sensores _multiespectrales_.

![[Resolución Espectral.png]]

3. **Resolución radiométrica**: es la sensibilidad del sensor ante variaciones en la radiación que percibe. Es el **número de niveles digitales** distintos que pueden recogerse. Determina el número de bits utilizados en cada píxel.

![[Resolución Radiométrica.png]]

4. **Resolución temporal**: es la periodicidad con la que el sensor adquiere imágenes de la misma porción de la superficie. Es el **tiempo de revisita** (puede ser horas o días).

![[Resolución Temporal.png]]

Hay un conflicto de intereses entre estas resoluciones, por lo que se necesita encontrar un balance. Ejemplos:

- Para lograr mayor resolución temporal, se necesita una órbita más alta, lo cual empeora la resolución espacial.
- Una resolución espacial menor permite una mayor resolución radiométrica y/o espectral.
