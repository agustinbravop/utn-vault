Dentro de las arquitecturas concretas de [[Agentes]], el **modelo BDI** se basa en el proceso de decisión deliberativo, es decir momento por momento. Tiene tres componentes:

- **Creencias**: el [[5to Nivel/Inteligencia Artificial/Conocimiento|Conocimiento]] del agente sobre su entorno.
- **Deseos**: hechos que el agente quiere que se cumplan. Están priorizados.
- **Intenciones**: deseos que el agente filtró y se comprometió a alcanzar. Deben ser consistentes entre sí.

El algoritmo es el siguiente (donde $brf$ significa "belief revision function"):

$$
\begin{aligned}
&\textbf{function } action(p : P) : A \\[6pt]
&\textbf{begin} \\[6pt]
&\qquad B := brf(B,p) \qquad\qquad  \text{// belief revision function actualiza creencias según la percepción} \\[6pt]
&\qquad D := options(D,I)\qquad \text{// generar nuevo conjunto de deseos} \\[6pt]
&\qquad I := filter(B,D,I)\qquad \text{// seleccionar deseos realistas y consistentes} \\[6pt]
&\qquad \textbf{return } execute(I) \\[6pt]
&\textbf{end function } action
\end{aligned}
$$

![[Agentes BDI.png]]
