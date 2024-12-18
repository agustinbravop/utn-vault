Un sistema de tipos es el enfoque que un lenguaje de programación le da a sus [[Tipos de Dato]]. Pueden ser:

- **Monomórficos**: cada variable y parámetro se declara con un tipo específico.
- **Polimórficos**: se usan estrategias que relajan el control de tipos.

## Polimorfismo

**Polimorfismo de Parámetros**: las [[Abstracciones]] pueden operar uniformemente sobre argumentos de una amplia gama de tipos. Los parámetros pueden ser de varios tipos, siempre y cuando respeten el formato establecido.

**Polimorfismo de Inclusión**: es la capacidad de las subclases y subtipos de heredar operaciones de sus tipos padres. Si $C$ es una clase, entonces incluye objetos de la clase $C$ o de subclases de $C$.

### Sobrecarga

La sobrecarga, o el **polimorfismo ad-hoc**, sucede cuando un número determinado de abstracciones están asociadas al mismo identificador en el mismo ámbito. Ej: una función del mismo nombre pero varias implementaciones distintas para parámetros de distinto tipo.

```
// Las 3 funciones calculan un sueldo, pero lo hacen de distinas maneras
calcSueldo(g Gerente)
calcSueldo(v Vendedor)
calcSueldo(f Freelance)
```

La sobre carga puede ser:

- **Independiente del contexto**: requiere que las implementaciones de la función tengan distintos parámetros para diferenciarlas.
- **Dependiente del contexto**: si los parámetros coinciden, pero el tipo de retorno es distinto, el compilador analiza el contexto de dónde se llama la función para decidir qué tipo se espera. Ej: para diferenciar entre `div(a, b: int) -> int` y `div(a, b: int) -> float`.

## Conversión de Tipos

La conversión de tipos es un [[Conceptos Generales de Programación#Mapeo|mapeo]] entre valores de un tipo a otro. Puede ser por:

- **Casteo**: es una conversión **explícita** solicitada por el programador. `(int) div(5.2, 2.4)`. 
- **Coerción**: es una conversión **implícita** inferida por el lenguaje. Suelen ser seguras.

## Tipos Parametrizados

Un **tipo parametrizado** toma otro tipo como parámetro. Ej: `List<int>`.
