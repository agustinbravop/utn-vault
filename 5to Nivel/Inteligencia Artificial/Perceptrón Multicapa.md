El **Perceptrón Multicapa** (MLP) es un tipo de [[Redes Neuronales]] similar a un [[Perceptrón]] simple pero con mayor cantidad de neuronas. Solucionan el problema de que los perceptrones simples solo pueden aprender funciones linealmente separables.

## Regla Delta

La **regla delta** o *Least Mean Squared* (LMS) es el método para hallar el vector de pesos $W$ deseado. Siendo $d$ la salida deseada, $s$ la salida obtenida, y $L$ el número de patrones, se minimiza el **error cuadrático medio** definido como:

$$<\epsilon^2_k>=\frac{1}{2L} \sum^L_{k=1} \epsilon_k^2 = \frac{1}{2L} \sum^L_{k=1} (d-s)^2$$

Las modificaciones en los pesos son proporcionales al **gradiente decreciente** del error:

$$\begin{align}\Delta w_i &= - \alpha \frac{\partial<\epsilon^2_k>}{\partial w_i} = - \alpha \frac{\partial<\epsilon^2_k>}{\partial s_k} \frac{\partial s_k}{\partial w_i} = \dots = \alpha \ \epsilon_k \ x_{ki} \\
w_i (t+1) &= w_i (t) + \alpha (d_k - s_k) x_{ki}
\end{align}$$

El error cuadrático medio se calcula al final de cada época teniendo en cuenta cada error de patrón $\epsilon_k$ obtenido al aplicar un patrón individual.

### Regla Delta Generalizada

La regla delta generalizada (*backpropagation*) permite entrenar redes neuronales con capas ocultas. Las funciones de activación deben ser crecientes, continuas y derivables.

$$\begin{align}
\Delta w_{ji} (t+1) &= \alpha \ \delta_{pj} \ y_{pi} \\
\text{donde }  \ \ \delta_{pk} &= (d_{pk} - y_{pk})  f'(net_k) \ \ \text{ si es una capa de salida} \\
\text{o bien }  \ \ \delta_{pj} &= (\sum_k d_{pk}\ w_{kj})  f'(net_k) \ \ \text{ si es una capa oculta}
\end{align}$$

El **error de patrón** y **error global** resultan:

$$E_p=\frac{1}{2} \sum_{k=1}^M (d_{pk} - y_{pk})^2  \ \ \text{ y } \ \ E_g=\frac{1}{L} \sum^L_{j=1}E_{p_j}$$

## Control de Convergencia

Dado un dataset dividido en dataset de entrenamiento y dataset de validación, se tiene un error global asociado al entrenamiento y un **error de validación**. Estos errores deberían ser similares.

Si el error global y el error de validación divergen antes de que termine el entrenamiento, puede haber **sobreajuste** (*overfitting*). Esto es un comportamiento no deseado que provoca que el modelo no se generalice bien a nuevos datos. El modelo **tiene que generalizar bien**, por lo que el overfitting es un problema.

Para solucionar el overfitting se debe ajustar el modelo o su entrenamiento:

- Cambiar la inicialización de los pesos.
- Cambiar la función de transferencia.
- Cambiar la cantidad de capas.
- Cambiar la cantidad de neuronas por capa.

## Momento

Se puede agregar un **término momento** en la regla delta generalizada:

$$\begin{align}
w_{ji} (t+1) &= w_{ji}(t) + \alpha \ \delta_{pj} \ y_{pi}  + \beta \ (w_{ji}(t) - w_{ji}(t-1)) \\
\Delta w_{ji} (t+1) &= \alpha \ \delta_{pj} \ y_{pi} \ + \beta \ \Delta w_{ji}(t) \\
\end{align}$$

El momento ayuda a **acelerar la convergencia** y **filtrar oscilaciones**. El coeficiente $\beta$ determina la importancia del término momento.

Este tipo de técnicas se llaman **optimizadores**:  algoritmos que ajustan los parámetros durante el entrenamiento para minimizar el error. El momento es un optimizador básico. Adam es una mejora sobre el momento que funciona mejor.
