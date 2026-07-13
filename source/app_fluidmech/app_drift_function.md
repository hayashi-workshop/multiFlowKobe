(app_drift_function)=
# Vorticity in terms of drift function

```{admonition} Referred from 
{ref}`auton_lift`
```

```{admonition} Reference
{cite:t}`Lighthill1956-ov` (the result in {cite:t}`Darwin1953-vk` is used in derivation.)
```

Lighthill considered a fixed sphere subjected to a weak shear flow: 
```{math}
:label: eq:app_DriftFunction_nonref_0
	\mathbf{v} = (v_{x}, v_{y}, v_{z}) = (u_{0} + A y, 0, 0)~~~\text{as}~x \rightarrow -\infty
```
where $A$ is the shear rate of the shear flow and is a positive constant. The upstream vorticity field for this flow is given by 
```{math}
:label: eq:app_DriftFunction_nonref_1
	\boldsymbol{\omega} = (\omega_{x}, \omega_{y}, \omega_{z}) = (0, 0, -A)~~~\text{as}~x \rightarrow -\infty
```
The perturbation is assumed to be weak, i.e., $aA/u_{0} \ll 1$, so that only the change in vorticity by the primary flow should be considered as discussed in Eq. {eq}`eq:Auton_eq_vorticity-eq-linearlized`. The primary flow is expressed by the stream function in Eq. {eq}`eq:Auton_eq_psi-primary`. The streamlines can also be written in the following form:
```{math}
:label: eq:app_DriftFunction_nonref_2
	y = y(x, y_{0}, z_{0}),~~~~z = z(x, y_{0}, z_{0})
```
where 
```{math}
:label: eq:app_DriftFunction_nonref_3
	y_{0} = \lim_{x \rightarrow \infty} (y),~~~~z_{0} = \lim_{x \rightarrow \infty} (z)
```
Since the flow is steady, a streamline given for $(y_{0}, z_{0})$ can be considered as the particle path of a fluid particle initially at $(- \infty, y_{0}, z_{0})$. The additional variable $t$, the so-called \textit{drift function}, is then introduced: 
```{math}
:label: eq:app_DriftFunction_nonref_4
	t = t(x, y_{0}, z_{0})
	= \frac{x}{u_{0}} + \int_{-\infty}^{x} \left\{ \frac{1}{V_{x}(x, y_{0}, z_{0})} - \frac{1}{u_{0}} \right\} dx
```
for this 
```{math}
:label: eq:app_DriftFunction_nonref_5
	t - \frac{x}{u_{0}} \rightarrow 0~~~~\text{as}~x \rightarrow - \infty
```
A surface of $t = \text{const.}$ far upstream of the sphere consists a material plane perpendicular to the $x$ axis. As approaching the sphere from far upstream, fluid particles around the $x$ axis become slower than those far from the sphere, resulting in deformation of the material surfaces of $t = \text{const.}$. See Darwin (1953) for more detail about \text{drift}. 

