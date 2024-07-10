Es un proceso de **experimentación** que va **ajustando parámetros** en base a una **hipótesis** para mejorar el [[Rendimiento de un SI]].

A rasgos generales, los estudios de sintonización siguen estos pasos:

1. Plantear el problema.
2. Medir e interpretar.
3. Tomar acciones y verificar sus efectos.

![[Proceso de Sintonización de un Sistema.png]]

## 1. Definición de Objetivos

Se determinan los objetivos del estudio y los tipos de datos a obtener. Da las prioridades a cada aspecto del estudio, lo que permite usar la metodología y herramientas más convenientes.

Analizar requerimientos $\to$ Definir entorno $\to$ Identificar variables a analizar.

## 2. Caracterización de la Carga

Se hace la [[Caracterización de la Carga]] para realizar pruebas con una [[Carga de Prueba]] o modelo de prueba.

Analizar información disponible $\to$ Seleccionar carga de test $\to$ Construir el modelo de carga.

## 3. Selección de la Instrumentación

¿Cómo medir las variables baho estudio?

Áreas de estudio:

- Componentes de HW del sistema.
- SW del sistema (SO + programas de sistema y de usuario).
- La carga.

## 4. Diseño del Experimento

Se toman **medidas** en un **entorno controlado** con **carga conocida**. Se debe conocer, aproximadamente, a carga y su evolución en el tiempo (especialmente los picos de carga).

Si se usa un [[Monitor]] de software: considerar los recursos que usa. Si es de hardware: verificar la correcta conexión de sus sensores.

## 5. Validación

Se **interpretan** los resultados para ver si se lograron los objetivos. Si no se lograron, se **sintoniza** y se experimenta de nuevo.
