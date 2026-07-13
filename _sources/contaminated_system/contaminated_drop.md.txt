(contaminated_drop)=
# Contaminated drops in Stokes flow

```{admonition} Summary
* **Subject:** Contaminated drop in Stokes flow
* **Main conclusion:** Marangoni stress retards drop rise velocity.
* **Key idea** Marangoni stress caused by non-uniform surfactant concentration changes the boundary condition at interface. 
* **References:** 
	- {cite:t}`Levich1962`	
```

## Drag on contaminated drop in Stokes flow ($\Gamma \sim \Gamma_{eq}$)

Let us consider a contaminated spherical drop moving at constant speed in the Stokes regime. The problem is similar to that for the Hadamard-Rybczinski solution {cite:p}`Hadamard1911-lz`. Even with the presence of surfactant, the functional forms of the external and internal velocities have the same form as we obtained for the Hadamard-Rybczinski solution, so that, 
```{math}
:label: eq:ContaminatedDrop_nonref_23
\begin{split}
	&\mathbf{v}^{(e)} = \mathbf{u} - \alpha \frac{\mathbf{u} + (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r}}{r} + \beta \frac{ 3 (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r} - \mathbf{u}}{r^{3}} \\
	&\mathbf{v}^{(i)} 
	= - A \mathbf{u} + B r^{2} \left( ( \mathbf{u} \cdot \mathbf{e}_{r} ) \mathbf{e}_{r} - 2 \mathbf{u} \right)
\end{split}
```
We need to determine the four constants so as to satisfy the boundary conditions: 
\begin{itemize}
	\item The velocity normal to the interface is continuous and is zero because the sphere is motionless: $\left. v_{r}^{(e)} \right|_{r=a} = \left. v_{r}^{(i)} \right|_{r=a} = 0$
	\item The velocity tangent to the interface is continuous: $\left. v_{\theta}^{(e)} \right|_{r=a} = \left. v_{\theta}^{(i)} \right|_{r=a}$
	\item the difference in the tangential viscous stresses balances with the Marangoni stress (the surface tension gradient): $\left. \tau_{r \theta}^{(e)} \right|_{r=a} - \left. \tau_{r \theta}^{(i)} \right|_{r=a} = - \frac{1}{a} \frac{\partial \sigma}{\partial \theta}$
\end{itemize}
Only the third one is different from the conditions for the analysis in the Hadamard-Rybczinski solution. 

