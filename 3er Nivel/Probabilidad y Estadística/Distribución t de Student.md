La [[Distribuciones de Probabilidad de Variable Continua|distribución]] t de Student supone que $Z$ y $\chi^2_n$ son variables aleatorias independientes, con $Z\sim N$ (que sigue una [[Distribución Normal]]) y $\chi^2_n \sim \chi^2_n$ (que sigue una [[Distribución Chi-Cuadrado]]). Se define una variable aleatoria $T_n$:

$$T_n = \frac{Z}{\sqrt \frac{\chi^2_n}{n}}$$

La cual sigue una **distribución t de Student** con $n$ grados de libertad. A medida que $n$ crece, la función se acerca cada vez más a la función normal estandarizada.

![[Distribución t de Student.png]]

Sea la siguiente variable aleatoria $t$ definida a partir de una variable aleatoria $X$ con media $\mu$ y varianza $\sigma^2$:

$$t = \frac{\overline X - \mu_{\overline X}}{\sqrt{\frac{\sum(X_i - \overline X )^2}{n (n-1)}}} = \frac{\overline X - \mu}{\frac{S}{\sqrt{n-1}}} = \frac{\overline X - \mu}{\frac{S_c}{\sqrt{n}}} \implies t=\frac{\frac{\overline X - \mu}{\frac{\sigma}{\sqrt n}}}{\sqrt\frac{S^2_c}{\sigma^2}} \implies t = \frac{Z}{\sqrt{\frac{\chi^2_v}{v}}}$$

Siendo $v = n-1$, por lo que $t$ es una variable aleatoria con distribución $t$ de Student con $v$ grados de libertad.
