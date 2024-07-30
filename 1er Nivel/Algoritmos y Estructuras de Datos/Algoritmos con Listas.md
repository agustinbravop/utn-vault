Una [[Lista]] requiere ciertos algoritmos comunes para su tratamiento.

Los siguientes ejemplos asumen este ambiente:

```
NODO: registro de
	siguiente: puntero a NODO
	dato: [tipo_de_contenido_almacenado]
FIN_REGISTRO
q: NODO
p, primero: puntero a NODO
objetivo: [tipo_de_contenido_almacenado]
```

## Insertar al Inicio

Se debe crear un nodo nuevo que apunte al primer nodo de la lista y actualizar el puntero al primer nodo de la lista para que apunte al nodo nuevo.

```
Nuevo(q)
q^.siguiente := primero
q^.dato := [contenido]
primero := q
```

## Insertar al Final

```
p := primero
MIENTRAS p <> nil HACER
	p := p^.siguiente
FIN_MIENTRAS
p^.siguiente := q  // q es el último nodo.
```

## Insertar `q` Entre `anterior` y `siguiente`

```
q^.siguiente := siguiente
anterior^.siguiente := q
```

## Iterar Sobre la Lista

```
p := primero
MIENTRAS p <> nil HACER
	Escribir(p^.dato)
	p := p^.siguiente
FIN_MIENTRAS
```

## Borrar la Lista Entera

```
p := primero
MIENTRAS p <> nil HACER
	a := p^.siguiente
	Borrar(p)
	p := a
FIN_MIENTRAS
```

## Buscar un Elemento

```
p := primero
Leer(objetivo)
MIENTRAS p <> nil Y p^.dato <> objetivo HACER
	p := p^.siguiente
FIN_MIENTRAS

SI p <> nil ENTONCES
	Escribir("Encontrado!")
FIN_SI
```
