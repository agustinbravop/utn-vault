En [[5to Nivel/DevOps/DevOps|DevOps]], la **alta disponibilidad** (High Availability, HA) consiste en minimizar el downtime de nuestros servicios. Es un principio de diseño que permite a un sistema soportar fallos y seguir funcionando con niveles de rendimiento aceptables. 

Requiere redundancia y replicación para evitar *single points of failure*. Un cluster de alta disponibilidad o cluster de conmutación por error es un grupo de máquinas que trabajan juntas para minimizar el downtime.

Diseños de HA:

- **Activo/activo**: ambas instancias manejan tráfico.
- **Activo/pasivo**: hay una instancia en espera.

La tolerancia a fallos potencia la High Availability, ofreciendo un mayor grado. 

Mientras que HA se centra en la disponibilidad de cada componente, la recuperación ante desastres se centra en no perder la disponibilidad del sistema completo.
