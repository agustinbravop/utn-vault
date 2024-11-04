LA asignación por **paginación simple** permite a la [[Administración de Memoria]] reducir la [[Fragmentación]] externa de una manera **transparente** para el usuario (o [[Proceso]]). 

![[Asignación por Paginación Simple.png]]

En la **tabla de páginas** del proceso, para cada página se guarda un **bit de permiso** ($v$ de válido o $i$ de inválido) para acceder a esa página, o algún código que indica el permiso de lectura/escritura/ejecución. 
