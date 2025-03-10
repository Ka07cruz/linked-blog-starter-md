$$ C = u_G\frac{\Delta t}{\Delta x} $$

- $C$ - número de Courant (0,25 para esse estudo)
- $u_G$ - velocidade total do gás e é calculada pelo modelo Drift-Flux
- $\Delta t$ - passo de tempo
- $\Delta x$ - comprimento da célula da malha

### Por que o critério CFL é importante?

Imagine que você está tentando simular o fluxo de água em um rio. Se você usar passos de tempo muito grandes, a água pode parecer pular obstáculos ou fluir através de paredes em sua simulação. Isso ocorre porque o esquema numérico não é capaz de capturar com precisão a física do fluxo em grandes passos de tempo.O critério CFL fornece uma diretriz para escolher um passo de tempo que seja suficientemente pequeno para capturar as características importantes do fluxo, mas ainda suficientemente grande para ser computacionalmente eficiente.

### O que acontece se o critério CFL for violado?

Se o critério CFL for violado, a simulação numérica pode se tornar instável e produzir resultados imprecisos ou até mesmo não físicos. No pior caso, a simulação pode travar completamente.

### Fontes

1. [https://www.sciencedirect.com/science/article/abs/pii/S0017931022001466](https://www.sciencedirect.com/science/article/abs/pii/S0017931022001466)
2. [https://www.sciencedirect.com/science/article/abs/pii/S0142727X17307865](https://www.sciencedirect.com/science/article/abs/pii/S0142727X17307865)
3. [https://www.thermopedia.com/content/277/](https://www.thermopedia.com/content/277/)
4. [https://scholars.cityu.edu.hk/files/126839759/120384626.pdf](https://scholars.cityu.edu.hk/files/126839759/120384626.pdf)
5. Applications of Drift-Flux Model in Predicting Two-Phase Flow Parameters in Horizontal and Vertical Pipes
6. Development and Application of Drift-Flux Model for Predicting Pressure Drop in Horizontal Wells
7. Recent Advances in Drift-Flux Model for Modeling Two-Phase Flow in Porous Media
8. Industrial Applications of Two-Phase Flow Modeling Using Drift-Flux Models