O Modelo **SST k-omega (Shear Stress Transport)** é um modelo de turbulência comumente utilizado por capturar a transição suave entre 

o modelo k-omega padrão perto da parede e k-epsilon longe dela, assim unindo o melhor de ambas as famílias Reynolds-averaged Navier Stokes RANS.

O modelo de viscosidade turbulenta possui duas equações k e omega, sendo k a equação da energia cinética e omega a taxa de dissipação

**Equação da energia cinética de turbulência (k)**
![[k.png]]
Equação para Latex:
````
\frac{D \rho k}{Dt} = \tau_{ij} \frac{\partial u_i}{\partial x_j} - \beta^* \rho \omega k + \frac{\partial}{\partial x_j}
[(\mu + \alpha_k \mu_t)\frac{\partial k}{\partial x_j}]
````

**Equação da taxa de dissipação específica da turbulência (w)**
![[w.png]]

Equação para Latex:
````
\frac{D \rho \omega}{Dt} = \frac{\gamma \rho}{\mu t}\tau_{ij} \frac{\partial u_i}{\partial x_j} - \beta \rho \omega ^2 + 
\frac{\partial}{\partial x_j} [(\mu + \alpha _\omega \mu_t)\frac{\partial \omega}{\partial x_j}] + 
2(1 - F_1)\frac{\rho \alpha _{\omega^2}}{\omega} \frac{\partial k}{\partial x_j} \frac{\partial \omega}{\partial x_j}
````
### Referencias

CFD SIMULATION OF TWO-PHASE VERTICAL FLOW WITH DIFFERENT TYPES OF INJECTION

[https://www.simscale.com/docs/simulation-setup/global-settings/k-omega-sst/](https://www.simscale.com/docs/simulation-setup/global-settings/k-omega-sst/)

[https://www.cfd-online.com/Wiki/SST_k-omega_model](https://www.cfd-online.com/Wiki/SST_k-omega_model)