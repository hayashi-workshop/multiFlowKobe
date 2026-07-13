(virtual_mass)=
# Virtual mass

```{admonition} Referred from 
{ref}`interfacial_momentum_transfer`
```

```{admonition} Summary
* **Subject:** (Fluid) particles feels their masses heavier than the actual. 
* **Main conclusion:** Particle mass is *virtually* $\rho_{P} + C_{VM} \rho$, where $\rho$ is the density of surrounding fluid, and $C_{VM} = 1/2$ for sphere. 
* **Key idea** Particles must accelerate surroundings, thereby the accelerating motion gives an inertial force. 
* **Reference:** {cite:t}`Landau1987` (Chap. 1)
```

In this section, a solid sphere moving in an incompressible inviscid fluid is considered. Therefore, let us introduce the velocity potential to express the fluid velocity $\mathbf{v}$:
```{math}
:label: eq:VirtualMass_nonref_0
	\mathbf{v} = \nabla \phi
```
Substituting this expression into the continuity equation
```{math}
:label: eq:VirtualMass_nonref_1
	\nabla \cdot \mathbf{v} = 0
```
yields the Laplace equation of $\phi$: 
```{math}
:label: eq:VirtualMass_nonref_2
	\nabla^{2} \phi = 0
```

```{figure} fig/cvm.pdf
:name: virtual_mass_setup
Spherical body in infinite fluid
```

The center of the sphere is set at the origin of the spherical coordinates. At <u>positions far from the sphere</u>, we assume that $\phi$ is a function of $r$. $\phi_{0} = 1/r$ obviously satisfies the Laplace equation: 
```{math}
:label: eq:VirtualMass_nonref_3
	\nabla^{2} \phi_{0} \rightarrow \frac{1}{r^{2}} \frac{d}{dr} r^{2} \frac{d \phi_{0}}{dr}
	= \frac{1}{r^{2}} \frac{d}{dr} r^{2} \left( - \frac{1}{r^{2}} \right) = 0
```
Derivatives of $\phi_{0}$, can also be solution of the Laplace equation since 
```{math}
:label: eq:VirtualMass_nonref_4
	\nabla^{2} \frac{\partial^{n} \phi_{0}}{\partial x_{i_{1}} \partial x_{i_{2}} \cdots \partial x_{i_{n}}} 
	= \frac{\partial^{n} }{\partial x_{i_{1}} \partial x_{i_{2}} \cdots \partial x_{i_{n}}}  \nabla^{2} \phi_{0}
	= 0
```
where $n \ge 1$. The velocity component $\mathbf{v}^{(1)}$ for $- a \phi_{0}$ is given by 
```{math}
:label: eq:VirtualMass_nonref_5
	\mathbf{v}^{(1)} 
	= \nabla \left( - \frac{\alpha}{r} \right)
	= \frac{\partial r}{\partial x_{i}} \frac{d}{dr} \left( - \frac{\alpha}{r} \right)
	= \alpha \frac{x_{i}}{r} \frac{1}{r^{2}}
	= \frac{\alpha x_{i}}{r^{3}}
```
where $a$ is a constant. The mass flow rate through the surface of a large sphere $S_{\infty}$ set at the origin is 
```{math}
:label: eq:VirtualMass_nonref_6
	\iint_{S_{\infty}} \rho \mathbf{v}^{(1)} \cdot \mathbf{n} dS
	&= \iint_{S_{\infty}} \rho \mathbf{v}^{(1)} \cdot \mathbf{e}_{r} dS
	\rightarrow \rho \alpha \iint_{S_{\infty}} \frac{x_{i} x_{i}}{r^{4}} dS
	= \rho \alpha \iint_{S_{\infty}} \frac{1}{r^{2}} dS \\
	&= 4 \pi \rho \alpha
```
where $\mathbf{n}$ is the outward unit normal to $S_{\infty}$. However, this must vanish because of the incompressibility; therefore, $\alpha = 0$. The next candidate is $\nabla \phi_{0}$. Let us therefore set $\mathbf{A} \cdot \nabla \phi_{0}$, where $\mathbf{A}$ is a constant vector. The vector component for this velocity potential is given by 
```{math}
:label: eq:VirtualMass_nonref_7
\begin{split}	
	\mathbf{v}^{(2)} 
	&= \nabla ( \mathbf{A} \cdot \nabla \phi_{0} )
	\rightarrow \frac{\partial }{\partial x_{i}} \left( A_{j} \frac{\partial }{\partial x_{j}} \frac{1}{r} \right)
	= \frac{\partial }{\partial x_{i}} \left( A_{j} \frac{\partial r}{\partial x_{j}} \frac{d}{dr} \frac{1}{r} \right)
	= A_{j} \frac{\partial }{\partial x_{i}} \left( \frac{x_{j}}{r} \frac{d}{dr} \frac{1}{r} \right)
	= - A_{j} \frac{\partial }{\partial x_{i}} \left( \frac{x_{j}}{r^{3}} \right) \\
	&= - A_{j} \left( \frac{\delta_{ij}}{r^{3}} - x_{j} \frac{3 x_{i}}{r^{5}} \right)
	= \frac{3 A_{j} x_{j} x_{i}}{r^{5}} - \frac{A_{i}}{r^{3}} 
	\rightarrow \frac{3 ( \mathbf{A} \cdot \mathbf{e}_{r} ) \mathbf{e}_{r} - \mathbf{A}}{r^{3}}
\end{split}
```
In the far field, velocity components given by the velocity potentials of higher order negligibly small compared with $\mathbf{v}^{(2)}$. Therefore, in the following, we may write $\mathbf{v}$ instead of $\mathbf{v}^{(2)}$. 

