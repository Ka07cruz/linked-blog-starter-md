O **Y+** é um parâmetro adimensional usado em CFD para avaliar a resolução da malha perto de superfícies sólidas em simulações de escoamentos turbulentos. Ele indica a posição do primeiro ponto da malha em relação à camada limite e é essencial para escolher corretamente os modelos de turbulência. Valores baixos de **Y+** (próximos de 1) são usados para resolver completamente a camada limite com equações como as do modelo **k-omega SST**, enquanto valores mais altos (30–300) permitem o uso de funções de parede para modelar a região próxima à superfície. Ajustar corretamente o **Y+** melhora a precisão das simulações sem aumentar desnecessariamente o custo computacional.
### **Defining Boundary Conditions for Turbulent flows in Ansys Fluent - Lesson 3**
- [https://courses.ansys.com/index.php/courses/turbulence-modeling-in-ansys-fluent/lessons/defining-boundary-conditions-for-turbulent-flows-in-ansys-fluent-lesson-3/](https://courses.ansys.com/index.php/courses/turbulence-modeling-in-ansys-fluent/lessons/defining-boundary-conditions-for-turbulent-flows-in-ansys-fluent-lesson-3/)
Obs.:Vale a pena dar uma olhada nesse site

### [CFD] What is the difference between y+ and y* ?

Os parâmetros são parecidos porém análise coisa diferentes: 
- [https://www.youtube.com/watch?v=nSdVaF3JnI0](https://www.youtube.com/watch?v=nSdVaF3JnI0)
### Calculadora Y+
- [https://www.cfd-online.com/Tools/yplus.php](https://www.cfd-online.com/Tools/yplus.php)

Sendo y+ = 1
![[y.png]]
 Equação para Latex:
 
````
 y^+ = \frac{yU^*}{\nu} 
````

y = comprimento do primeiro elemento

Viscosidade cinemática $\nu$
![[v.png]]
 Equação para Latex:
 
````
 \nu = \frac{\mu}{\rho}
````

Velocidade de fricção $U^*$

![[U.png]]
 Equação para Latex:
 
````
 U^* = \sqrt{\frac{\tau_w}{\rho}}
````

Tensão de cisalhamento na parede $\tau_w$
![[T.png]]
 Equação para Latex:
 
````
 \tau_w = \frac{1}{2}C_f \rho \bar{U}^2
````

Coeficiente de atrito da pele para fluxo do duto $C_f$
![[C.png]]
 Equação para Latex:
 
````
 C_f = 0,078 Re^{-0,25}
````
Obs.: Com essas informações calcula-se o comprimento do primeiro elemento (y)

## Calculo do Fator Bias

Soma da progressão geométrica com n termos, sendo l1 o termo inicial

![[L.png]]
Equação para Latex:
 
````
L = \sum_{0}^{i} l1 * r^2
````

![[b.png]]
Equação para Latex:
 
````
bf = r^{(n-1)}
````

L = Comprimento edge = Comprimento inlet = 26 mm

r = Taxa de crescimento

bf = Fator Bias

n = numero de divisões

i = n-1

l1 = comprimento do primeiro elemento = y

Video com os calculos
-  [https://www.youtube.com/watch?v=-lIC6UKWByQ&list=WL&index=3](https://www.youtube.com/watch?v=-lIC6UKWByQ&list=WL&index=3)