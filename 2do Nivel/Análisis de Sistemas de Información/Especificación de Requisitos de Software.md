Luego de la [[Educción de Requisitos]], se escribe la **especificación de requisitos de software** (ERS) desde un punto de vista técnico para especificar los [[Requisitos de Software]] del [[Proyecto de Software]]. Se enfoca en el comportamiento externo del software y sirve de base para la validación que el cliente hará del software real. Se suele seguir la especificación del estándar IEEE 830.

LA ERS debe ser:

1. **Completa**: incluye todos los requisitos y todas las respuestas del software ante entradas válidas e inválidas. Incluye todo lo que se supone que el software debe hacer. El producto solo hace lo que dice la ERS.
2. **Correcta**: todo requerimiento formulado en ella es satisfecho por el software.
3. **Consistente**: no hay conflictos internos o con otros documentos, como por ejemplo el [[Documento de Requerimientos del Usuario]].
4. Modificables: debe ser ordenado y fácil de usar, sin redundancia. Expresar requisitos por separado.

Los documentos de requisitos deben ser:

- Comprensibles.
- No ambiguos.
- Verificables.
- Priorizados.
- Anotados con estabilidad.
- Independientes del diseño.
- Independientes de la implementación.

![[Especificación de Requisitos de Software.png]]

## Calidad

La **calidad del software** no puede reducirse a un solo número y el concepto de calidad es específico al proyecto. Se especifica de antemano. Luego, el desarrollo se debe encargar de cumplir con la calidad preestablecida.

Una ERS perfecta es imposible y su calidad es difícil de cuantificar.

### FURPS

El modelo _FURPS_ de Hewlett-Packard en 1987 propone 5 características de la calidad:

1. **Functionality**: requerimientos específicos del software, representan código a escribir.
2. **Usability**: facilidad de uso del software. Estética, documentación, interfaz consistente, etc.
3. **Reliability**: es la confiabilidad del software. Recuperabilidad, precisión, tolerancia a fallos, etc.
4. **Performance**: tiempo de respuesta, velocidad, consumo de recursos, etc.
5. **Supportability**: mantenibilidad, flexibilidad, compatibilidad, requisitos de instalación.

IBM luego inventa _FURPS+_, agregando **restricciones**:

- De diseño.
- De implementación.
- De interfaz.
- Físicas (de hardware).
