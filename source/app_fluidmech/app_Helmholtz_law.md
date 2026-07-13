(app_Helmholtz_law)=
# Helmholtz's law

```{admonition} Referred from 
{ref}`auton_lift`
```

```{admonition} References
{cite:t}`Aris1990`: Highly recommended to those who want to learn vector/tensor calculus in fluid mechanics. 
```

Let us derive Helmholtz's law of vortex motion. The rate of change in $\boldsymbol{\omega}/\rho$ is expressed as 
```{math}
:label: eq:Auton_eq_rate-of-change-in-omega-by-rho
	\frac{D}{Dt} \frac{\boldsymbol{\omega}}{\rho} 
	= \frac{1}{\rho} \frac{D \boldsymbol{\omega}}{Dt} - \frac{\boldsymbol{\omega}}{\rho^{2}} \frac{D \rho}{Dt}
	= \frac{1}{\rho} \left( - \boldsymbol{\omega} ( \nabla \cdot \mathbf{v} ) + \boldsymbol{\omega} \cdot \nabla \mathbf{v} \right) + \frac{\boldsymbol{\omega}}{\rho} \nabla \cdot \mathbf{v}
	= \frac{\boldsymbol{\omega} }{\rho} \cdot \nabla \mathbf{v}
```
Let $\mathbf{X}$ be the initial coordinates of each fluid particle in the system. Therefore, 
```{math}
:label: eq:app_HelmholtzLaw_nonref_0
\begin{split}
	&\mathbf{x} = \mathbf{x} ( \mathbf{X}, t ) \\
	&\mathbf{X} = \mathbf{X} ( \mathbf{x}, t )
\end{split}
```
The coordinates $\mathbf{x}$ and $\mathbf{X}$ are referred to as the space and material coordinates, respectively. The space coordinate $\mathbf{x}(\mathbf{X}, t)$ is the trajectory of the fluid particle $\mathbf{X}$, and indeed
```{math}
:label: eq:app_HelmholtzLaw_nonref_1
	\frac{D \mathbf{x}}{Dt} = \mathbf{v}
```
The difference between $\mathbf{x}$ of a fluid particle and its neighbor at distance $d \mathbf{X}$ is written by 
```{math}
:label: eq:app_HelmholtzLaw_nonref_2
	d\mathbf{x} = \mathbf{x}( \mathbf{X} + d\mathbf{X}, t ) - \mathbf{x}( \mathbf{X}, t ) \rightarrow \frac{\partial x_{i}}{\partial X_{j}} dx_{j}
```
Let us assume a solution having the following functional form:
```{math}
:label: eq:app_HelmholtzLaw_nonref_3
	\omega_{i} = \rho c_{j} \frac{\partial x_{i}}{\partial X_{j}}
```
Using this, we observe  
```{math}
:label: eq:app_HelmholtzLaw_nonref_4
	\frac{D}{Dt} \frac{\omega_{i}}{\rho} 
	= \frac{D}{Dt} \left( c_{j} \frac{\partial x_{i}}{\partial X_{j}} \right)
	= \frac{D c_{j}}{Dt} \frac{\partial x_{i}}{\partial X_{j}} + c_{j}\frac{\partial v_{i}}{\partial X_{j}}
```
```{math}
:label: eq:app_HelmholtzLaw_nonref_5
	\frac{ \omega_{j} }{\rho} \frac{\partial v_{i}}{\partial x_{j}}
	= c_{k} \frac{\partial x_{j}}{\partial X_{k}} \frac{\partial v_{i}}{\partial x_{j}}
	= c_{k} \frac{\partial v_{i}}{\partial X_{k}}
```
According to Eq. {eq}`eq:Auton_eq_rate-of-change-in-omega-by-rho`, 
```{math}
:label: eq:app_HelmholtzLaw_nonref_6
	\frac{D c_{j}}{Dt} \frac{\partial x_{i}}{\partial X_{j}} = 0
```
However, $| \partial x_{i} / \partial X_{j} |$ is non-zero, we have 
```{math}
:label: eq:app_HelmholtzLaw_nonref_7
	\frac{D c_{j}}{Dt} = 0~~~~\text{and}~~~~\mathbf{c} = \mathbf{c} ( \mathbf{X} )
```
Thus, $\mathbf{c}$ depends only on the initial condition. By writing the initial vorticity $\boldsymbol{\omega}_{0}$ as 
```{math}
:label: eq:app_HelmholtzLaw_nonref_8
	\omega_{i}^{0} = \rho_{0} c_{j} \frac{\partial X_{i}}{\partial X_{j}} = \rho_{0} c_{j} \delta_{ij} = \rho_{0} c_{i}
	\rightarrow \mathbf{c} = \frac{\boldsymbol{\omega}_{0}}{\rho_{0}}
```
Thus, 
```{math}
:label: eq:app_HelmholtzLaw_nonref_9
	\frac{\omega_{i}}{\rho} = \frac{\omega_{j}^{0}}{\rho_{0}} \frac{\partial x_{i}}{\partial X_{j}}
```
According to this result, if the vorticity of a fluid particle is initially non-zero, that particle will have non-zero vorticity at the later time. Or, if the initial vorticity is zero, the particle will never have non-zero vorticity. This is a part of Helmholtz's law of vortex motion. For incompressible fluids,
```{math}
:label: eq:Auton_eq_Lagrange-vortex-theorem
	\omega_{i} = \omega_{j}^{0} \frac{\partial x_{i}}{\partial X_{j}}
```

