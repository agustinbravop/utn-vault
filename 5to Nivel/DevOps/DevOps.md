> **DevOps** es la unión de personas, procesos y productos para permitir la [[Entrega Continua]] de valor a nuestros usuarios finales. - Donovan Brown

El [[Ciclo de Vida]] de desarrollo tradicional presenta conflictos entre los desarrolladores y los sysadmins (encargados de operaciones). Surge DevOps como un movimiento para resolver esos conflictos. Principios DevOps:

1. Reducir los silos organizacionales.
2. Aceptar los fallos.
3. Implementar cambios graduales.
4. Aprovechar las herramientas y la automatización.
5. Medir todo.

Topologías:

![[DevOps.png]]

IT ha ido evolucionando a lo largo del tiempo:

- Cascada $\longrightarrow$ [[Agilidad]] $\longrightarrow$ DevOps.
- Servidores físicos $\longrightarrow$ servidores virtuales $\longrightarrow$ containers.
- Datacenter $\longrightarrow$ hosted $\longrightarrow$ cloud.

Ciclo de vida de desarrollo usando DevOps:

![[DevOps-1.png]]

7 tareas principales:

1. Continuous development ([[Esquemas de Versionado de Software]]).
2. Continuous integration ([[5to Nivel/DevOps/Integración Continua|Integración Continua]]).
3. Continuous testing.
4. Continuous deployment ([[Estrategias de Despliegue]], [[Infraestructura como Código]], [[Contenedores]]).
5. Continuous feedback.
6. Continuous monitoring ([[Monitoreo y Optimización de Aplicaciones]]).
7. Continuous operations ([[Cloud Computing]], [[Alta Disponibilidad]]).

## DORA

DevOps Research and Assessment es el programa de investigación más grande y de mayor duración. Busca comprender las capacidades que impulsan la entrega de software y el rendimiento de las operaciones. Se busca derrumbar la "pared de confusión" que hay entre los devs y los ops.

Cada capacidad de DORA se centra en uno de 3 tipos:

- Técnica.
- De proceso.
- Cultural.

Los mejores equipos rinden bien en estas 4 **métricas DORA**:

1. **Deployment frequency**.
2. **Lead time for changes**.
3. **Mean time to restore**.
4. **Change failure rate**.
