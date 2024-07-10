Es una disciplina que permite entregar software a producción en cualquier momento. El software se desarrolla de una manera que permita sacar una nueva versión a producción con sólo apretar un botón, sin romper nada. Esto requiere otra mentalidad en el equipo.

La entrega continua significa **tener siempre disponible una versión del software lista para ser entregada**. Así, el Product Manager puede en cualquier momento decir "vamos al mercado ya". Hay que evaluar si el **ROI** de hacer entrega continua vale la pena. El negocio quiere ir **rápido** pero también quiere ir **bien**: **testing y calidad** es fundamental. Tiene sentido en un mercado hiper-competitivo para realizar entregas constantes.

Incluye a la [[Integración Continua]] y se la expande con [[Estrategias de Deployment a Entornos Masivos]], feature flags, etc.

Conviene cuando:

1. El software es entregable durante todo el ciclo de vida.
2. El equipo prioriza el punto anterior.
3. Se quiere feedback automatizado y rápido.
4. Existe un _push-button deployment on demand_.

Seguimos llevando al máximo la iteratividad. Waterfall > Scrum > CI/CD.

## Antipatrones

1. Despliegue manual.
2. Entorno de desarrollo muy distinto al de producción.
3. Gestión manual de los entornos de entrega.
