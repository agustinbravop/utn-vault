Un conjunto de objetos está organizado en forma de secuencia si se puede definir:

1. **El primer objeto de la secuencia**: un primer objeto que se distingue de los demás. **Acceder a este objeto** permite acceder a los demás elementos.
2. **Relación de sucesión entre los objetos**: todo objeto salvo el último **precede a un sucesor**, o todo elemento excepto el primero es sucesor de otro.
3. **Finitud**: debe estar definido un indicador de **fin de secuencia** que sea un elemento final conocido, o una marca, o la longitud exacta de la secuencia. Sirve para saber cuando dejar de recorrer la secuencia.
4. **Orden**: existe o no un orden cuando la sucesión es estricta.
5. **Completitud**: no se puede suponer. Explicita que entre elementos no hay ausencias.

Las secuencias se almacenan en **memoria persistente** (disco). El **tamaño** de una secuencia no es fijo, y para su procesamiento se debe emplear un esquema de asignación de almacenamiento en memoria dinámico.

## Procesamiento

Según su procesamiento, las secuencias se clasifican en:

1. **Definida**: se usa una [[Estructuras de Código#Iterativas|estructura iterativa]] manejada por **contador**.
2. **Indefinida pura**: se usa una estructura **post-test** porque se conoce el \*\*último elemento.
3. **Indefinida impura**: se usa una estructura **pre-test** porque tiene **marca de fin**.

## Máquina de Caracteres

Si imaginamos la secuencia como una **cinta** de caracteres de los cuales solo se puede ver un caracter a la vez a través de una **ventana**, surgen las siguientes instrucciones:

- `ARR`: arranca el tratamiento de la secuencia (no avanza la cinta, no se ve ningún caracter).
- `AVZ`: avanza la cinta mostrando el siguiente caracter.
- `ventana`: [[Variable]] que muestra el valor de un caracter de la cinta (al que se puede acceder).

Ejemplo del recorrido de una secuencia indefinida pura:

```
ARR(s);
cont := 0;
REPETIR
	AVZ(S, ventana);
	cont := cont + 1;
HASTA QUE ventana = "."
FIN_REPETIR
```

Ejemplo del recorrido de una secuencia indefinida impura:

```
ARR(s);
cont := 0;
AVZ(S, ventana);
mientras V <> "." hacer
	cont := cont + 1;
	avz(s, VENTANA);
FIN_MIENTRAS
```
