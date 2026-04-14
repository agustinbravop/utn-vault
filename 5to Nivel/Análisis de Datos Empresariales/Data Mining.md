**Data mining** (DM) es el análisis de conjuntos de datos observacionales para encontrar relaciones no especificadas y resumir los datos de manera novedosa. Es la extracción de información implícita, previamente desconocida y potencialmente útil de los datos.

**Machine learning** se refiere a la detección de patrones en los datos. En el [[Análisis de Datos Empresariales]], ML se centra en problemas de clasificación, mientras que DM es más amplio. Se necesita en el [[Análisis de Datos Moderno]] porque estamos sobrepasados por la cantidad de datos.

El trabajo del científico de datos es buscar patrones en los datos. 

Las técnicas de DM se aplican sobre datos ya almacenados. No influye en la recolección ni en la medición de los datos, por lo que es un análisis "secundario".

## Metodologías para Minería de Datos

1. **CRISP-DM**: Cross Industry Standard Process for Data Mining.
![[CRISP-DM.png]]
2. **KDD**: Knowledge Discovery in Databases.
![[KDD.png]]
3. **SEMMA**: centrada en el desarrollo del proceso de data mining.
   Sample $\longrightarrow$ Explore $\longrightarrow$ Modify $\longrightarrow$ Model $\longrightarrow$ Assess.

## Modelos de Data Mining

Tipos de modelos:

1. Clasificación.
2. Regresión.
3. Pronóstico.
4. Agrupamiento (clustering).
5. Reglas de asociación.
6. Secuenciación.

Machine learning:
- Aprendizaje supervisado:
	- Clasificación.
	- Regresión.
- Aprendizaje no supervisado:
	- Análisis cluster.
	- Reducción de dimensiones.

En el *análisis exploratorio*, para entender los datos, se detectan las variables predictoras: las que mejor discriminan los valores de las variables dependientes.

Las variables pueden tener problemas:

1. **Outliers**: datos inconsistentes o desviados altamente de la media.
2. **Valores ausentes**: pérdida de información.
3. **Variables con varianza cercana a cero**: es casi una constante, por lo que no sirve.

En aprendizaje automático (ML), el conjunto de datos se divide en un conjunto de entrenamiento (70%) y un conjunto de testeo (30%).

Para crear un modelo predictivo: Conseguir datos $\longrightarrow$ Preparar datos $\longrightarrow$ Elegir modelo $\longrightarrow$ Modelar $\longrightarrow$ Testear modelo $\longrightarrow$ Usar modelo.

### Técnicas de Medición de la Calidad de un Modelo Supervisado

1. **No Information Rate**: NIR. Mejor estimación posible sin información.
2. **Matriz de confusión**: tabla cruzada de clases reales y predicciones. Métricas útiles:
	- Exactitud.
	- Sensibilidad.
	- Especifidad.
	- Precisión.
	- Valor de predicción negativa.
	- Prevalencia.
	- Tasa de detección.
	- Prevalencia de detección.
	- Precisión balanceada.
	- Kappa.
	- Mcnemar's Test P-Value.
3. **Curva ROC**: optimizar el área bajo la curva ROC.
4. **Curva lift**.
