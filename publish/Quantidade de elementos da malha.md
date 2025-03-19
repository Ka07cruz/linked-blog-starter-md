- A geometria da malha pode ser feita no Space Claim ou no Design Modeler. Para minha malha usei Space e depois importei para Modeler para criar seção na geometria.
	- [https://www.youtube.com/watch?v=AHVxgndCMZE](https://www.youtube.com/watch?v=AHVxgndCMZE)

Obs.: O video mostra como faz a seção

- A divisão é feita para fazer malha triangular na região de encontro dos fluidos, pois precisa de mais precisão
    
- Para cada parte da geometria faz um Multizone e Inflation
    
- Multizone
    
    - Method - Multizone Quad/Tri
    - Surface Mesh Method - Pave
    - Free Face Mesh Type - All Tri (para região triangular) e All Quad (para região retangular)
    - Obs.: Coloquei o Size igual para ambos os lados
    
    ![[mesh.png]]
        
### Verificar Elementos da Malha
    
- Seleciona malha inteira > selection informantion > elements
    
    Ou
- Mesh > Statistics > Elements
    - [https://doc.comsol.com/5.5/doc/com.comsol.help.comsol/comsol_ref_mesh.15.15.html](https://doc.comsol.com/5.5/doc/com.comsol.help.comsol/comsol_ref_mesh.15.15.html)
    
	 Obs.: Multizone para mesh