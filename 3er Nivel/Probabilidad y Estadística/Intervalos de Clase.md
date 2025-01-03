El _intervalo de clase_ es un intervalo de variación de los datos entre dos valores dados. Cada intervalo tiene asociados los siguientes atributos:

1. **Número de intervalos de clase**: según la fórmula de Sturges ($NI = 1 + 3.3 \cdot \log n$) o la fórmula de Rice ($NI = 2 \sqrt[3]{n}$).
2. **Límite inferior del intervalo de clase**: es el menor valor del intervalo ($LI$).
3. **Límite superior del intervalo de clase**: es el mayor valor del intervalo ($LS$).
4. **Verdadero límite del intervalo de clase**: $VL_i = LI_i$ si la variable es continua. Si la variable es discreta, entonces $VL_i = \frac{LS_{i-1}+LI_i}{2}$.
5. **Amplitud del intervalo de clase**: $C_i = | VL_i - VL_{i+1}|$. Si la distribución es _equispaciada_, entonces $c = \frac{R}{NI}$.
6. **Frecuencia absoluta**: representa la cantidad de observaciones de cada clase ($f_i$).
7. **Punto medio del intervalo de clase**: $x_i = \frac{VL_i + VL_{i+1}}{2}$.
8. **Frecuencia acumulada creciente**: acumula las frecuencias absolutas anteriores. $F_i = \sum_{k=1}^i f_k$.
9. **Freciencia relativa**: $h_i = \frac{f_i}{n}$. Se suele expresar como porcentaje.
10. **Frecuencia relativa acumulada**: acumula las frecuencias relativas anteriores. $H_i = \sum_{k=1}^i \frac{h_k}{n}$.

![[Intervalos de Clase.png]]

Un _histograma_ es un gráfico de la distribución de frecuencias. Cada intervalo de clase es una barra del gráfico. Otro gráfico alternativo es un _polígono de frecuencias_, que une los puntos medios del lado superior de cada barra del histograma.

![[Histograma.png]]

La _ojiva_ (creciente o decreciente) sirve para graficar frecuencias acumuladas.:

![[Ojiva.png]]
