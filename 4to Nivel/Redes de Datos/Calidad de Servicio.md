La **calidad de servicio** (_Quality of Service_, QoS) busca minimizar el problema de la congestión en las [[Redes de Datos]].

> "El santo grial de las redes de computadoras es diseñar una red que tenga la flexibilidad y el bajo costo de la internet, pero que ofrezca las garantías de calidad de servicio extremo a extremo de la red telefónica". - S. Keshav.

La calidad de servicio busca **mantener sana** la red: esto significa distintas cosas para los administradores, ISPs, vendedores, usuarios, etc. Muchas veces se trata de que la red se mantenga predecible, similar a dar **garantías del servicio**.

> La calidad de servicio implica un conjunto de tecnologías para diferenciar la asignación de recursos en la subred entre distintas **clases de servicio**, proveyendo control de congestión, bajo retardo, y máxima utilización de la capacidad disponible.

Los [[Acuerdos de Nivel de Servicio]] o _Service Level Agreements_ (SLA) son útiles para plasmar los **requisitos** de disponibilidad, ancho de banda, pérdida de paquetes, latencia, etc.

La QoS es útil cuando hay congestión moderada, para evitar llegar a una congestión fuerte.

![[Calidad de Servicio.png]]

La QoS es principalmente importante en aplicaciones de tiempo real, o sensibles a retardos. El _jitter_ es la variación en el retardo, lo que es problemático para aplicaciones de streaming.

Los mecanismos de QoS tienen tres componentes:

1. QoS en cada nodo.
2. Señalización de QoS.
3. Políticas, gestión, y contabilidad.

Se aplican políticas para:

1. Admisión y clasificación (hay inequidad entre paquetes).
2. Modelado y conformación de tráfico.
3. Encolamiento.
4. Descarte.

El _traffic shaping_ es un mecanismo para adaptar un flujo de entrada variable (con **ráfagas**) a un flujo de salida constante. Hay dos técnicas:

- **Leaky bucket**: repite paquetes a intervalos constantes. Si se desborda, los descarta.
- **Token bucket**: respeta las ráfagas. Si no hay fichas (tokens), los paquetes esperan.

![[Traffic Shaping vs Policing.png]]

Políticas de encolamiento:

1. **FIFO**: no permite QoS.
2. **PQ**: Priority Queuing. Puede producir inanición.
3. **FFQ**: favorece paquetes pequeños.
4. **WFQ**: combina las anteriores, pero no escala bien.
5. **CBQ**: basada en clases para mayor granularidad.

Políticas de descarte para evitar la congestión:

1. **FIFO**: no permite QoS.
2. **RED**: Random Early Detection. Descartes probabilísticos.
3. **WRED**: RED con prioridades basadas en QoS.
4. **RIO**: Red con un umbral para entradas y otro para salidas.
5. **AQM**: Active Queue Management.

[[TCP]] con ECN (_Explicit Congestion Notification_), que aprovecha los 8 bits del campo TOS del header [[IP]], es un ejemplo de AQM. Los [[Enrutadores]] notifican al origen TCP de una congestión incipiente. RFC 3168.

[[IntServ]] y [[DiffServ]] son propuestas para implementar QoS.

## Policy Routing

El "problema del pez" se resuelve con **ingeniería del tráfico**.

![[Policy Routing.png]]

Con IP, el ISP no puede controlar en X que solo el tráfico desde A vaya por la ruta de alta capacidad. _Multi Protocol Label Switching_ (MPLS) consiste en insertar etiquetas al acceder al núcleo de la red para así tener una conmutación rápida.

## Label Switching Routers

Los _Label Switching Routers_ (LSR) son routers centrales que pueden conmutar etiquetas. Pueden ser:

- Interiores.
- De frontera de ingreso: ponen etiquetas.
- De frontera de egreso: sacan etiquetas.

Los LSR encaminan paquetes en función del valor de la etiqueta MPLS. Esto permite combinar QoS con el enrutamiento, mediante la asignación dinámica de recursos.

La ingeniería del tráfico es un área que está en **constante desarrollo**.
