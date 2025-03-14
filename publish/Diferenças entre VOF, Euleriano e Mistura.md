Na abordagem Euler-Euler, diferentes fases são tratadas como se fossem fluidos contínuos que se misturam, mas sem ocupar o mesmo espaço ao mesmo tempo. Para isso, usa-se o conceito de fração volumétrica, que indica a proporção de cada fase em um determinado ponto do espaço e do tempo. A soma dessas frações sempre dá 1. As equações de conservação são formuladas para cada fase e possuem uma estrutura parecida. Para resolver essas equações, são adicionadas relações baseadas em dados experimentais ou, no caso de partículas sólidas, na teoria cinética.

No **ANSYS FLUENT**, existem três modelos multifásicos baseados nessa abordagem: **VOF (Volume de Fluido), Mistura e Euleriano**.

### Modelo VOF

O modelo VOF rastreia superfícies de separação entre fluidos imiscíveis, como óleo e água. Ele compartilha um único conjunto de equações de movimento entre os fluidos e acompanha a fração volumétrica de cada um nas células computacionais. Esse modelo é usado em casos como ondas, movimentação de grandes bolhas em líquidos, rompimento de barragens e jatos de fluido.

### Modelo de Mistura

O modelo de mistura é aplicado a sistemas com duas ou mais fases, podendo ser líquidos, gases ou partículas. Ele resolve uma equação geral de movimento e usa velocidades relativas para descrever como as fases se movem entre si. É útil para fluxos com partículas em baixa concentração, borbulhamento, sedimentação e separadores ciclônicos. Se necessário, pode ser usado sem considerar velocidades relativas para modelar um fluxo homogêneo.

### Modelo Euleriano

O modelo Euleriano é o mais complexo e resolve equações de movimento e continuidade para cada fase separadamente. As fases interagem por meio de trocas de pressão e forças de interface, que variam conforme o tipo de mistura. Para misturas sólido-fluido, são usadas equações baseadas na teoria cinética. Esse modelo é aplicado em colunas de bolhas, risers, suspensão de partículas e leitos fluidizados. Além disso, o **ANSYS FLUENT** permite personalizar essas interações com funções definidas pelo usuário.

Essas informações foram tiradas do proprio site da [Anays](https://www.afs.enea.it/project/neptunius/docs/fluent/html/th/node293.htm)
