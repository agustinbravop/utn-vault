Para comunicarse con todos los dominios de colisión, los [[Protocolo|protocolos]] usan tramas *broadcast* (de difusión) y *multicast* a nivel de [[Capa de Enlace]]. Estas difusiones hacen una ocupación costosa de la capacidad del canal.

Para la conmutación en redes LAN, se utilizan dispositivos como [[Puentes de Red]] y [[Switches]].

Formas de conmutación de tramas para conmutadores LAN:

1. **Cut-through**: retransmite la trama tan pronto lee la dirección de destino (primeros 6 bytes).
2. **Almacenamiento y reenvío**: recibe la trama completa y solo la repite si el CRC es correcto.
3. **Cut-through libre de fragmentos**: espera a los primeros 64 bytes para asegurarse que no es un fragmento de colisión.

## LAN Virtuales

Una **LAN virtual** es una agrupación lógica (lograda mediante el *etiquetado* de tramas) de estaciones por grupo de trabajo, independiente de su ubicación física. 

Se extiende la función de filtrado del puente de red para no modificar el cableado. Se puede distinguir entre el tráfico de usuario y el tráfico backbone. Para cambiar de VLAN, se debe procesar en la [[Capa de Red]] (en un *router*).

Las VLANs mejoran la *escalabilidad* de la red, mientras que siguen siendo *transparentes* al usuario.
