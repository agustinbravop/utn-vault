En un [[Sistema Operativo]], el *file system* establece la forma en la que se almacenan los archivos y se administran los espacios de manera eficiente y confiable. Es el componente que establece la **correspondencia** entre archivos y discos.

Suele contener:

1. Métodos de **acceso**.
2. [[Administración de Archivos]]: cómo almacenarlos, compartirlos, referenciarlos.
3. Administración del **almacenamiento auxiliar**: secundario.
4. **Integridad** del archivo.

La administración involucra aspectos como:

1. Cuotas de disco (como en los proveedores de nubes).
2. Respaldos.
3. Desfragmentación.

![[Distribución del Sistema de Archivos.png]]

Una cuestión importante es la [[Asignación del Sistema de Archivos]].

## Sistemas de Archivos por Bitácora

En una **bitácora** se mantiene un registro de lo que va a realizar el sistema antes de hacerlo para poder retomar su trabajo planeado ante una falla. Esto está relacionado al concepto de **transacciones** atómicas de las bases de datos.

## Servidores de Archivos

- **FTP**: File Transfer Protocol establece un sistema cliente-servidor para intercambiar archivos a través de TCP/IP.
- **NFS**: Network File System establece un sistema de archivos distribuido con una arquitectura cliente servidor. Está basado en RPC v2.
