En el [[Proceso Unificado de Desarrollo de Software]], en el flujo anterior de [[Captura de Requisitos en el PU]] se construyeron modelos con el comportamiento externo del software. Ahora, se analiza, diseña, e implementa la **estructura interna**.

Las primeras iteraciones se centran en el análisis, luego en el diseño, y luego en la implementación.

## Roles y Artefactos

El flujo de análisis define los siguientes _roles_, responsables de ciertos _artefactos_:

1. **Arquitecto**: responsable de la **integridad** del modelo de análisis y de la **arquitectura** del modelo. Es responsable del:
   - **Modelo de análisis**: representa la estructura global del software y sus capas.
   - **Descripción de la arquitectura**: descompone el modelo de análisis en paquetes, identificando sus dependencias y las funcionalidades críticas del software.
2. **Ingeniero de Casos de Uso**: garantiza que las realizaciones de caso de uso cumplan con sus requisitos. Es responsable de la:
   - **Realización de casos de uso-análisis**: un conjunto de diagramas de clase con una descripción textual del flujo de sucesos (la interacción entre el usuario y el sistema).
3. **Ingeniero de Componentes**: define y mantiene responsabilidades, atributos, y relaciones de varias clases, y la integridad de uno o varios paquetes del análisis. Es responsable de la:
   - **Clase del análisis**: se definen responsabilidades. Hay estereotipos de _entidad_ (información), _control_ (comportamiento), e _interfaz_ (presentación).
   - **Paquete del análisis**: divide el trabajo en subsistemas de diseño, buscando la alta cohesión y bajo acoplamiento.

## Actividades

![[Flujo de Análisis en el PU.png]]

Se definen las siguientes _actividades_, ejecutadas por cierto rol y que a partir de ciertos artefactos generan otros nuevos o mejorados.

1. **Análisis de la Arquitectura**: el análisis arquitectónico consiste en realizar un boceto del modelo de análisis identificando los paquetes de análisis y los requerimientos especiales o importantes. Se busca separar funcionalidades por intereses para minimizar las dependencias.
2. **Análisis de un [[Caso de Uso del Sistema]]**: la realización en análisis de un caso incluye la descripción textual del flujo de eventos, diagramas de clases, y diagramas de interacción.
3. **Análisis de una Clase**: a una clase se le asigna un nombre, atributos, y relaciones. Se determinan las _responsabilidades_ de la clase.
4. **Análisis de un Paquete**: ante la necesidad o conveniencia, se agrupan clases en paquetes lo más independientes entre sí posible. Estos paquetes deben ser cohesivos y poco acoplados.

El modelo de análisis sirve como punto de inicio para el diseño, pero luego si durante el diseño surge la necesidad de cambiar el modelo, se lo puede hacer.

Así, el análisis ofrece una **visión general del sistema** de una manera conceptual, precisa, y unificada.