The velocity component normal to the solid sphere $v_{r}~(= \mathbf{v} \cdot \mathbf{e}_{r})$ must be equal to that of the sphere $u_{r}~(= \mathbf{u} \cdot \mathbf{e}_{r})$, i.e. the boundary condition $( \mathbf{v} - \mathbf{u} ) \cdot \mathbf{e}_{r} = 0$. 
```{math}
:label: eq:Virtual_eq_A-of-sphere
\begin{split}	
	&\left. \left( \frac{3 A_{j} x_{j} x_{i}}{r^{5}} - \frac{A_{i}}{r^{3}} - u_{i} \right) \frac{x_{i}}{r} \right|_{r=a} = 0
	\rightarrow \left. \frac{2 A_{i} x_{i} }{r^{4}} - u_{i} \frac{x_{i}}{r} \right|_{r=a} = 0 
	\rightarrow \left. \left( \frac{2 A_{i}}{r^{3}} - u_{i} \right ) \frac{x_{i}}{r} \right|_{r=a} = 0 \\
	&\rightarrow A_{i} = \frac{a^{3} u_{i}}{2}
\end{split}
```

The total kinetic energy $E$ of the fluid is given by 
```{math}
:label: eq:VirtualMass_nonref_8
	E = \iiint_{V_{\infty}-V} \frac{\rho v^{2}}{2} dV
```
where $V_{\infty}$ is the fluid volume of a sphere of large size, while its radius will be taken as infinity later to cover the whole system. $V$ is the volume of the sphere, $V = 4 \pi a^{3} / 3$. $( \mathbf{v} - \mathbf{u} ) \cdot ( \mathbf{v} + \mathbf{u} ) = v^{2} - u^{2}$. Therefore, $v^{2} = u^{2} + ( \mathbf{v} - \mathbf{u} ) \cdot ( \mathbf{v} + \mathbf{u} )$. The integral of the $v$ square is therefore rewritten as 
```{math}
:label: eq:VirtualMass_nonref_9
	\iiint_{V_{\infty}-V} \left\{ u^{2} + ( \mathbf{v} - \mathbf{u} ) \cdot ( \mathbf{v} + \mathbf{u} ) \right\} dV
	= \iiint_{V_{\infty}-V} u^{2} dV + \iiint_{V_{\infty}-V} ( \mathbf{v} - \mathbf{u} ) \cdot ( \mathbf{v} + \mathbf{u} ) dV
```
The first term can be immediately integrated as 
```{math}
:label: eq:VirtualMass_nonref_10
	\iiint_{V_{\infty}-V} u^{2} dV 
	= u^{2} \iiint_{V_{\infty}-V} dV
	= u^{2} \left( V_{\infty} - V \right)
```
For the second term, by writing $\mathbf{v} = \nabla \phi$ and $\mathbf{u} = \nabla ( \mathbf{u} \cdot \mathbf{r} )$, we have 
```{math}
:label: eq:VirtualMass_nonref_11
	\mathbf{v} + \mathbf{u} = \nabla \phi + \nabla ( \mathbf{u} \cdot \mathbf{r} ) = \nabla ( \phi + \mathbf{u} \cdot \mathbf{r} )
```
Then, 
```{math}
:label: eq:VirtualMass_nonref_12
\begin{split}	
	( \mathbf{v} - \mathbf{u} ) \cdot ( \mathbf{v} + \mathbf{u} )
	&= ( \mathbf{v} - \mathbf{u} ) \cdot \nabla ( \phi + \mathbf{u} \cdot \mathbf{r} )
	= \nabla \cdot ( \mathbf{v} - \mathbf{u} ) ( \phi + \mathbf{u} \cdot \mathbf{r} ) - ( \phi + \mathbf{u} \cdot \mathbf{r} ) \nabla \cdot ( \mathbf{v} - \mathbf{u} ) \\
	&= \nabla \cdot ( \mathbf{v} - \mathbf{u} ) ( \phi + \mathbf{u} \cdot \mathbf{r} )
\end{split}
```
The second term in the third term vanishes since $\nabla \cdot \mathbf{v} = \nabla \cdot \mathbf{u} = 0$. Applying the divergence theorem yields 
```{math}
:label: eq:VirtualMass_nonref_13
\begin{split}	
	&\iiint_{V_{\infty}-V} u^{2} dV + \iiint_{V_{\infty}-V} ( \mathbf{v} - \mathbf{u} ) \cdot ( \mathbf{v} + \mathbf{u} ) dV \\
	&= u^{2} \left( V_{\infty} - V \right) + \iiint_{V_{\infty}-V} \nabla \cdot ( \mathbf{v} - \mathbf{u} ) ( \phi + \mathbf{u} \cdot \mathbf{r} ) dV \\
	&= u^{2} \left( V_{\infty} - V \right) + \iint_{S_{\infty}} ( \mathbf{v} - \mathbf{u} ) ( \phi + \mathbf{u} \cdot \mathbf{r} ) \cdot \mathbf{e}_{r} dS - \iint_{S} ( \mathbf{v} - \mathbf{u} ) ( \phi + \mathbf{u} \cdot \mathbf{r} ) \cdot \mathbf{e}_{r} dS
\end{split}
```
where $S_{\infty}$ is the surface surrounding $V_{\infty}$. However, $( \mathbf{v} - \mathbf{u} ) \cdot \mathbf{e}_{r} = 0$ on $S$. 
\begin{equation*}
\begin{split}	
	u^{2} \left( V_{\infty} - V \right) + \iint_{S_{\infty}} ( \mathbf{v} - \mathbf{u} ) ( \phi + \mathbf{u} \cdot \mathbf{r} ) \cdot \mathbf{e}_{r} dS
