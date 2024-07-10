Los **test doubles** son mecanismos que facilitan **simular dependencias** en la [[Automatización de Pruebas]] de **integración** entre componentes o APIs.

## Stub

Es un patrón que permite proporcionar **respuestas enlatadas** a llamadas hechas durante las pruebas. Suelen responder algo **básico**. Puede o no estar desarrollado en la misma tecnología de la solución (es flexible).

## Spy

Son stubs con la funcionalidad adicional de **registrar logs** y salidas para su análisis posterior.

## Mock

Similar al spy pero el código no se escribe como un caso de prueba, sino como un **objeto normal**. Es desarrollado en la **misma tecnología** de la solución, y permite probar con un **mayor nivel de lógica**. Puede **verificar outputs** en el test.

## Fakes

Son **implementaciones** que usan algún tipo de **atajo** que generalmente los hace inviables en un entorno de producción pero ideales para un entorno de pruebas. No es ni controlado ni observado por el test. Ejemplo: una base de datos en memoria.
