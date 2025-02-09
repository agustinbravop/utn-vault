*Routing Internet Protocol* (RIP) es un [[Protocolo]] para el [[Ruteo IP]] que implementa el mecanismo de [[Enrutadores#Ruteo Dinámico por Vector Distancia|vector distancia]], lo cual lo hace útil solo para redes pequeñas.

Cada [[Enrutadores|router]] envía la tabla completa a todos sus vecinos. Los vecinos calculan las métricas e instalan las rutas estrictamente menores. Esto usa el puerto [[UDP]] 520.

El problema inherente a Vector-Distancia (VD) es la **convergencia lenta**. Hay varias soluciones propuestas que lo mitigan:

1. Max saltos = 15. Se limitan saltos para evitar bucles infinitos.
2. Hold down.
3. Triggered updates.
4. Route poisoning: establece los saltos a 16 si envía a la interfaz por la que recibió esa información, para evitar saltos innecesarios.
5. Split horizon.
6. Split horizon with poison reverse (no funciona en todas las topologías).

Luego surge RIPv2 (RFC 2453) que agrega soporte a classless ([[Subnetting]]), soporte de autenticación, soporte para etiquetado, y multicast. Lamentablemente, sigue con el problema de convergencia lenta, inherente a VD.
