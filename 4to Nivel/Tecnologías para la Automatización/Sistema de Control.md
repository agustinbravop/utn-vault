La [[Teoría de Control]] nos ayuda a crear **sistemas de control** (SC).

Un **sistema de control automático** posee subsistemas conformados por dispositivos, que efectúan acciones de **control, corrección, procesamiento, y medición** de la variable que se desea regular.

Un sistema de control *dinámico* está expuesto a *perturbaciones* (internas y externas). Se aplica la teoría general de sistemas para determinar bajo qué condiciones el sistema opera en **régimen estable**.

Para elaborar un modelo de un SC, se deben definir estos elementos:

1. Definición del [[Sistema]] y su objetivo.
2. Componentes del sistema: control, corrección, proceso, y medición.
3. Determinación del valor esperado de respuesta.
4. Determinación del error.
5. Condiciones de [[Estabilidad]].
6. Perturbaciones que puedan afectar al sistema.
7. [[Función de Transferencia]] del sistema.

Modelo clásico de un SC:

![[Sistema de Control.png]]

La *retroalimentación* puede ser:

- **Positiva**: desestabiliza el sistema, creando un círculo vicioso.
- **Negativa**: la salida vuelve a entrar pero negada, lo que estabiliza el sistema.

Los sistemas pueden ser:

- **Lineales**: las ecuaciones que controlan su comportamiento son lineales.
- **No lineales**: no responden al principio de superposición (no se puede cambiar el orden).

Los sistemas pueden ser:

- **Continuos**: respuesta analógica.
- **Discretos**: señales de salida digitales.

El sistema de control puede ser de:

- **Lazo abierto**: no obtienen información por retroalimentación.
- **Lazo cerrado**: mide la señal de salida para realimentarla a la entrada.

La [[Ingeniería de Control]] debe no solo definir los *límites* del sistema, sino también hacer recomendaciones para su *diseño*.

Modelo de capas de un SC:

![[Modelo de Capas de un Sistema de Control.png]]

1. **Física**: transmite señales.
2. **Conectividad**: conecta los dispositivos.
3. **Control**: comanda todo el sistema de control.
4. **Aplicación**: software que controla a la capa de control.

Un [[Sistema de Control]] se implementa con varios **dispositivos**:

- [[Sensores]]: dispositivos que recogen información del mundo real que miden magnitudes físicas y las transforman a señales eléctricas útiles para el SC.
- [[Actuadores]]: dispositivos que siguen las órdenes del SC y realizan acciones que repercuten en el mundo real de forma directa.
