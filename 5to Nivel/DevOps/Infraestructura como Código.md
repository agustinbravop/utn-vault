***Infrastructure as Code*** (IaC) es la práctica de gestionar y provisionar la infraestructura de IT mediante configuración. Se trata a la infraestructura de la misma manera que al código:

- Se [[Esquemas de Versionado de Software|versiona]], revisa, prueba.
- Permite [[5to Nivel/DevOps/Integración Continua|Integración Continua]].

Código IaC $\longrightarrow$ Motor IaC $\longrightarrow$ [[Cloud Computing]].

Ventajas de IaC:

- Automatización.
- Estandarización.
- Control de versiones.
- Reutilización.
- Reducción de costos.
- Recuperación ante desastres.

Casos de uso:

- Crear entornos desde cero.
- Crear entornos efímeros.
- Infraestructura inmutable.
- Gestión multi-cloud.
- Autoremediación.

## Terraform

*Terraform* es la herramienta de IaC declarativa líder en el mercado. Características:

- Platform agnostic.
- State files.
- Plan/apply workflow.
- Wide ecosystem.

Se usa escribiendo archivos de configuración HCL.

Los *providers* son plugins de terraform para interactura con la API de un servicio. El  provider maneja la lógica de la API y reporta el estado actual del recurso a terraform. 

Los *modules* agrupan recursos que se usan juntos. Permiten abstracción y reutilización.

El *terraform state* registra el estado de la infraestructura. Es la fuente de la verdad de terraform.
