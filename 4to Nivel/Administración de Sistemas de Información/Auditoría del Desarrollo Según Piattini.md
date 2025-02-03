Para la [[Auditoría del Desarrollo]], Piattini y Del Peso proponen auditar todo: no solo el [[Ciclo de Vida]] sino también cómo lo estamos gestionando. El enfoque de Piattini divide la auditoría del desarrollo en dos apartados:

1. Auditoría de la organización y gestión del área de desarrollo.
2. Auditoría de proyectos de desarrollo de sistemas de información.

Se basa en la metodología ISACA: _Information Systems Audit and Control Association_, basada en la evaluación del [[4to Nivel/Administración de Sistemas de Información/Riesgo|Riesgo]]. Propone evaluar los riesgos a partir de riesgos potenciales a los que está sometida una actividad definiendo **objetivos de control** que **minimicen los riesgos**. Los objetivos de control son los objetivos a cumplir en el control de procesos.

```mermaid
flowchart LR;
1["Objetivo
de control"] --especifica--> 2["Técnicas
de control"] --validadas
por--> 3["Pruebas de
cumplimiento"]
```

Ejemplo:

```
Objetivo de control X: ...
C-X-1: Técnica de control 1 del objetivo de control X ...
	- Pruebas de cumplimiento de C-X-1 ...
```

Para obtener el entramado de [[Controles y Contra Medidas]]:

![[Auditoría del Desarrollo (Piattini) 2024-08-31 18.08.18.excalidraw.svg]]

## Auditoría de la Organización y Gestión del Área de Desarrollo

Todo desarrollo de un proyecto necesita apoyarse en el **personal** y en los **procedimientos** establecidos. Se consideran 8 objetivos de control, cada uno con varias técnicas de control, cada una con varias pruebas de cumplimiento que permiten su **comprobación**.

A1. El área de desarrollo tiene cometidos asignados y una organización para cumplirlos. \
A2. El personal del área de desarrollo cuenta con la formación y motivación adecuada. \
A3. Si existe un plan de sistemas, los proyectos se basarán en dicho plan. \
A4. La propuesta y aprobación de nuevos proyectos se hace de forma reglada. \
A5. La asignación de recursos a los proyectos se hace de forma reglada. \
A6. El desarrollo de SI aplica principios de ingeniería del software aceptados ampliamente. \
A7. Las relaciones con el exterior del departamento son de acuerdo a un procedimiento. \
A8. La organización del área está siempre adaptada a las necesidades de cada momento.

## Auditoría de Proyectos de Desarrollo de Sistemas de Información

Se enfoca en el ciclo de vida de la metodología.

**Auditoría de la aprobación, planificación, y gestión del proyecto**:

B1. El proyecto de desarrollo debe estar aprobado, definido y planificado formalmente. \
B2. El proyecto se debe gestionar para conseguir los mejores resultados según las restricciones.

**Auditoría de la fase de análisis**: el análisis de requisitos del sistema y la especificación funcional.

C1. Los usuarios y responsables afectados establecerán los requisitos de forma clara. \
C2. Se utilizará la alternativa más favorable para que el sistema cumpla los requisitos. \
D1. El nuevo sistema debe especificarse de forma completa y funcional, y aprobada por usuarios.

**Auditoría de la fase de diseño**: el diseño técnico del sistema.

E1. Definir una arquitectura física coherente con la especificación funcional y el entorno tecnológico.

**Auditoría de la fase de construcción**: se divide en las subfases de desarrollo de los componentes del sistema y desarrollo de los procedimientos de usuario.

F1. Los componentes se desarrollan con técnicas de programación correctas. \
G1. Al término del proyecto los futuros usuarios deben poder hacer uso del sistema.

**Auditoría de la fase de implantación**: realiza las pruebas, implantación y aceptación del sistema.

H1. El sistema debe ser aceptado formalmente por los usuarios antes de ser explotado. \
H2. El sistema se pondrá en explotación solo cuando el entorno de ejecución esté preparado.
