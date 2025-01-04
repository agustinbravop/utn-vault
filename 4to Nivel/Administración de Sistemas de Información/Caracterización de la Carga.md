En el subsistema de [[Aplicación de SI y TI]], para evaluar correctamente las prestaciones de un SI, la [[Carga de Trabajo]] debe ser cuidadosamente seleccionada. La [[Carga de Prueba]] es la carga utilizada en la [[Evaluación de las Prestaciones]]. Esta carga puede ser _real_ o _sintética_.

## Magnitudes que Caracterizan la Carga

Estas [[Magnitudes de un SI]] dependerán del tipo y modo de trabajo el sistema. Son **mediciones del rendimiento** del hardware y del sistema operativo del SI cuando está **bajo esfuerzo** de la carga. La carga de trabajo queda caracterizada por un conjunto de **parámetros**:

- **Cuantitativos**: **surgen directamente** de la carga y sus variables. Se suelen poder medir.
- **Cualitativos**: surgen indirectamente del **comportamiento**. Suelen ser representadas como porcentajes o niveles. Por ejemplo, las [[Magnitudes de un SI#Variables Relativas al Comportamiento|variables relativas al comportamiento]] (fiabilidad, etc).

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

Solo para [[Sistemas Interactivos]]:

- **Tiempo de reflexión del usuario** (lo que el usuario tarda para generar una nueva petición)
- **Número de usuarios simultáneos** (en un instante dado)
- **Intensidad del usuario** (relación entre tiempo de respuesta y tiempo de reflexión)

## Magnitudes para Controlar el Comportamiento

Permiten **mejorar el comportamiento** del sistema cuando no es satisfactorio. Son **modificaciones** que pueden introducirse en todos los niveles sistema que influyen en su comportamiento:

- **Ajuste de los parámetros del SO**: hay variedad de parámetros de un SO que adaptan con facilidad la planificación de la CPU y la partición de memoria.
- **Modificación de las políticas de gestión del SO**: personalizar el SO es riesgoso y dificulta actualizarse a versiones nuevas. Solo útil cuando la carga tiene particularidades específicas.
- **Equilibrado de la distribución de cargas**: (_load balancing_) utilizar todos los dispositivos del SI de la forma más **uniforme** posible.
- **Sustitución o ampliación de los [[Componentes de un SI|componentes]] del sistema**: cuando los métodos anteriores resultan ineficaces, se debe **modificar la configuración** del sistema para despejar el cuello de botella en el elemento saturado. Puede ser:
  - Vertical: se sustituyen elementos por otros de mayor capacidad o rapidez.
  - Horizontal: se aumenta el número de dispositivos.
- **Modificación de los programas**: recodificación para que sean más eficientes respecto de los recursos que consumen. Si bien es un procedimiento frecuente, normalmente se considerará a la carga como un dato del problema que no se puede modificar.

## Representatividad de un Modelo de Carga

La **carga de prueba** es obtenida al **caracterizar la carga real** mediante parámetros cualitativos y cuantitativos y funciones descriptivas del funcionamiento del sistema.

El **modelo de carga** $W'$ resultante representa perfectamente a la carga $W$ si es representativo a nivel físico, virtual, funcional y de comportamiento.

### Representatividad a Nivel Físico

Se basa en los **consumos** absolutos o unitarios de los **recursos** de hardware y software. Útil para evaluar la eficiencia de la **sintonización** de un sistema o determinar su **capacidad residual**. Los parámetros (mediciones de variables) son recopilados por rutinas de _logging_ del SO, fácilmente obtenibles.
$$W' \equiv  W \iff \text{solicita los mismos recursos físicos en las mismas proporciones.}$$

### Representatividad a Nivel Virtual

Se consideran los **recursos lógicos** desde el punto de vista del **programador**. Tiene que ver con la **configuración** del sistema. Aparecen variables del sistema operativo. Los parámetros son difíciles de obtener y requieren instrumentos especiales.
$$W' \equiv  W \iff \text{solicita los mismos recursos físicos con la misma frecuencia.} $$

### Representatividad a Nivel Funcional

La carga se determina por las **aplicaciones** que la componen (programas que simulan funciones de la carga original). Es **independiente del sistema** y por eso es útil para comparar sistemas en un estudio de **adquisición**.
$$W' \equiv  W \iff \mbox{realiza las mismas funciones con las mismas proporciones.} $$

### Representatividad a Nivel de Comportamiento

Tiene en cuenta los [[Magnitudes de un SI#Variables Relativas al Comportamiento|índices de comportamiento]] conocidos del sistema real para evaluar la validez del modelo por los **efectos** que produce en el sistema. El modelo depende del sistema.
$$W' \equiv  W \iff \mbox{produce los mismos valores de los índices de comportamiento.} $$
