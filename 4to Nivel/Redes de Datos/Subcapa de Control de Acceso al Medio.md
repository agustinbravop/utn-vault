La subcapa de Control de Acceso al Medio (MAC) es la subcapa inferior de la [[Capa de Enlace]].

Se necesita MAC en _redes de difusión_ (no en las punto a punto) para resolver la **asignación del canal** a uno de los varios usuarios que lo usan.

El primer enfoque fue la asignación estática. Las alternativas eran [[Multiplexación#FDM|FDM]] y [[Multiplexación#TDM Síncrona|TDM]], pero ambas presentaban inconvenientes, por lo que se evolucionó hacia la **asignación dinámica**.

Además, hay algunas particularidades cuando el canal es inalámbrico, por ende son relevantes p protocolos inalámbricos como [[MACA y MACAW]].

## Asignación Dinámica

Se suponen $N$ dispositivos usuarios capaces de generar tramas con una tasa de generación fija de $\lambda$ tramas por segundo. Cuando una estación genera una trama, se bloquea hasta que haya sido transmitido con éxito.

Se asume un **canal único**. Cuando dos tramas se transmiten a la misma vez, sucede una _colisión_: las tramas se destruyen, y se deben retransmitir.

### Aloha

Aloha es la primera aproximación. Supone infinitos usuarios que generan tramas de longitud fija $L$ según una [[Distribución de Poisson]] con media $\lambda$. La población total de usuarios también sigue una distribución de Poisson, con media $N$, al generar tramas.

El total de tramas nuevas y retransmitidas forma una distribución $G$, con $G \approx N$ para un $N$ chico. La probabilidad de que ocurran $k$ colisiones es $P(k) = \frac{G^k \cdot e^{-G}}{k!}$. El rendimiento es $S = G \cdot P(0)$.

![[Intervalo de Vulnerabilidad en Aloha.png]]

Teniendo en cuenta el _intervalo de vulnerabilidad_ $2t$, debido a que se necesita asegurar dos ranuras de tiempo, el rendimiento resulta $S = G \cdot P(0) \cdot P(0) \implies S = G \cdot e^{-2G}$.

## Aloha Ranurado

Se introduce una _central de radio_ que ranure el tiempo en intervalos de transmisión. Con esto, se puede reducir el intervalo de vulnerabilidad a la mitad, lo que duplica el rendimiento: $S = G \cdot e^{-G}$.

![[Rendimiento de Aloha Ranurado.png]]

### CSMA

Carrier Sense Media Access (CSMA) propone que las estaciones hagan un _censado_ del canal. Puede ser:

1. **1-persistente**: escucha el canal y transmite tan prono esté libre. Sirve para cargas bajas.
2. **No**-persistente\*\*\*\*: si el medio está ocupado, espera un tiempo aleatorio extremo. Sirve para cargas altas.
3. **p-persistente**: transmite con probabilidad $p$, y espera un tiempo aleatorio con probabilidad $q=1-p$.

![[Rendimiento de CSMA.png]]

### CSMA/CD

CSMA con Collision Detection. Un canal puede estar en tres estados: contención, transmisión, o inactivo.

### Métodos sin Colisión

Algunos métodos sin colisión son el [[Protocolo]] de mapa de bits o recorrido de árbol adaptativo.
