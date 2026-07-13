(levich_drag)=
# Drag acting on a spherical bubble at high $Re$

```{admonition} Summary
* **Subject:** Levich drag {cite:p}`Levich1962`
* **Main conclusion:** Drag $F_{D} = 12 \pi \mu u a$ for $Re \rightarrow \infty$. 
* **Key idea** Drag balances with viscous dissipation, which concentrates at bubble surface due to high $Re$. 
* **Reference:** Derivation presented here is given by G. K. Batchelor {cite:p}`Batchelor2000` (Chap. 5).
```

Consider a spherical bubble steadily rising through stagnant incompressible fluid at a high Reynolds number. The bubble is rising along the $z$ axis toward the $+z$ side ($\theta = 0$) at a uniform velocity $\mathbf{u}~(= u \mathbf{e}_{z})$. The drag force acting on the bubble is $\mathbf{F}~(= - F_{D} \mathbf{e}_{z})$, which directs $-z$, so that the reaction on the fluid is $-\mathbf{F}$. The rise motion of the bubble pushing the fluid in the direction parallel to $\mathbf{u}$. Therefore, the work done by the reaction on the fluid is given by $- \mathbf{F} \cdot \mathbf{u} = F_{D} u$. 
```{toggle}
If we ride on the bubble we may see $\mathbf{u} = - u \mathbf{e}_{z}$. The drag force $\mathbf{F}~(= - F_{D} \mathbf{e}_{z})$ directing toward $-z$, and therefore, the reaction on the fluid is $- \mathbf{F}$. The fluid is traveling downward ($-z$) while experiencing the reaction, so that the work done on the fluid is $- \mathbf{F} \cdot \mathbf{u} = F_{D} u$.
```
Since the bubble velocity is constant the work produced by the rise motion is dissipated by the viscous dissipation in the fluid, that is, 
```{math}
:label: eq:LevichDrag_nonref_0
	F_{D} u \delta t 
	= \delta t \iiint_{V} 2 \mu e_{ij} e_{ij} dV
```
where $\delta t$ is an infinitesimal time variation, $e_{ij}$ is the rate of strain tensor defined by 
```{math}
:label: eq:LevichDrag_nonref_1
	e_{ij} = \frac{1}{2} \left( \frac{\partial v_{i}}{\partial x_{j}} + \frac{\partial v_{j}}{\partial x_{i}} \right)
```
A brief description of the viscous dissipation is given in Appendix {ref}`app_viscous_dissipation`. In the limiting case of $Re \rightarrow \infty$ the vorticity produced at the bubble surface is limited only in a thin layer on the surface, so that the velocity field in the bulk fluid can be assumed to be irrotational. Therefore, there exists a velocity potential deriving the velocity field: 
```{math}
:label: eq:LevichDrag_nonref_2
	\mathbf{v} = \nabla \phi
```
By the potential flow theory (Appendix {ref}`app_potential_flow_sphere`), $\phi$ for a spherical body moving along the $z$ axis ($\theta = 0$) at the constant speed $u$ is given by 
```{math}
:label: eq:LevichDrag_nonref_3
	\phi = - \frac{u a^{3}}{2 r^{2}} \cos \theta
```
Note that the bubble center at this instant locates the origin of the coordinate. The velocity components for this potential are
```{math}
:label: eq:LevichDrag_nonref_4
\begin{split}
	&v_{r} 
	= \frac{\partial \phi}{\partial r} 
	= \frac{u a^{3}}{r^{3}} \cos \theta \\
	&v_{\theta} 
	= \frac{1}{r} \frac{\partial \phi}{\partial \theta} 
	= \frac{u a^{3}}{2 r^{3}} \sin \theta
\end{split}
```