As we saw in Eq. {eq}`eq:Auton_eq_Lagrange-vortex-theorem`, the vorticity is changed by stretching of associated fluid element. The stretching of fluid element can be expressed in terms of the change in the distance between two neighbors having same $t$. Let us take a fluid element joining $(y_{0}, z_{0})$ and $(y_{0}, z_{0} + \delta z_{0})$ in the far upstream and denote the displacement between these fluid particles at later time as $\delta \mathbf{r}~(= \delta x, \delta y, \delta z)$. The fluid element is stretched with the factor of $|\delta \mathbf{r}| / \delta z_{0}$ and the vorticity lies along the new position of the fluid element, so that the vorticity is give by 
```{math}
:label: eq:app_DriftFunction_nonref_6
	\boldsymbol{\omega} 
	= \left( \omega_{x}, \omega_{y}, \omega_{z} \right)
	= \left( -A \left( \frac{\partial x}{\partial z_{0}} \right)_{t, y_{0}}, -A \left( \frac{\partial y}{\partial z_{0}} \right)_{t, y_{0}}, -A \left( \frac{\partial z}{\partial z_{0}} \right)_{t, y_{0}} \right)
```
By $t = t(x, y_{0}, z_{0})$, 
```{math}
:label: eq:app_DriftFunction_nonref_7
	dt = 
	\left( \frac{\partial t}{\partial x} \right)_{y_{0}, z_{0}} dx
	+ \left( \frac{\partial t}{\partial y_{0}} \right)_{x, z_{0}} dy_{0} 
	+ \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} dz_{0}
```
Setting $dt = dy_{0} = 0$, we have 
```{math}
:label: eq:app_DriftFunction_nonref_8
	0 = 
	\left( \frac{\partial t}{\partial x} \right)_{y_{0}, z_{0}} \left( \frac{\partial x}{\partial z_{0}} \right)_{t, y_{0}}
	+ \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} 
```
then 
```{math}
:label: eq:app_DriftFunction_nonref_9
	\left( \frac{\partial x}{\partial z_{0}} \right)_{t, y_{0}}
	= - \frac{ \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} }{ \left( \frac{\partial t}{\partial x} \right)_{y_{0}, z_{0}} }
	= - \left( \frac{\partial x}{\partial t} \right)_{y_{0}, z_{0}} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}}
	= - V_{x} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}}
```
where 
```{math}
:label: eq:app_DriftFunction_nonref_10
	\left( \frac{\partial x}{\partial t} \right)_{y_{0}, z_{0}} = V_{x}
```
was used; the temporal change in the $x$ position of a fluid particle specified by $(y_{0}, z_{0})$ is its velocity component in the $x$ direction. For the differentiation $dy$, 
```{math}
:label: eq:app_DriftFunction_nonref_11
	dy = 
	\left( \frac{\partial y}{\partial x} \right)_{y_{0}, z_{0}} dx
	+ \left( \frac{\partial y}{\partial y_{0}} \right)_{x, z_{0}} dy_{0} 
	+ \left( \frac{\partial y}{\partial z_{0}} \right)_{x, y_{0}} dz_{0}
```
Setting $dt = dy_{0} = 0$ gives 
```{math}
:label: eq:app_DriftFunction_nonref_12
\begin{split}	
	\left( \frac{\partial y}{\partial z_{0}} \right)_{t, y_{0}} 
	&= \left( \frac{\partial y}{\partial x} \right)_{y_{0}, z_{0}} \left( \frac{\partial x}{\partial z_{0}} \right)_{t, y_{0}} + \left( \frac{\partial y}{\partial z_{0}} \right)_{x, y_{0}} 
	= \frac{ \left( \frac{\partial y}{\partial t} \right)_{y_{0}, z_{0}} }{ \left( \frac{\partial x}{\partial t} \right)_{y_{0}, z_{0}} } \left( - V_{x} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} \right) + \left( \frac{\partial y}{\partial z_{0}} \right)_{x, y_{0}} \\
	&= - \frac{V_{y}}{V_{x}} V_{x} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} + \left( \frac{\partial y}{\partial z_{0}} \right)_{x, y_{0}} \\
	&= - V_{y} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} + \left( \frac{\partial y}{\partial z_{0}} \right)_{x, y_{0}} 
\end{split}
```
Being similar to $dy$, for $dz$ we obtain
```{toggle}
The differentiation $dz$ is written as 


$dz = 
	\left( \frac{\partial z}{\partial x} \right)_{y_{0}, z_{0}} dx
	+ \left( \frac{\partial z}{\partial y_{0}} \right)_{x, z_{0}} dy_{0} 
	+ \left( \frac{\partial z}{\partial z_{0}} \right)_{x, y_{0}} dz_{0}$

Setting $dt = dy_{0}$ yields 

$\begin{split}	
	\left( \frac{\partial z}{\partial z_{0}} \right)_{t, y_{0}} 
	&= \left( \frac{\partial z}{\partial x} \right)_{y_{0}, z_{0}} \left( \frac{\partial x}{\partial z_{0}} \right)_{t, y_{0}} + \left( \frac{\partial z}{\partial z_{0}} \right)_{x, y_{0}} 
	= \frac{ \left( \frac{\partial z}{\partial t} \right)_{y_{0}, z_{0}} }{ \left( \frac{\partial x}{\partial t} \right)_{y_{0}, z_{0}} } \left( - V_{x} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} \right) + \left( \frac{\partial z}{\partial z_{0}} \right)_{x, y_{0}} \\
	&= - \frac{V_{z}}{V_{x}} V_{x} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} + \left( \frac{\partial z}{\partial z_{0}} \right)_{x, y_{0}} = - V_{z} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} + \left( \frac{\partial z}{\partial z_{0}} \right)_{x, y_{0}} 
\end{split}$
```

