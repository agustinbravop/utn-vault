El proceso **ETL** (Extracción, Transformación y Carga) es el proceso para transferir, formatear, limpiar y cargar datos desde aplicaciones de producción a los sistemas de BI. El data engineer hace un ETL para cada [[Data Warehouse]]. Implementar el ETL representa el 50% del esfuerzo del proyecto.

![[Extracción, Transformación y Carga.png]]

En general todas las herramientas ETL tienen diagramas visuales y son similares entre sí.

## Extracción

El primer paso consiste en extraer los datos desde los sistemas de origen, causándoles mínimo impacto.

Los formatos de las fuentes pueden ser muy variados. Se debe identificar los cambios en los datos fuentes antes de extraerlos, para asegurar la correspondencia entre el DW y los OLTPs (sistemas transaccionales). Métodos:

- Carga total (empezar de cero en cada carga).
- Comparar instancias de la BD operacional.
- Usar timestamps en los registros del sistema operacional.
- Usar triggers en el sistema operacional.
- Usar logs del gestor de transacciones del sistema operacional.

## Transformación

Consiste en aplicar reglas o funciones a los datos extraídos. **Cleansing** es la limpieza de datos y estandarización. 

Resuelve varios problemas:

- Claves con estructura.
- Múltiples codificaciones.
- Unidades de medida.
- Formatos.
- Varias columnas en una/una en varias.
- Duplicados y/o sinónimos.
- Integridad referencial (que debe reconstruirse desde cero).
- Creación de claves.


La **calidad de datos** consiste en asegurar su:

- Exactitud.
- Completitud.
- Consistencia.
- Credibilidad.
- Actualidad.

## Carga

Consiste en mover los datos al sistema destino. Hay dos etapas:

1. Carga inicial: para el gran volumen de datos disponibles.
2. Mantenimiento periódico: para volúmenes pequeños pero recurrentes.

Hay dos maneras:

- **Truncate and Load**: limpiar el data warehouse y cargar toda la información de nuevo.
- **Incremental**: el DW se va actualizando con solo la nueva información.

Hay que determinar la frecuencia del mantenimiento periódico. Los índices conviene generarlos luego de la carga. La integridad referencial se puede deshabilitar para acelerar la carga.