The rate of strain tensor is rewritten as 
```{math}
:label: eq:LevichDrag_nonref_5
	e_{ij} = \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}}
```
Therefore, 
```{math}
:label: eq:LevichDrag_nonref_6
	e_{ij} e_{ij} = \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}} \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}}
```
The R.H.S. can be rewritten as 
```{math}
:label: eq:Levich_eq_phi-phi-rhs
	\frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}} \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}}
	= \left( \frac{\partial}{\partial x_{i}} \frac{\partial \phi}{\partial x_{j}} \right) \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}}
	= \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}} \right) - \frac{\partial \phi}{\partial x_{j}} \frac{\partial^{3} \phi}{\partial x_{i} \partial x_{i} \partial x_{j}}
```
However, the last term vanishes since $\nabla^{2} \phi = 0$ by the continuity equation, $\nabla \cdot \mathbf{v} = 0$. Then, the remaining term becomes 
```{math}
:label: eq:LevichDrag_nonref_7
\begin{split}	
	\frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}} \right) 
	&= \frac{\partial}{\partial x_{i}} \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right) - \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}}  \right) \\
	&= \frac{\partial}{\partial x_{i}} \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right) 
	- \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}} \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}}
	- \frac{\partial \phi}{\partial x_{j}} \frac{\partial^{3} \phi}{\partial x_{i} \partial x_{i} \partial x_{j}}
\end{split}
```
The third term vanishes and the second term is the same as the L.H.S. pf Eq. {eq}`eq:Levich_eq_phi-phi-rhs`, so that, 
```{math}
:label: eq:LevichDrag_nonref_8
	\frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}} \frac{\partial^{2} \phi}{\partial x_{i} \partial x_{j}}
	= \frac{1}{2} \frac{\partial}{\partial x_{i}} \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right)
```
Therefore, 
```{math}
:label: eq:LevichDrag_nonref_9
	\iiint_{V} 2 \mu e_{ij} e_{ij} dV
	= \mu \iiint_{V} \frac{\partial}{\partial x_{i}} \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right) dV
```
Applying the divergence theorem yields 
```{math}
:label: eq:LevichDrag_nonref_10
	\mu \iiint_{V} \frac{\partial}{\partial x_{i}} \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right) dV = \mu \iint_{S_{\infty}} \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right) n_{i} dS - \mu \iint_{S} \mathbf{e}_{r} \cdot \nabla \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right)  dS
```
where $n_{i}$ is the unit outward normal to $V$, $S_{\infty}$ is the surface area surrounding $V$, and $S$ is the surface area of the bubble. The fluid is at rest in the far field; hence, the surface integral for $S_{\infty}$ vanishes: 
```{math}
:label: eq:LevichDrag_nonref_11
	\mu \iiint_{V} \frac{\partial}{\partial x_{i}} \frac{\partial}{\partial x_{i}} \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right) dV = - \mu \iint_{S} \mathbf{e}_{r} \cdot \nabla \left( \frac{\partial \phi}{\partial x_{j}} \frac{\partial \phi}{\partial x_{j}} \right)  dS
```
The operator $\mathbf{e}_{r} \cdot \nabla$ is the gradient in the $r$ direction and $\nabla \phi \cdot \nabla \phi$ is the square, $v^{2}$, of the velocity magnitude. We therefore have 
```{math}
:label: eq:Levich_eq_FDu-work-expand
	F_{D} u = - \mu \int_{0}^{2 \pi} \int_{0}^{\pi} \frac{\partial v^{2}}{\partial r} a^{2} \sin \theta d\theta d\varphi
```
The velocity square is 
```{math}
:label: eq:LevichDrag_nonref_12
	v^{2} = v_{r}^{2} + v_{\theta}^{2}
	= \frac{u^{2} a^{6}}{r^{6}} \left( \cos^{2} \theta + \frac{\sin^{2} \theta}{4}\right)
```
The derivative $\partial v^{2} / \partial r$ is then given by 
```{math}
:label: eq:LevichDrag_nonref_13
	\frac{\partial v^{2}}{\partial r} 
	= - \frac{6 u^{2} a^{6}}{r^{7}} \left( \cos^{2} \theta + \frac{\sin^{2} \theta}{4} \right)
```
At the bubble surface, 
```{math}
:label: eq:LevichDrag_nonref_14
	\left. \frac{\partial v^{2}}{\partial r} \right|_{r=a}
	= - \frac{6 u^{2}}{a} \left( \cos^{2} \theta + \frac{\sin^{2} \theta}{4} \right)
```
By substituting this into Eq. {eq}`eq:Levich_eq_FDu-work-expand` we obtain
```{math}
:label: eq:LevichDrag_nonref_15
\begin{split}
	F_{D} u 
	&= 12 \pi \mu u^{2} a \int_{0}^{\pi} \left( \cos^{2} \theta + \frac{\sin^{2} \theta}{4} \right) \sin \theta d\theta \\
	&= 12 \pi \mu u^{2} a \left( \frac{2}{3} + \frac{1}{3} \right) = 12 \pi \mu u^{2} a
\end{split}
```
and 
```{math}
:label: eq:LevichDrag_nonref_16
	F_{D} = 12 \pi \mu u a
```
The drag coefficient is given by 
```{math}
:label: eq:LevichDrag_nonref_17
	C_{D} = \frac{48}{Re}
```
This result was obtained by Levich. In an air-water system bubbles from 0.5 to 1 mm in diameter behave to obey this theory. 
