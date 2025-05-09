---
title: Two Phase Flow
excerpt: Create your own template or use someone else's. Changing the template is a matter of updating one line
---
## Sobre
Olá. Meu nome é Kauê Cruz, estudante de engenharia mecânica na UTFPR Campus Cornélio Procópio. Inicie como voluntário para pesquisar sobre escoamento bifásico em 2023. Tive um pouco de dificuldade no começo com esse estudo, devido a complexidade da análise numérica e do tema escoamento multifásico. 

Eu comecei fazer notas para me ajudar a lembra das configurações das simulações no Notion. Entretanto um amigo começou a fazer um estudo semelhante ao meu então compartilhei as notas, porém tinha limite de notas compartilhadas no Notion. Foi quando precisei mudar para Obsidian que me ajudou bastante por ter notas ilimitadas.

![[Contorno_Legenda.png]]
## Artigos

Link para [Artigos](https://github.com/Ka07cruz/linked-blog-starter-md/tree/main/Artigos)

## Introdução
Importante mencionar que boa parte do site apenas foram reunidas as informações que fui buscando ao longo da pesquisa, entretanto os links originais de onde vieram as informações estão mencionados no final de cada página do parágrafo. Esse site é apenas minhas notas do Obsidian que são publicadas automaticamente. 

Escoamento bifásico (Two Phase Flow) é o movimento simultâneo de duas fases distintas (líquido-líquido, líquido-gás, sólido-líquido ou sólido-gás) dentro de um meio, como em tubulações ou canais. Esse tipo de escoamento é comum em indústrias como petróleo, química e energia, onde pode envolver misturas como água e vapor, óleo e gás, ou partículas suspensas em líquidos. A interação entre as fases influencia características como pressão, velocidade e padrões de fluxo, tornando sua análise complexa e essencial para projetos e operações eficientes. 

![[geometria.jpg]]
## Sites para Iniciar a Pesquisa
Para facilitar as pesquisas acadêmicas, foram selecionados e organizados diversos sites e repositórios que disponibilizam artigos científicos e trabalhos de conclusão de curso (TCC).
- [[Sites para Pesquisar]]
## Modelos Numéricos 
Esses são modelos numéricos utilizados na dinâmica dos fluidos computacional (CFD) para simular escoamentos complexos, especialmente em cenários com múltiplas fases e turbulência.
- [[Modelo Euleriano]]
- [[Modelo VOF]]
- [[Diferenças entre VOF, Euleriano e Mistura]]
- [[Modelo de turbulência K-omega SST]]
- [[Modelo de tensão superficial]]
- [[Modelos de Turbulência e Método de especificação de turbulência]]
## Sobre Malha 
A malha em CFD (Computational Fluid Dynamics) é a discretização do domínio de estudo em pequenas células, onde as equações de escoamento são resolvidas numericamente. Ela pode ser estruturada (grade regular), não estruturada (elementos irregulares) ou híbrida, influenciando diretamente a precisão e o custo computacional da simulação. Um refinamento adequado da malha em regiões de alto gradiente, como bordas e interfaces, melhora a captura dos fenômenos físicos sem gerar um excesso de elementos que aumente o tempo de processamento.

Em CFD, a malha deve ter uma quantidade de elementos suficiente para capturar corretamente os fenômenos do escoamento, equilibrando precisão e custo computacional. O refinamento deve ser maior em regiões de alto gradiente, como fronteiras sólidas e interfaces de fases. O parâmetro adimensional **Y+** é crucial para definir a resolução da malha próxima às paredes, influenciando a escolha dos modelos de turbulência. Para resolver completamente a camada limite, a malha deve garantir **Y+ ≈ 1**, enquanto valores entre **30 e 300** permitem o uso de funções de parede, reduzindo a necessidade de refinamento excessivo.

![[malha.png]]
### Como saber a quantidade elemento de malha ?
- [[Quantidade de elementos da malha]]
### Parâmetro adimensional Y+
- [[Y+]]
## Critério
O critério de estabilidade em CFD determina as condições necessárias para que a solução numérica das equações de escoamento permaneça estável e convergente. Um dos mais conhecidos é o **Critério de Courant-Friedrichs-Lewy (CFL)**, que define o limite de tempo de integração em métodos explícitos, garantindo que a informação não se propague além de um elemento da malha em um passo de tempo. Para métodos implícitos, restrições de estabilidade podem ser menos rígidas, mas o refinamento da malha e a escolha dos esquemas numéricos ainda influenciam a precisão e a robustez da simulação.
- [[Critério de Estabilidade]]
## Problemas Comuns
- [[Como resolver erro de ponto flutuante]]
- [[The following project file may not have been backed up...]]
- [[FFF.1-Setup-Output.cas.h5 not found !]]
## Tutoriais
Aqui estão alguns tutoriais semelhantes ao modelo de escoamento bifásico horizontal:
- [[Theory and CFD simulation of Two-phase flow in vertical conduit using ANSYS Fluent]]
- [[Using the Mixture and Eulerian Multiphase Models]]
- [[ANSYS-Fluent Tutorial Two-phase flow Slug flow Multiphase flow simulation]]
## Casos Simulados
- [[Tubo Horizontal Modelo VOF]]
- [[Tubo Horizontal Modelo Euleriano]]
## Adicionais
- [[Tempo de Resolução ou Solving Time]]
- [[Sites informações adicionais]]
- [[Exportando]]
- [[Monitoramento Remoto]]
