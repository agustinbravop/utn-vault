Robert C. Martin (Uncle Bob) enuncia en el 2000 un conjunto de 5 principios para el diseño [[Métodos Orientados a Objetos|orientado a objetos]] enfocados en elaborar **software de calidad**. Varios de estos principios ya existían, pero Robert C. Martin los agrupa en el acrónimo **SOLID**:

1. **Single Responsibility**: toda pieza de software debe tener una sola responsabilidad. Agrupar las cosas que cambian por el mismo motivo, y separar las cosas que cambian por distintos motivos.
2. **Open/Closed**: una clase debe estar abierta a la extensión pero cerrada a la modificación. Facilitar la [[Herencia]], composición, y [[Polimorfismo]].
3. **Liskov Substitution**: una subclase debe poder tomar el rol de su superclase. El cliente de una interfaz no debe confundirse por una implementación.
4. **Interface Segregation**: mantener pequeñas a las interfaces para que los usuarios no dependan de cosas que no usan.
5. **Dependency Inversion**: módulos de alto nivel no deberían depender de detalles de bajo nivel. Ambos deben depender de abstracciones.

SOLID se centra en **usar interfaces para facilitar el cambio** en el código.
