Sea la siguiente [[Diagrama Causal|relación causal]]:

$$
\begin{align}\text{Flujo de agua} &\overset{+}{\longrightarrow} \text{Nivel} \\
\text{(} \underline{\text{variación}} \text{ de X)} \ \frac{dX}{dt} &\longrightarrow X \ \text{(} \underline{\text{acumulación}} \text{ de X)}
\end{align}
$$

En la cual se considera a $\frac{dX}{dt}$ una _variable de flujo_ y a $X$ una _variable de nivel_.

En la [[Dinámica de Sistemas]], los **diagramas de Forrester** nos permiten diagramar relaciones de ese tipo para analizar la evolución de las variables de nivel del [[Modelo]] que concierne a nuestro estudio de [[Simulación]].

Las variables que brindan información del sistema pero no son de flujo o de nivel se denominan _variables auxiliares_.

Símbolos en un diagrama de Forrester:

![[Diagrama de Forrester (Símbolos).png]]

Ejemplo de diagrama de Forrester, para el caso de la dinámica poblacional de una población con una distribución uniforme:

![[Diagrama de Forrester (Dinámica Poblacional).png]]

Otro ejemplo, esta vez para un depósito con capacidad de 100 litros, contenido inicial de 50 litros, una sola entrada por donde ingresa 1/10 del volumen vacío, y una salida por donde sale 1/10 del volumen contenido.

![[Diagrama de Forrester (Depósito).png]]
