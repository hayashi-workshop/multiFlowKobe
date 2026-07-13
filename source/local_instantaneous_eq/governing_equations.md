(governing_equations)=
# Governing equations

We will deal with an incompressible isothermal two-phase system of Newtonian fluids without phase change only. The momentum and continuity equations of each phase are given by 
```{math}
:label: eq:LocalInstantaneousEq_nonref_0
    \frac{\partial \mathbf{v}}{\partial t} + \mathbf{v} \cdot \nabla \mathbf{v} = - \frac{\nabla p}{\rho} + \frac{\nabla \cdot \boldsymbol{\tau}}{\rho} + \mathbf{g} 
```
```{math}
:label: eq:LocalInstantaneousEq_nonref_1
    \frac{1}{\rho} \frac{D \rho}{Dt} + \nabla \cdot \mathbf{v} = 0
```
where $\mathbf{v}$ is the velocity, $t$ is the time, $p$ is the pressure, $\rho$ is the density, $\mathbf{g}$ is the acceleration of gravity, and $\boldsymbol{\tau}$ is the viscous stress tensor given by 
```{math}
:label: eq:LocalInstantaneousEq_nonref_2
    \boldsymbol{\tau} = \mu \left\{ \nabla \mathbf{v} + ( \nabla \mathbf{v} )^{T} \right\}
```
Here, $\mu$ is the viscosity. For fluids with constant density and viscosity, these equations reduce to
```{math}
:label: eq:LocalInstantaneousEq_nonref_3
    \frac{\partial \mathbf{v}}{\partial t} + \mathbf{v} \cdot \nabla \mathbf{v} = - \frac{\nabla p}{\rho} + \nu \nabla^{2} \mathbf{v} + \mathbf{g} 
```
```{math}
:label: eq:LocalInstantaneousEq_nonref_4
    \nabla \cdot \mathbf{v} = 0
```
where $\nu~(=\mu / \rho)$ is the kinematic viscosity. These equations hold in each phase, while we need to account for boundary conditions at the interfaces between the two phases. 

