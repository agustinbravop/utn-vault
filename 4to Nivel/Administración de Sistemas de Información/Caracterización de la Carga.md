En el subsistema de [[Aplicación de SW y HW]], para evaluar correctamente las prestaciones de un SI, la [[Carga de Trabajo]] debe ser cuidadosamente seleccionada. La **carga de prueba** es la carga utilizada en la [[Evaluación de las Prestaciones]]. Esta carga puede ser *real* o *sintética*.

La **carga real** de un sistema informático **cambia continuamente** y las mediciones no pueden repetirse (excepto al trabajar en un entorno controlado de carga). Por esto para probar el sistema se suele usar un modelo de carga o **carga sintética** construida por un conjunto de programas que reproduce la carga real de manera compacta y repetible.

Son **cualidades deseables** de la carga de prueba:
- **Reproductibilidad**: poder probar varias veces.
- **Compacidad**: que compacte el tiempo de prueba.
- **Compatibilidad**: consistente con el uso de la carga.
- **Representatividad**: el modelo retiene los aspectos de la carga real. 
- **Flexibilidad**: que sea fácil adaptar el modelo.
- **Independencia del sistema**.
## Magnitudes que Caracterizan la Carga

Estas [[Magnitudes de un SI]] dependerán del tipo y modo de trabajo el sistema. Son **mediciones del rendimiento** del hardware y del sistema operativo del SI cuando está **bajo esfuerzo** de la carga. La carga de trabajo queda caracterizada por un conjunto de **parámetros**:
- **Cuantitativos**: **surgen directamente** de la carga y sus variables. Se suelen poder medir.
- **Cualitativos**: surgen indirectamente del **comportamiento**. Suelen ser representadas como porcentajes o niveles. Por ejemplo, las [[Magnitudes de un SI#Variables Relativas al Comportamiento|variables relativas al comportamiento]] (fiabilidad, etc).

La **carga de prueba** es obtenida al **caracterizar la carga real** mediante parámetros cualitativos y cuantitativos y funciones descriptivas del funcionamiento del sistema. Este **modelo de carga** resultante debe ser representativo.

### Para cada Componente de la Carga

Analizando cada transacción o programa por separado:
- **Tiempo de CPU por trabajo** (programa, transacción, etc).
- **Número de operaciones de E/S por trabajo**.
- **Características de las operaciones de E/S por trabajo** (soporte físico como cinta, disco, etc).
- **Prioridad** (asignada por el usuario para el procesador).
- **Memoria** (para la ejecución).
- **Localidad de las referencias** (páginas del SO).

### Para el Conjunto de la Carga

Analizando todo el conjunto de trabajos al mismo tiempo:
- **Tiempo entre llegadas** (entre dos requerimientos sucesivos)
- **Frecuencia de llegada** (promedio de llegadas por unidad de tiempo)
- **Distribución de trabajos** (proporción entre las ejecuciones de los distintos trabajos)

### Para Cargas Conversacionales

Solo para sistemas interactivos:
- **Tiempo de reflexión del usuario** (lo que el usuario tarda para generar una nueva petición)
- **Número de usuarios simultáneos** (en un instante dado)
- **Intensidad del usuario** (relación entre tiempo de respuesta y tiempo de reflexión)

## Magnitudes para Controlar el Comportamiento

Permiten **mejorar el comportamiento** del sistema cuando no es satisfactorio. Son **modificaciones** que pueden introducirse en todos los niveles sistema que influyen en su comportamiento:
- **Ajuste de los parámetros del SO**: hay variedad de parámetros de un SO que adaptan con facilidad la planificación de la CPU y la partición de memoria.
- **Modificación de las políticas de gestión del SO**: personalizar el SO es riesgoso y dificulta actualizarse a versiones nuevas. Solo útil cuando la carga tiene particularidades específicas.
- **Equilibrado de la distribución de cargas**: (*load balancing*) utilizar todos los dispositivos del SI de la forma más **uniforme** posible.
- **Sustitución o ampliación de los [[Componentes de un SI|componentes]] del sistema**: cuando los métodos anteriores resultan ineficaces, se debe **modificar la configuración** del sistema para despejar el cuello de botella en el elemento saturado. Puede ser:
	- Vertical: se sustituyen elementos por otros de mayor capacidad o rapidez.
	- Horizontal: se aumenta el número de dispositivos.
- **Modificación de los programas**: recodificación para que sean más eficientes respecto de los recursos que consumen. Si bien es un procedimiento frecuente, normalmente se considerará a la carga como un dato del problema que no se puede modificar.

## Representatividad de un Modelo de carga

La carga