O **modelo Euleriano** consiste em resolver as equações de momento e continuidade para cada fase separadamente. O acoplamento é feito por uma única pressão entre as fases.

O número de fases de um escoamento para o Euleriano é limitado apenas por memória e comportamento de convergência. Para escoamento complexo o fator mais limitante é comportamento de convergência.

Outra limitação do Euleriano é a dificuldade em diferenciar multifásico fluido-fluido do fluido-solido (granulado)

Fluido não pode ser invíscido

**Equação da Continuidade**

![[Equação da Continuidade.png]]

 Equação para Latex:
 
````
\frac{\partial}{\partial t} (\alpha _i \rho _i) + \nabla \centerdot (\alpha _i \rho _i \overline{u} _i) = 0
````

 **Equação do Momentum**

![[Equação do Momentu.png]]

Equação para Latex:
````
\frac{\partial}{\partial t} (\alpha _i \rho _i \overline{u} _i) + \nabla \centerdot (\alpha _i \rho _i \overline{u} _i \overline {u} _i) = - \alpha _i \nabla P + \alpha _i g + \nabla [\alpha _i (\tau _i + \tau^t _i) + M_i ]
````

### Referencias
- [https://www.afs.enea.it/project/neptunius/docs/fluent/html/th/node320.htm](https://www.afs.enea.it/project/neptunius/docs/fluent/html/th/node320.htm)
- https://support.ptc.com/help/creo/creo_pma/r9.0/portuguese_br/index.html#page/simulate/cfd/EulerianModels.html](https://support.ptc.com/help/creo/creo_pma/r9.0/portuguese_br/index.html#page/simulate/cfd/EulerianModels.html)
- [https://www.sciencedirect.com/science/article/abs/pii/B9780128166734000080](https://www.sciencedirect.com/science/article/abs/pii/B9780128166734000080)
- file:///C:/Users/kaue1/Downloads/Referencias_Guilherme/COMPARISON%20BETWEEN%20EULERIAN%20AND%20VOF%20MODELS%20FOR%20TWO-PHASE%20FLOW%20ASSESSMENT%20IN%20VERTICAL%20PIPES.pdf