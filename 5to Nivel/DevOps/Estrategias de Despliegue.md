![[Estrategias de Despliegue.png]]

- **Recreate**: simple pero riesgosa. Se espera downtime.
- **Blue/Green**: consiste en tener levantados dos entornos (el viejo y el nuevo), lo cual permite *rollback* pero implica más costos.
- **Canary**: los usuarios se van migrando lenta y progresivamente a la nueva versión. Si se detectan problemas, se puede hacer un rollback habiendo afectado a solo una pequeña cantidad de usuarios.
- **A/B testing**: se muestran variantes de la aplicación a distintos usuarios para hacer testing a nivel de producto. Se capturan métricas para validar una hipótesis.
- **Shadow deployment**: todo el tráfico al entorno público se duplica hacia un entorno oculto para ver si la aplicación funciona correctamente.
- **Feature flags**: es un patrón a nivel de desarrollo para poder activar y desactivar funcionalidades mediante una configuración de runtime. Son combinables con el resto de estrategias. Implica tener una sola build de la aplicación con varios comportamientos configurables.
- **Rolling update**: se redespliega de a un servicio a la vez. Es simple y gradual.

