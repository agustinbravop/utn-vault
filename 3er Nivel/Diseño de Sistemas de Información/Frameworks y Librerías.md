Los **frameworks y librerías** son paquetes de código que aceleran el desarrollo de software. Existen algunos que son específicos para los [[Métodos Orientados a Objetos]].

Un *framework* es un conjunto de clases cooperantes que constituyen una solución de diseño genérico que se puede adaptar a varios problemas específicos dentro de un dominio dado. Es una estructura predeterminada que ayuda a los desarrolladores a mantener sus soluciones.

Una *librería* o biblioteca es un conjunto de clases instanciadas por el cliente, quien llama a sus funciones a medida que las necesita. Suelen resolver un problema mucho más específico que un framework.

Mientras que las librerías son llamadas por el código del cliente, un framework **invierte el flujo de control**: el framework llama a las funciones del cliente, y ofrece cierto comportamiento por defecto.

Existen multitudes de frameworks. Por ejemplo: .NET Core.

## .NET Core

.NET Core es un sucesor open-source y multiplataforma del framework .NET, un framework de C#, F#, o Visual Basic, creado por Microsoft para Windows.

Sus componentes son:

1. **Common Language Runtime**: un entorno de ejecución para los programas .NET, similar a la JVM de Java.
2. **Class library**: módulos compartidos entre múltiples aplicaciones. Hay librerías de clase portables, específicas a la plataforma, o estándares de .NET.

Algunas de las muchas herramientas de .NET:

- NuGet: gestor de paquetes.
- RazorPages: HTML + C# templating para crear páginas web.
- Blazor: alternativa a React para crear clientes web.
- NUnit: framework de pruebas unitarias.
- WPF: framework de UI para aplicaciones de escritorio Windows.
- Visual Studio: IDE con soporte específico para .NET.

### ASP.NET Core

ASP.NET Core es un framework que utiliza el patrón MVC (Modelo-Vista-Controlador) para el desarrollo web. 

Su flujo de trabajo es el siguiente