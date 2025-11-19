El perceptrón es un modelo de [[Redes Neuronales]] simple que surgió en 1958 (propuesto por Rosemblatt). Es una red neuronal monocapa.

![[Perceptrón.png]]

Se agrega una entrada ficticia llamada **umbral** o *bias* con un valor constante 1.

El algoritmo recibe **conjuntos de patrones de entradas y salidas deseadas**, y devuelve una configuración de pesos estables. Funcionamiento:

1. Inicialmente se asignan valores aleatorios a los parámetros: pesos $w_i$ y umbral $-w_0=\theta$.
2. Presentación de un nuevo patrón $X_p = (x_1,\dots,x_n)$ junto con la salida esperada $d(t)$.
3. Cálculo de la salida actual $y(t) = f[\sum_i w_i (t)x_i(t)-\theta]$ siendo $f(x)$ la función de transferencia escalón.
4. Adaptación de los pesos (este paso es el [[5to Nivel/Inteligencia Artificial/Aprendizaje|Aprendizaje]]). Siendo $\alpha$ el **coeficiente de aprendizaje** e $y(t)$ la salida obtenida:

$$w_i(t+1) = w_i(t) + \alpha \ [d(t) - y(t)]  \ x_i(t)$$

5. Repetir desde el paso 2 hasta que todos los errores sean cero, es decir que ocurra una **época** sin error. En la práctica se usan otras condiciones, como una tolerancia aceptable o un límite de épocas.

Dada su simplicidad, este modelo permite hacer una resolución iterativa, analítica, y/ gráfica, aunque distintos métodos no necesariamente llegan a la misma solución.

## ADALINE

ADALINE (ADAptative LINear Element) es un ejemplo concreto de un perceptrón. Es una arquitectura de aprendizaje supervisado offline.

![[ADALINE.png]]

A diferencia del perceptrón, en ADALINE la salida se obtiene antes de la función de activación. La salida es:

$$s=w_0 + \sum_{j=1}^N w_j \cdot x_j= X \cdot W^T$$

Esta salida lineal implica que el error es una función continua mucho más fácil de navegar.