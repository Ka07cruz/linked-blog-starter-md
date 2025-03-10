Obs.: Diagrama de Padrões precisar ser na horizontal tbm haha

Double Precision

Time >Transient

Gravity > -9,81 m/s^2

### Materials

Fluid > air > Fluent Database >Water-liquid(H2O liquido) > copy > close

## Models

### Multiphase

Model> Volume of Fluid

Formulation > Explicit

Obs.: Explícito oferece mais precisão, mas os intervalos de tempo podem precisar ser menores; o implícito permite intervalos de tempo maiores e estado estacionário. Você provavelmente desejará algo explícito, portanto, talvez seja necessário revisar o tamanho do intervalo de tempo.

Obs.: O VOF explícito está convergindo melhor em comparação com o VOF implícito, mas mostra uma "exceção de ponto flutuante" depois de algum tempo (após alguma porcentagem de conclusão).

[https://forum.ansys.com/forums/topic/explicit-vof-vs-implicit-vof-for-laser-melting/](https://forum.ansys.com/forums/topic/explicit-vof-vs-implicit-vof-for-laser-melting/)

Obs.: O apesar da formulação explicita trazer melhores resultados, por calcular todos parâmetros do tempo anterior, essa precisão aumenta o tempo de simulação. Já a formulação implícita não utiliza todos os parâmetros para calcular os tempos futuros, diminui na precisão mas tbm diminui o tempo de simulação. Como não interessa os período transiente pode-se utilizar.

Body Implicit Force Formulation > Implicit Body Force

Phase > phase-1 = water, phase-2 = air

Obs.: Ordem das fases não importa, mas prefiro colocar a fazer que vai preencher tubo primeiro. Nesse caso a agua vai preencher e será visto fração do vazio do ar

### Energy

Off ( tudo é isotérmico, então não precisa)

### Viscous

Transition SST k-w

OBS.: Ele é melhor porque consegue fazer a transição de k-e e k-w. Os três são para escoamento turbulento. Guilherme fala isso no tcc dele

[https://www.cfd-online.com/Forums/main/75554-use-k-epsilon-k-omega-models.html](https://www.cfd-online.com/Forums/main/75554-use-k-epsilon-k-omega-models.html)

### Boundary Conditions

inlet

Phase air = 1

Phase water = 0

Obs.: Não é na mistura e sim na phase de cada um

método de especificação de turbulência: intermitente, intensidade e diâmetro hidráulico

### Methods

Scheme > PISO

### Controls

[https://www.cfd-online.com/Forums/fluent/44367-what-under-relaxation-factor.html](https://www.cfd-online.com/Forums/fluent/44367-what-under-relaxation-factor.html)

### Initialization

Initialization Methods > Hybrid

Obs.: Li em algum lugar que Hybrid é mais realista a análise

[https://courses.ansys.com/index.php/courses/solution-setup-in-ansys-fluent/lessons/how-to-initialize-the-solution-in-ansys-fluent-lesson-5/](https://courses.ansys.com/index.php/courses/solution-setup-in-ansys-fluent/lessons/how-to-initialize-the-solution-in-ansys-fluent-lesson-5/)

### Run Calculation

Numero de Courant - o _número de volumes da malha atravessados por uma perturbação naquele passo de tempo_.

[https://uxcfd.com/2012/11/16/numero-de-courant-cfl-e-condicao-cfl/](https://uxcfd.com/2012/11/16/numero-de-courant-cfl-e-condicao-cfl/)

### Descobrindo time step

$C = Jg*deltaT/deltaX$

C - numero de courant

Jg - velocidade da phase ar

deltaT - time step

deltaX - menor elemento de malha

Obs.: Essa equação da estabilidade para a simulação. Se o time step for muito pequeno vai dar floating point e se for muito grande vai dar divergência.

segundos / time step = iteração

itaração * time step = segundos

Autosave Solution after every few iterations

File > Write > Autosave

Obs.: Importante marcar a opção de deixar os 5 ultimos arquivos

[https://www.youtube.com/watch?app=desktop&v=4JT--GT0XU0](https://www.youtube.com/watch?app=desktop&v=4JT--GT0XU0)