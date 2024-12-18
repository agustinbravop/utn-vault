En el [[Paradigma Orientado a Objetos]], la **herencia** nos permite crear nuevas [[Clases]] que tengan los mismos atributos y métodos que otras clases, y expandirlos o cambiarlos. Esto generará una **jerarquía de clases** entre clases padres y clases hijas. Esta es la principal manera de reutilizar código en POO.

La relación se la debe pensar como *es-un*. Ej: un "Auto *es-un* Vehículo". Puede ser:

- **Herencia Simple**: la subclase tiene una sola clase padre.
- **Herencia Múltiple**: la subclase puede tener varias superclases. Esto puede llevar a un conflicto de nombres al tener dos métodos con el mismo identificador. Esta ambigüedad debe poderse resolver de alguna manera.

La herencia múltiple provoca el **problema del diamante**:

![[Problema del Diamante en la Herencia Múltiple.png]]

## Sobreescritura

Una subclase puede **redefinir** un método que hereda de la superclase para **personalizar su comportamiento**. Si bien puede cambiar su implementación, debe mantener la misma interfaz. Esto nos permite expandir sus capacidades sin romper interfaces existentes.

```
// Un método de una clase exhibe comportamiento distinto en subclases distintas
Cocinero.cocinar()  // "Hice comida."
Panadero.cocinar()  // "Hice pan."
```

En Java la sobreescritura se señala con `@Override`.