```{math}
:label: eq:app_DriftFunction_nonref_15
	\left( \frac{\partial y}{\partial z_{0}} \right)_{t, y_{0}} 
	= - V_{z} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} + \left( \frac{\partial z}{\partial z_{0}} \right)_{x, y_{0}} 
```
The vorticity components are thus give by the drift function as 
```{math}
:label: eq:app_DriftFunction_nonref_16
	(\omega_{x}, \omega_{y}, \omega_{z}) 
	= 
	\left( 
	A V_{x} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}},
	A V_{y} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} - A \left( \frac{\partial y}{\partial z_{0}} \right)_{x, y_{0}},
	A V_{z} \left( \frac{\partial t}{\partial z_{0}} \right)_{x, y_{0}} - A \left( \frac{\partial z}{\partial z_{0}} \right)_{x, y_{0}} 
	\right)
```

Far downstream of the sphere ($x \rightarrow \infty$), the velocity components of the primary flow and the drift function become
```{math}
:label: eq:app_DriftFunction_nonref_17
	V_{x} \rightarrow u_{0},~~~~V_{y} \rightarrow 0,~~~~V_{z} \rightarrow 0,~~~~t - \frac{x}{u_{0}} \rightarrow \frac{X(y, z)}{u_{0}}
```
where $X(x, y)$ is the so-called \textit{total drift}, which explains that the ultimate displacement of a fluid particle relative to fluid particles initially in the same plane, but far from the $x$ axis ({numref}`Auton_drift`).
```{toggle}
The sum of the total drift is known to be the same as the virtual mass: (derived by Darwin, 1953)

$\frac{1}{\rho \frac{4 \pi a^{3}}{3}} \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} \rho X(y, z) dy dz = \frac{1}{2}$
```
In this limit, $\left( \partial y / \partial z_{0} \right)_{x, y_{0}}$ goes to zero, so that $\omega_{y} \rightarrow 0$. Then, $\left( \partial z / \partial z_{0} \right)_{x, y_{0}} \rightarrow 1$, giving $\omega_{z} \rightarrow -A$. These results show that $\omega_{y}$ and $\omega_{z}$ recovers the far upstream values. On the other hand, $\omega_{x}$ becomes non-zero even in far downstream, that is, the new component is 
```{math}
:label: eq:app_DriftFunction_nonref_19
	\omega_{x} \rightarrow A \frac{\partial X}{\partial z}
```
This can be observed in {numref}`Auton_Auton-vortex-line`. 

```{figure} ../python/drift.png
:name: Auton_drift
Total drift $X(0,z)$. For a sphere moving steadily in stagnant fluid, fluid particles are taken away from their initial positions by the motion of the sphere.
```

```{figure} ../fig/Auton-ring-vorticity.png
:name: Auton_Auton-ring-vorticity
Ring vorticity $\omega_{\varphi}$ always lie on the $\varphi$ coordinate.
```

