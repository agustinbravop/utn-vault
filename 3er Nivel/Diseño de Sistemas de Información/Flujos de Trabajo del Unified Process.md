Todos los [[Flujos de Trabajo]] del [[Unified Software Development Process]] definen _artefactos_ y _roles_ estáticos unidos por un _workflow_ dinámico. Los principales son:

1. Captura de Requisitos.
2. Análisis.
3. Diseño.
4. Implementación.
5. Prueba.

Cada rol es responsable de ciertos artefactos, los cuales son las entradas o salidas de ciertas actividades de cada flujo de trabajo.

A estos flujos de trabajo el [[Rational Unified Process]] los denomina _disciplinas_.

## Captura de Requisitos

En este flujo de trabajo se encuentran los casos de uso definidos desde el punto de vista del cliente. Se tiene en cuenta:

1. Lista de características: las cosas generales que el sistema debería hacer.
2. [[Modelado del Dominio]]: para entender los conceptos del negocio.
3. [[Modelado del Negocio]]: para entender los procesos del negocio.

![[Flujo de Captura de Requisitos-1.png]]

Roles y sus artefactos:

1. **Analista de sistema**: responsable del modelo de casos de uso, de los actores, y del glosario.
2. **Especificador de casos de uso**: responsable de los casos de uso.
3. **Diseñador de UI**: responsable del prototipo de la UI.
4. **Arquitecto**: responsable de la descripción de la arquitectura, que considera a los CU críticos.

La _descripción de la arquitectura_ es un extracto adecuado de los modelos que evoluciona a medida que se avanza por el proceso. Tiene cinco secciones, una para cada modelo:

1. **Vista de casos de uso**: presenta los actores y casos de uso más importantes.
2. **Vista de análisis**: no siempre se mantiene.
3. **Vista de diseño**: subsistemas, interfaces, y clases más importantes.
4. **Vista de despliegue**: nodos (hardware) asignados a objetos activos (hilos de ejecución).
5. **Vista de implementación**: componentes que implementan los modelos de diseño y de despliegue.

## Flujo de Análisis

Estructuramos los requisitos en un modelo de análisis con lenguaje técnico. Se considera que este flujo de trabajo es opcional, por lo que no es necesario mantenerlo a lo largo del tiempo.

![[Flujo de Análisis.png]]

Roles:

1. **Arquitecto**: responsable del modelo de análisis.
2. **Ingeniero de casos de uso**: responsable de la realización de CU-análisis.
3. **Ingeniero de componentes**: responsable de las clases y de los paquetes del análisis.

## Flujo de Diseño

En este flujo se le da forma al sistema. Se trasladan los requisitos a un modelo para ser implementado. Se piensa en requisitos no funcionales, en tecnologías, en interfaces. El modelo de diseño es físico y específico a una implementación, por lo que debe mantenerse a lo largo del proceso.

![[Flujo de Diseño.png]]

Roles:

1. **Arquitecto**: responsable del modelo de diseño, del modelo de desarrollo, y de la descripción de la arquitectura (que considera subsistemas, interfaces, dependencias, y clases críticas).
2. **Ingeniero de casos de uso**: responsable de la realización de CU-diseño.
3. **Ingeniero de componentes**: responsable de las interfaces y las clases y subsistemas de diseño.

Una _realización de caso de uso-diseño_ es una [[Diagrama de Colaboración|colaboración]] en el modelo de diseño que describe cómo se realiza y ejecuta un caso de uso específico, en términos de clases de diseño y sus objetos.

## Flujo de Implementación

El modelo se implementa en términos de _componentes_, los cuales son scripts, ejecutables, etc.

![[Flujo de Implementación.png]]

Roles:

1. **Arquitecto**: responsable del modelo de implementación, la descripción de la arquitectura, y el modelo de despliegue.
2. **Integrador del sistema**: responsable de la integración del sistema ([[Integración Continua]]).
3. **Ingeniero de componentes**: responsable de las interfaces, los componentes (que resuelven el empaquetamiento físico del modelo), y las implementaciones de subsistemas.

## Flujo de Prueba

Se verifican las construcciones logradas.

![[Flujo de Prueba.png]]

Roles:

1. **Ingeniero de pruebas**: responsable del modelo de pruebas, los casos de pruebas (que tienen _trazabilidad_ hacia los casos de uso que prueban), el procedimiento de pruebas, la evaluación de pruebas, y el plan de pruebas.
2. **Ingeniero de pruebas de integración**: responsable de los defectos (anomalías a resolver).
3. **Ingeniero de pruebas del sistema**: responsable de los defectos (anomalías a resolver).
4. **Ingeniero de componentes**: responsable de los componentes de prueba, que _automatizan_ los procedimientos de prueba ([[Automatización de Pruebas]]).
