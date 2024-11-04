En la [[Administración de Memoria]] de un [[Sistema Operativo]], es relevante el tiempo efectivo de acceso a memoria, que varía según el tipo de asignación de espacio (contiguo o no) que se utilice.

Sea $\text{TEAM}$ el tiempo efectivo de acceso a memoria y $\text{TAM}$ el tiempo de acceso a memoria básico. **Sin paginación**, se tiene $\text{TEAM} = \text{TAM}$.

**Con [[Asignación por Paginación Simple]]**, debido a que se debe acceder primero a la tabla de páginas y luego a la página propiamente dicha, se tiene $\text{TEAM} = 2 \ \text{TAM}$.

**Con paginación con registro asociativo** (caché), siendo $\text{Hit}$ la probabilidad de que la página esté en el caché y $\text{TAMA}$ el tiempo de acceso a la memoria asociativa, finalmente se tiene $\text{TEAM} = \text{Hit} (\text{TAMA} + \text{TAM}) + \overline{\text{Hit}} (\text{TAMA} + 2 \ \text{TAM})$.

## TEAM con Memoria Virtual

Ahora también se utiliza [[Memoria Virtual]]. Sea $p$ la probabilidad de que suceda un fallo de página (intentar acceder a una página ausente). Sea $\text{TSFP}$ el tiempo de servicio de fallo de página, lo que se demora en cargar a memoria la página ausente.

Sin registro asociativo, se tiene $\text{TEAM} = \overline{p} \ \text{TAM} + p \ \text{TSFP}$.

Con registro asociativo, se tiene: $\text{TEAM} = H \ (\text{TAMA} + \text{TAM}) + \overline{H} \ (p \ (\text{TAMA} + 2 \ \text{TAM}) + \overline{p} \ (\text{TAMA} + \text{TAM} + \text{TSFP}))$.

Se puede usar un bit $M$ para cada página de la tabla de páginas, el cual se pone en $0$ cuando se carga la página y luego en $1$ cuando se escribe en esa página. Si el bit $M$ de una página es $0$, entonces la página puede ser descartada sin escribirse de vuelta en el disco, ya que la información no se modificó y por ende no se pierde nada. Esto da un tiempo de servicio de fallo de página reducido. Si se usa el bit $M$, se tiene:

$$TEAM = H (\text{TAMA} + \text{TAM}) + \overline{H} (p (\text{TAMA} + 2 \ \text{TAM}) + \overline{p} (\overline{M} (\text{TAMA}+\text{TAM}+\text{TSFPNM}) + M (\text{TAMA}+\text{TAM}+\text{TSFPM})))$$
