Todo lo estudiado en la materia hasta el momento sobre [[Seguridad de la Información]] está pensado para infraestructuras on-premise, pero una infraestructura de [[Cloud Computing]] tiene algunas diferencias.

La CSA (*Cloud Security Alliance*) tiene guías de seguridad que consideran 15 dominios:

1. Conceptos y arquitecturas.
2. Gobierno y gestión del riesgo corporativo.
3. Cuestiones legales.
4. Cumplimiento y auditoría.
5. Gobierno de la información.
6. Plano de gestión y continuidad del negocio.
7. Seguridad de la infraestructura.
8. Virtualización y contenedores.
9. Respuesta ante incidentes.
10. Seguridad de aplicaciones.
11. Cifrado de datos.
12. Gestión de identidades, derechos y accesos.
13. Seguridad como servicio.
14. Tecnologías relacionadas.

En cloud computing hay 3 modelos de servicio:

1. **IaaS**: mayor responsabilidad de seguridad nuestra.
2. **PaaS**.
3. **SaaS**: menor responsabilidad nuestra, dependemos del proveedor.

La responsabilidad de los datos y las aplicaciones, y su seguridad, sigue siendo de la empresa. Como mucho, se comparte parcialmente con el proveedor.

El *management plane* de la nube permite administrarla. El proveedor debe asegurar que sea seguro y con permisos granulares.

En cuestión de continuidad de negocios, hay que considerar opciones para la portabilidad (es decir, que sea posible poder migrar a otro proveedor).

En conclusión, la seguridad no debería ser un factor importante para decidir entre una infraestructura cloud y una on-premise, sino que se debería poder lograr en ambas.

## Contratos

¿Cómo mapear los controles de los estándares y normas ya existentes a la nube? Los **contratos** son la herramienta de gobierno a usar en la nube. Establecen relaciones entre los proveedores y clientes, de manera que los clientes extienden la gobernanza a sus proveedores.

Hay énfasis en **documentación** y contratos. Lo que el contrato no cubre, cae en nosotros asegurarlo.

Hay *leyes* de varios países que se pueden aplicar en simultáneo. Por eso es importante dónde se almacenan los datos. El contrato puede determinar la jurisdicción legal a usar si hay litigio. De todas maneras, los contratos con grandes proveedores (AWS, Azure, Google Cloud), suelen estar estandarizados y ser poco negociables.

La *subcontratación de servicios* debe ser informada por el proveedor.

## Vendor Lock-In

El vendor lock-in sucede cuando un cliente no puede cambiar de proveedor, o hacerlo es económicamente inviable. En cloud computing puede suceder por:

1. Incompatibilidad entre tecnologías.
2. Restricciones contractuales.
3. Procesos ineficientes.

Para evitarlo:

1. Revisar la letra pequeña.
2. Averiguar herramientas de migración de datos.
3. Elegir un proveedor comprometido con estándares como CDMI (Cloud Data Management Interface).
4. Montar apps sobre [[Contenedores]].

## Cumplimiento y Auditoría

En la nube hay responsabilidad compartida. El **cumplimiento legal** valida la adherencia a las obligaciones corporativas. Las *auditorías* son una herramienta clave para probar o refutar el cumplimiento legal. El cumplimiento y la auditoría deben ser procesos continuos.

La recopilación de artefactos de cumplimiento legal es diferente en la nube:

1. Registros de auditoría.
2. Reportes de actividad.
3. Detalles de configuración de sistemas.
4. Detalles de gestión de cambios.

## Seguridad de los Datos

En cloud, el [[Gobierno de Seguridad de la Información]] consiste en:

1. Políticas y procedimientos.
2. Clasificación de la información.
3. Políticas de gestión de la información.
4. Políticas jurisdiccionales y de localización.
5. Autorizaciones.
6. Propiedad.
7. Custiodia.

Ciclo de vida del dato: Creación $\longrightarrow$ Almacenamiento $\longrightarrow$ Uso $\longrightarrow$ Distribución $\longrightarrow$ Archivado $\longrightarrow$ Destrucción. La seguridad del dato cambia según su fase y ubicación actual. También es necesario saber quién accede a ellos y cómo. En base a esto se definen actores y controles (permisos de roles).
