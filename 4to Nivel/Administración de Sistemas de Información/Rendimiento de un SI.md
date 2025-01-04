El **rendimiento** de un sistema establece los **parámetros** con los que se deben dar las [[Prestaciones de un SI]]. Es un **nivel** de qué tan bien los servicios del **sistema informático** (HW + SO) ejecutan las aplicaciones del sistema y cómo utilizan el hardware disponible, dada una [[Carga de Trabajo]].

Son **medidas cuantitativas** del comportamiento de un software que miden **requerimientos no funcionales**. El rendimiento de las prestaciones depende del **entorno** del sistema (el rendimiento del SYSACAD es muy distinto al de Mercado Libre).

## Relación entre Rendimientos y Costes

Sean dos computadores $x$ e $y$ que tardan $T_x$ y $T_y$ unidades de tiempo en ejecutar un programa. Si $T_x = T_y \implies$ el rendimiento es **equivalente**.

**Aceleración**: representa el incremento del rendimiento de una máquina respecto de otra. En la ecuación, $X$ es un $n$% más rápido que $X$.
$$\text{Aceleración} = \frac{T_y}{T_x} = 1 + \frac{n}{100}$$

Los computadores también tienen los costes $C_x$ y $C_y$ con un incremento entre ellos.
$$\text{Incremento} = \frac{C_y}{C_x} = 1 + \frac{n}{100}$$
Se busca la mejor relación costo-rendimiento. Se busca **maximizar** el índice:
$$\frac{\text{Rendimiento}_x}{\text{Coste}_x} \ vs \ \frac{\text{Rendimiento}_y}{\text{Coste}_y}$$

Para analizar cierta mejora en un sistema informático se puede usar la [[Ley de Amdahl]].
