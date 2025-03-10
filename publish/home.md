---
title: Two Phase Flow
excerpt: Create your own template or use someone else's. Changing the template is a matter of updating one line
---
Escoamento bifásico (Two Phase Flow) é o movimento simultâneo de duas fases distintas (líquido-líquido, líquido-gás, sólido-líquido ou sólido-gás) dentro de um meio, como em tubulações ou canais. Esse tipo de escoamento é comum em indústrias como petróleo, química e energia, onde pode envolver misturas como água e vapor, óleo e gás, ou partículas suspensas em líquidos. A interação entre as fases influencia características como pressão, velocidade e padrões de fluxo, tornando sua análise complexa e essencial para projetos e operações eficientes. 

## Sites para Iniciar a Pesquisa
Para facilitar as pesquisas acadêmicas, foram selecionados e organizados diversos sites e repositórios que disponibilizam artigos científicos e trabalhos de conclusão de curso (TCC).
- [[Sites para Pesquisar]]

## Modelos Numéricos 
Esses são modelos numéricos utilizados na dinâmica dos fluidos computacional (CFD) para simular escoamentos complexos, especialmente em cenários com múltiplas fases e turbulência.
- [[Modelo Euleriano]]
- [[Modelo VOF]]
- [[Modelo de turbulência K-omega SST]]
- [[Modelo de tensão superficial]]
- [[Modelos de Turbulência e Método de especificação de turbulência]]
## Sobre Malha 
A malha em CFD (Computational Fluid Dynamics) é a discretização do domínio de estudo em pequenas células, onde as equações de escoamento são resolvidas numericamente. Ela pode ser estruturada (grade regular), não estruturada (elementos irregulares) ou híbrida, influenciando diretamente a precisão e o custo computacional da simulação. Um refinamento adequado da malha em regiões de alto gradiente, como bordas e interfaces, melhora a captura dos fenômenos físicos sem gerar um excesso de elementos que aumente o tempo de processamento.

Em CFD, a malha deve ter uma quantidade de elementos suficiente para capturar corretamente os fenômenos do escoamento, equilibrando precisão e custo computacional. O refinamento deve ser maior em regiões de alto gradiente, como fronteiras sólidas e interfaces de fases. O parâmetro adimensional **Y+** é crucial para definir a resolução da malha próxima às paredes, influenciando a escolha dos modelos de turbulência. Para resolver completamente a camada limite, a malha deve garantir **Y+ ≈ 1**, enquanto valores entre **30 e 300** permitem o uso de funções de parede, reduzindo a necessidade de refinamento excessivo.
### Como saber a quantidade elemento de malha ?
- [[Quantidade de elementos da malha]]
### Parâmetro adimensional Y+
- [[Y+]]

## Critério 
- [[Critério de Estabilidade]]

## Problemas Comuns
- [[Como resolver erro de ponto flutuante]]
- [[Velocidade Magnitude]]

## Casos Simulados
- [[Tubo Horizontal]] 

## Adicionais
- [[Sites informações adicionais ]]