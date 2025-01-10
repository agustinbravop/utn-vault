Las **redes celulares** (RC) utilizan múltiples transmisores de baja [[Potencia Efectiva]]. La tecnología celular es la vase de la [[Comunicación de Datos]] móvil e inalámbrica. El mayor problema a resolver es el _desvanecimiento_: la variación temporal de la potencia de la señal.

![[Redes Celulares Inalámbricas.png]]

Para organizar estas redes, se usan transmisores de aproximadamente 100 W y de corto alcance. A cada _celda_ se le asigna su propia antena, una estación base, y una banda del [[Señales y Espectros|espectro]]. Celdas adyacentes utilizan bandas diferentes para evitar la diafonía.

Para aumentar la capacidad de la red, se puede:

- Agregar canales de reserva.
- Usar frecuencias prestadas.
- Dividir celdas en subceldas.
- Usar microceldas.

Cada _estación base_ (BS) se sitúa aproximadamente en el centro de cada celda. Están conectadas con una _MTSO_ (Central de Conmutación de Telecomunicaciones Móviles). Una MTSO le da servicio a varias estaciones base: conecta las llamadas entre unidades móviles, asigna canales de voz a cada llamada, y realiza los _handoffs_.

Una llamada entre dos usuarios involucra:

1. Inicialización de la unidad móvil.
2. Inicio de la llamada desde la unidad móvil.
3. Localización.
4. Aceptación de la llamada.
5. Traspaso, bloqueo, terminación, corte, etc.

## Generaciones

1. **Primera**: desarrollado por AT&T en los 80s. Usa **canales analógicos** de tráfico. Sistema AMPS. Se usaba la asignación espectral para definir una banda de subida y otra de bajada, lo que permite transmisión full duplex.
2. **Segunda**: apareció en 1991 y fue disruptiva. La tecnología D-AMPS y **digital** permitió el uso de la criptografía. Tres usuarios pueden compartir un par de frecuencias con [[Multiplexación#TDM Síncrona|multiplexación por división de tiempo síncrona]]. Se usan [[Códigos]] correctores de errores.
3. **Tercera**: en 1998. Es el 3G especificado por la ITU. Ofrece hasta 2048 KBps para oficina y 144 KBps para vehículos en movimiento. Tiene una interfaz adaptativa para internet que posibilita su uso en IoT. Da mayor soporte y flexibilidad. Tiende al **acceso universal**.
4. **Cuarta**: aparece en 2008 el 4G basado completamente en tecnología IP con el objetivo de lograr una **convergencia** entre redes analógicas y dispositivos digitales. Introduce "High Speed Downlink Packet Access" y la Banda Ancha Móvil. Es una mejora de las prestaciones, la simultaneidad, y la conectividad.
5. **Quinta**: aparece en 2018 el 5G, una tecnología de banda ancha móvil disruptiva que promete la **comunicación sin límites**. Utiliza un ancho de banda de frecuencias más altas (ondas milimétricas), actualmente poco usado. Se usan _microceldas_ para evitar obstáculos. Ofrece MIMO (_multiple input, multiple output_) masivo. Utiliza _beamforming_, un haz direccionado a cada usuario específico.
