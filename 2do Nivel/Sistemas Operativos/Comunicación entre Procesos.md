Entre los [[Proceso|procesos]] hay:

- **Competencia**: procesos independientes compiten por un recurso. En estos casos hay que gestionar los [[Interbloqueos]].
- **Cooperación**: los procesos comparten el acceso a un recurso. Esto requiere mecanismos de comunicación.

Modelos de comunicación entre procesos:

![[Modelos de Comunicación entre Procesos.png]]

## Condiciones de Competencia

Las _race conditions_ establecen situaciones en las que el resultado de la ejecución de varios procesos concurrentes depende del orden de ejecución de los mismos. La **exclusión mutua** garantiza que no hayan condiciones de competencia.

**Sección Crítica**: es la parte del programa que accede a la memoria compartida. Si se garantiza que solo un proceso está en su sección crítica a la vez, entonces se evitan las condiciones de competencia.

Para solucionar el problema de la sección crítica se requieren soluciones o **mecanismos de sincronización**. Existe:

- [[Sincronización de Procesos por Software]].
- [[Sincronización de Procesos por Hardware]].
