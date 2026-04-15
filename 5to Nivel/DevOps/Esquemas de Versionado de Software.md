Los *versioning schemas* son una forma de asignar una versión a una build. El versionado que se quiera usar depende del equipo y del proyecto. Esquemas:

- **SemVer**: `v1.4.0-beta.2`. Es muy popular.
- **Según la etapa de desarrollo**: `alpha`, `beta`, `RC` (release candidate), `release`.
- **CalVer**: según el calendario.
- **URLs**: `/api/v1/products`, `/api/products?version=1`.

Se debe mantener la compatibilidad con versiones anteriores. Los cambios se deben comunicar con claridad y la documentación también debe ser versionada.

Es conveniente seguir estándares y convenciones de la industria. Conviene planificar esto y diseñar para el crecimiento a largo plazo.

Las [[Bases de Datos]] también deberían ser versionadas (al menos sus esquemas).
