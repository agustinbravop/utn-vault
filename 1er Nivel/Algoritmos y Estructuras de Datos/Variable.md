Una variable en [[Pseudocódigo]] es un **identificador** asociado a un **dato**. Se definen en el **ambiente** de los programas.

```
AMBIENTE
	FILA = 12           // constante.
	RESP: AN(1)         // variable alfanumérica de un caracter.
	a, b: N(3)          // dos variables enteras de tres cifras.
	día: RANGO 1...31   // variable entera con valores posibles entre 1 y 31.
	v: caracter         // idéntico a AN(1).
	S: secuencia de caracteres
	VOCAL = { "a"; "e"; "i"; "o"; "u" }  // secuencia definida por nosotros.
```

## Constante

Es una variable cuyo valor inicialmente asignado **no se puede cambiar**.

## Global

Variables declaradas en el [[Algoritmo]] principal, usable por cualquier subproceso del algoritmo.

## Local

Variable solo disponibles dentro de la subacción (por ejemplo una [[Función]] o un [[Procedimiento]]) que la declara.
