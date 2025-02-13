Las primeras redes se diseñaron con foco en el hardware, por lo que eran poco flexibles. Para reducir la complejidad del diseño, se organizan las redes en **pilas de capas**.

Las capas inferiores _ofrecen servicios_ a capas superiores.

$$\begin{rcases}\text{Avances académicos muy rápidos} \\ \text{Empresas compitiendo por mercado} \\ \text{Gobiernos defendiendo sus intereses} \end{rcases} \ \text{Caos} \longrightarrow \text{Necesidad de estandarización}$$

Una _entidad_ es un elemento activo de una capa que implementa un servicio (puede ser SW o HW).

Un _Service Access Point_ (SAP) es un punto de acceso al servicio, lugar donde el usuario (la capa $n+1$) accede al servicio de la capa $n$.

La _Interface Data Unit_ (IDU) se subdivide en la _Service Data Unit_ (SDU) y la _Interface Control Information_ (ICI). El _Protocol Data Unit_ (PDU) es el bloque que la capa $n$ usa para pasar la información a las capas más bajas.

![[Redes de Datos.png]]

Un _servicio_ se especifica mediante las operaciones (_primitivas_) que ofrece. Hay primitivas de:

1. **Request**: una entidad requiere una tarea del servicio.
2. **Indication**: una entidad es informada de un evento.
3. **Response**: una entidad desea responder a un evento.
4. **Confirm**: la respuesta a una petición anterior ha llegado.

Los servicios se clasifican en:

- **Orientados a conexión**: se establece una conexión, se usa, y se libera. Ej: telefonía.
- **Sin conexión**: modo sin conexión (suele ser más robusto). Ej: correos.

Un [[Protocolo]] define reglas que gobiernan el **formato y significado** de los mensajes intercambiados por pares de entidades dentro de una capa.