\end{split}
\end{equation*}
Expanding the second term gives 
```{math}
:label: eq:VirtualMass_nonref_14
\begin{split}	
	\iint_{S_{\infty}} ( \mathbf{v} - \mathbf{u} ) ( \phi + \mathbf{u} \cdot \mathbf{r} ) \cdot \mathbf{e}_{r} dS
	&= \iint_{S_{\infty}} \left( \frac{3 ( \mathbf{A} \cdot \mathbf{e}_{r} ) \mathbf{e}_{r} - \mathbf{A}}{r^{3}} - \mathbf{u} \right) \left( \mathbf{A} \cdot \nabla \phi_{0} + \mathbf{u} \cdot \mathbf{r} \right) \cdot \mathbf{e}_{r} dS \\
	&\rightarrow \iint_{S_{\infty}} \left( \frac{3 A_{j} x_{j} x_{i} - A_{i} r^{2}}{r^{5}} - u_{i} \right) \left( A_{k} \frac{\partial}{\partial x_{k}} \frac{1}{r} + u_{k} x_{k} \right) \frac{x_{i}}{r} dS \\
	&= \iint_{S_{\infty}} \left( \frac{2 A_{j} x_{j}}{r^{3}} - u_{j} x_{j} \right) \left( - \frac{A_{k} x_{k}}{r^{3}} + u_{k} x_{k} \right) \frac{ dS }{r} \\
	&= \iint_{S_{\infty}} \left( - \frac{2 ( A_{j} x_{j} )^{2}}{r^{3}} + 3 A_{j} x_{j} u_{k} x_{k} - r^{3} ( u_{j} x_{j} )^{2} \right) \frac{dS}{r^{4}} 
\end{split}
```
Since the radius $a_{\infty}$ of the sphere $S_{\infty}$ is large, the first term of the integrand is negligible in comparison with the other two terms, so that, 
```{math}
:label: eq:VirtualMass_nonref_15
\begin{split}	
	\iint_{S_{\infty}} \left( - \frac{2 ( A_{j} x_{j} )^{2}}{r^{3}} + 3 A_{j} x_{j} u_{k} x_{k} - r^{3} ( u_{j} x_{j} )^{2} \right) \frac{dS}{r^{4}} 
	&\rightarrow \iint_{S_{\infty}} \left( 3 A_{j} x_{j} u_{k} x_{k} - r^{3} ( u_{j} x_{j} )^{2} \right) \frac{dS}{r^{4}} \\
	&= \frac{3 A_{j} u_{k} - a_{\infty}^{3} u_{j} u_{k}}{a_{\infty}^{2}} \iint_{S_{\infty}} \frac{x_{j} x_{k}}{r^{2}} dS \\
\end{split}
```
The integrand of the surface integral is the dyadic $\mathbf{e}_{r} \mathbf{e}_{r}$. 
```{math}
:label: eq:VirtualMass_nonref_16
\begin{split}
	\iint_{S_{\infty}} \frac{x_{j} x_{k}}{r^{2}} dS 
	= \iint_{S_{\infty}} \mathbf{e}_{r} \mathbf{e}_{r} dS 
\end{split}
```
For the $xx$ component,  
```{math}
:label: eq:VirtualMass_nonref_17
\begin{split}
	\int_{0}^{2 \pi} \int_{0}^{\pi} ( \sin \theta \cos \varphi )^{2} a_{\infty}^{2} \sin \theta d\theta d\varphi
	= a_{\infty}^{2} \int_{0}^{\pi} \sin^{3} \theta d\theta \int_{0}^{2 \pi} \cos^{2} \varphi d\varphi
	= \cdot \frac{4 \pi a_{\infty}^{2}}{3}
\end{split}
```
For the $xy$ component,  
```{math}
:label: eq:VirtualMass_nonref_18
\begin{split}
	\int_{0}^{2 \pi} \int_{0}^{\pi} ( \sin \theta \cos \varphi ) ( \sin \theta \sin \varphi ) a_{\infty}^{2} \sin \theta d\theta d\varphi
	= a_{\infty}^{2} \int_{0}^{\pi} \sin^{3} \theta d\theta \int_{0}^{2 \pi} \cos \varphi \sin \varphi d\varphi
	= 0
\end{split}
```
In summary, 
```{math}
:label: eq:VirtualMass_nonref_19
\begin{split}
	\iint_{S_{\infty}} \mathbf{e}_{r} \mathbf{e}_{r} dS 
	\rightarrow \frac{4 \pi a_{\infty}^{2}}{3} \delta_{jk}
\end{split}
```
Therefore, 
```{math}
:label: eq:VirtualMass_nonref_20
\begin{split}	
	\frac{3 A_{j} u_{k} - a_{\infty}^{3} u_{j} u_{k}}{a_{\infty}^{2}} \iint_{S_{\infty}} \frac{x_{j} x_{k}}{r^{2}} dS 
	= 4 \pi A_{j} u_{j} - \frac{ 4 \pi a_{\infty}^{3} }{3} u_{j} u_{j}
	= 4 \pi A_{j} u_{j} - V_{\infty} u_{j} u_{j}
\end{split}
```
Thus, 
```{math}
:label: eq:VirtualMass_nonref_21
\begin{split}	
	E = \iiint_{V_{\infty}-V} \frac{\rho v^{2}}{2} dV 
	= \frac{\rho}{2} \left( 4 \pi A_{j} u_{j} - V u^{2} \right)
	= \frac{\rho}{2} ( 4 \pi A_{j} - V u_{j} ) u_{j}
\end{split}
```
As we have confirmed (Eq. {eq}`eq:Virtual_eq_A-of-sphere`), $\mathbf{A}$ is proportional to $\mathbf{u}$. Therefore, we may write 
```{math}
:label: eq:Virtual_eq_induced-mass-with-u
	P_{j} = m_{ij} u_{i} = 4 \pi \rho A_{j} - \rho V u_{j}
```
where $\mathbf{P}$ is the total momentum of the fluid, and the symmetric tensor $m_{ij}$ is referred to as the induced-mass tensor. Thus, the total kinetic energy of the fluid is expressed as 
```{math}
:label: eq:VirtualMass_nonref_22
	E = \frac{1}{2} m_{ij} u_{i} u_{j}
```
By substituting Eq. {eq}`eq:Virtual_eq_A-of-sphere` into Eq. {eq}`eq:Virtual_eq_induced-mass-with-u` we obtain 
```{math}
:label: eq:VirtualMass_nonref_23
	m_{ij} u_{i} = ( 2 \pi \rho a^{3} - \rho V ) u_{j}
```
Hence, 
```{math}
:label: eq:Virtual_eq_virtual-mass-sphere
	m_{ij}= \rho \frac{2 \pi a^{3}}{3} \delta_{ij} = \frac{1}{2} \rho V \delta_{ij}
```
For the sphere, the induced mass is the half of the fluid mass removed by the sphere. 

