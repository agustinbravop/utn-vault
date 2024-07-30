Una función es un _subalgoritmo_ que recibe **parámetros** y devuelve un único **resultado**. Hay **funciones internas** (o intrínsecas o predefinidas) que ya vienen incorporadas al sistema. El usuario puede **definir funciones** de manera externa.

```
FUNCION [nombre]([parámetros]): [tipo_retorno]
	[declaraciones_locales]
	[acción]
FIN_FUNCIÓN
```

Ejemplo de la lista de parámetros: `l: char, n: numérico`.

En algún lugar del cuerpo ejecutable de la función, debe estar la [[Asignación]] `nombre_función := valor_de_retorno` para que la función devuelva un **resultado**.

Una [[Variable]] **formal** se usa para definir la función y luego es reemplazada por los **parámetros**. Las funciones tienen acceso al **ambiente global** del [[Algoritmo]] y se suelen definir allí.
