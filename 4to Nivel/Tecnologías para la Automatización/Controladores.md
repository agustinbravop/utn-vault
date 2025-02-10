Un **controlador automático** compara el valor real de la salida de un [[Sistema de Control]] con la *entrada de referencia*, determina la desviación, y produce una *señal de control* que reducirá la desviación.

Un controlador introduce *polos* en la [[Función de Transferencia]] del sistema para forzar la [[Estabilidad de los Sistemas de Control]] y hacer **estable** al sistema.

![[Controladores.png]]

Tipos de controladores:

1. De dos posiciones (on/off).
2. Proporcionales.
3. Integrales.
4. Proporcionales-integrales.
5. Proporcionales-derivativos.
6. Proporcionales-integrales-derivativos.

## Acción de Control Proporcional

El **controlador proporcional** es sencillo. Es básicamente un amplificador con cierta ganancia constante $u(t) = K_p \cdot e(t)$.

Si bien es un controlador simple, el problema es que siempre habrá un [[Error en Estado Estable de los Sistemas de Control|error]] en estado estacionario frente a una entrada escalón. Siempre habrá una desviación u *offset* con respecto al valor de referencia.

![[Controlador Proporcional.png]]

## Acción de Control Integral

Un **controlador integral** busca solucionar el problema del control proporcional. La ganancia $u(t)=K_i \int_0^t e(t)dt$ asegura que se cumpla $e_{ss}(t)=0$ para una entrada escalón $S_i(s) = \frac{1}{s}$.

![[Controlador Integral.png]]

Esto elimina el error en estado estacionario en respuesta a un escalón unitario.

## Acción de Control PID

Un **controlador proporcional-integral-derivativo** tiene tres parámetros:

1. **Proporcional**: depende del error actual.
2. **Integral**: depende de los errores pasados.
3. **Derivativo**: predicción de los errores futuros. Es sensible al ruido.

![[Controlador PID.png]]

$$u(t) = \underbrace{K_p e(t)}_\text{proporcional} + \underbrace{\frac{K_p}{T_i}\int_0^te(t)dt}_\text{integral} + \underbrace{K_pT_d\frac{de(t)}{dt}}_\text{derivativo}$$

Un controlador PID también puede ser simplemente PD o PI, si es que no se necesitan todas las acciones de control.
