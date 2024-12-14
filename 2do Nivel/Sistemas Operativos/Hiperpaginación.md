La **hiperpaginación** es un problema de la [[Memoria Virtual]] que sucede cuando el sistema pierde mucho tiempo trayendo/sacando páginas.

Si un proceso tiene pocas páginas, la **tasa de fallos de página** es alta. A mayor grado de multiprogramación, más fallos de páginas.

Una técnica para evitar la hiperpaginación es el conjunto de trabajo o _working set_.

## Conjunto de Trabajo

El _working set_ $\text{WS}(t, \Delta)$ es el conjunto de páginas que se referenciaron en las últimas $\Delta$ unidades de tiempo.

> **Principio del Working Set**: un proceso solo puede ejecutarse si su $\text{WS}$ está en memoria principal. Una página no puede retirarse de memoria principal si está en el $\text{WS}$ del proceso en ejecución.

> **Principio de Localidad**: durante cualquier fase de ejecución, un proceso referencia un porcentaje bajo de sus páginas. Esas localidades pueden solaparse.

Sea $\sum{\text{WS}_i}$ la cantidad de **marcos demandados**. Si $\sum{\text{WS}_i} \gt$ marcos totales $\implies$ hay hiperpaginación $\implies$ se debe suspender un proceso.
