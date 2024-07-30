Las estrategias de prueba le dan una estructura a las [[Técnicas de Diseño de Casos de Prueba]] para integrarlas en una serie de pasos.

**Verificación**: ¿Estamos construyendo correctamente? (es interno, del equipo)
**Validación**: ¿Estamos construyendo lo correcto? (es externo, del cliente)

![[Estrategias de Prueba 2024-06-21 03.26.28.excalidraw.svg]]

Conviene hacer muchas pruebas unitarias (porque son baratas) y solo las suficientes pruebas de alto nivel (porque son caras).

## Tipos de Pruebas

### Pruebas Unitarias

Testean un **componente** (función o método) atómico.

### Pruebas de Integración

Testean la **interacción** entre varios componentes. Se utilizan mocks y fakes para simular dependencias.

- **Pruebas de regresión**: detectan que nuevos cambios no rompan funciones previas. Alcanzan mucha amplitud, pero poca profundidad. Son las que conviene automatizar.
- **Pruebas de humo**: prueban el funcionamiento correcto de nuevas funcionalidades o cambios.

### Pruebas de Validación

Prueban que el software funcione acorde a las **expectativas razonables** del **cliente**.

### Prueba del Sistema

El software es **solo una pieza más** del sistema. Probamos el software junto con el hardware, las personas, los procedimientos, etc. Es el **uso real**. Ejemplos: de **recuperación**, de **seguridad**, de **resistencia**, de **rendimiento**.
