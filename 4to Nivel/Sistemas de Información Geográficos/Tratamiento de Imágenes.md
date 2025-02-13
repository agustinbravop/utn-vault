El **tratamiento de imágenes** es común en el proceso de [[Teledetección]]. Hay 3 tipos de procesos:

1. **Pre-procesamiento**: correcciones geométricas (de forma) y radiométricas (de valores).
2. **Mejoras o realces**: de punto y locales.
3. **Análisis y extracción de información**: visualizar, estimar parámetros físicos, operaciones morfológicas, y detectar elementos.

## Pre-Procesamiento

### Distorsiones Geométricas

Las _distorsiones geométricas_ son distorsiones de forma provocadas por los movimientos y oscilaciones del sensor, o por el relieve del terreno, etc.

La **rectificación** (similar a la _georreferenciación_) de la imagen consiste en:

1. Establecer los puntos de control.
2. Calcular las funciones de transformación.
3. Transferir los niveles digitales originales a la posición corregida.

La **ortorrectificación** es similar, pero también incluye la **elevación**. Su resultado final es una _ortofotografía_.

### Distorsiones Radiométricas

Las _distorsiones radiométricas_ son valores erróneamente registrados, o ruido presente en la imagen.

Para reconstruir los valores, es necesario recurrir a los píxeles circundantes o a otros elementos como el **histograma** de la imagen.

![[Tratamiento de Imágenes (Pre-procesamiento).png]]

## Mejoras o Realces

Las **operaciones de punto** son píxel a píxel, donde se aplica una transformación $\text{ND}' = f(\text{ND})$. Hay varias:

1. **Segmentación**: para destacar los elementos que nos interesan.
2. **Expansión del histograma**: busca mayor definición visual.
3. **Modificación de brillo y contraste**: mejora la visibilidad.
4. **Ecualización del histograma**: armoniza la distribución de luminosidad para que cada nivel del histograma tenga el mismo número de píxeles.

![[Operaciones de Punto.png]]

Por otro lado, las **operaciones locales** tienen en cuenta píxeles circundantes:

1. **Filtros**: pueden ser de:
   - **Suavizado**: o de paso bajo. Efecto de desenfoque, restando definición y eliminando ruido.
   - **Realce**: o de paso alto. Efecto de enfoque, aumentando la definición.
2. **Fusión de imágenes**: es una serie de procesos para integrar la información de varias [[Fuentes de la Información Geográfica]] en una única imagen, englobando las características más destacables de las imágenes originales.

![[Operaciones Locales.png]]

## Análisis y Extracción de Información

En la **visualización**, se convierten los niveles digitales en colores interpretables. Hay imágenes:

- **Habituales**: pueden ser de una banda (representación en escala de grises), o de tres bandas (representación con el modelo RGB).
- **Multiespectrales**: se toman las 3 bandas más relevantes y se las asocian a los canales RGB, creando una "imagen de falso color".

Las **operaciones morfológicas** modifican las formas presentes en la imagen para facilitar operaciones posteriores. Por ejemplo, la operación de cierre ensancha líneas de píxeles para conectar objetos.

![[Operación de Cierre.png]]

La **estimación de parámetros físicos** se basa en el concepto de _firma espectral_. Según la propiedad a conocer o elemento a detectar, será una u otra longitud de onda la que aporte una información más relevante.

1. **Vegetación**: los índices de vegetación permiten detectar la presencia y actividad de plantas debido a su **fotosíntesis**, la cual provoca alta respuesta en la zona del infrarrojo. Las diferencias en el contenido de agua pueden indicar especies diferentes. Índice de Vegetación de Diferencia Normalizada: $\text{NDVI} = \frac{(\text{NIR} - \text{red})}{(\text{NIR} + \text{red})}$.

![[Vegetación.png]]

2. **Suelo**: la reflectancia se ve afectada por factores como la humedad, textura, materia orgánica, y composición minerológica. Se detecta gracias a que la reflectancia aumenta entre el espectro visible y la zona del infrarrojo medio.

![[Suelo.png]]

1. **Agua**: sirve para localizar elementos hidrográficos, temperatura, compuestos químicos, etc. Esto sirve para el estudio de mares, océanos, nieve, y hielo.

La **detección de elementos** consiste en identificar elementos que pueden ser zonales, lineales, o puntuales.

Dado un conjunto de elementos, la **clasificación de imágenes** los agrupa en clases homogéneas en cuanto a los elementos suyos. Métodos de clasificación:

- **Supervisada**: se debe añadir información adicional.
- **No supervisada**: solo requiere las [[Capa de Información Geográfica|capas]] y el número de clases.
