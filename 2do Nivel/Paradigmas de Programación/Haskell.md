**Haskell**, en nombre a Haskell Curry, es un lenguaje de programación perteneciente al [[Paradigma Funcional]] que implementa conceptos del [[Cálculo Lambda]]. Su primera especificación fue en 1980. Algunas de sus características son:

- **Inferencia de Tipos**: Haskell es fuertemente tipado pero puede deducir el tipo de una entidad declarada analizando sus parámetros y las expresiones de su cuerpo. Usa el método de Hindley-Milner.
- **Polimorfismo de Parámetros**.

Un programa consiste en un conjunto de definiciones `<nombre> <parámetros> = <cuerpo>`. Por ejemplo: `factorial 0 = 1; factorial n = n * factorial(n - 1)`.

## Tipos

La función `name p1 p2 = <expr>` es de tipo `name :: t1 -> t2 -> result_type`, y es este último `result_type` el tipo de dato del valor retornado.

Todos los tipos son de primera clase:

```
Int                      // entero corto
Integer                  // entero ilimitado
Char                     // carácter
[Char]                   // lista de caracterse (string)
[Char] -> (Bool, Double) // función que aplica un string sobre una tupla
```

Se pueden crear sinónimos de tipos: `type Nombre = [Char]`.

Se puede hacer **álgebra booleana** con los valores `True` y `False`. El AND lógico se hace con el operador `&&`, definido como `&& :: Bool -> Bool -> Bool` (toma dos parámetros booleanos y devuelve un resultado booleano).

Se puede crear **operadores nuevos** combinando los símbolos `:!#$%&*+./<=>?@\^|`. Se les puede declarar una **asociatividad**: `infixl`, `infixr`, o `infix`, y una **precedencia** (su "fuerza de atracción"): entre 0 y 9.

```
infixr 2 ||
infixr 3 &&  // Primero se resuelve el AND, luego el OR
infix 4 ==
```

La asociatividad se puede evitar poniendo al operador entre paréntesis.

```
x || y = (||) x y
x <op> y = (<op>) x y
```

Los **tipos algebráicos** son la suma de otros tipos. Se pueden definir por enumeración, unión, y recursión:

```haskell
data Color = Red | Green | Blue  -- definido por enumeración
data Maybe a = Nothing | Just a  -- definido por unión
data Arbol a = Hoja a | Rama (Arbol a) (Arbol a)  -- definido por recursión
```

## Patrones

Los parámetros formales de una función pueden ser **patrones** y no solo identificadores. Estos patrones se _matchean_ a los parámetros reales al momento de llamar la función.

```
x, _                   // `_` es un patrón irrefutable, siempre matchea
3                      // patrones literales
[], (x:xs), [_, x, _]  // patrones para listas
(x, y)                 // patrones para tuplas
```

## Cláusulas

`where` sirve para declarar expresiones/definiciones locales dentro de una función.

```haskell
inversa lista = inv_ac lista []
	where
		inv_ac [] ys = ys
		inv_ac (x:xs) ys = inv_ac xs (x:ys)
```

El bloque `let-in` permite que identificadores definidos en `let` sean accesibles dentro de `in`.

```haskell
4 * (let a = 9 in a + 1) == 40
```

`case` es similar a un `switch` condicional, pero que además permite usar _pattern matching_.

```haskell
describeList xs = case xd of
	[] -> "Lista vacía"
	[x] -> "Lista unitaria"
	xs -> "Lista larga"
```

## Listas por Compresión

Se pueden crear listas por compresión siguiendo la notación Zermelo-Fraenkel: `[exp | x <- xs, <guardas_booleanas>]`. Por ejemplo, para generar una lista con todos los múltiplos de dos:

```haskell
[2 * x | x <- [1..]]
```

Una lista vacía:

```haskell
[2 | 2 > 3]  -- devuelve `[]`
```

El espacio muestral de tirar dos dados de seis caras:

```haskell
[(x, y) | x <- [1..6], y <- [1..6]]
```

## Funciones

Las **funciones lambda** son funciones anónimas que se pasan por parámetro a otras funciones. Se escriben de la forma `\x y -> <cuerpo>`. Son usadas por funciones de orden superior, que son funciones que reciben o devuelven otras funciones.

Existen varios esquemas funcionales:

1. **Filtros**: `filter :: (a -> Bool) -> [a] -> [a]` retorna una lista con solo los elementos que cumplen una condición.
2. **Iteradores**: `map :: (a -> b) -> [a] -> [b]` retorna una lista de misma longitud, aplicando la función recibida por parámetro a cada elemento para obtener el elemento nuevo.
3. **Generadores**: `iterate :: (a - a) -> a -> [a]` genera una lista según el valor dado.
4. **Plegadores**: `foldl :: (b -> a -> b) -> b -> [a] -> b` retorna un único valor acumulado al recorrer todos los elementos de la lista (desde la izquierda). `scanl` es una alternativa que también devuelve los valores totales intermedios como una lista.

Se puede **componer funciones** con el operador `. :: (b -> c) -> (a -> b) -> a -> c`. Por ejemplo, para negar los números positivos (generados con una lista por comprensión `[1..]`), en lugar de hacer `map (\x -> negate (abs x)) [1..]` se podría simplemente hacer `map (negate . abs) [1..]`.

### Redes de Procesos de Kahn (KNP)

Se considera que las funciones que consumen o producen listas infinitas trabajan con **flujos de datos**. Gracias a la [[Abstracciones#Orden de Evaluación|evaluación peresoza]], esto se hace de forma incremental (en lugar de que el programa se estanque por nunca terminar de generar la lista infinita):

```haskell
fibs = 1 : 1 : zipWith (+) fibs (tail fibs)  -- Genera la serie de Fibonacci
```
