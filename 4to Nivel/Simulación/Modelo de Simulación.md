En el contexto de una [[Simulación]], los **modelos** nos permiten representar la realidad de una manera controlada y configurable. Si realizamos simulaciones sobre los modelos, entonces los modelos pasan a ser el [[Sistema]] bajo estudio.

Mientras más representativo es un modelo de la realidad, más confiables son sus resultados, pero también se vuelve más costoso crearlo y simularlo.

Para modelar un sistema debemos primero poder tomar una muestra representativa de su comportamiento, con tal de no crear un modelo incorrecto.

Existen:

- **Modelos de predicción**: buscan un resultado lo más preciso posible.
- **Modelos de gestión**: facilitan decidir la alternativa más conveniente. Se utilizan para la toma de decisiones de variables de control. No se necesita un resultado demasiado preciso, solamente uno que permita tomar decisiones efectivas.

## Proceso de Modelado

![[Modelo 2025-01-28 20.28.46.excalidraw.svg]]

## Elementos del Sistema

Hay varios elementos de un sistema que son relevantes para construir su modelo de Simulación:

1. **Entidades**: flujos de entrada al sistema. Alteran al sistema.
2. **Estado**: una foto del sistema en cierto instante, con sus variables puntuales y acumuladas.
3. **Eventos**: cambios en el estado actual. Pueden ser _actuales_ o _futuros_.
4. **Localizaciones**: lugares en los que la entidad espera a ser atendida.
5. **Recursos**: dispositivos necesarios para realizar una operación.
6. **Atributos**: características de una entidad.
7. **Variables**: condiciones cuyos valores surgen de ecuaciones. Son _discretas_ o _continuas_. Son _exógenas_ (del entorno) si son _datos_ o de _control_. Son _endógenas_ (de la simulación) si son de _estado_ o de _resultado_. Si no son ni exógenas ni endógenas, son _auxiliares_.
8. **Reloj**: es el contador de tiempo de la simulación. Puede ser _absoluto_ (se cuenta desde el inicio de la simulación) o _relativo_ (se cuenta el lapso de tiempo desde el último evento).