In a coordinate system moving with the drop $\mathbf{v} \cdot \mathbf{n} = 0$ at the interface, and Eq. {eq}`eq:contami_eq_gamma-equation` therefore reduces to 
```{math}
:label: eq:ContaminatedDrop_nonref_24
	\nabla_{s} \cdot \Gamma \mathbf{v}_{s} = \nabla_{s} \cdot D_{s} \nabla_{s} \Gamma + \dot{S}_{\Gamma}
```
We assume that the drop interface is covered by surfactant at a concentration close to the equilibrium value, i.e., 
```{math}
:label: eq:ContaminatedDrop_nonref_25
	\Gamma = \Gamma_{eq} + \Gamma'
```
where $\Gamma' / \Gamma_{eq} \ll 1$. Substituting this condition into the transport equation to linearize the problem gives 
```{math}
:label: eq:ContaminatedDrop_nonref_26
	\Gamma_{eq} \nabla_{s} \cdot \mathbf{v}_{s} + \nabla_{s} \cdot \Gamma' \mathbf{v}_{s} = D_{s} \nabla_{s}^{2} \Gamma' + \dot{S}_{\Gamma}
```
where $D_{s}$ is assumed to be constant. The interface velocity is retarded by the surfactant effect. For small $\mathbf{v}_{s}$, the convective transport $\nabla_{s} \cdot \Gamma' \mathbf{v}_{s}$ is negligible, so that, 
```{math}
:label: eq:ContaminatedDrop_nonref_27
	\Gamma_{eq} \nabla_{s} \cdot \mathbf{v}_{s} = D_{s} \nabla_{s}^{2} \Gamma' + \dot{S}_{\Gamma}
```
With the spherical coordinates, 
```{math}
:label: eq:ContaminatedDrop_nonref_28
	\frac{\Gamma_{eq}}{a \sin \theta} \frac{\partial v_{\theta} \sin \theta}{\partial \theta} = \frac{D_{s}}{a \sin \theta} \frac{\partial}{\partial \theta} \left( \frac{\partial \Gamma'}{\partial \theta} \sin \theta \right) + \dot{S}_{\Gamma}
```
The velocity profile is assumed to have the form of $v_{\theta} \propto \sin \theta$ as in the Hadamard-Rybczinski solution. Writing $v_{0}$ as the velocity at $\theta = \pi / 2$, $v_{\theta} = v_{0} \sin \theta$. Therefore, 
```{math}
:label: eq:ContaminatedDrop_nonref_29
	\frac{\Gamma_{eq}}{a \sin \theta} \frac{\partial v_{\theta} \sin \theta}{\partial \theta} 
	= \frac{\Gamma_{eq}}{a \sin \theta} \frac{\partial v_{0} \sin^{2} \theta}{\partial \theta} 
	= \frac{2 \Gamma_{eq} v_{0}}{a} \cos \theta  
```
By expanding the adsorption flux 
```{math}
:label: eq:ContaminatedDrop_nonref_30
	\dot{S}_{\Gamma} = Q(C_{0}, \Gamma) - P(\Gamma)
```
we obtain 
```{math}
:label: eq:ContaminatedDrop_nonref_31
	\dot{S}_{\Gamma} = Q(C_{0}, \Gamma_{eq}) - P(\Gamma_{eq}) + \left( \frac{\partial Q}{\partial \Gamma} - \frac{\partial P}{\partial \Gamma} \right) \Gamma'
```
For the equilibrium, $Q(C_{0}, \Gamma_{eq}) = P(\Gamma_{eq})$. Hence, 
```{math}
:label: eq:ContaminatedDrop_nonref_32
	\dot{S}_{\Gamma} = - \lambda \Gamma'
```
where 
```{math}
:label: eq:ContaminatedDrop_nonref_33
	\lambda = \frac{\partial Q}{\partial \Gamma} - \frac{\partial P}{\partial \Gamma}
```
and for Eq. {eq}`eq:contami_frumkin-levich-c0`
```{math}
:label: eq:ContaminatedDrop_nonref_34
	\lambda = k_{a} C_{0} + k_{d}
```
Since $\lambda$ is positive, surfactant molecules come from the bulk liquid to the interface when $\Gamma' < 0$. The linearized transport equation is thus given by 
```{math}
:label: eq:ContaminatedDrop_nonref_35
	\frac{2 \Gamma_{eq} v_{0}}{a} \cos \theta = \frac{D_{s}}{a \sin \theta} \frac{\partial}{\partial \theta} \left( \frac{\partial \Gamma'}{\partial \theta} \sin \theta \right) - \lambda \Gamma'
```
The functional form $\Gamma' = A_{\Gamma} \cos \theta$ satisfies the transport equation when 
```{math}
:label: eq:ContaminatedDrop_nonref_36
	A_{\Gamma} = - \frac{2 \Gamma_{eq} v_{0}}{a \lambda + 2 D_{s}}
```
The diffusion coefficient is usually small ($\sim 10^{-9}$~m$^{2}$/s in many cases) and the diffusive flux is smaller than the advection flux. The diffusion is therefore neglected in the following discussion, and therefore, 
```{math}
:label: eq:ContaminatedDrop_nonref_37
	\Gamma' = - \frac{2 \Gamma_{eq} v_{0}}{a \lambda} \cos \theta
```

