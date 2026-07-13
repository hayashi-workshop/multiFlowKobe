(drag_vorticity)=
# Drag-vorticity relation

```{admonition} Summary
* **Subject:** Drag in terms of surface vorticity
* **Main conclusion:** Drag coefficient of spherical particle can be expressed in terms of maximum surface vorticity. 
* **Key idea** The vorticity source is only at surface, and therefore the magnitude of drag is scaled by the maximum surface vorticity. 
* **Reference:** 
	- {cite:t}`Legendre2007-nv`
	- {cite:t}`Saffman1995-ic`
```

Let us begin by the following equation of motion for incompressible inviscid flows.
```{math}
:label: eq:Legendre_eq_equation-of-motion-inviscid
	\frac{\partial \mathbf{v}}{\partial t} +  \mathbf{v} \cdot \nabla \mathbf{v} = - \frac{\nabla p}{\rho} + \mathbf{f} 
```
Expanding $\boldsymbol{\omega} \times \mathbf{v}$, we have
```{math}
:label: eq:DragVorticity_nonref_0
\begin{split}
	\boldsymbol{\omega} \times \mathbf{v}
	\rightarrow \epsilon_{ijk} \omega_{j} v_{k}
	&= \epsilon_{ijk} \epsilon_{jmn} \frac{\partial v_{n}}{\partial x_{m}} v_{k}
	= ( \delta_{km} \delta_{in} - \delta_{kn} \delta_{im} )
	\frac{\partial v_{n}}{\partial x_{m}} v_{k}
	= \frac{\partial v_{i}}{\partial x_{k}} v_{k} - \frac{\partial v_{k}}{\partial x_{i}} v_{k} \\
	&= \frac{\partial v_{i}}{\partial x_{k}} v_{k} - \frac{\partial}{\partial x_{i}} \left( \frac{v^{2}}{2} \right)
\end{split}
```
The advection term can therefore be decomposed into two terms as 
```{math}
:label: eq:DragVorticity_nonref_1
	\mathbf{v} \cdot \nabla \mathbf{v} = \nabla \left( \frac{v^{2}}{2} \right) + \boldsymbol{\omega} \times \mathbf{v}
```
Eq. {eq}`eq:Legendre_eq_equation-of-motion-inviscid` becomes 
```{math}
:label: eq:DragVorticity_nonref_2
	\frac{\partial \mathbf{v}}{\partial t} 
	= - \frac{1}{\rho} \nabla \left( p + \frac{\rho v^{2}}{2} \right) + \mathbf{v} \times \boldsymbol{\omega} + \mathbf{f} 
	= - \frac{\nabla p_{T}}{\rho} + \mathbf{v} \times \boldsymbol{\omega} + \mathbf{f} 
```
where $p_{T} = p + \rho v^{2}/2$ is the total pressure. Integrating the equation of motion for the volume $V$ enclosed by $S$ yields
```{math}
:label: eq:DragVorticity_nonref_3
	\frac{\partial }{\partial t} \iiint_{V} \rho \mathbf{v} dV
	= - \iint_{S} p_{T} \mathbf{n} dS + \iiint_{V} \left( \rho \mathbf{v} \times \boldsymbol{\omega} + \rho \mathbf{f} \right) dV
```
When a flow is steady the L.H.S. vanishes. In addition, taking $S$, on which $p_{T}$ is constant, shows that the external force must be balanced with the so-called vortex force $\rho \mathbf{v} \times \boldsymbol{\omega}$ to maintain the steady flow {cite:p}`Saffman1995-ic`. The drag force, $\mathbf{F}$, acting on a body embedded in a incompressible inviscid flow can therefore be given by the total vortex force: 
```{math}
:label: eq:DragVorticity_nonref_4
	\mathbf{F} = \iiint_{V} \rho \mathbf{v} \times \boldsymbol{\omega} dV
```
If a flow is irrotational this relation gives no drag force. The proportionality inspired {cite:t}`Legendre2007-nv` to establish a drag-vorticity relation for a body in a viscous fluid. 

