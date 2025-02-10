Los **modelos matemáticos** son ecuaciones que representan las relaciones entre la entrada y la salida de un sistema. Se establecen de acuerdo con las leyes físicas que gobiernan el funcionamiento de los [[Diagrama de Bloques Funcionales|bloques funcionales]] del [[Sistema de Control]].

Los SC se pueden modelar matemáticamente para describir su comportamiento. Tiene elementos:

- **Pasivos**: resistores, capacitores, e inductores. no requieren alimentación.
- **Activos**: requieren alimentación eléctrica para operar.

En general, los modelos en el dominio del tiempo involucran ecuaciones diferenciales difíciles de solucionar. Se busca encontrar una [[Función de Transferencia]] del sistema, la cual explica su comportamiento desde el dominio de las frecuencias, lo cual resulta más sencillo:

- [[Transformada de Laplace Aplicada a los Sistemas de Control]].
- [[Transformada Z Aplicada a los Sistemas de Control]].

## Lazo Abierto vs Lazo Cerrado

Los sistemas pueden ser de:

- **Lazo abierto**: la salida no se mide ni se retroalimenta (no afecta a la acción de control). La precisión del sistema depende de la calibración. No hay trayectoria de retroalimentación.
- **Lazo cerrado**: cada subsistema en el sistema global tiene su propia función de transferencia.

|                          | Lazo abierto                | Lazo cerrado             |
| ------------------------ | --------------------------- | ------------------------ |
| Perturbación externa     | Relativamente afectado      | Prácticamente insensible |
| Componentes internos     | De costo medio-alto         | De bajo costo            |
| Estabilidad              | Fácil de lograr             | Problema importante      |
| Cantidad de componentes  | Escasa                      | Importante               |
| Potencia o amplificación | Solo limitada por el diseño | Moderada a baja          |

![[Sistema de Lazo Cerrado.png]]

### Perturbaciones Externas

- **En sistemas de lazo abierto**: la perturbación se arrastra.

![[Perturbaciones Externas en Sistemas de Lazo Abierto.png]]

$$S_0 = T_2 (T_1S_i+P) = T_2T_1S_i+\underbrace{T_2P}_\text{error}$$

- **En sistemas de lazo cerrado**: presentan mejor performance y control.

![[Perturbaciones Externas en Sistemas de Lazo Cerrado.png]]

### Sensibilidad a los Cambios

- **En sistemas de lazo abierto**: la función de transferencia es $\text{FT} = T_1T_2T_3$. Si un elemento cambia un $\Delta$, entonces la función será $\text{FT}' = \Delta T_1 T_2T_3$.
- **En sistemas de lazo cerrado**: $\text{FT}=\frac{T_1T_2T_3}{1+RT_1T_2T_3}$. Si un elemento cambia un $\Delta$, entonces la función será $\text{FT}=\frac{T_1T_2T_3}{1+R\Delta T_1T_2T_3}$.

La principal diferencia es el trayecto de realimentación, que reduce la sensibilidad ante perturbaciones externas y cambios no deseados en los componentes, pero se pierde ganancia y tiene una probabilidad de ser inestable.

La **conversión analógico-digital** permite trabajar con señales digitales para acotar los errores. Consiste en tres pasos:

1. Muestreo con PAM.
2. Cuantificación.
3. Codificación.

![[Conversión Analógico Digital.png]]
