Un **controlador lógico programable** (*Programmable Logic Controller*, PLC) es una computadora usada en la automatización industrial para la [[Automatización de Procesos]] de producción.

> Es un aparato electrónico operado digitalmente que usa una memoria programable para almacenar instrucciones internamente para controlar varios tipos de máquinas o procesos a través de módulos de entrada/salida.

![[PLC vs Automatismo Eléctrico.png]]

Los PLCs son un tipo de autómata programable. Están diseñados para **múltiples señales de entrada y salida, rangos de temperatura ampliados, e inmunidad al ruido eléctrico**.

Un PLC es un [[Sistema de Control]] de **tiempo real** donde los resultados de salida deben ser producidos en respuesta a las condiciones de entrada dentro de un tiempo muy limitado.

La interfaz humano-máquina de estos dispositivos es muy potente, lo que facilita el trabajo del personal de mantenimiento y de producción.

![[Arquitectura de un PLC.png]]

Componentes del PLC:

1. **Hardware**: activa o desactiva las funciones controlables según cierta secuencia lógica determinada. La parte esencial del hardware PLC es la CPU.
2. **Software**: son programas elaborados por el programador en un listado de instrucciones, un diagrama de contactos, o un diagrama de funciones.
3. **Entradas/salidas**: son los [[Canales]] que le permiten al PLC comunicarse.

El **funcionamiento** del PLC tiene dos modos: `stop` y `run`. Cuando está en modo `run`, está indefinida y continuamente ejecutando *ciclos de scan*. Cada ciclo de scan consiste en 4 pasos:

1. Lectura de las entradas del PLC.
2. Ejecución del programa de control.
3. Escritura de las salidas del PLC.
4. Tareas internas del PLC.

Hoy en día los PLC también necesitan un **sistema para enlace con el computador**, para poder ser monitoreados. Hay dos tipos de interfaces:

- Módulos de Comunicación Asíncrona Punto a Punto: RS-232.
- Módulos de Comunicación Multipunto: varias estaciones en un esquema maestro/esclavo.

Existen **sistemas de red** que permiten supervisar elementos del proceso para controlarlo en forma más precisa y óptima. Estos programas permiten generar alarmas, reportes, archivos históricos, tendencias en tiempo real, etc. Hay módulos de red *propietarias* (de un fabricante) y *comerciales* (siguen normas internacionales para facilitar la integración).

## Elementos de Programación

Hay lenguajes gráficos:

- Diagrama de escalera (LD).
- [[Diagrama de Bloques Funcionales]] (FBD).

O también lenguajes literales:

- Texto estructurado (ST).
- Lista de instrucciones (IL).

![[Controlador Lógico Programable.png]]

Dispositivos con los que puede interactuar un PLC:

- [[Actuadores]]: luces, motores, bombas.
- [[Sensores]]: botones/switches, fotosensores.

Criterios de selección de un PLC:

1. Número de entradas/salidas.
2. Capacidad de la memoria.
3. Potencia de las instrucciones.
4. Posibilidad de periféricos y comunicaciones.

Clasificación del PLC según el tipo de formato:

- **Compactos**: son integrados.
- **Modulares**: se pueden expandir.

El **tiempo de respuesta** de un PLC es el tiempo necesario para el control. Viene determinado por:

- El tiempo de scan de la CPU, y
- El tiempo de on/off de las entradas/salidas.

La memoria se suele dividir en:

1. Área del [[Sistema Operativo]].
2. Área de programa.
3. Área de datos.

## Tarjetas de Entrada/Salida

Las tarjetas de entrada/salida se pueden clasificar según si tienen **aislamiento galvánico**:

- **Sí**: acoplamiento óptico.
- **No**: conexión directa.

Según el tipo de señales que aceptan:

- **Analógicas**: continuas.
- **Digitales**: discretas.

O según la excitación de señales que implementan:

- **Tensión**: voltaje.
- **Corriente**: amperaje.
