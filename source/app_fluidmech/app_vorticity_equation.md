(app_vorticity_equation)=
# Vorticity equation

```{admonition} Referred from 
{ref}`auton_lift`
```

The equation of motion for incompressible inviscid flow is given by 
```{math}
:label: eq:Auton_eq_equation-of-motion-inviscid-without-f
	\frac{\partial \mathbf{v}}{\partial t} +  \mathbf{v} \cdot \nabla \mathbf{v} = - \frac{\nabla p}{\rho} 
```
The advection term can be expressed in terms of the kinetic energy and the vortex force, i.e.
```{toggle}
$\boldsymbol{\omega} \times \mathbf{v}
	\rightarrow$
$\epsilon_{ijk} \omega_{j} v_{k}
	= \epsilon_{ijk} \epsilon_{jmn} \frac{\partial v_{n}}{\partial x_{m}} v_{k}
	= ( \delta_{km} \delta_{in} - \delta_{kn} \delta_{im} )
	\frac{\partial v_{n}}{\partial x_{m}} v_{k}
	= \frac{\partial v_{i}}{\partial x_{k}} v_{k} - \frac{\partial v_{k}}{\partial x_{i}} v_{k}
	= \frac{\partial v_{i}}{\partial x_{k}} v_{k} - \frac{\partial}{\partial x_{i}} \left( \frac{v^{2}}{2} \right)
	$
$\rightarrow \mathbf{v} \cdot \nabla \mathbf{v} - \nabla \frac{v^{2}}{2}$
```

```{math}
:label: eq:app_vorticity_equation_nonref_1
	\frac{\partial \mathbf{v}}{\partial t} 
	+ \boldsymbol{\omega} \times \mathbf{v} = - \frac{1}{\rho} \nabla \left( p + \frac{\rho v^{2}}{2} \right)
```
where $\boldsymbol{\omega}$ is the vorticity defined by 
```{math}
:label: eq:app_vorticity_equation_nonref_2
	\boldsymbol{\omega} = \nabla \times \mathbf{v}
```
By taking $rot$ of this equation and using the identity 
```{math}
:label: eq:app_vorticity_equation_nonref_3
	\nabla \times \nabla ( \text{any scalar} ) = 0
```
we have 
```{math}
:label: eq:app_vorticity_equation_nonref_4
	\frac{\partial \boldsymbol{\omega}}{\partial t} 
	+ \nabla \times \boldsymbol{\omega} \times \mathbf{v} = 0
```
The second term can be decomposed into four terms as demonstrated below: 
```{math}
:label: eq:app_vorticity_equation_nonref_5
\begin{split}	
	&\nabla \times \boldsymbol{\omega} \times \mathbf{v} 
	\rightarrow \epsilon_{ijk} \frac{\partial }{\partial x_{j}} \left( \epsilon_{kmn} \omega_{m} v_{n} \right)
	= ( \delta_{im} \delta_{jn} - \delta_{in} \delta_{jm} ) \frac{\partial \omega_{m} v_{n}}{\partial x_{j}} 
	= \frac{\partial \omega_{i} v_{j}}{\partial x_{j}} - \frac{\partial \omega_{j} v_{i}}{\partial x_{j}} \\
	&= \omega_{i} \frac{\partial v_{j}}{\partial x_{j}} + \frac{\partial \omega_{i}}{\partial x_{j}} v_{j} - \omega_{j} \frac{\partial v_{i}}{\partial x_{j}} - \frac{\partial \omega_{j}}{\partial x_{j}} v_{i}
	\rightarrow \boldsymbol{\omega} ( \nabla \cdot \mathbf{v} ) + \mathbf{v} \cdot \nabla \boldsymbol{\omega} - \boldsymbol{\omega} \cdot \nabla \mathbf{v} - ( \nabla \cdot \boldsymbol{\omega} ) \mathbf{v}
\end{split}
```
The first term in the last equation vanishes due to the incompressibility. In addition, according to the identity 
```{math}
:label: eq:app_vorticity_equation_nonref_6
	\nabla \cdot \nabla \times ( \text{any vector} ) = 0
```
the fourth term also vanishes. Therefore, the vorticity equation becomes 
```{math}
:label: eq:app_vorticity_equation_nonref_7
	\frac{\partial \boldsymbol{\omega}}{\partial t} + \mathbf{v} \cdot \nabla \boldsymbol{\omega} = \boldsymbol{\omega} \cdot \nabla \mathbf{v} 
```
or 
```{math}
:label: eq:app_vorticity_equation_nonref_8
	\frac{D \boldsymbol{\omega}}{D t} = \boldsymbol{\omega} \cdot \nabla \mathbf{v} 
```
The R.H.S. term represents the vorticity change due to stretching of vortex line. 

The relative motion between the fluid particles specified by $\mathbf{s}$ and $\mathbf{s} + d\mathbf{s}$ is given by 
```{math}
:label: eq:app_vorticity_equation_nonref_9
	d\mathbf{v} = \mathbf{v} (\mathbf{s} + d\mathbf{s}) - \mathbf{v} (\mathbf{s})
```
Applying Taylor series expansion to the first term yields 
```{math}
:label: eq:app_vorticity_equation_nonref_10
	dv_{i} = \frac{\partial v_{i}}{\partial x_{j}} ds_{j}
```
where terms higher than the first order were neglected. The velocity gradient tensor $\nabla \mathbf{v}$ can be decomposed into the rate-of-strain tensor and the rate-of-rotation tensor as 
```{math}
:label: eq:app_vorticity_equation_nonref_11
	\frac{\partial v_{i}}{\partial x_{j}} = e_{ij} + g_{ij}
```
where 
```{math}
:label: eq:app_vorticity_equation_nonref_12
	e_{ij} = \frac{1}{2} \left( \frac{\partial v_{i}}{\partial x_{j}} + \frac{\partial v_{j}}{\partial x_{i}} \right)
```
```{math}
:label: eq:app_vorticity_equation_nonref_13
	g_{ij} = \frac{1}{2} \left( \frac{\partial v_{i}}{\partial x_{j}} - \frac{\partial v_{j}}{\partial x_{i}} \right)
```
These are the symmetric and asymmetric part of the velocity gradient tensor. With them, 
```{math}
:label: eq:app_vorticity_equation_nonref_14
	dv_{i} = e_{ij} ds_{j} + g_{ij} ds_{j}
```
where the first term represents pure deformation. On the other hand, the second term represents rotational motion of fluid particle as follows. The rate of rotation tensor can be expressed as 
```{math}
:label: eq:app_vorticity_equation_nonref_15
	g_{ij} = - \frac{1}{2} \epsilon_{ijk} \omega_{k}
```
The asymmetric part of the relative motion is therefore
```{math}
:label: eq:app_vorticity_equation_nonref_16
	dv_{i}^{(a)} = - \frac{1}{2} \epsilon_{ijk} \omega_{k} ds_{j}
```
Exchanging the suffixes $j$ and $k$ of the permutation symbol gives 
```{math}
:label: eq:app_vorticity_equation_nonref_17
	dv_{i}^{(a)} = \frac{1}{2} \epsilon_{ikj} \omega_{k} ds_{j}
```
In the vectorial form, 
```{math}
:label: eq:app_vorticity_equation_nonref_18
	d\mathbf{v}^{(a)} = \frac{1}{2} \boldsymbol{\omega} \times d\mathbf{s}
```
This equation shows the rotating motion about the axis given by $\boldsymbol{\omega}$ and the angular velocity is $\boldsymbol{\omega}/2$. 
