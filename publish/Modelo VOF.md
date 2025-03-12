O **modelo volume de fluido (VOF)** é uma técnica que consiste em analisar as interfaces de fluidos imiscíveis. Dessa forma o VOF captura as frações volumétricas de cada fase dentro do volume de controle, a soma das frações de todas as fases é igual à unidade, ou seja, igual 1. O conjunto de equações de momento e continuidade são resolvidos para todas as fases.

**Equação da continuidade**

![[Equação da ContinuidadeVOF.png]]
Equação para Latex:
````
\frac{\partial \rho}{\partial t} + \nabla \centerdot (\rho \overline{u}) = 0
````

**Equação do momentum**

![[Equação do Momentu VOF.png]]

Equação para Latex:
````
\frac{\partial}{\partial t} (\rho \overline{u}) + \nabla \centerdot (\rho \overline{u} \overline{u}) = - \nabla P + \rho g + \nabla (\tau + \tau ^t)
````
### Referencias

[https://www.sciencedirect.com/science/article/abs/pii/B9780128219553000029](https://www.sciencedirect.com/science/article/abs/pii/B9780128219553000029)
[https://support.ptc.com/help/creo/creo_pma/r9.0/portuguese_br/index.html#page/simulate/cfd/SpclConsiderationsVOF.html](https://support.ptc.com/help/creo/creo_pma/r9.0/portuguese_br/index.html#page/simulate/cfd/SpclConsiderationsVOF.html)

COMPARISON BETWEEN EULERIAN AND VOF MODELS FOR TWO-PHASE FLOW ASSESSMENT IN VERTICAL PIPES

Relatório do Guilherme