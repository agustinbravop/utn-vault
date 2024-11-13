Un hilo, **thread**, o proceso ligero, comparte la imagen de memoria y otra información con otros hilos de un [[Proceso]]. Si un proceso tiene varios hilos, tiene más de un flujo de ejecución.

![[Hilos.png]]

En un [[Sistema Operativo]] **multihilos**, la unidad básica de uso del CPU es el hilo. Cada hilo tiene su propio contador de programa, registros, pila, y estado. El resto de información del proceso es compartida entre los hilos.

| Procesos hijos de un proceso | Hilos de un mismo proceso    |
| ---------------------------- | ---------------------------- |
| Manejados por el SO          | Manejados por el proceso     |
| Memoria privada              | Memoria compartida           |
| Más pesados                  | Más livianos                 |
| Más lentos de crear          | Más rápidos de crear         |
| Independientes               | Relacionados con otros hilos |
| Pueden crear procesos hijos  | No existen "hilos hijos"     |

La [[Planificación de Procesos]] para los hilos puede ser:

1. **Por prioridades**.
2. **Variación dinámica del quantum**: para sistemas interactivos.
3. **Forzada**: el proceso decide.
4. **Por afinidad**: un hilo busca ejecutarse siempre en el mismo procesador.

## Hilos a Nivel de Usuario

El proceso gestiona los hilos con una librería de hilos, sin que el SO se entere.

![[Hilos a Nivel de Usuario.png]]

Los cambios de contexto son rápidos porque no requieren [[Llamadas al Sistema]], pero las aplicaciones multihilo no pueden usar paralelismo, porque una syscall del proceso bloquea a todos sus hilos.

## Hilos a Nivel de Kernel

El SO soporta los hilos y crea un thread de kernel por cada thread de usuario.

![[Hilos a Nivel de Kernel.png]]

El kernel puede planificar múltiples hilos en simultáneo, incluso las propias funciones del SO, pero el paso de control de un hilo a otro requiere un cambio de modo.
