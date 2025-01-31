> "La **simulación** es la imitación de la operación de un proceso del mundo real o de un sistema a través del tiempo". - Banks, 1988.

Realizar una simulación implica la generación de una _historia artificial_ del sistema y la observación de esa historia artificial para hacer inferencias concernientes al funcionamiento operativo del sistema real que se estudia.

Desde el punto de vista de la simulación, los elementos del [[Sistema]] deben tener una frontera clara, y se lo considera la "porción de la realidad" que separamos para estudiar. Los sistemas pueden ser:

- **Estáticos**: la variable tiempo no importa.
- **Dinámicos**: analizamos su evolución a lo largo del tiempo. Pueden ser continuos o discretos.

Además, los sistemas pueden ser:

- **Determinísticos**: tienen una solución analítica ($y = f(x)$).
- **Estocásticos**: son probabilísticos ($y = P(x)$), y por eso es necesario simularlos.

Utilizar un [[Modelo de Simulación]] para nalizar los posibles resultados de un sistema estocástico nos permite plantear distintos escenarios para pensar respuestas a ellos. A la larga, la simulación es una herramienta para la toma de decisiones.

## Aplicaciones de la Simulación

La simulación permite **acercarse a un sistema para entenderlo**, diagnosticar problemas, y explorar posibilidades de cambio, todo sin necesidad de simular sobre el sistema real, lo que abarata costos. Algunas aplicaciones:

- **Procesos de manufactura**: para detectar cuellos de botella, distribuir personal.
- **Plantas industriales**: para establecer condiciones óptimas de operación.
- **Sistemas públicos**: construcción, educación, salud, recolección de basura.
- **Sistemas de transporte**: colectivos, subtes, aviones.

La desventaja es que desarrollar un modelo requiere experiencia con el sistema y puede ser costoso, laborioso, y lento. Los resultados pueden ser malinterpretados, y se puede desconocer el verdadero grado de imprecisión de los datos.

## Etapas de Una Simulación

Estas etapas no son estrictamente secuenciales, y pueden ser cíclicas:

1. **Formulación del problema**: normalmente es traído por un cliente.
2. **Definición del sistema**: entender el sistema real mediante la observación y análisis.
3. **Formulación del modelo**: definir elementos para una aproximación artificial del sistema real.
4. **Colección de datos**: es crítico hacer una buena recolección de datos representativos del sistema. Esto es lo que más tiempo lleva, y la eficacia depende de la calidad de los datos.
5. **Implementación del modelo en la computadora**: programación.
6. **Verificación**: se comprueba no haber cometido errores en la implementación.
7. **Validación**: se comprueba la exactitud del modelo desarrollado.
8. **Diseño de experimentos**: se definen características de los experimentos a realizar, como el tiempo de arranque, la cantidad de simulaciones, etc.
9. **Experimentación**: se corren las simulaciones y se recolectan sus resultados.
10. **Interpretación**: se analiza la sensibilidad del modelo.
11. **Documentación**: se reporta un informe sobre los resultados de la simulación.
12. **Implementación**: se toma una decisión que impacte al sistema real. Esto suele ser trabajo de otra persona, no del analista que diseña la simulación.

Este proceso suele ser iterativo y colaborativo, tiempo durante el cual uno se familiariza con el sistema y aprende sobre su comportamiento.

Se irá construyendo y validando la historia ficticia del sistema, para así hacer confiable a la simulación.
