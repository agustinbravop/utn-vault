El análisis operacional es una **técnica analítica** de [[Modelado]] para la [[Evaluación de las Prestaciones]] que usa **modelos de colas** para calcular **índices de prestaciones** del sistema.

**Operacional**: significa algo que es **directamente medible**.

**Estación de servicio**: es un **servidor** (con recursos) junto a una **cola de espera** (con trabajos). Vamos a estudiar su **tiempo de servicio** y su **tiempo de respuesta**.

![[Estación de servicio para el análisis operacional.png]]

## Variables Operacionales

Estas variables son cantidades directamente medibles durante un período de observación. Sobre un dispositivo $i$ del sistema informático, se definen:

1. $T$: período de observación.
2. $A_i$: número de arribos durante $T$.
3. $C_i$: número de trabajos completados durante $T$.
4. $B_i$: tiempo en el que el dispositivo $i$ está ocupado.

Se deducen:

1. **Tasa de llegada**: $\lambda_i = \frac{A_i}{T}$
2. **Productividad**: $X_i = \frac{C_i}{T}$
3. **Utilización**: $U_i = \frac{B_i}{T}$
4. **Tiempo de servicio**: $S_i = \frac{B_i}{C_i}$

## Leyes Operacionales

Estas leyes definen **relaciones** entre las variables operacionales.

### Hipótesis del Flujo Equilibrado de Trabajos

Se supone que durante el período de observación $T$ se opera en **equilibrio**, donde la cantidad de trabajos que entran es igual a los que salen. Se puede asumir para un $T$ suficientemente grande.

$$Entradas = Salidas \implies A_i = C_i \implies \lambda_i = X_i$$

### Ley de la Utilización

$$U_i = \frac{B_i}{T} = \frac{C_i}{T} \frac{B_i}{C_i} \implies U_i = X_i * S_i$$
La utilización del recurso depende directamente de la productividad y del tiempo de servicio.

### Ley del Flujo Forzado

Sea $V_i = \frac{C_i}{C_o}$ la **razón de visitas** al dispositivo $i$.
$$X_i = \frac{C_i}{T} = \frac{C_i}{C_o} \frac{C_o}{T} \implies X_i = X_o * V_i$$
El flujo a través de determinado dispositivo de la red determina el flujo en otros dispositivos.

Si se une esta ley con la ley de la utilización:

$$U_i = X_i * S_i = X_0 * V_i * S_i = X_o * D_i$$

Surge la **demanda de servicio** $D_i = V_i * S_i$ sobre el dispositivo $i$ en todas las visitas que un trabajo realiza al mismo.

### Ley de Little

Sean $N_i$ el **número de trabajos** y $R_i$ el **tiempo de respuesta**.
$$N_i = \lambda_i * R_i \implies N_i = X_i * R_i$$

### Ley General del Tiempo de Respuesta

$$R = \frac{\sum X_i R_i}{X_o} \implies R = \sum_{i=1}^{k} V_i * R_i$$
El tiempo de permanencia de un trabajo depende del número de visitas que hace a cada dispositivo y cuánto demora cada visita.

### Ley del Tiempo de Respuesta Interactivo

Sirve para [[Sistemas Interactivos]] donde $Z$ es el **tiempo de reflexión**.

$$N = X_o (Z + R) \implies R = \frac{N}{X_o} - Z$$