Lighthill also showed the vorticity components in the polar systems. With the cylindrical coordinates $(\hat{\rho}, \varphi, x)$
```{math}
:label: eq:app_DriftFunction_nonref_20
	y = \hat{\rho} \cos \varphi,~~~~z = \hat{\rho} \sin \varphi
```
The initial vorticity of the oncoming shear flow is 
```{math}
:label: eq:Auton_eq_initial-vorticity-in-cylinderical-coordinates
	\left( \omega_{x}, \omega_{\hat{\rho}}, \omega_{\varphi} \right)
	= \left( 0, - A \sin \varphi, - A \cos \varphi \right)~~~~\text{as}~x \rightarrow -\infty
```
Considering axial symmetry of the primary flow, a fluid element along the $\varphi$ coordinate line does not change its angle $\delta \varphi$, so that the stretching of the fluid element is simply expressed as $\hat{\rho} \delta \varphi / \hat{\rho}_{0} \delta \varphi = \hat{\rho} / \hat{\rho}_{0}$ ({numref}`Auton_Auton-ring-vorticity`). Therefore, 
```{math}
:label: eq:app_DriftFunction_nonref_21
	\omega_{\varphi} = (-A \cos \varphi) \frac{\hat{\rho}}{\hat{\rho}_{0}}
```
With the spherical polar coordinates
```{math}
:label: eq:app_DriftFunction_nonref_22
	x = r \cos \theta,~~~~\hat{\rho} = r \sin \theta
```
we have 
```{math}
:label: eq:app_DriftFunction_nonref_23
	\omega_{\varphi} = -A \cos \varphi \frac{r \sin \theta}{\hat{\rho}_{0}}
```
Then, we consider a fluid element joining streamlines $(\hat{\rho}_{0}, \varphi)$ and $(\hat{\rho}_{0} + \delta \hat{\rho}_{0}, \varphi)$. The $\hat{\rho}$ component of the initial vorticity is given in Eq. {eq}`eq:Auton_eq_initial-vorticity-in-cylinderical-coordinates`, i.e., $-A \sin \varphi$. The fluid element, whose length is initially $\delta \hat{\rho}_{0}$, may become $\delta r \mathbf{e}_{r} + r \delta \theta \mathbf{e}_{\theta}$ in the plane of constant $\varphi$. The vorticity associated with $\delta \hat{\rho}$ is therefore 
```{math}
:label: eq:eq_vorticity_54
	\omega_{r} = (-A \sin \varphi) \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t, \varphi},~~~~\omega_{\theta} = (-A \sin \varphi) \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
```
after experiencing stretching by the primary flow. The differentiation $dt$ is given by 
```{math}
:label: eq:app_DriftFunction_nonref_24
	dt 
	= \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} d\hat{\rho}_{0}
	+ \left( \frac{\partial t}{\partial r} \right)_{\hat{\rho}_{0}, \varphi} dr
	+ \left( \frac{\partial t}{\partial \varphi} \right)_{r, \hat{\rho}_{0}} d\varphi
```
Setting $dt = d\varphi = 0$ gives 
```{math}
:label: eq:app_DriftFunction_nonref_25
	0 
	= \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} 
	+ \left( \frac{\partial t}{\partial r} \right)_{\hat{\rho}_{0}, \varphi} \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
```
Then, 
```{math}
:label: eq:Auton_eq_drdrho
	\left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
	= - \frac{ \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} }{ \left( \frac{\partial t}{\partial r} \right)_{\hat{\rho}_{0}, \varphi} }
	= - \left( \frac{\partial r}{\partial t} \right)_{\hat{\rho}_{0}, \varphi} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi}
	= - V_{r} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi}
```
Substituting this into the expression of $\omega_{r}$ yields
```{math}
:label: eq:app_DriftFunction_nonref_26
	\omega_{r} = ( A \sin \varphi ) V_{r} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi}
```
For $d\theta$, 
```{math}
:label: eq:app_DriftFunction_nonref_27
	d\theta
	= \left( \frac{\partial \theta}{\partial \hat{\rho}_{0} } \right)_{r, \varphi} d\hat{\rho}_{0}
	+ \left( \frac{\partial \theta}{\partial r } \right)_{\hat{\rho}_{0}, \varphi} dr
	+ \left( \frac{\partial \theta}{\partial \varphi } \right)_{\hat{\rho}_{0}, r} d\varphi
```
We take $dt = d\varphi = 0$ to have 
```{math}
:label: eq:app_DriftFunction_nonref_28
	\left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
	= \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} 
	+ \left( \frac{r \partial \theta}{\partial r} \right)_{\hat{\rho}_{0}, \varphi} \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
	= \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} 
	+ \frac{\left( \frac{r \partial \theta}{\partial t} \right)_{\hat{\rho}_{0}, \varphi}}{\left( \frac{\partial r}{\partial t} \right)_{\hat{\rho}_{0}, \varphi} } \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
	= \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} 
	+ \frac{V_{\theta}}{V_{r}} \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
```
By Eq. {eq}`eq:Auton_eq_drdrho`, the second term in the last equation is however 
```{math}
:label: eq:app_DriftFunction_nonref_29
	\frac{V_{\theta}}{V_{r}} \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t, \varphi}
	= - V_{\theta} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi}
```
Therefore, 
```{math}
:label: eq:eq_omega_theta_54
	\omega_{\theta} = (A \sin \varphi) \left( V_{\theta} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} - \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{r, \varphi} \right)
```
If the drift function is expressed by $t(\hat{\rho}_{0}, \theta)$, 
```{math}
:label: eq:eq_dt_rho_theta
	dt = \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta} d\hat{\rho}_{0} + \left( \frac{\partial t}{r \partial \theta} \right)_{\hat{\rho}_{0}} r d\theta
```
Note that $\varphi$ is omitted in the calculation for simplicity. Setting $dt = 0$ yields
```{math}
:label: eq:app_DriftFunction_nonref_30
	\left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{t} 
	= - \frac{\left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta}}{\left( \frac{\partial t}{r \partial \theta} \right)_{\hat{\rho}_{0}}}
	= - V_{\theta} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta}
```
Substituting this result into Eq. {eq}`eq:eq_vorticity_54` yields
```{math}
:label: eq:app_DriftFunction_nonref_31
	\omega_{\theta} = (A \sin \varphi) V_{\theta} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta, \varphi}
```
For $dr$, we have
```{math}
:label: eq:app_DriftFunction_nonref_32
	dr = \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{\theta} d\hat{\rho}_{0} + \left( \frac{\partial r}{r \partial \theta} \right)_{\hat{\rho}_{0}} r d\theta
```
Setting $dt = 0$, 
```{math}
:label: eq:app_DriftFunction_nonref_33
	\left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t} 
	= \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{\theta} + \left( \frac{\partial r}{r \partial \theta} \right)_{\hat{\rho}_{0}} \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{t}
	= \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{\theta} + V_{r} \left( \frac{\partial t}{r \partial \theta} \right)_{\hat{\rho}_{0}} \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{t}
```
However, from Eq. {eq}`eq:eq_dt_rho_theta`, 
```{math}
:label: eq:app_DriftFunction_nonref_34
	\left( \frac{\partial t}{r \partial \theta} \right)_{\hat{\rho}_{0}} \left( \frac{r \partial \theta}{\partial \hat{\rho}_{0}} \right)_{t}
	= - \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta} 
```
Therefore, 
```{math}
:label: eq:app_DriftFunction_nonref_35
	\left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{t} 
	= \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{\theta} - V_{r} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta} 
```
Substituting this into Eq. {eq}`eq:eq_vorticity_54` gives 
```{math}
:label: eq:app_DriftFunction_nonref_36
	\omega_{r} = (A \sin \varphi) \left( V_{r} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta, \varphi} - \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{\theta, \varphi} \right) 
```
The vorticity components used in the Auton's analysis (Eq. {eq}`eq:Auton_eq_vorticity_p`) have thus been obtained. 
