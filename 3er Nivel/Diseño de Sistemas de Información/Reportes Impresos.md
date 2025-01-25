Los reportes impresos son [[Diseño de Entradas y Salidas|salidas]] con información constante (logos) y variable (datos). Sus *atributos* pueden ser:

- **Funcionales**: sirven un propósito para el usuario.
- **Estéticos**: dan formato a la salida.

Pasos para preparar un formato impreso:

1. Determinar necesidades.
2. Identificar usuarios.
3. Determinar información.
4. Decidir dimensión y espacios.
5. Titular y numerar páginas.
6. Incluir fecha de generación o impresión.
7. Rotular las columnas de datos.
8. Definir las líneas de detalle.
9. Indicar la posición de los totales y cortes.
10. Revisar el prototipo con los usuarios.

## Diagramas de Warnier

Los **diagramas de Warnier** nos permiten *jerarquizar* la información variable de reportes impresos. Las hojas del árbol son la información, y el resto de nodos son tablas, estructuras, listas, etc. La información constante, como logos o formatos, no van en las hojas del árbol.

$$\text{Resumen} \begin{cases} 
\begin{matrix}\text{Cabecera} \\ \text{(1 vez)}\end{matrix} \begin{cases} \begin{matrix}\text{Titulo} \\ \text{(1 vez)}\end{matrix} \begin{cases}\text{Mes} \\ \text{Año} \end{cases}\end{cases} \\ \\
\begin{matrix}\text{Cuerpo} \\ \text{(1 vez)}\end{matrix} \begin{cases} \begin{matrix}\text{Página} \\ \text{(n veces)}\end{matrix} \begin{cases}\begin{matrix}\text{Cuerpo} \\ \text{(1 vez)}\end{matrix} \begin{cases}\begin{matrix}\text{Filas} \\ \text{(m veces)}\end{matrix}\end{cases} \begin{cases}\begin{matrix}\text{Fecha}\\ \text{Precio unitario} \\ \text{Cantidad}\end{matrix}\end{cases} \\\\ \begin{matrix}\text{Pie} \\ \text{(1 vez)}\end{matrix} \begin{cases}\begin{matrix}\text{Página actual} \\ \text{Total de páginas}\end{matrix}\end{cases} \end{cases}\end{cases} \\ \\
\begin{matrix} \text{Pie} \\ \text{(1 vez)}\end{matrix} \begin{cases}\text{Total}\end{cases} \\
\end{cases}$$

Se indica en la estructura cuántas veces se repite cada nodo. Las hojas siempre son datos variables, y solo se indican una vez.

Este tipo de diagramas no es capaz de representar la estructura de absolutamente todos los tipos de reportes que existen, pero es un diagrama fácil de realizar y puede abarcar una gran variedad de diseños que no sean muy complejos.
