**SOLID** es un acrónimo con 5 principios de diseño [[Paradigma Orientado a Objetos|orientado a objetos]] que nos ayudan a crear código más **mantenible**, **entendible**, y **flexible**. Fue propuesto por Robert C. Martin (Uncle Bob). Los 5 principios son:

1. **Single Responsibility**: una clase/módulo/componente debe tener una sola responsabilidad a un solo usuario. También debe tener un solo motivo por el cual ser cambiado. Esto aumenta la cohesión del componente y mejora su reusabilidad.
2. **Open-Closed**: una clase debe estar abierta para su extensión (crear subclases) pero cerrada para su modificación. Se busca la mantenibilidad y el evitar bugs.
3. **Liskov Substitution**: si la clase `B` es subclase de `A`, deberíamos poder reemplazar `A` por `B` en todo lugar que se use `A` sin romper el comportamiento del programa. Esta flexibilidad se suele lograr mediante el uso de _interfaces_.
4. **Interface Segregation**: interfaces grandes deberían dividirse en interfaces más pequeñas para que sus clientes e implementadores solo se preocupen por los métodos que sí les interesan. Se busca una organización del código que fomente la reusabilidad.
5. **Dependency Inversion**: los módulos de alto nivel no deberían depender de módulos de bajo nivel, sino que ambos deberían depender de abstracciones. Una forma de invertir las dependencias es inyectarlas por parámetros en lugar de instanciarlas directamente.