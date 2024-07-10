Un **cuello de botella** es una **limitación** de las [[Prestaciones de un SI]]. Causa una ralentización considerable del tráfico en un área del sistema, problema atribuible a uno o dos recursos.

Causas de un cuello de botella:

1. Un componente de **hardware**.
2. Un componente de **software**.
3. La **organización** del sistema.

Mejorar el [[Rendimiento de un SI]] implica localizar el **cuello de botella** del sistema (que puede estar en el SW o en el HW) y actuar sobre él. Hay dos técnicas generales para hacerlo:

- **_Upgrading_**: es aumentar la cantidad de componentes físicos o reemplazarlos.
- **_Tuning_**: es ajustar los programas para mejorar su uso de los recursos disponibles. Esto es menos costoso y radical que cambiar el hardware. Una forma de _tuning_ es la [[Sintonización]].

## Detección y Eliminación

Los cuellos de botella se pueden **detectar** de muchas maneras: [[Monitorización]], [[Modelado]], etc. Cuando se sospecha uno, se busca **localizarlo** para identificar su **causa**. Se lo puede eliminar con técnicas de _upgrading_ o _tuning_.

Eliminar un cuello de botella puede provocar que aparezca otro en otro recurso del sistema. Se deben eliminar todos los cuellos de botella hasta que se logre **equilibrar** el sistema.

![[Detección y Eliminación de Cuellos de Botella.png]]
