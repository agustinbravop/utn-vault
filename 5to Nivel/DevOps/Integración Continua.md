
La **integración continua** (CI) es una práctica de desarrollo, dentro de la [[Entrega Continua]], que requiere que los desarrolladores integren su código varias veces al día. Cada registro ([[Sistemas de Control de Versiones|commit]]) es verificado por una build automatizada.

Principios de CI:

- Mantener un único repositorio.
- Automatizar la construcción y su [[Testing]].
- Todos deben mergear código todos los días.
- Probar en un clon del ambiente productivo.
- Todos deben poder ver los resultados.
- Arreglar los tests rotos lo más rápido posible.

Beneficios:

- Detecta errores temprano.
- Aumenta la visibilidad.
- Facilita las integraciones.

## Inspección de Código Estática

El linting y otros static checks buscan elevar la calidad del código. Puede facilitar el mantenimiento. El análisis es estático porque no se ejecuta el código. Técnicas:

- Análisis de sintaxis.
- Análisis de flujo de control.
- Seguridad.
- Estándares de formato.

Estos analizadores usan heurísticas y conjuntos de reglas, por lo que son best-effort y pueden dar falsos negativos/positivos. Se pueden usar durante todo el ciclo de desarrollo.
