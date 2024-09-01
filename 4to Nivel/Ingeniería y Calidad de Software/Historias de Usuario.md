Representan una **funcionalidad mínima que aporta valor** para el negocio. Lo ideal es que tarde entre 2 y 3 días de desarrollo para ser completada. Si es muy grande la llamamos **Épica** y la desglosamos en varias historias de usuario.

Son un **recordatorio** de qué hay que hacer para que el equipo determine cómo hacerlo. El objetivo de usarlas es el **entendimiento compartido**. Se ordenan en el [[Product Backlog]].

## Las 3 C

Las HU tienen tres partes:

- **Card:** la tarjeta es el medio físico. Incluye la descripción de la funcionalidad.
- **Conversación:** incentiva la discusión para generar un **entendimiento compartido** del requerimiento. Se busca lograr la colaboración con el cliente por sobre la documentación.
- **Confirmación:** son los **criterios de aceptación**. Incluye pruebas para la validación de su completitud. El testing pasa de ser una etapa del desarrollo a una actividad.

## Formato

Las HU se escriben desde el punto de vista del usuario que necesita la funcionalidad. Dicen el qué, NO el cómo.

```
[Título]
Como [rol]
quiero hacer [funcionalidad]
con el objetivo de [beneficio]
```

Aclarar el **rol** ayuda a identificar y diferenciar los **permisos** de los distintos **roles** del sistema. En la industria y algunos autores omiten el título y el beneficio.

## Criterios de Aceptación

Se pueden escribir en _lenguaje Gherkin_:

```
Scenario
	Given [context]
	When [event]
	Then [result]
```

Además pueden incluir **restricciones** **no funcionales** asociadas al requisito de la HU.

## Alcance

**Tema > Épicas > Historias de Usuario > Tareas**.
![[Desagregación de las Historias de Usuario.png]]
Los temas son aspectos enormes del sistema e inicialmente no es claro que HUs contienen.
Las tareas son el "cómo hacerlo" y las escribe el equipo de desarrollo con certidumbre.

## Redacción de Historias de Usuario

Es importante escribir buenas historias de usuario.

### Método INVEST

Comprueba (NO asegura) la calidad. La HU debe reunir estas características:

- **Independent:** se busca minimizar las dependencias. Difícil de lograr en la realidad.
- **Negotiable:** debe ser discutible con el cliente.
- **Valuable:** aportar valor.
- **Estimable:** poder planear.
- **Small:** pequeña.
- **Testeable:** se tiene que poder probar.

### Tips de Mike Cohn

1. **Empezar por historias objetivo:** ¿qué necesita hacer el usuario?
2. **Cortar la torta:** dividir historias verticalmente en funcionalidades mínimas end-to-end.
3. **Escribir historias cerradas:** el usuario logra un objetivo al terminarlas.
4. **Poner restricciones en las tarjetas:** requisitos no funcionales.
5. **Tamaño en base al horizonte:** detallar las más cercanas.
6. **Mantener la UI lo más lejos posible:** funcionalidad > interfaz.
7. **Algunas cosas no son HU:** por ejemplo la paleta de colores.
8. **Incluir el rol del usuario:** aclara permisos.
9. **Escribir para un rol individual:** pensar en un usuario específico.
10. **Escribir en voz activa:** mayor claridad.
11. **El cliente escribe:** lo obliga a pensar qué quiere.
12. **No numerar las tarjetas:** hablar de features, no números.
13. **No olvidar el propósito:** son un **recordatorio** de discutir la funcionalidad.

### Bad Smells de Mike Cohn

**Indicadores** de una mala historia de usuario:

1. Historias demasiado pequeñas: dificulta la estimación.
2. Historias interdependientes: dificulta la planificación.
3. **Goldplating**: generarle necesidades al cliente que no tiene.
4. Demasiados detalles.
5. Detalles de interfaz muy tempranos.
6. Pensando demasiado adelante.
7. Separando demasiadas historias.
8. Al cliente se le dificulta la priorización.
9. El cliente no quiere escribir o priorizar las historias.