Consider a spherical particle oscillating in a fluid under the action of an external force $\mathbf{f}$, which is the source of the change in the total momentum in the system, i.e., the momentum of the fluid and that of the particle. Therefore,
```{math}
:label: eq:VirtualMass_nonref_24
	\frac{d ( M \mathbf{u} + \mathbf{P} )}{dt} = \mathbf{f}
```
where $M$ is the mass of the particle. Substituting Eq. {eq}`eq:Virtual_eq_induced-mass-with-u` yields 
```{math}
:label: eq:VirtualMass_nonref_25
	\left( M \delta_{ij} + m_{ij} \right) \frac{d u_{j}}{dt} = f_{i}
```
We then consider a spherical particle in a fluid under oscillation. If this particle was the fluid, the momentum of this volume is $\rho V \mathbf{v}$ and the force acting on the fluid particle of volume $V$ is given by 
```{math}
:label: eq:VirtualMass_nonref_25_1
	\rho V \frac{d v_{i}}{dt}
```
where the particle is assumed to be much smaller than the length scale for the spatial change in $\mathbf{v}$. This volume is actually the particle and may have velocity $\mathbf{u}$ different from the fluid velocity $\mathbf{v}$. We therefore need to account for the force due to the relative motion $\mathbf{u} - \mathbf{v}$: 
```{math}
:label: eq:VirtualMass_nonref_25_2
	- m_{ij} \frac{d (u_{j} - v_{j})}{dt} 
```
where the negative sign is added since this is a force acting on the particle as the reaction. 
```{toggle}
When the relative velocity $\mathbf{u} - \mathbf{v}$ increases, the force acts on the sphere so as to retard the relative velocity.
```
The equation of motion of the particle is therefore given by 
```{math}
:label: eq:VirtualMass_nonref_26
	M \frac{d u_{i}}{dt} = \rho V \frac{d v_{i}}{dt} - m_{ij} \frac{d (u_{j} - v_{j})}{dt} 
```
The second term on the R.H.S. is the so-called *virtual (added) mass* force. By making use of Eq. {eq}`eq:Virtual_eq_virtual-mass-sphere`, we have 
```{math}
:label: eq:VirtualMass_nonref_27
	M \frac{d u_{i}}{dt} = \rho V \frac{d v_{i}}{dt} - \frac{1}{2} \rho V \frac{d (u_{i} - v_{i})}{dt} 
```
Denoting the particle density as $\rho_{P}~(=M/V)$, one can write 
```{math}
:label: eq:VirtualMass_nonref_28
	\left( \rho_{P} + \rho C_{VM} \right) \frac{d u_{i}}{dt} = \rho \left( 1 + C_{VM} \right) \frac{d v_{i}}{dt} 
```
where $C_{VM} = 1/2$ is the virtual mass coefficient of the sphere. 

