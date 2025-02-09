Los **enrutadores** o *routers* son dispositivos de la [[Capa de Red]], capa 3 del modelo OSI. Los enrutadores cumplen dos funciones:

- Determinación de la ruta.
- Conmutación.

La determinación de la ruta se hace mediante **métricas** (longitud de ruta, confiabilidad, retardo, costo, carga, etc) y **tablas** (asociaciones o pares de destino y próximo salto).

La conmutación es relativamente simple, aunque puede incluir cambios de encapsulamiento y/o resolución de direcciones L2 ([[Capa de Enlace]]). Se aplica **encolamiento** para los paquetes.

## Principio de Optimalidad

Si el enrutador $J$ está en ruta óptima del enrutador $I$ al enrutador $K$, entonces la ruta óptima de $J$ a $K$ también está en la misma ruta.

$$\text{Si } J \in \text{opt}(I,K) \implies (J,K) \text{ es óptimo}$$

Debido a esto, el grupo de rutas óptimas de todos los orígenes a un destino dado forma un *árbol sumidero* con raíz en el destino. La métrica de distancia es la **cantidad de saltos**.

El objetivo de los algoritmos de enrutamiento es descubrir y utilizar los árboles sumideros de todos los enrutadores.

## Algoritmos de Enrutamiento

Los [[Algoritmo|algoritmos]] que eligen las rutas (y las estructuras de datos que usan) son un aspecto principal del diseño de la capa de red. Propiedades deseables:

1. Exactitud.
2. Sencillez.
3. Robustez.
4. Estabilidad.
5. Equidad.
6. Optimización (en conflicto con la equidad).

### Ruteo Estático

El algoritmo de Dijkstra de la **ruta más corta** es un ejemplo de ruteo estático. Cada nodo se etiqueta con su distancia al nodo de origen a través de la mejor ruta conocida.

![[Ruteo Estático.png]]

### Ruteo Dinámico por Vector Distancia

Se utiliza el algoritmo de Bellman-Ford o de Ford-Fulkerson. Se almacena un vector con las distancias.

Esta estrategia hace que cada enrutador mantenga una **tabla** (vector) que da tanto la mejor distancia conocida a cada destino como la línea que se puede usar para llegar ahí. Estas tablas se actualizan **intercambiando información con los vecinos**.

En la práctica, este enrutamiento resulta muy **lento**, sobre todo porque reacciona con lentitud ante fallos en los nodos. Además, se puede dar el problema de la **cuenta a infinito**: los routers incrementan recursivamente la distancia a un enrutador que está caído, porque todos los vecinos creen que lo pueden alcanzar (aunque no esté disponible).

### Ruteo Dinámico por Estado de Enlace

El algoritmo link-state (LS) tiene 4 etapas:

1. **Descubrir vecinos**: tiene que conocer sus enlaces con el mundo.
2. **Calcular métricas**: por ejemplo, el retardo.
3. **Distribuir LSA**: anuncia su estado propio a todos los enrutadores.
4. **Calcular la ruta más corta**: para armar su árbol de optimalidad.

En lugar de contar información de todos los routers a solo sus vecinos, este router cuenta información de **solo sus enlaces a todos los enrutadores**. Esa distribución es complicada: se agregan datos de control (número de secuencia y edad para asegurar la consistencia de los datos) a estos paquetes del enlace para evitar errores.

Esto logra una **convergencia rápida**, aunque la difusión puede consumir muchos recursos de la red. Para evitar repetir información ya conocida, se puede usar un mecanismo de **difusión dirigida** que agrega banderas de transmisión y de confirmación de recepción (ACK) para cada una de las líneas del router.

## Enrutamiento Jerárquico

En el **enrutamiento jerárquico**, los routers se dividen en *regiones*.

Cada enrutador conoce todos los detalles para enrutar paquetes a destinos dentro de su propia región, pero no sabe nada de la *estructura interna* de las otras regiones. Se puede considerar a cada región como una red conectada a través de un solo *gateway* con otras regiones (o redes).

![[Enrutamiento Jerárquico.png]]

Un router que no sea el *gateway router*, no necesita conocer de otras regiones, por lo que su **tabla jerárquica** de direcciones puede ser más corta, porque solo incluye direcciones de su misma región.

Para una subred de $N$ routers, el número óptimo de niveles es $\ln N$.
