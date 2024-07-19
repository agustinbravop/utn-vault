Formas de tratar a los [[Archivo|archivos]].

## Individuales

Un solo fichero de entrada. Puede o no haber un fichero de salida.

1. **Genérico**: es el proceso de **carga** o generación, tiene como objetivo crear un archivo **consistente** y, de ser posible, **congruente grueso**.
2. **Emisión**: tiene como objetivo la salida impresa de datos.
	- **Listador en bruto**: imprime tal cual lo que está en el fichero.
	- **Padrón**: los datos están ordenados. Puede haber encabezados y totales.
3. Estadísticos: hacen un recorrido del archivo para contabilizar elementos, emitiendo un cuadro estadístico de resumen, ahorrando papel pero usando memoria mucha interna.
4. **Corte de control**: dan padrones con totales parciales. Requieren entradas ordenadas por un [[Campo Clave]] de **clave compleja**.

## Múltiples

Dos o más ficheros de entrada y uno o más ficheros de salida.

### Mezcla

Por lo menos dos ficheros de entrada y uno de salida que es el resultado de la **combinación** de las entradas.

- **Homogénea**: entradas con igual formato.
- **Heterogénea**: entradas con distintos formatos.

Los ciclos de apareo pueden ser:

- **Incluyentes**: `MIENTRAS clave_1 <> HV O clave_2 <> HV HACER...`
- **Excluyentes**: `MIENTRAS NFDA(archivo_1) Y NFDA(archivo_2) HACER...`

### Actualización Secuencial

No se cambia el archivo original, sino que se crea uno nuevo. Involucran un archivo **maestro** y uno de **movimiento**.

![[Esquema de la Actualización Secuencial.png]]

**Unitaria**: cero o un [[Registro]] del fichero movimiento por cada registro del maestro.

```
[abrir_archivos]
[leer_maestro]
[leer_movimiento]
MIENTRAS clave_mae <> HV O clave_mov <> HV HACER
	SI clave_mae = clave_mov ENTONCES
		[procedimiento_para_registros_iguales]  // bajas y modificaciones.
	CONTRARIO
		SI clave_mae < clave_mov ENTONCES
			registro_salida := reg_maestro
			Escribir(archivo_salida, registro_salida)
			Leer_Maestro()
		CONTRARIO
			[procedimiento_para_archivos_distintos]  // altas.
		FIN_SI
	FIN_SI
FIN_MIENTRAS
[cerrar_archivos]
```

**Por lotes**: cero o más registros del fichero movimiento por cada registro del fichero maestro.

```
[abrir_archivos]
[leer_maestro]
[leer_movimiento]
MIENTRAS clave_mae <> HV O clave_mov <> HV HACER
	SI clave_mae < clave_mov ENTONCES         // maestro sin movimiento.
		registro_salida := registro_maestro
		Escribir(archivo_salida, registro_salida)
		[leer_maestro]
	CONTRARIO
		SI clave_mae = clave_mov ENTONCES     // lote con movimiento.
			auxiliar := registro_maestro
			MIENTRAS clave_mae = clave_mod HACER
				[procedimiento_para_lote_con_movimiento]  // bajas o modifs.
				[leer_movimiento]
			FIN_MIENTRAS
			registro_salida := auxiliar
			Escribir(archivo_salida, registro_salida)
			[leer_maestro]
		CONTRARIO                             // movimiento sin maestro.
			auxiliar := registro_movimiento
			auxiliar.marca_baja := ''
			[leer_movimiento]
			MIENTRAS clave_auxiliar = clave_mov HACER
				[procedimiento_para_lote_con_movimiento]  // altas.
				[leer_movimiento]
			FIN_MIENTRAS
			Escribir(archivo_salida, auxiliar)
		FIN_SI
	FIN_SI
FIN_MIENTRAS
[cerrar_archivos]
```

### Actualización Indexada

Para archivos indexados.