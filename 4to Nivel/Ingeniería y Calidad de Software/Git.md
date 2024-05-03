Git es un [[Sistemas de Control de Versiones|Sistema de Control de Versiones]] que trabaja con repositorios distribuidos. Es de código abierto y es el estándar actual en la industria.

Terminología:

- Repositorio = linea base.
- Pull = check out.
- Commit o push = check in.

## Merges

Dada la gran variedad de merges que se pueden hacer, conviene utilizar una [[Estrategias de Branch y Merge]]. La más popular y completa actualmente es [[Estrategias de Branch y Merge#Gitflow Workflow|GitFlow]].
![[Pasted image 20240428191713.png]]

### Fast-Forward Merge

Mueve el label de la rama base a la punta de la rama con la funcionalidad. La historia de commits resultante es lineal. Por defecto el comando `git pull` hace un fast-forward merge.
![[Pasted image 20240428185529.png]]

### Merge Commit

Un merge commit combina el trabajo de ambos HEAD y coloca el resultado en un solo commit. Ese commit siempre tiene múltiples padres, resultando en una **historia no lineal**, la cual facilita de identificar las distintas ramas usadas en el desarrollo.
![[Pasted image 20240428191005.png]]

### Merge Conflict

Sucede cuando una persona necesita tomar una decisión. Pueden ocurrir cuando ramas distintas cambian la misma parte de un archivo de maneras diferentes.
![[Pasted image 20240428190314.png]]
Están en juego tres commits:

- El HEAD de la rama actual ("ours").
- El HEAD de la rama a mergear ("theirs").
- El primer commit que sea un ancestro común ("merge base").
  ![[Pasted image 20240428190845.png]]

### Rebase

Un rebase mueve commits a un nuevo padre o nueva base. Como regla general NO se debe reescribir historia compartida con otros. Solo es seguro rebasear una rama cuando nadie más utilizó la rama en cuestión.

Al rebasear, Git aplica los diffs de cada commit al nuevo commit padre. Esto es una forma de merge ==> es **susceptible a producir merge conflicts**.
![[Pasted image 20240428191234.png]]
