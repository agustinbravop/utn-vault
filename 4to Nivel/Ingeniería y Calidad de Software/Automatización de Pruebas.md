**Testing Automation** es software que prueba software. Sin automatización de pruebas solo tenemos "compilación continua". Mientras más veces se tiene que ejecutar un [[Casos de Prueba]], más conviene automatizarlo. Para implementar casos de prueba, se utilizan [[Test Doubles]].

En la [[Agilidad]], se vuelve útil la automatización de pruebas porque se espera realizar **muchos cambios** al software $\implies$ se espera **probar muchas veces** el software. La TA nos **facilita ser ágiles**.

3 mitos falsos:

- Siempre mejora la calidad del software (no es suficiente).
- Cualquier equipo puede usar herramientas de TA (requiere formación).
- TA es un todo o nada (hay grises y adopción gradual).

3 realidades:

- TA requiere mayor inversión inicial, pero obtiene mejor ROI.
- Requiere conocimientos y **herramientas**.
- Siempre se necesita algo de [[Pruebas Manuales]].

## ¿Cuándo y cuanto automatizar?

![[Economics of Testing.png]]

Automatizar cuando:

- El ROI lo permita.
- Se mira a largo plazo.
- Hay muchos cambios que requieren volver a probar.

## Pirámide de Pruebas Automatizadas

![[Pirámide de pruebas automatizadas.png]]
![[Pirámide de pruebas.png]]

Hacer muchas pruebas unitarias, que son **eficientes**. Hacer pocas pruebas de UI, que son caras y frágiles.

## Pruebas Unitarias

Buenas pruebas unitarias se describen con el acrónimo **FIRST** de Uncle Bob:

1. **Fast**
2. **Independent** (entre ellas)
3. **Repeatable**
4. **Self** (tienen lo necesario para ejecutarse)
5. **Timely**