Then, we consider a material line along a vortex line at the initial moment. Let $\omega_{0}$ be the magnitude of $\boldsymbol{\omega}_{0}$. We can choose a parameter $\epsilon$ so as to 
```{math}
:label: eq:app_HelmholtzLaw_nonref_10
	dX_{i} = \epsilon \frac{\omega_{i}^{0}}{\rho_{0}} 
```
where $d\mathbf{X} \parallel \boldsymbol{\omega}_{0}$. At a later time, 
```{math}
:label: eq:app_HelmholtzLaw_nonref_11
	dx_{i}= \frac{\partial x_{i}}{\partial X_{j}} dX_{j}
```
However, the initial displacement $d\mathbf{X}$ can be expressed using the initial vorticity: 
```{math}
:label: eq:app_HelmholtzLaw_nonref_12
	dx_{i}
	= \epsilon \frac{\partial x_{i}}{\partial X_{j}} \frac{\omega_{j}^{0}}{\rho_{0}} 
	= \epsilon \frac{\omega_{i}}{\rho} 
```
This results shows that $d\mathbf{x} \parallel \boldsymbol{\omega}$, in other words, the vortex line moves with the material line. The lengths, $ds$ and $ds_{0}$, for $d\mathbf{x}$ and $d\mathbf{X}$, respectively, are
```{math}
:label: eq:app_HelmholtzLaw_nonref_13
\begin{split}
	&ds^{2} = dx_{i} dx_{i} = \epsilon^{2} \frac{\omega^{2}}{\rho^{2}}  \\
	&ds_{0}^{2} = dX_{i} dX_{i} = \epsilon^{2} \frac{\omega_{0}^{2}}{\rho_{0}^{2}}  
\end{split}
```
where $\omega = \omega_{i} \omega_{i}$ and $\omega_{0} = \omega_{i}^{0} \omega_{i}^{0}$. From these expressions we have 
```{math}
:label: eq:Auton_eq_dsds0
	\frac{ds^{2}}{ds_{0}^{2}} = \frac{\rho_{0}^{2} \omega^{2}}{\rho^{2} \omega_{0}^{2}}  \\
```
According to the continuity equation, 
```{math}
:label: eq:Auton_eq_continuity-along-vortex-line
	\rho \sigma ds = \rho_{0} \sigma_{0} ds_{0}
```
where $\sigma$ is the cross-sectional area occupied by the vortex line. Combining Eqs. {eq}`eq:Auton_eq_dsds0` and {eq}`eq:Auton_eq_continuity-along-vortex-line` gives 
```{math}
:label: eq:app_HelmholtzLaw_nonref_14
	\omega \sigma = \omega_{0} \sigma_{0} 
```
This provides the last one of Helmholtz's law, that is, the strength of the vortex line is constant. 
