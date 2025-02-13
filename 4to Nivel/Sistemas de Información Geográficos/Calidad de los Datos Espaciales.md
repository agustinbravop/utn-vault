> "La [[Calidad]] es la propiedad o conjunto de _propiedades inherentes_ a una cosa que permiten apreciarla como igual, mejor o peor que las restantes de su especie". - RAE

> "La calidad es el grado en que un conjunto de características inherentes cumple con los requisitos". - ISO 9000.

En un [[Sistema de Información Geográfica]], los **datos espaciales de calidad** son aquellos que puedan servir para **alcanzar los objetivos** de un proyecto. La calidad _depende_ del proyecto.

Hay que conocer el _tipo_ de error y su _magnitud_ para gestionar el error y ser conscientes de las _limitaciones_ de los datos con los que se trabaja. Esto permite realizar el trabajo de la mejor manera posible, considerando que se trabaja con un conjunto de datos que tiene cierto error.

Utilizar datos de mala calidad produce resultados de mala calidad. Los [[Metadatos para la Información Geográfica]] son elementos clave para encontrar datos de calidad.

El _error_ es la discrepancia entre el valor real y el valor recogido en una [[Capa de Información Geográfica]]. Puede ser:

- **Sistemático**: se produce en todas las mediciones. Es predecible.
- **Aleatorio**: se produce por eventos no controlables. Afecta a la precisión.

La _precisión_ es el número de dígitos significativos de una medida. Indica la repetibilidad o nivel de detalle.

La _exactitud_ es el grado en que los valores estimados se asemejan al valor real.

![[Exactitud y Precisión.png]]

Si corregimos todos los errores sistemáticos, entonces la exactitud es igual a la precisión.

La _incertidumbre_ refleja la medida en que no podemos tener certeza de la validez de nuestros datos. Se compone por:

1. **Error**.
2. **Vaguedad**: definiciones pobres o incompletas.
3. **Ambigüedad**: cuando no hay definiciones inequivocas.

Modelar la incertidumbre es una alternativa a modelar el error.

Puede haber errores en varios procesos:

1. Recogida de datos.
2. Captura de datos.
3. Almacenamiento.
4. Manipulación.
5. Salidas cartográficas.
6. Uso de los resultados.

Hay errores:

- De concepto y modelo.
- En las [[Fuentes de la Información Geográfica]] primarias.
- En los procesos de creación de la capa.
- En los procesos de análisis.

**Componentes de la calidad** recopiladas en varios estándares, donde cada una de estas características es susceptible de incorporar errores;

1. **Exactitud posicional**: es la cercanía a la posición verdadera.
2. **Exactitud de atributos**: es la cercanía al valor verdadero de la componente temática.
3. **Consistencia lógica**: el dato respeta el formato de la definición.
4. **Coherencia [[Topología|topológica]]**: la relación entre los datos tiene sentido topológico.
5. **Completitud**: frente a las necesidades que ha de cubrir un producto.
6. **Linaje**: procedencia del dato. Registra la historia de las [[Bases de Datos Espaciales]] usadas.
7. **Exactitud temporal**: relevancia actual o _vigencia_ de los datos.
8. **Accesibilidad**: facilidad de encontrar y disponer de datos espaciales.

Tipos de errores:

- **Cualitativos**: modifican la conclusión o interpretación del dato.
- **Cuantitativos**: solamente son un desvío respecto del valor real.

![[Erroes Cualitativos y Cuantitativos.png]]
