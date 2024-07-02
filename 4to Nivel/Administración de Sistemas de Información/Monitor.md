Los monitores son **herramientas** de la [[Monitorización]] para el **seguimiento** del comportamiento de los principales elementos de un SI cuando está sometido a una carga de trabajo dada. Son imprescindibles para **tomar mediciones** con las que realizar la [[Evaluación de las Prestaciones]] de un **sistema existente**, aunque puedan introducir ciertas **perturbaciones**.

## Clasificación

Según su mecanismo de **activación**:

- **Por eventos**: se activan por la aparición de algún acontecimiento que cambia algún estado.
- **Por muestreo**: se activan a intervalos de tiempo mediante interrupciones de reloj.

Según las muestras de los resultados:

- **En tiempo real**: procesa datos continuamente a medida que los recibe.
- **Batch**: primero recoge toda la información y luego la procesa.

Según la **implantación**:

- **Monitor software**: **programas** o ampliaciones del SO que acceden al estado del sistema. Causan cierta interferencia. Adecuados para aplicaciones, redes, bases de datos, SOs, etc.
- **Monitor hardware**: **dispositivos electrónicos** que se conectan a ciertos puntos del sistema mediante sondas electromagnéticas.
- **Monitor híbrido**: intenta combinar las ventajas de ambos. Se usan en prototipos para diseñar nuevas arquitecturas.

| Característica          | Monitor software | Monitor hardware    | Monitor híbrido |
| ----------------------- | ---------------- | ------------------- | --------------- |
| **Dominio de medición** | Alto nivel       | Bajo nivel (físico) | Todos           |
| **Resolución**          | Baja (variable)  | Alta (fija)         | Alta            |
| **Anchura**             | Infinita         | Finita              | Infinita        |
| **Interferencia**       | Alta             | Baja                | Media           |
| **Coste**               | Bajo             | Alto                | Alto            |
| **Reducción**           | Sí               | No                  | Sí/No           |
| **Portabilidad**        | No               | Sí                  | No              |

## Características

Estas características definen la **calidad** del monitor:

1. **Sobrecarga o interferencia**: introducen perturbaciones en el funcionamiento del SI.
2. **Precisión**: el error en los datos medidos.
3. **Resolución**: máxima frecuencia de medición.
4. **Ámbito o dominio de medida**: características y acontecimientos que puede observar.
5. **Anchura de entrada**.
6. Capacidad de **reducción de datos**: mejor comprensión y menor espacio de almacenamiento.
7. **Compatibilidad**.
8. **Coste**.
9. Facilidad de **instalación**.
10. Facilidad de **utilización**.
11. Monitorización **continua** durante la operación.
12. **Presentación** orientada a la aplicación.
13. **Integración**: al sistema existente.
14. **Retroalimentación**: para sistemas adaptativos.

## Estructura del Monitor

![[Monitor 2024-07-02 18.55.32.excalidraw.svg]]
