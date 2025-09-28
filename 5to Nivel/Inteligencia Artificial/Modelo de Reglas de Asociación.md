Las **reglas de asociación** introducen incertidumbre (probabilidades) a las reglas de los [[Sistemas Basados en Reglas]].

Las **asociaciones** son relaciones de co-ocurrencia entre elementos:

$$\underset{(X)}{\text{Queso}} \longrightarrow \underset{(Y)}{\text{Cerveza}} \ \  \ [\text{Soporte} \ 10\%, \text{Confianza} \ 80\%]$$

Donde:

- El **soporte** representa el porcentaje de transacciones en $T$ que contienen $X\cup Y$. Mide la _frecuencia_ de la regla.
- La **confianza** representa el porcentaje de transacciones en $T$ que contienen $X$ e $Y$. Mide la _predictibilidad_ de la regla.

El **conteo de soporte** de $X$ es $X.count$.

$$
\text{Soporte} = \frac{X \cup Y) .count}{n} \ \ \ \ \ \ \ \ \text{Confianza} = \frac{(X\cup Y).count}{X.count} = Pr(Y | X)
$$

El objetivo es, dado un conjunto de transacciones $T$, encontrar todas las reglas de asociación en en $T$ cuyos valores de soporte y confianza sean iguales o mayores a los establecidos por el usuario.

El problema está en encontrar todas las reglas. Existen varios algoritmos para esto, y todos dan el mismo conjunto de reglas.

## Algoritmo A Priori

Este algoritmo trabaja en dos pasos:

1. Crear el conjunto de items frecuentes, es decir filtrados por soporte mínimo.
2. Generar todas las reglas de asociación confiables, es decir filtradas por la confianza mínima.

Se asume que los items en $I$ están **ordenados lexicográficamente**. La **propiedad de cierre hacia abajo** (_downward closure_) dice que, si un itemset contiene soporte mínimo, entonces todos sus subconjuntos no vacíos también lo contienen. Esto _poda_ un gran número de itemsets y hace eficiente al algoritmo.

El algoritmo puede funcionar con mucha cantidad de datos ya que solamente tiene en cuenta $k$ items en cada pasada (lo que se conoce como _level-wise search_).

