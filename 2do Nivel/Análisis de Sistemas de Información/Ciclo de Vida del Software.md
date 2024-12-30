El **ciclo de vida del software** (CVS) describe la vida de un producto de software desde su definición, diseño, implementación, verificación, validación, entrega, operación, y mantenimiento. Se definen las siguientes etapas:

1. **Definición**: se hace un _reconocimiento_ para conocer los clientes, sus motivos, y su contexto. Se hace un _estudio de factibilidad_ para saber si realmente se puede realizar el [[Proyecto de Software]]. Luego, se hace un _relevamiento_ de los requisitos (necesidades).
2. **Diseño**: se hace el **modelado lógico** de la solución, evaluando alternativas de arquitecturas y tecnologías para elegir las mejores soluciones.
3. **Codificación**: se escribe el código del software, lo que se denomina el **modelo físico**.
4. **Prueba**: se realizan pruebas del software antes de entregarlo al usuario. Se establecen métricas y estándares que cumplir para asegurar **calidad**.
5. **Implementación**: se pone en funcionamiento el sistema. Hay que realizar una cuidadosa _conversión_:
   - **En paralelo**: se usa el sistema nuevo a la par del viejo, hasta cierta fecha límite.
   - **Cambio directo**: se usa de golpe. Es radical pero peligroso.
   - **Estudio piloto**: se prueba el sistema en una parte de la organización.
   - **Por fases**: se va implementando el nuevo sistema de a partes (funcionalidades).
6. **Mantenimiento**: consiste en extender la **vida útil** del sistema, manteniendo viable la solución. Hay varios tipos de mantenimiento:
   - **Correctivo**: se arreglan errores no detectados previamente.
   - **Adaptativo**: se adapta el sistema a un cambio del contexto. Relacionado a la [[Homeostasis]].
   - **Perfectivo**: todo va bien, y se van agregando nuevas funcionalidades.
   - **Preventivo**: no es visible para el usuario, pero se realiza para facilitar el mantenimiento del SI y evitar el problema de la entropía. Le compete a la _reingeniería del software_.

Se subdivide el ciclo de vida en dos partes:

1. **Ciclo de desarrollo**: desde el inicio hasta la entrega.
2. **Ciclo de vida útil**: desde la implementación hasta que se deje de utilizar.