The Marangoni stress can now be calculated using the expression of $\Gamma'$, i.e.,
```{math}
:label: eq:ContaminatedDrop_nonref_38
	- \frac{1}{a} \frac{\partial \sigma}{\partial \theta}
	= - \frac{1}{a} \frac{\partial \Gamma}{\partial \theta} \frac{\partial \sigma}{\partial \Gamma}
	= - \frac{1}{a} \frac{\partial \Gamma'}{\partial \theta} \frac{\partial \sigma}{\partial \Gamma}
	= - \frac{2 \Gamma_{eq}}{a^{2} \lambda} \frac{\partial \sigma}{\partial \Gamma} v_{0} \sin \theta 
	= \frac{3 \gamma}{a} v_{0} \sin \theta 
```
where 
```{math}
:label: eq:ContaminatedDrop_nonref_39
	\gamma = - \frac{2 \Gamma_{eq}}{3 a \lambda} \frac{\partial \sigma}{\partial \Gamma}
```
According to the velocity profile 
```{math}
:label: eq:Contami_eq_vtheta
	\left. v_{\theta}^{(i)} \right|_{r=a} 
	= u \sin \theta \left( - A - 2 B a^{2} \right) 
```
we may write 
```{math}
:label: eq:ContaminatedDrop_nonref_40
	v_{0} = u ( - A - 2 B a^{2} )
```
The boundary condition for the tangential stresses is thus given by 
```{math}
:label: eq:ContaminatedDrop_nonref_41
	\left. \tau_{r \theta}^{(e)} \right|_{r=a} = \left. \tau_{r \theta}^{(i)} \right|_{r=a} - \frac{1}{a} \frac{\partial \sigma}{\partial \theta}
	~~\rightarrow~~
	\beta \frac{6 \mu^{(e)} u}{a^{4}} \sin \theta = - 3 B \mu^{(i)} a u \sin \theta + \frac{3 \gamma}{a} ( - A - 2 B a^{2} ) u \sin \theta
```
The set of the boundary conditions to determine the constants are 
```{math}
:label: eq:ContaminatedDrop_nonref_42
\begin{split}
	&A + a^{2} B = 0 \\
	&- 2 a^{2} \alpha + 2 \beta + a^{3} = 0 \\
	&a^{3} A + 2  a^{5} B - a^{2} \alpha - \beta + a^{3} = 0 \\
	&\left\{ \mu^{(i)} + 2 \gamma \right\} a^{5} B + \gamma a^{3} A + 2 \mu^{(e)} \beta = 0
\end{split}
```
Solving the simultaneous equations gives 
```{math}
:label: eq:ContaminatedDrop_nonref_43
\begin{split}
	&\alpha = \frac{a}{4} \frac{2 \mu^{(e)} + 3 \mu^{(i)} + 3 \gamma}{\mu^{(e)} + \mu^{(i)} + \gamma} \\
	&\beta = \frac{a^{3}}{4} \frac{\mu^{(i)} + \gamma}{\mu^{(e)} + \mu^{(i)} + \gamma} \\
	&A = \frac{1}{2} \frac{\mu^{(e)}}{\mu^{(e)} + \mu^{(i)} + \gamma} \\
	&B = - \frac{1}{2 a^{2}} \frac{\mu^{(e)}}{\mu^{(e)} + \mu^{(i)} + \gamma}
\end{split}
```
By substituting $A$ and $B$ into Eq. {eq}`eq:Contami_eq_vtheta` we obtain
```{math}
:label: eq:ContaminatedDrop_nonref_44
	\left. v_{\theta}^{(e)} \right|_{r=a} 
	=
	\left. v_{\theta}^{(i)} \right|_{r=a} 
	= \left( \frac{\mu^{(e)}}{\mu^{(e)} + \mu^{(i)} + \gamma} \right) \frac{u}{2} \sin \theta 
```
This results shows that the surface tension gradient ($\gamma$) causes retardation of the interface motion and the interface becomes immobile when $\gamma$ is large. 

The drag force is given by 
```{math}
:label: eq:ContaminatedDrop_nonref_45
	F_{D} = 8 \pi \mu^{(e)} u \alpha = \left( \frac{2 \mu^{(e)} + 3 \mu^{(i)} + 3 \gamma}{\mu^{(e)} + \mu^{(i)} + \gamma} \right) 2 \pi \mu^{(e)} u a
```
The drag coefficient is 
```{math}
:label: eq:ContaminatedDrop_nonref_46
	C_{D} = \frac{8}{Re} \left( \frac{2 \mu^{(e)} + 3 \mu^{(i)} + 3 \gamma}{\mu^{(e)} + \mu^{(i)} + \gamma} \right)
```
$\gamma$ is positive for $\partial \sigma / \partial \Gamma < 1$. When 
$\gamma \gg \mu^{(e)} + \mu^{(i)}$, the Stokes solution recovers: 
```{math}
:label: eq:ContaminatedDrop_nonref_47
	C_{D} \rightarrow \frac{24}{Re}
```
On the other hand, when $\gamma \ll \mu^{(e)} + \mu^{(i)}$, the drag correlation becomes the Hadamard-Rybczinski solution 
```{math}
:label: eq:ContaminatedDrop_nonref_48
	C_{D} \rightarrow \frac{8}{Re} \left( \frac{2 \mu^{(e)} + 3 \mu^{(i)}}{\mu^{(e)} + \mu^{(i)}} \right)
```
