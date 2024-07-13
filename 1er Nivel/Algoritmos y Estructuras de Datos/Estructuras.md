Las estructuras en [[Pseudocódigo]] son un conjunto de instrucciones que tiene un encabezado y un pie con palabras reservadas. Permiten modificar el **flujo de control**.

## Condicionales

Ejecutan cierto código solo si se cumple cierta condición.

### Simple

```
SI [condición] ENTONCES [acción] FIN_SI
```

### Alternativa

```
SI [condición] ENTONCES 
	[acción_1]
SINO
	[acción_2]
FIN_SI
```

### Múltiple

```
SEGÚN [variable_de_control] HACER 
	[valor_1]: [acción_1]
	[valor_2]: [acción_2]
	[valor_3]: [acción_3]
	[valor_4]: [acción_4]
OTROS [acción_por_defecto]
FIN_SEGUN
```

## Iterativas

Ejecutan el mismo código repetidas veces.

### Definidas

Son manejadas por un [[Asignación#Contador|Contador]].

```
PARA x := 1 a [tope] HACER
	[acción]
FIN_PARA
```

### Indefinidas

**Post test**: repite hasta que sea verdadero (mientras que sea falso). Siempre se ejecuta al menos una vez, dado que la condición de freno se evalúa al final de cada iteración.

```
REPETIR
	[acción]
HASTA QUE [condición] FIN_REPETIR
```

**Pre test**: repite mientras sea verdadero (hasta que sea falso).

```
MIENTRAS [ccondición] HACER
	[acción]
FIN_MIENTRAS
```
