Identificar el **canal de suministro** adecuado es una decisión esencial en el proceso de [[Provisión de SI y TI]]. Responde a la pregunta "¿De **dónde obtener** el HW y SW?" El HW siempre es fuente externa, pero para el SW es más complejo.

![[Continuo de alternativas de obtención de SW.png]]

La comparativa entre [[Desarrollo Interno de SW]] y comprar [[Paquetes Estándar]] de soluciones es una negociación entre **control y flexibilidad contra certidumbre y plazos breves**.

Si al final de esta etapa se decide la **adquisición de SW**, se debe utilizar un [[Método de Evaluación de Paquetes Estándares]].

![[Canal de Obtención de SW 2024-05-10 15.26.54.excalidraw]]

Existen muchas **técnicas para la determinación** del canal de obtención más adecuado. Vemos una que se basa en una lista de criterios y un análisis de riesgos.

## 1. Lista de Criterios

Son criterios sujetos a la situación particular de la organización. Ni exclusivos ni excluyentes. No son criterios del SW, sino que evalúan aspectos del canal de obtención de SW que tendrán impacto empresarial.

- **Costo**: justificar el gasto desde la relación costo/beneficio.
- **Disponibilidad**: tiempo hasta la puesta en operación y uso del SW.
- **Especificidad**: satisface necesidades específicas a nuestra organización.
- **Mantenimiento**: responsabilidad y facilidad de hacer modificaciones correctivas.
- **Modificaciones**: flexibilidad del SW para hacer modificaciones adaptativas y perfectivas.
- **Documentación**: código fuente legible, manual de usuario, documentación entendible.
- **Utilización de recursos**: cómo utilizará a los recursos del área de SI para las operaciones diarias.

## 2. Análisis de Alternativas de Obtención

Una vez determinados todos los canales posibles:

1. Determinar un **subconjunto de criterios** que serán la base de la evaluación.
2. Asignar **pesos** a cada criterio según su **importancia relativa**. (se distribuyen un 100%)
3. Asignar **puntajes** a cada combinación alternativa-criterio según una **escala** definida.
4. Calcular **resultados** para cada alternativa. $\sum puntaje * peso$

La alternativa con mayor puntaje será el canal de obtención de SW que mejor satisface los requerimientos de la empresa. Ejemplo:

![[Tabla de evaluación entre alternativas de obtención.png]]

## 3. Análisis de las Probabilidades de Éxito y Riesgo

Otra comparación que sirve para descartar opciones que tienen un riesgo con **alta probabilidad** de suceder y un **alto impacto estratégico** asociado:

1. Determinar los **factores de riesgo**. (ej: escaso mantenimiento, sobreutilización de recursos)
2. Asignar a cada riesgo una **probabilidad de ocurrencia** (**Alta, Media, Baja**) y un puntaje similar por el **impacto** que tendrá en la organización (**Alto, Medio, Bajo**).
3. Obtener los totales.
4. Seleccionar la alternativa de menor impacto o riesgo.
5. **Descartar las opciones con alta probabilidad y alto impacto en un factor de riesgo.**
