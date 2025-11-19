Este modelo de [[Redes Neuronales]] está inspirado en la neuroplasticidad del cerebro. T. Kohonen desarrolló el modelo basado en el **comportamiento autoasociativo**. Hay dos variantes:

- **LVQ**: Learning Vector Quantization. Es unidimensional (analizamos este modelo).
- **TPM**: Topology-Preserving Map (o SOM). Es bidimensional/tridimensional.

![[Self-Organizing Maps.png]]

Este no es un modelo backforward ni autorecurrente. Cada una de las $N$ neuronas de entrada se conecta con las $M$ neuronas de salida. Entre las neuronas de salida hay **relaciones laterales de inhibición**, que son como "conexiones" implícitas sin peso. Los valores que se asignan a los pesos dependerán de la interacción lateral.

La influencia que ejerce una neurona sobre las demás es función de la **distancia** entre ellas, siendo muy poca cuando están alejadas. La **zona de influencia** se calcula mediante una **función de vecindad**.

Cuando se presenta una información:

$$\begin{align}
E_k &= \left(e^{(k)}_1, \dots, e^{(k)}_N \right) \\
s_j (t+1) &= f\left(\underbrace{\sum^N_{i=1} w_{ji} \cdot e_i^{(k)}}_\text{net} + \underbrace{\sum^M_{i=1} Int_{pj} \cdot s_p(t)}_\text{interacciones} \right)
\end{align}$$

El entrenamiento tiene dos fases:

1. **Competencia**: consiste en activar una sola **neurona ganadora**, aquella que tenga sus pesos más parecidos a la entrada.

$$s_j = \begin{cases}1 & \min ||E_k-W_j|| = \min \left( \sqrt{\sum^N_{i=1} \left(w_{ji} - e^{(k)}_i\right)^2}\right) \\
0 & \text{el resto de neuronas} \end{cases}$$

2. **Colaboración**: se adaptan los pesos de la neurona ganadora y los pesos de las neuronas más cercanas a ellas.

**Los valores finales de los pesos se corresponderán con los valores del patrón de entrada que consigue activar la neurona correspondiente.**

La etapa de entrenamiento sigue refinando el mapa hasta que las neuronas de salida representan específicamente una zona del espacio de entradas. Se quiere que los pesos queden estables.

## Algoritmo

1. Inicializar los pesos $w_{ji}$ con valores aleatorios pequeños. Fijar la zona de vecindad inicial.
2. Presentar un vector de entrada $E_k$.
3. Determinar la neurona ganadora:

$$d_j = \sum_{i=1}^N \left(w_{ji} - e^{(k)}_i\right)^2 \ \ \ \ \text y \ \ \ \ d_{j^*} = \min(d_j)$$

4. Actualizar los pesos:

$$w_{ji}(t+1) = w_{ji}(t) + \alpha (t) \ h_{ji}(t) \left[\underbrace{e^{(k)} - w_{ji}(t)}_\text{error}\right]$$

Siendo $h_{ji}(t) = e^{\frac{-d_{ji}^2}{2\sigma^2(t)}}$ la **función de vecindad gaussiana** y $\alpha(t)=\frac{1}{t}$ el **coeficiente de aprendizaje** (donde un $1/t\to 0$ ayuda a evitar oscilaciones y acelerar la convergencia).

La función de vecindad representa la influencia lateral entre neuronas de salida. Es común usar la función o distribución gaussiana. También se puede usar vecindad nula (implica un modelo sin cooperación).

Gráficamente, los pesos del SOM se van acercando al os patrones presentados conforme avanza el entrenamiento de la red. 

Una vez entrenada la red, ya no se usa la fase de cooperación. El SOM agrupa cada patrón nuevo en uno de los grupos ya formados durante el [[5to Nivel/Inteligencia Artificial/Aprendizaje|Aprendizaje]]. No se trata de clasificación sino de **agrupamiento**.
