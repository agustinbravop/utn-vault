Usar ramas permite aislar cambios y errores en una historia paralela a la principal del repositorio o linea base. Usar una estrategia permite **estandarizar** en el equipo de desarrollo el cómo utilizar ramas y cómo unirlas.

## Feature Branching

Se crea una rama por cada nueva funcionalidad y solo se une a la historia principal cuando está terminada y sin errores. Esto significa que `main` no debería tener código que no funciona.

## Release Branching

Se crea una rama por cada release a entregar.

## Task Branching

Se crea una rama por cada tarea concreta. Estas ramas son las más minimalistas. Propuesto por Atlassian.

## Gitflow Workflow

Es una combinación de las otras estrategias y es el estándar actual de la industria. Tiene en cuenta la integración continua. Surge de un blog de 2010 por Vincent Driessen.
![[Gitflow.png]]
Las ramas que define son:

- **Main**: es la rama principal que representa a producción.
- **Develop**: la rama más usada, representa a la versión actual de desarrollo.
- **Release**: cada rama que sea candidata a mergearse a main y pasar a producción.
- **Hotfixes**: ramas para arreglar rápidamente algún defecto.
- **Features**: ramas que agregan una funcionalidad nueva.
