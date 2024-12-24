Al insertar un [[Materiales Dieléctricos|dieléctrico]] entre las placas de un [[Capacitor]], el dieléctrico se polariza, generando un pequeño [[Campo Eléctrico]] $\vec E_i$ en sentido opuesto a $\vec E_0$. Dado $E = E_0 - E_i$, el campo eléctrico **disminuye**.

![[Polarización por un Dieléctrico.png]]

## Vector Polarización

El **vector polarización** es el momento dipolar por unidad de volumen: $\vec P = \frac{\vec p}{V}$, y tiene la misma dirección y sentido que $\vec E$. El campo eléctrico induce una densidad superficial de polarización $\sigma_p$. 

Un dieléctrico sometido a un campo se comporta como un [[Dipolo Eléctrico]] con carga $Q p = \pm \sigma_p A$, por ende $p = \sigma _p A L$, siendo $A$ el área de la placa y $L$ la separación entre las placas. 

El módulo del vector está dado por $|\vec P| = \frac{p}{V} = \frac{p}{AL} = \frac{\sigma_p AL}{AL} = |\sigma_p| \implies PA = - Q_p$, donde $PA$ representa el flujo del vector polarización a través de $A$. Aplicando Gauss, para una superficie cerrada que contenga la carga de polarización $-Qp$, se tiene $\oint \vec P \cdot d \vec S = - Q_p$. El flujo del vector polarización a través de una superficie cerrada es el opuesto de la carga de polarización superficial.

## Vector Desplazamiento Eléctrico

Sea $\sigma_p = \pm P_n \ \land \ E_l = E_0 - E_p \ \land \ E_p \lt E_0$. Dado que sin dieléctrico se tiene $E_l = E_0 = \frac{\sigma_l}{\varepsilon_0}$, y con dieléctrico se tiene $E_l = \frac{\sigma_l + \sigma_p}{\varepsilon_0} = \frac{\sigma_l - P}{\varepsilon_0}$. Entonces, $\sigma_l = \varepsilon_0 E_l + P \implies \vec D = \varepsilon_0 \vec E_l + \vec P$. Se define un nuevo campo vectorial creado por las cargas libres del conductor denominado vector desplazamiento $\vec D$.

La polarización $\vec P$ es proporcional al campo eléctrico aplicado: $\vec P = \chi_e \varepsilon_0 \vec E$, donde $\chi_e$ es una constante de proporcionalidad adimensional que mide la facilidad de polarización de un dieléctrico, lo que se conoce como **susceptibilidad eléctrica**.

Se puede obtener la permitividad $\varepsilon$ del material:
$$\vec D = \varepsilon_0 \vec E + \chi_e \varepsilon_0 \vec E = (1 + \chi_e) \varepsilon_0 \vec E = \varepsilon \vec E \implies \varepsilon = (1 + \chi_e) \varepsilon_0$$

## Ley de Gauss Generalizada

$$\oint \vec E d \vec S = \frac{q_l + q_p}{\varepsilon_0} = \frac{q_l}{\varepsilon_0} - \frac{1}{\varepsilon_0} \oint \vec P d \vec S \implies \varepsilon_0 \oint \vec E d \vec S + \oint \vec P d \vec S = q_l \implies q_l = \oint (\varepsilon_0 \vec E + \vec P) d \vec S$$

Se encuentra que el **flujo del vector desplazamiento eléctrico** a través de una superficie cerrada es igual a la carga libre neta encerrada en su interior.

$$\Phi = \oint \vec D \cdot \vec {dS} = \oint \varepsilon \vec E \cdot \vec {dS} = q_{\text{libre}} \implies \oint \vec E \cdot \vec {dS} = \frac{q_{\text{libre}}}{\varepsilon}$$

El vector desplazamiento $\vec D$ no tiene un claro significado físico. La única razón para definirlo es que permite calcular campos en presencia de dieléctricos sin tener primero conocimiento de las distribuciones de carga de polarización.