$$
\begin{aligned}
&\textbf{Algorithm Apriori}(T) \\[6pt]
&C_1 \gets \text{init-pass}(T); \quad\quad\quad\;\; \\[6pt]
&F_1 \gets \{ f \mid f \in C_1, \; f.count/n \geq minsup \}; \quad  \\[6pt]
&\textbf{for } (k = 2; \; F_{k-1} \neq \varnothing; \; k{+}{+}) \;\textbf{do} \\[6pt]
&\qquad C_k \gets \text{candidate-gen}(F_{k-1}); \\[6pt]
&\qquad \textbf{for each transaction} \; t \in T \;\textbf{do} \quad \\[6pt]
&\qquad\qquad \textbf{for each candidate} \; c \in C_k \;\textbf{do} \\[6pt]
&\qquad\qquad\qquad \textbf{if } c \;\text{is contained in } t \;\textbf{then} \\[6pt]
&\qquad\qquad\qquad\qquad c.count{+}{+}; \qquad\qquad\qquad \text{// conteo de soporte} \\[6pt]
&\qquad\qquad \textbf{endfor} \\[6pt]
&\qquad \textbf{endfor} \\[6pt]
&\qquad F_k \gets \{ c \in C_k \mid c.count/n \geq minsup \} \ \ \ \ \text{// filtrar por soporte mínimo} \\[6pt]
&\textbf{endfor} \\[6pt]
&\textbf{return } F \gets \textstyle\bigcup_k F_k
\end{aligned}
$$

$$
\begin{aligned}
&\textbf{Function } \text{candidate-gen}(F_{k-1}) \\[6pt]
&C_k \gets \varnothing \\[6pt]
&\textbf{forall } f_1, f_2 \in F_{k-1} \;\textbf{do} \qquad\qquad\qquad \ \ \text{// pares de itemsets frecuentes} \\[6pt]
&\qquad \text{with } f_1 = \{ i_1, \dots, i_{k-2}, i_{k-1} \} \qquad \text{// que solo difieren en el último item} \\[4pt]
&\qquad \text{and } f_2 = \{ i_1, \dots, i_{k-2}, i'_{k-1} \} \\[4pt]
&\qquad \text{and } i_{k-1} < i'_{k-1} \;\textbf{do} \qquad\qquad\qquad \text{// en orden lexicográfico} \\[6pt]
&\qquad\qquad c \gets \{ i_1, \dots, i_{k-1}, i'_{k-1} \}; \quad \ \ \ \text{// unir los dos itemsets} \\[6pt]
&\qquad\qquad C_k \gets C_k \cup \{c\}; \qquad\qquad \quad  \text{// agregar el nuevo candidato} \\[6pt]
&\qquad\qquad \textbf{for each } (k-1)\text{-subset } s \text{ of } c \;\textbf{do} \\[6pt]
&\qquad\qquad\qquad \textbf{if } (s \notin F_{k-1}) \;\textbf{then} \\[6pt]
&\qquad\qquad\qquad\qquad \text{delete } c \text{ from } C_k; \quad \text{// filtrar por cierre hacia abajo}  \\[6pt]
&\qquad\qquad \textbf{endfor} \\[6pt]
&\textbf{endfor} \\[6pt]
&\textbf{return } C_k
\end{aligned}
$$

Una vez generado el conjunto $F$ de todos los itemsets frecuentes filtrados por soporte mínimo, se generan todas las reglas de asociación confiables (filtradas por la confianza mínima).

$$
\begin{aligned}
&\textbf{Algorithm } \text{genRules}(F) \\[6pt]
&\textbf{for each frequent } k\text{-itemset } f_k \in F, \; k \geq 2 \;\textbf{do} \\[6pt]
&\qquad \text{output every 1-item consequent rule of } f_k \\[0pt]
&\qquad\qquad \text{with confidence } \geq minconf  \qquad\qquad \text{// filtrar por confianza mínima} \\[0pt]
&\qquad\qquad \text{and support } \gets f_k.count / n \\[6pt]
&\qquad H_1 \gets \{ \text{consequents of all 1-item consequent rules derived from } f_k \text{ above} \}; \\[6pt]
&\qquad \text{ap-genRules}(f_k, H_1); \\[6pt]
&\textbf{endfor}
\end{aligned}
$$

$$
\begin{aligned}
&\textbf{Procedure } \text{ap-genRules}(f_k, H_m) \quad // H_m \text{ es el conjunto de consecuentes de } m\text{-items} \\[6pt]
&\textbf{if } (k > m+1) \;\wedge\; (H_m \neq \varnothing) \;\textbf{then} \\[6pt]
&\qquad H_{m+1} \gets \text{candidate-gen}(H_m); \\[6pt]
&\qquad \textbf{for each } h_{m+1} \in H_{m+1} \;\textbf{do} \\[6pt]
&\qquad\qquad conf \gets f_k.count / (f_k - h_{m+1}).count; \\[6pt]
&\qquad\qquad \textbf{if } (conf \geq minconf) \;\textbf{then} \qquad \text{// filtrar por confianza mínima} \\[6pt]
&\qquad\qquad\qquad \text{output the rule } (f_k - h_{m+1}) \to h_{m+1} \\
&\qquad\qquad\qquad\qquad \text{with confidence } = conf \\
&\qquad\qquad\qquad\qquad \text{and support } = f_k.count / n \\[6pt]
&\qquad\qquad \textbf{else} \\[6pt]
&\qquad\qquad\qquad \text{delete } h_{m+1} \text{ from } H_{m+1}; \\[6pt]
&\qquad\qquad \textbf{endif} \\[6pt]
&\qquad \textbf{endfor} \\[6pt]
&\qquad ap\text{-}genRules(f_k, H_{m+1}); \\[6pt]
&\textbf{endif}
\end{aligned}
$$
