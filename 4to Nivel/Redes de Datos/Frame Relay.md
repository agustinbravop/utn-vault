**Frame Relay** es un [[Protocolo]] que surge como una evolución de [[Conmutación de Paquetes#X.25|X.25]] y elimina gran parte de su overhead, pero usa la infraestructura existente.

Rangos de velocidad desde fraccionales T1 (64 Kbps) hasta OC-3 (155 Mbps). Usa líneas digitales de alta velocidad, prácticamente libres de errores.

El cliente contrata un enlace sujeto a los parámetros $B_c$ y $B_e$. Es supervisado en un intervalo de tiempo $T_c$, durante el cual el cliente puede enviar todas las tramas $\text{CIR} = \frac{B_c}{T_c}$, y aquellas $\text{EIR} = \frac{B_e}{T_c}$ que no superen la velocidad del enlace.

Cuando recibe una trama dañada, la descarta sin más.
