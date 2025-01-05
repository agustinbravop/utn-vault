En el [[Desarrollo de Software]], **probamos** el software para:

- Comprobar el funcionamiento y comportamiento.
- Validar pre-condiciones y post-condiciones.

Hay varios tipos de _dummies_, objetos especiales que se utilizan durante el testing:

- **Método Stub**: un fragmento de código que sustituye alguna funcionalidad pequeña. Se utiliza para verificar el estado.
- **Objeto Mock**: simula un objeto entero de forma controlada. Se utiliza para verificar el comportamiento.
- **Spy**: estos objetos hacen un mock _parcial_ de un objeto, es decir, usan el comportamiento por defecto para las partes no explícitamente mockeadas.

Mientras que los dummies simulan objetos, un _fake_ tiene una implementación funcional cómoda para el testing pero no apta para producción. Por ejemplo, ejecutar una base de datos en memoria.

Para crear casos de prueba, se puede utilizar el patrón **Arrange-Act-Assert**:

1. Establecer pre-condiciones.
2. Realizar acción.
3. Validar post-condiciones.

Existen muchas métricas útiles para el testing. Una muy importante es el _coverage_, que especifica el porcentaje del código testeado total, aunque no asegura el comportamiento correcto del software. Se subdivide en:

- Statement coverage.
- Branch coverage.
- Complexity coverage.
