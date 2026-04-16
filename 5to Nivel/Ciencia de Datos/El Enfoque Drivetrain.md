El *drivetrain approach* surge de un artículo O'Reilly de Howard, Zwemer y Loukides. Consiste en un proceso de 4 pasos para construir un [[Producto de Datos]]:

1. **Objetivo definido**: ¿Que resultado estamos buscando?
2. **Palancas**: ¿Qué inputs podemos controlar?
3. **Datos**: ¿Qué datos podemos recolectar?
4. **Modelos**: cómo las palancas influyen el objetivo.

Podemos usar datos para producir resultados accionables.

*Model assembly line*:

![[El Enfoque Drivetrain.png]]

Ejemplo para un sistema de recomendaciones:

- **Objetivo**: lograr ventas adicionales sorprendiendo clientes con items que no hubieran comprado sin la recomendación.
- **Model Assembly Line**: 
	1. **Modeler**: probabilidad de una compra al ver vs no ver una recomendación.
	2. **Simulator**: probar la utilidad de todos los libros en stock.
	3. **Optimizer**: rankear libros recomendados según su utilidad.

Es importante definir un objetivo claro con palancas que produzcan resultados accionables. Simplemente construir modelos no es suficiente.