The Stokes drag for a spherical particle is given by 
```{math}
:label: eq:Legendre_eq_Stokes-drag
	F_{D} = 6 \pi \mu u a
```
The velocity components are 
```{math}
:label: eq:DragVorticity_nonref_5
	v_{\theta} = u \sin \theta \left\{ 1 - \frac{a^{3}}{4 r^{3}} - \frac{3 a}{4 r} \right\}
```
```{math}
:label: eq:DragVorticity_nonref_6
	v_{r} = - u \cos \theta \left\{ 1 - \frac{3 a}{2 r} + \frac{1}{2} \left( \frac{a}{r} \right)^{3} \right\}
```
The azimuthal component, $\omega_{\varphi}$, of $\boldsymbol{\omega}$ is only non-zero and is given by 
```{math}
:label: eq:DragVorticity_nonref_7
	\omega_{\varphi} = \frac{\partial v_{\theta}}{\partial r} + \frac{v_{\theta}}{r} - \frac{1}{r} \frac{\partial v_{r}}{\partial \theta}
	= \frac{3}{2} \left( \frac{a}{r^{2}} \right) u \sin \theta 
```
At the solid surface, 
```{math}
:label: eq:DragVorticity_nonref_8
	\omega_{\varphi} = \frac{3 u \sin \theta}{2 a}~~~~\text{at}~r = a
```
The maximum vorticity at $r = a$ is then 
```{math}
:label: eq:Legendre_eq_vorticity-max-Stokes
	\omega_{\max} = \frac{3 u}{2 a}
```
The solid surface is the only source of the vorticity in the system. Hence, the magnitude of the drag would be scaled by $\omega_{\max}$. Substituting Eq. {eq}`eq:Legendre_eq_vorticity-max-Stokes` into Eq. {eq}`eq:Legendre_eq_Stokes-drag` yields 
```{math}
:label: eq:DragVorticity_nonref_9
	F_{D} = 4 \pi \mu a^{2} \omega_{\max}
```
The drag coefficient is then 
```{math}
:label: eq:DragVorticity_nonref_10
	C_{D} 
	= \frac{4 \pi \mu a^{2} \omega_{\max}}{\frac{1}{2} \rho u^{2} \pi a^{2}}
	= \frac{16 \mu}{2 \rho u a} \frac{\omega_{\max} a}{u}
	= \frac{16}{Re} \omega_{\max}^{*}
```
where 
```{math}
:label: eq:DragVorticity_nonref_11
	\omega_{\max}^{*} = \frac{\omega_{\max} a}{u}
```
For a bubble, the Hadamard-Rybczynski drag is given by 
```{math}
:label: eq:Legendre_eq_HR-drag
	F_{D} = 4 \pi \mu u a
```
The velocity components are 
```{math}
:label: eq:DragVorticity_nonref_12
	v_{\theta} = u \sin \theta \left\{ 1 - \frac{a}{2 r} \right\}
```
```{math}
:label: eq:DragVorticity_nonref_13
	v_{r} = - u \cos \theta \left\{ 1 - \frac{a}{r} \right\}
```
The azimuthal vorticity for this velocity fields is 
```{math}
:label: eq:DragVorticity_nonref_14
    \omega_{\varphi} = \frac{u a \sin \theta}{r^{2}}
```
Therefore,
```{math}
:label: eq:DragVorticity_nonref_15
	\omega_{\varphi} = \frac{u \sin \theta}{a}~~~~\text{at}~r = a
```
The drag can be expressed in terms of this surface vorticity as 
```{math}
:label: eq:DragVorticity_nonref_16
	F_{D} = 4 \pi \mu a^{2} \omega_{\max}
```
and the drag coefficient is given by 
```{math}
:label: eq:DragVorticity_nonref_17
	C_{D} = \frac{16}{Re} \omega_{\max}^{*}
```
Therefore, the drag-vorticity relation for solid and fluid spheres in the Stoke regime can be integrated in the following form: 
```{math}
:label: eq:Legendre_eq_drag-vorticity-Legendre
	C_{D} Re = 16 \omega_{\max}^{*}
```

It is also shown that the Levich drag for the infinite $Re$ limit has the same form as for the drag-vorticity relation. The drag is 
```{math}
:label: eq:DragVorticity_nonref_18
	F_{D} = 12 \pi \mu u a
```
As discussed in the previous section, the surface vorticity is given by 
```{math}
:label: eq:DragVorticity_nonref_19
	\omega_{\varphi} = \frac{3 u \sin \theta}{a}~~~~\text{at}~r = a
```
and 
```{math}
:label: eq:DragVorticity_nonref_20
	\omega_{\max} = \frac{3 u}{a}~~~~\text{and}~~~~\omega_{\max}^{*} = 3
```
For the drag and the maximum surface vorticity, Eq. {eq}`eq:Legendre_eq_drag-vorticity-Legendre` holds:
```{math}
:label: eq:DragVorticity_nonref_21
    C_{D} Re = 16 \omega_{\max}^{*} = 48
```

Numerical simulations of spherical bubbles demonstrated that Eq. {eq}`eq:Legendre_eq_drag-vorticity-Legendre` is valid not only in the limiting cases of $Re \ll 1$ and $Re \rightarrow \infty$ but also at intermediate Reynolds numbers. The following drag correlation proposed by {cite:t}`Mei1994-mx` is applicable to a wide range of $Re$: 
```{math}
:label: eq:Legendre_eq_drag-Mei
	C_{D} = \frac{16}{Re} \frac{16 + 3.315 \sqrt{Re} + 3 Re}{16 + 3.315 \sqrt{Re} + Re}
```
Substituting Eq. {eq}`eq:Legendre_eq_drag-Mei` into Eq. {eq}`eq:Legendre_eq_drag-vorticity-Legendre` yields the maximum surface vorticity expressed in terms of $Re$: 
```{math}
:label: eq:DragVorticity_nonref_22
	\omega_{\max}^{*} = \frac{16 + 3.315 \sqrt{Re} + 3 Re}{16 + 3.315 \sqrt{Re} + Re}
```
It should be noted that Eq. {eq}`eq:Legendre_eq_drag-vorticity-Legendre` is no longer valid for solid spheres of $Re > 1$. However, a linear relationship between $C_{D} Re$ and $\omega_{\max}^{*}$ can be found up to a certain $Re$, below which a stable wake is formed. 

{cite:t}`Legendre2007-nv` also showed for ellipsoidal bubbles that 
```{math} 
:label: eq:DragVorticity_nonref_23
C_{D} Re = 16 f(\chi, Re) \omega_{\text{max}}^{*}
```
where $f(\chi, Re)$ is shape deformation factor: $f(1, \infty) = 1$ and $f(\chi, \infty)$ is given by Eq. {eq}`eq:negative_lift_6`. Note also that $\omega_{\text{max}}^{*} = \chi$ at low $Re$. 