_Differentiated Services_ (DiffServ) es un [[Protocolo]] para la [[Calidad de Servicio]] en el cual el usuario marca sus paquetes con un determinado nivel de prioridad.

A diferencia de [[IntServ]], no necesita guardar el estado de cada flujo, por lo que tiene mejor escalabilidad. Se configura en cada [[Enrutadores|router]] por separado.

El comportamiento en cada salto afecta la política de encolamiento y/o descarte. Se definen dos:

- **EF**: garantía absoluta. Usa el token bucket.
- **AF1-AF4**: garantía estadística. Usa 3 niveles de descarte.

![[DiffServ.png]]

IntServ y DiffServ pueden coexistir. Se puede usar RSVP en el acceso, mapeando los 3 servicios IntServ a DiffServ.