```{seealso}
{ref}`interfacial_momentum_transfer`
```

The virtual mass coefficient is a function of particle shape. According to {cite:t}`Tomiyama2004-ee`, for an oblate spheroild moving vertically {cite:p}`Lamb1945`, 
```{math}
:label: eq:VirtualMass_nonref_29
C_{VM}
=
\left(
\begin{array}{ccc}
C_{VM}^{H} &0 &0 \\
0 &C_{VM}^{H} &0 \\
0 &0 &C_{VM}^{V}
\end{array}
\right)
```
where 
```{math} 
C_{VM}^{V} = 
\chi^{2} \frac{\sec^{-1} \chi - \sqrt{\chi^2 - 1}}{\sqrt{\chi^2 - 1} - \chi^2 \sec^{-1} \chi} 
```
and 
```{math} 
C_{VM}^{H} = 
\frac{\chi^2 \sec^{-1} \chi - \sqrt{\chi^2 - 1}}{(2 \chi^2 - 1) \sqrt{\chi^2 - 1} - \chi^2 \sec^{-1} \chi} 
```
For a prolate ellipsoids, see {cite:t}`Tomiyama2004-ee`. 

```{figure} python/cvm.pdf
:name: virtual_mass_ellipse
Virtual mass coefficients, $C_{VM}^{V}$ and $C_{VM}^{H}$, of ellipsoidal body.
```