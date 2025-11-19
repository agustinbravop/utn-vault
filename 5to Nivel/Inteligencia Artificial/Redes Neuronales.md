Estos modelos de [[Inteligencia Artificial]] están inspirados en las redes neuronales biológicas. 

Toda **red neuronal artificial** está constituida por **neuronas**:

![[Redes Neuronales.png]]

Una red es de **propagación hacia adelante** (*feedforward*) cuando ninguna salida de las neuronas es entrada de neuronas del mismo nivel. Caso contrario, la red se conoce como de **propagación hacia atrás**.

Cada neurona tiene asociada una **función de activación** $f_i(t)$ que transforma el **estado actual de activación** en una **señal de salida** $y_i$. Esta función de transferencia puede ser:

$$\begin{align}
a_i(t+1) &=F(a_i(t), net_i) \\
y_i(t+1) &=f(net_i - \theta_i) = f(\sum w_{ji} y_i(t) - \theta_j)\\
\end{align}$$

Las funciones de transferencia básicas son las de escalón y de escalón mixta. Existen muchas otras.

En cada neurona se calculan los **pesos** $w_{ji}$ de las conexiones por el valor de las salidas $y_i$ de las neuronas que se conectan a ella. Dependiendo del valor del peso se puede decir que la **interacción** entre dos neuronas es:

- **Inhibidora**: si $w_{ji} \lt 0$.
- **Nula**: si $w_{ji} = 0$.
- **Excitadora**: si $w_{ji} \gt 0$.

La red [[5to Nivel/Inteligencia Artificial/Aprendizaje|aprende]] modificando sus pesos. La **regla de aprendizaje** es el mecanismo que determina la correcta modificación de los pesos de las conexiones.

Modelos de redes neuronales:

- [[Perceptrón]].
- [[Perceptrón Multicapa]].
- [[Modelo de Hopfield]].
- [[Self-Organizing Maps]].
