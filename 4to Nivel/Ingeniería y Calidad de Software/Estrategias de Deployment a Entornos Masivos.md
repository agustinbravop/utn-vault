Organizan el pase a producción de cierta nueva versión del software. Nos permiten hacer **rollback** si algo sale mal, pero son caros por que requieren que dos versiones coexistan (solo por un tiempo). Hay que analizar el **Return Of Investment** para decidir si usar o no una de estas estrategias.

## Blue/Green Deployment

1. El router o API Gateway dirige inicialmente a todos los usuarios a la versión blue mientras se despliega la nueva versión green del software.
2. El router redirige todo el tráfico a la versión green.
   Nos permite desplegar nuevas versiones sin downtime, pero requiere temporalmente tener dos despliegues paralelos (un mayor costo) y configurar un router para realizar el switch.

## Canary Release

_Los canarios en minas detectaban la presencia de monóxido de carbono._

Los usuarios se van actualizado gradualmente a la nueva versión. Si no se detectan errores entonces se pasa el 100% de usuarios. Este método es todavía más complejo pero permite usar un pequeño grupo de usuarios para detectar problemas antes de pasar al resto.
