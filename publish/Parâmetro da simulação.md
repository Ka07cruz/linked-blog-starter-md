Esses parâmetros de simulação são para escoamento interno em tubo horizontal com modelo VOF

### Solver Options
- Double Precision

Click "Start"
### General
1. Time >Transient
2. Gravity > -9,81 m/s^2
### Materials

- Fluid > air > Fluent Database >Water-liquid(H2O liquido) > copy > close

## Models

1. Multiphase>Model> Volume of Fluid
2. Formulation > Explicit

Obs.: Explícito oferece mais precisão, mas os intervalos de tempo podem precisar ser menores; o implícito permite intervalos de tempo maiores e estado estacionário. Você provavelmente desejará algo explícito, portanto, talvez seja necessário revisar o tamanho do intervalo de tempo.

Obs.: O VOF explícito está convergindo melhor em comparação com o VOF implícito, mas mostra uma "exceção de ponto flutuante" depois de algum tempo (após alguma porcentagem de conclusão). Pode ser visto no [link](https://forum.ansys.com/forums/topic/explicit-vof-vs-implicit-vof-for-laser-melting/](https://forum.ansys.com/forums/topic/explicit-vof-vs-implicit-vof-for-laser-melting/)

Obs.: O apesar da formulação explicita trazer melhores resultados, por calcular todos parâmetros do tempo anterior, essa precisão aumenta o tempo de simulação. Já a formulação implícita não utiliza todos os parâmetros para calcular os tempos futuros, diminui na precisão mas tbm diminui o tempo de simulação. Como não interessa os período transiente pode-se utilizar.

3. Body Implicit Force Formulation > Implicit Body Force

Na aba Phases

- Phases > phase-1 = water, phase-2 = air

Obs.: Ordem das fases não importa, mas prefiro colocar a fazer que vai preencher tubo primeiro. Nesse caso a agua vai preencher e será visto fração do vazio do ar

Na aba Phase Interaction

1. Surface Tension Coefficient> constant> 0.073 N/m

Obs.: Valor para água

2. Global Options> Surface Tension Force Modeling
3. Model> Continuum Surface Force
4. Adhesion Options> Wall Adhesion

### Energy

Off ( tudo é isotérmico, então não precisa)

### Viscous

- Transition SST k-w

OBS.: Ele é melhor porque consegue fazer a transição de k-e e k-w. Os três são para escoamento turbulento. Pode ser visto no [link]([https://www.cfd-online.com/Forums/main/75554-use-k-epsilon-k-omega-models.html](https://www.cfd-online.com/Forums/main/75554-use-k-epsilon-k-omega-models.html)

### Boundary Conditions

#### Inlet air (Phase> mixture)

1. Velocity Magnitude> Velocidade do diagrama de padrões

Obs.: Diagrama de Padrões de Padrão de escoamento precisar ser na horizontal, pois existe para vertical e inclinado. 

2. Turbulence> Specification Method> Intensity and Hydraulic Diameter
3. Turbulent Intensity> 5%
4. Hydraulic Diameter> 26 mm
##### Inlet air (Phase> air) 

- Multiphase> Volume Fraction>  1
#### Inlet water (Phase> mixture)

- Mesmo processo da Inlet air
##### Inlet water (Phase> air)

- Multiphase> Volume Fraction>  0
#### Outlet (Phase> mixture)
1. Turbulence> Specification Method> Intensity and Hydraulic Diameter
2. Turbulent Intensity> 5%
3. Hydraulic Diameter> 26 mm
##### Outlet (Phase> air)
- Multiphase> Backflow Volume Fraction>  0

#### Wall (Phase> mixture)
1. Wall Motion> Stationary Wall
2. Shear Condition> No slip
3. Wall Adhesion> Contact Angles> 60 
Obs.: Valor para água
### Methods
- Scheme > PISO
### Controls
- Não é preciso mexer, pode ser usado os fatores de relaxamento como no [video]([https://www.cfd-online.com/Forums/fluent/44367-what-under-relaxation-factor.html](https://www.cfd-online.com/Forums/fluent/44367-what-under-relaxation-factor.html)
### Initialization

Initialization Methods > Hybrid

Obs.: Li no [video]([https://courses.ansys.com/index.php/courses/solution-setup-in-ansys-fluent/lessons/how-to-initialize-the-solution-in-ansys-fluent-lesson-5/](https://courses.ansys.com/index.php/courses/solution-setup-in-ansys-fluent/lessons/how-to-initialize-the-solution-in-ansys-fluent-lesson-5/)) fala que Hybrid é mais realista a análise

### Surfaces
- Botão direito > New > Line/Rake > definir linha para análise
	- x = 0.63 m 
	- y = 0.026

### Report Definitions 
- Botão direito > New > Surface Report > Facet Average
	- Filed Variable
		- Phases
		- Volume fraction
	- Phase > air
	- Surfaces > nome da linha criada 

### Monitors 
- Report Files > Botão direito > New 
	- Available Report Definitions > nome o report definitions 
	- Get data Every > Write Instantaneous Values

### Graphics 
- Contours > 
	- Contours of > 
		- Phases
		- Volume fraction
- Phase > Air

### Calculation Activities
- Solution Animations > Storage Type > PNG Image
- Animation Object > Animation View > front

### Run Calculation
Para  começar a simulação precisa calcular o Passo de tempo (dx) pelo [[Critério de Estabilidade]]. No começo tinha muita duvida sobre CFL e Número de Courant (C) até achar esse [site]([https://uxcfd.com/2012/11/16/numero-de-courant-cfl-e-condicao-cfl/](https://uxcfd.com/2012/11/16/numero-de-courant-cfl-e-condicao-cfl/)

Para facilitar as análise crie uma tabela que gera os passo de tempo e numero de passo de tempo, porque muda para diferentes tamanho de elemento de malha e velocidade superficial. Link para [tabela](https://docs.google.com/spreadsheets/d/1G2iAOQAPcQ7JpwevCkmBhT1wlSGFV_2o5JiT1iEVv74/edit?usp=sharing)

### Autosave
Autosave Solution after every few iterations

- File > Write > Autosave
	- Save Data File Every = 3
	- Save Associated Case Files > Only if Modified
	- File Storage Options > Retain Only the Most Recent Files
		- Maximum Number of Date Files = 5

Obs.: Importante marcar a opção de deixar os 5 últimos arquivos

[https://www.youtube.com/watch?app=desktop&v=4JT--GT0XU0](https://www.youtube.com/watch?app=desktop&v=4JT--GT0XU0)