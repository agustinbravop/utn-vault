Es requisito que un [[Sistema de Control]] sea [[Estabilidad|estable]]. Bajo condiciones óptimas sin fallas ni [[Error en Estado Estable de los Sistemas de Control|perturbaciones]], un sistema de lazo cerrado siempre es estable.

Un SC es estable si al aplicarle una entrada de referencia finita, la salida también tiene un valor finito. Un SC es estable si:

- Ante una entrada escalón, la salida es finita.
- Ante una entrada impulso, la salida tiende a cero.

Los sistemas pueden ser:

- Estables.
- Marginalmente o críticamente estables.
- Inestables (no sirven para la [[Teoría de Control]]).

Se puede determinar la estabilidad mediante el **método de polos y ceros**. Se analiza la [[Función de Transferencia]] en lazo cerrado de un SC. Las raíces de su denominador son los _polos_ a analizar.

Para determinar la estabilidad del sistema, se le puede introducir una _señal impulso_ y ver si al cabo de un tiempo la salida tiende a cero.

Ejemplos:

- Polos con parte real positiva $\Longrightarrow$ función exponencial creciente $\Longrightarrow$ inestable.
- Polos con parte real negativa y parte imaginaria conjugada $\Longrightarrow$ sinusoidal estable.
- Si todos los polos están en el semiplano izquierdo $\Longrightarrow$ el sistema es estable.
