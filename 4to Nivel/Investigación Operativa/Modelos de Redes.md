Muchas situaciones, interesantes para la [[Investigación Operativa]], se pueden modelar y resolver como **redes**. Los algoritmos basados en redes muchas veces pueden ser más eficientes que el método Simplex de la [[Programación Lineal]].

Una _red_ es una serie de _nodos_ enlazados con _arcos_.

Cada red tiene asociado un _flujo_ limitado a la _capacidad_ (finita o infinita) de cada uno de sus arcos. Un arco es _dirigido_ u orientado si permite flujo positivo en una dirección y flujo cero en la dirección opuesta. Una _red dirigida_ tiene todos sus arcos dirigidos.

Una _ruta_ es una sucesión de arcos distintos que unen dos nodos. Un _ciclo_ es una ruta que conecta un nodo consigo mismo, pasando por algún arco. Una red es _conectada_ si todo par de nodos está enlazado por al menos una ruta.

Un [[Árbol]] es una red conectada sin ciclos de solo un subconjunto de todos los nodos de la red. Un _árbol de expansión_ es un árbol que enlaza todos los nodos de la red.

Hay dos algoritmos interesantes para los modelos de redes:

- Algoritmo para calcular el árbol de expansión mínima.
- Algoritmo para calcular el flujo máximo.

Los [[Métodos CPM y PERT]] están inspirados en los modelos de redes.

## Algoritmo para el Árbol de Expansión Mínima

Sean $N$ el conjunto de nodos, $C_k$ los nodos conectados en la iteración $k$, y $C_k'$ los restantes.

1. Inicializar con $C_0 = \phi$ y $C'_0 = N$.
2. Comenzar la primera iteración con cualquier nodo y hacer $C_1=\set{i}, \ C'_1 = N - \set{i}$.
3. Iterativamente, en cada paso $k$, seleccionar un nodo $j \in C'_{k-1}$ que produzca el arco más corto a un nodo del conjunto conectado $C_{k-1}$. Hacer $C_k = C_{k-1} + \set{j}, \ C_k'=C_{k-1}' -\set{j}$. Luego, $k=k+1$ y repetir.
4. Detenerse cuando $C_k = \phi$. Los arcos utilizados son la **ruta más corta que conecta toda la red**.

## Algoritmo para el Flujo Máximo

Este algoritmo se utiliza para determinar _rutas de irrupción_ con flujo neto positivo.

1. Inicio: para todos los arcos $(i,j)$ se iguala la capacidad residual con la inicial: $(c_{ij}, c_{ji}) = (\overline c_{ij}, \overline c_{ji})$. Se etiqueta el nodo fuente $1$ con $[\infty, -]$. Se iguala $i=1$.
2. Determinar $S_i$: el conjunto de nodos $j$ no etiquetados directamente alcanzables desde el nodo $i$, con residuales positivos ($c_{ij} \gt 0 \ \forall \ j \in S$). Si $S \ne \phi$, ir al paso 3. Si $S = \phi$, ir al paso 4.
3. Determinar $k \in S_i / c_{ik} = \max \set{c_{ij}} \ \forall \ j \in S$. Igualar $a_k = c_{ij}$ y etiquetar el nodo $k$ con $[a_k, i]$. Si $k=n$, se encontró una ruta de irrupción, y hay que ir al paso 5. Sino, hacer $i=k$ e ir al paso 2.
4. Retroceso: si $i=1$, entonces no hay otras irrupciones posibles, entonces hay que ir al paso 6. Sino, sea $r$ el nodo etiquetado inmediatamente antes del actual. Quitar $i$ del conjunto de nodos adyacentes a $r$. Igualar $i=r$. Ir al paso 2.
5. Red residual: sean $(1,k_1,\dots,n)$ los nodos de la $p$-ésima ruta de irrupción. Se calcula el **flujo máximo** por la ruta: $f_p=\min \set{a_1,a_{k_1}, \dots, a_n}$. La capacidad residual de cada arco a lo largo de la ruta se disminuye o se aumenta en $f_p$ unidades. $\forall \ (i,j)$ en la ruta: $(c_{ij}, c_{ji})=(c_{ij}-f_p, c_{ji}+f_p)$ si el flujo va de $i$ a $j$. Se reinstalan todos los nodos eliminados en el paso 4. Poner $i=1$ y volver al paso 2, a buscar nuevas rutas potencialmente mejores.
6. Solución: para $m$ rutas de irrupción, el flujo máximo en la red es $F=f_1+\dots+f_m$.
