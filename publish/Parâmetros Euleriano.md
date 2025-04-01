Esses parâmetros de simulação são para escoamento interno em tubo horizontal com modelo Euleriano

### Solver Options
- Double Precision

Click "Start"
### General
1. Time >Transient
2. Gravity > -9,81 m/s^2
### Materials

- Fluid > air > Fluent Database >Water-liquid(H2O liquido) > copy > close

## Models

1. Multiphase>Model> Eulerian
2. Regime Transition Modeling > AIAD
3. 2. Formulation > Implicit

Na aba Phases

- Phases > phase-1 = water, phase-2 = air

Obs.: Para Diameter na Phase Air, deixar Default 

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
##### Inlet air (Phase> air) 
- **Momentum**

Velocity Magnitude> Velocidade do diagrama de padrões

1. Turbulence> Specification Method> Intensity and Hydraulic Diameter
2. Turbulent Intensity> 5%
3. Hydraulic Diameter> 26 mm

- **Multiphase**

Volume Fraction = 1 
##### Inlet air (Phase> Water) 

Default Ou Velocity = 0

--------------------------------------------------------------------------
#### Inlet water (Phase> mixture)

- Mesmo processo da Inlet air
##### Inlet water (Phase> air)

- Multiphase> Volume Fraction>  0
#### Outlet (Phase>Water)
1. Turbulence> Specification Method> Intensity and Hydraulic Diameter
2. Turbulent Intensity> 5%
3. Hydraulic Diameter> 26 mm
##### Outlet (Phase> air)
- Igual ao Phase > Water
#### Wall (Phase> mixture)
1. Wall Motion> Stationary Wall
2. Shear Condition> No slip
3. Wall Adhesion> Contact Angles> 60 
Obs.: Valor para água

### Methods
- Scheme > Coupled
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