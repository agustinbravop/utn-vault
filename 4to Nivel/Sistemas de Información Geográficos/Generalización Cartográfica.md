La **generalización cartográfica** se refiere a representar un dato a una [[Fundamentos Cartográficos y Geodésicos#Escala|escala]] diferente de la que le corresponde en realidad. 

Ampliar [[Mapas]] sin agregar detalle o encogerlo sin sacar detalle es incorrecto porque genera una representación inadecuada y confusa. El detalle innecesario genera una densidad excesiva de información.

El ojo humano solo distingue hasta 0.2 mm. Algo más pequeño debe ser agrandado. 

La generalización es importante para el rendimiento del [[Sistema de Información Geográfica]] y la visualización. Es un proceso que busca:

1. Producir una imagen cartográfica legible.
2. Reducir el contenido a solo lo necesario.
3. Enfatizar lo importante y suprimir distracciones.

Las **operaciones de generalización** más relevantes son:

1. **Simplificación**: se sustituyen los elementos originales por otros más sencillos. Optimiza las operaciones con los datos.
2. **Agregación**: un conjunto de muchos elementos se reemplaza por otro conjunto con menos elementos.
3. **Suavizado**: se sustituyen formas angulosas por otras más suaves.
4. **Exageración**: se exagera su tamaño para que pueda interpretarse con mayor facilidad.
5. **Desplazamiento**: un objeto se mueve a otra posición para garantizar su visibilidad.

La generalización es importante en un SIG por la variedad de escalas de la [[Información Geográfica]] con la que se trabaja. Busca resolver el manejo de grandes volúmenes de datos con gran precisión a una escala de menor detalle.

Tipos de generalización:

- **Al vuelo**: trabaja con todo el conjunto de datos y generaliza a medida que se necesita. Esto resulta poco óptimo por la demora de los algoritmos.
- **Multiescalar**: se maneja información de una misma zona a diferentes escalas ya procesadas. Se usa en cada momento la escala más conveniente. Esto es similar a físicamente tener varios mapas.

![[Enfoque Multiescalar.png]]

En los SIG se añade un aspecto de rendimiento/optimización a la generalización.

En el caso de imágenes a representar por pantalla con píxeles, se las puede pensar como una generalización "al vuelo", aunque ajustar la escala puede ser lento en imágenes de gran tamaño, Es conveniente que el SIG prepare varias versiones de la imagen para luego recurrir a la más conveniente (enfoque multiescalar).
