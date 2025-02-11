Nos enfocamos en particular en la **robótica industrial**.

> Un *robot industrial* es un manipulador multifuncional reprogramable con varios grados de libertad capaz de manipular objetos según trayectorias programadas.

> Es una máquina de manipulación automática, reprogramable, y multifuncional, con tres o más ejes que pueden posicionar y orientar objetos para la ejecución de trabajos diversos en las diferentes etapas de la producción industrial.

Clasificación de los **robots** según el punto de vista industrial:

1. **Robots manipuladores**: pueden ser *manuales*, de *secuencia fija*, o de *secuencia variable*.
2. **Robots de repetición o aprendizaje**: repiten las acciones de un humano.
3. **Robots con control por computador**: muchos micro-procesadores.
4. **Robots inteligentes**: similares pero además tienen sensores para adaptarse al entorno.
5. **Micro-robots**.

**Generaciones** de robots:

1. **Primera**: repiten tareas secuencialmente. no tienen en cuenta el espacio ni su entorno.
2. **Segunda**: adquieren información limitada de su entorno.
3. **Tercera**: se programan con lenguaje natural, y auto-planifican sus tareas.

Principales **características** o factores a tener en cuenta, donde los requisitos de la producción determinarán cuáles factores son críticos:

1. **Grados de libertad**.

Cada **grado de libertad** es cada uno de los movimientos independientes (*giros* y *desplazamientos*) que puede realizar cada articulación. Se necesitan 3 grados para *posicionar* un cuerpo en el espacio, y otros 3 grados más para definir su *orientación*.

![[Grados de Libertad.png]]

Matemáticamente, cada grado de libertad representa una ecuación.

2. **Morfología**.

La estructura del manipulador y la relación entre sus elementos proporcionan una *configuración mecánica*. Configuraciones clásicas:

- **Cartesiana/rectilínea**: trayectorias lineales.
- **Cilíndrica**: 2 movimientos lineales y 1 rotacional.
- **Angular**: 3 juntas de rotación para posicionarse.
- **Scara**: *Selective Compliance assembly Robot Arm*.

Los movimientos pueden ser *lineales* (rectas) o *por articulación* (arcos).

3. **Espacio de trabajo**.

![[Espacio de Trabajo.png]]

El espacio de trabajo es el espacio o volumen en el que el robot se mueve. Distintas morfologías ocupan distintos volúmenes (por ejemplo, el robot cartesiano genera una figura cúbica, y el robot angular suele generar un espacio esférico).

4. **Alcance máximo**.

El alcance máximo es la medida desde el centro del robot en la mayor extensión del brazo.

5. **Precisión de los movimientos**.

La precisión es el incremento más pequeño de movimiento en el que el robot puede dividir su espacio de trabajo.

6. **Resolución espacial**.

La resolución espacial depende de las *inexactitudes* de la parte mecánica, y suele ir acompañada de un margen de error. Un [[Sistema de Control]] sirve para controlar todos los incrementos individuales de una articulación.

7. **Exactitud**.

La exactitud es la capacidad de un robot para *situar* el extremo de su muñeca en un punto señalado dentro de su volumen de trabajo. La exactitud disminuye a medida que el brazo se aleja de la base.

8. **Repetitividad**.

La repetitividad es la capacidad del robot de regresarse al punto programado las veces que sean necesarias.

9. **Capacidad de carga**.

La capacidad de carga es el peso que puede transportar la garra del robot. A mayor carga, menor precisión. 

![[Familia de Robots.png]]

Los robots suelen venir en familias del mismo fabricante. Cada robot de la misma familia se suele diferenciar del resto por su capacidad de carga.

10. **Velocidad y aceleración**.

Las velocidades altas aceleran el trabajo pero dificultan la operación. Es un dato considerable a la hora de elegir un robot, según la tarea que realizará.

11. **Seguridad**.

![[Seguridad de un Robot.png]]

La seguridad involucra definir por dónde es seguro que los operarios caminen y trabajen.

12. **Métodos de programación**.

Se puede programar un robot por programación *gestual* (por *aprendizaje directo*, como con un guante, o con un *dispositivo de enseñanza*, como un joystick), o por programación *textual* (usando un lenguaje de programación especial).

13. **[[Sensores]] y [[Actuadores]]**.
