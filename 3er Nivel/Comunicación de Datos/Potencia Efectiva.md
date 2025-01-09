Una fuente realiza una [[Transmisión de Señales]] a cierta **potencia**. La *densidad de potencia* es $P_i= \frac{P_r}{4\pi R^2}$, donde $P_r$ es la potencia de emisión o radiación de la fuente, y $R$ es el radio de la esfera (la distancia desde la fuente). La densidad de potencia va disminuyendo a medida que el frente de onda se aleja, pero la $P_r$ es siempre igual. 

La *potencia efectiva* es la potencia con la que el frente de onda impacta en el objetivo.

Fenómenos físicos que afectan a la potencia:

1. **Atenuación**: a medida que el frente de onda se aleja, crece la esfera de isotropismo.
2. **Absorción**: el medio disipa la potencia porque sus partículas interactúan con la PEM. Esto aumenta con la frecuencia y con la distancia.
3. **Reflexión**: cambia la dirección de un haz al impactar en una superficie que no absorba energía.
4. **Refracción**: es el desvío en la dirección de un haz cuando pasa de un medio a otro con otra densidad. A mayor densidad, menor velocidad.
5. **Difracción**: o "efecto de borde". Sucede cuando el frente de onda pasa cerca de un cuerpo opaco, y parte de su energía se redistribuye.

## Interferencia de Ondas

La **interferencia** de [[Ondas]] es la superposición de trenes de onda en la misma banda del [[Señales y Espectros|espectro]], que resulta en una degradación de los trenes de onda originales.

Esto puede darse entre ondas 100% distintas, análogas (con las mismas propiedades), y divergentes (de la misma fuente). Generalmente se da una cancelación parcial, lo que *degrada* la señal.

Los *filtros* suprimen ondas de ciertas frecuencias, lo que puede ayudar a eliminar el [[Ruido]]. Nos permiten eliminar armónicas indeseadas. Los medios pueden actuar como filtros naturales. Los filtros típicos son:

1. **Pasa-altos**: suprimen hasta cierta frecuencia máxima.
2. **Pasa-bajos**: suprimen desde cierta frecuencia mínima.
3. **Pasa-banda**: solo pasa cierto rango objetivo.

## Ganancia y Pérdida

Los **circuitos** pueden mejorar o degradar las señales que los atraviesan. Un **circuito lineal** no altera el período de la señal, ni su frecuencia, ni su longitud de onda. Puede cumplir dos roles:

- **Amplificador**: la amplitud de la señal a la salida es mayor que a la entrada.
- **Atenuador**: la amplitud se reduce.

Es típico usar decibelios: $dB = 10 \cdot \log \frac{P_a}{P_b}$. Dada las potencias $P_e$ de entrada y $P_s$ de salida:

$$G(dB) = -P(dB) = 10\cdot \log \frac{P_s}{P_e} = 20 \cdot \log \frac{V_s}{V_e}$$
