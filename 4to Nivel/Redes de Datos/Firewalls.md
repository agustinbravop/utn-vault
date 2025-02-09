Son dispositivos que aíslan [[Redes de Datos]], controlando y filtrando tráfico. Inspeccionan cada paquete y deciden si dejarlo pasar o descartarlo. Son esenciales para una [[Ciberseguridad|red segura]].

Hay firewalls basados en HW o en SW. Pueden estar integrados en [[Enrutadores]] o ser dispositivos separados. Se pueden usar en diferentes configuraciones.

Los firewalls de primera generación pueden filtrar paquetes por dirección [[IP]] de origen o destino, y por [[Puertos]] [[TCP]]/[[UDP]]. Son los más rudimentarios y estrictos, con poca flexibilidad. Son stateless.

## ALG

Los *Application Level Gateway* (ALG) son firewalls a nivel de aplicación que combinan HW y SW y generalmente están integrados en un proxy.

Los ALG establecen conexiones en nombre del host y puede examinar en detalle cada conexión. La performance puede ser un problema.

Con *stateful inspection*, los paquetes son inspeccionados en tiempo real, y teniendo en cuenta el flujo de paquetes previos para detectar patrones de comportamiento. Con *dynamin packet inspection*, se puede modificar las reglas reaccionando al entorno.

## IDS

Los *Intrusion Detection System* (IDS) estudian **patrones de comportamiento hostiles**, considerados actividad sospechosa.

Existen IDSs a nivel de red (NIDS, no monitorean datos encriptados) y a nivel de host (HIDS, afectan la performance).
