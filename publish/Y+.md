### **Defining Boundary Conditions for Turbulent flows in Ansys Fluent - Lesson 3**

[https://courses.ansys.com/index.php/courses/turbulence-modeling-in-ansys-fluent/lessons/defining-boundary-conditions-for-turbulent-flows-in-ansys-fluent-lesson-3/](https://courses.ansys.com/index.php/courses/turbulence-modeling-in-ansys-fluent/lessons/defining-boundary-conditions-for-turbulent-flows-in-ansys-fluent-lesson-3/)

Vale a pena dar uma olhada nesse site

### __[CFD] What is the difference between y+ and y_?_*

[https://www.youtube.com/watch?v=nSdVaF3JnI0](https://www.youtube.com/watch?v=nSdVaF3JnI0)

### Calculadora Y+

[https://www.cfd-online.com/Tools/yplus.php](https://www.cfd-online.com/Tools/yplus.php)

Sendo y+ = 1

$$ y^+ = \frac{yU^*}{\nu} $$

y = comprimento do primeiro elemento

Viscosidade cinemática $\nu$

$$ \nu = \frac{\mu}{\rho} $$

Velocidade de fricção $U^*$

$$ U^* = \sqrt{\frac{\tau_w}{\rho}} $$

Tensão de cisalhamento na parede $\tau_w$

$$ \tau_w = \frac{1}{2}C_f \rho \bar{U}^2 $$

Coeficiente de atrito da pele para fluxo do duto $C_f$

$$ C_f = 0,078 Re^{-0,25} $$

Obs.: Com essas informações calcula-se o comprimento do primeiro elemento (y)

## Calculo do Fator Bias

Soma da progressão geométrica com n termos, sendo l1 o termo inicial

$$ L = \sum_{0}^{i} l1 * r^2 $$

$$ bf = r^{(n-1)} $$

L = Comprimento edge = Comprimento inlet = 26 mm

r = Taxa de crescimento

bf = Fator Bias

n = numero de divisões

i = n-1

l1 = comprimento do primeiro elemento = y

Video com os calculos

[https://www.youtube.com/watch?v=-lIC6UKWByQ&list=WL&index=3](https://www.youtube.com/watch?v=-lIC6UKWByQ&list=WL&index=3)