(stokes_drag_LL)=
# Drag acting on a solid sphere in Stokes flow (LL)

```{admonition} Summary
* **Subject:** Stokes drag 
* **Main conclusion:** Drag $F_{D} = 6 \pi \mu u a$ in Stokes flow ($Re \ll 1$). 
* **Key idea** NS eq is linearlized by dropping the inertial term, thereby allowing the problem falls into ODE of $f(r)$. 
* **Reference:** Derivation presented here is given by Landau and Lifshitz {cite:p}`Landau1987` (Chap. 2), but the author broke down the math path for students. See the textbook for more elegant logical strucutre. 
```

The Navier-Stokes equation for incompressible fluids is given by
```{math}
:label: eq:StokesDrag_nonref_0
	\rho \frac{\partial \mathbf{v}}{\partial t} + \rho \mathbf{v} \cdot \nabla \mathbf{v} = - \nabla p + \mu \nabla^{2} \mathbf{v}
```
For steady flows, 
```{math}
:label: eq:StokesDrag_nonref_1
	\rho \mathbf{v} \cdot \nabla \mathbf{v} = - \nabla p + \mu \nabla^{2} \mathbf{v}
```
When the Reynolds number is sufficiently small, the advection term can be omitted. Hence, the viscous terms balances with the pressure gradient: 
```{math}
:label: eq:Stokes_eq_Stokes-equation
	\mu \nabla^{2} \mathbf{v} - \nabla p = 0
```
Taking $rot$ yields, 
```{math}
:label: eq:StokesDrag_nonref_2
	\nabla \times \nabla^{2} \mathbf{v} = 0
```
since $\nabla \times \nabla p = 0$ by the vector identity $\nabla \times \nabla \text{(any scalar)}$ (See Appendix {ref}`app_identities` in which some vector identities frequently used in handling equations are given). Then, the order of the differential operators can be exchanged as 
```{math}
:label: eq:StokesDrag_nonref_3
	\nabla \times \nabla^{2} \mathbf{v} 
	\rightarrow \epsilon_{ijk} \frac{\partial }{\partial x_{j}} \frac{\partial^{2} }{\partial x_{m} \partial x_{m}} v_{k} 
	= \frac{\partial^{2} }{\partial x_{m} \partial x_{m}} \epsilon_{ijk} \frac{\partial v_{k}}{\partial x_{j}} 
```
Thus, 
```{math}
:label: eq:Stokes_eq_laplacian-rot-v
	\nabla^{2} \nabla \times \mathbf{v} = 0
```

```{figure} ../fig/Stokes-problem-setting.pdf
:name: Stokes_Solid sphere in uniform flow
Solid sphere in uniform flow
```

Suppose that a solid sphere of radius $a$ is fixed in a uniform flow and the far field velocity is given by $\mathbf{u}$, which is constant ({numref}`Stokes_Solid sphere in uniform flow`). The velocity field about the sphere can therefore be written as a superposition of $\mathbf{u}$ and perturbation $\mathbf{v}'$: 
```{math}
:label: eq:StokesDrag_nonref_4
	\mathbf{v} = \mathbf{v}' + \mathbf{u}
```
Since $\nabla \cdot \mathbf{v} = 0$ and $\nabla \cdot \mathbf{u} = 0$, taking $div$ of this equation yields 
```{math}
:label: eq:StokesDrag_nonref_5
	\nabla \cdot \mathbf{v}' = 0
```
Considering the vector identity 
```{math}
:label: eq:Stokes_eq_div-rot-vector=0
	\nabla \cdot \nabla \times \text{(any vector)} = 0
```
$\mathbf{v}'$ can be written as the rotation of a vector potential. Therefore, we may write 
```{math}
:label: eq:StokesDrag_nonref_6
	\mathbf{v}' = \nabla \times \mathbf{A}
```
where $\mathbf{A}$ is a vector potential and $\nabla \times \mathbf{A} \rightarrow 0$ as $r \rightarrow \infty$. Here $r$ is the radial coordinate and the origin of the coordinate system is located at the center of the sphere. The vector potential is an axial vector and depends on the radial vector $\mathbf{r}$ and $\mathbf{u}$, which are both polar vectors and it should be noted that a cross product between two polar vectors becomes an axial vector (see Appendix {ref}`app_pseudo_vector`). Considering the boundary conditions, $\mathbf{v} = 0~(\nabla \times \mathbf{A} = -\mathbf{u})$ at $r = a$ and $\mathbf{v} \rightarrow \mathbf{u}$ at $r \rightarrow \infty$, $\mathbf{A}$ should be proportional to $\mathbf{u}$. Therefore, it should have the form of $\mathbf{A} = g(r) \mathbf{e}_{r} \times \mathbf{u}$, where $\mathbf{e}_{r} = \mathbf{r}/r$. Setting $g(r) = df/dr$, 
```{math}
:label: eq:StokesDrag_nonref_7
	\nabla f = \frac{df}{dr} \nabla r = \frac{df}{dr} \mathbf{e}_{r} = g(r) \mathbf{e}_{r}
```
Therefore, 
```{math}
:label: eq:StokesDrag_nonref_8
	\mathbf{A} = \nabla f \times \mathbf{u}
```
Since $\mathbf{u}$ is constant, 
```{math}
:label: eq:StokesDrag_nonref_9
	\mathbf{A} 
	= \nabla f \times \mathbf{u}
	\rightarrow \epsilon_{ijk} \frac{\partial f}{\partial x_{j}} u_{k}
	= \epsilon_{ijk} \frac{\partial f u_{k}}{\partial x_{j}} 
	\rightarrow \nabla \times ( f \mathbf{u} )
```
The velocity is thus given by 
```{math}
:label: eq:Stokes_eq_rot-rot-fu+u
	\mathbf{v} = \nabla \times \nabla \times ( f \mathbf{u} ) + \mathbf{u}
```
Taking $rot$ of this equation gives 
```{math}
:label: eq:StokesDrag_nonref_10
	\nabla \times \mathbf{v} 
	= \nabla \times \nabla \times \nabla \times ( f \mathbf{u} ) + \nabla \times \mathbf{u}
	= \nabla \times \nabla \times \nabla \times ( f \mathbf{u} )
```
since $\nabla \times \mathbf{u} = 0$. Using the vector identity 
```{math}
:label: eq:StokesDrag_nonref_11
	\nabla \times \nabla \times (\text{any vector}) = \nabla (\nabla \cdot (\text{any vector})) - \nabla^{2} (\text{any vector})
```
we have 
```{math}
:label: eq:StokesDrag_nonref_12
	\nabla \times \mathbf{v} 
	= \nabla \{ \nabla \cdot ( \nabla \times (f \mathbf{u}) ) \} - \nabla^{2} ( \nabla \times f \mathbf{u} )
	= - \nabla^{2} ( \nabla \times f \mathbf{u} )
```
where the first term in the second equation vanishes due to the identity Eq. {eq}`eq:Stokes_eq_div-rot-vector=0`. Taking $\nabla^{2}$ of this equation yields 
```{math}
:label: eq:StokesDrag_nonref_13
	\nabla^{2} \nabla \times \mathbf{v} 
	= - \nabla^{2} \nabla^{2} ( \nabla \times f \mathbf{u} )
```
The Laplacian and the rotation in the L.H.S. is exchangeable, i.e., $\nabla^{2} \nabla \times \mathbf{v} = \nabla \times \nabla^{2} \mathbf{v}$. However, this is zero due to Eq. {eq}`eq:Stokes_eq_laplacian-rot-v`. Hence, 
```{math}
:label: eq:StokesDrag_nonref_14
	\nabla^{2} \nabla^{2} ( \nabla \times f \mathbf{u} ) = 0
```
Writing the L.H.S. with components, 
```{math}
:label: eq:StokesDrag_nonref_15
\begin{split}
	\frac{\partial^{2}}{\partial x_{m} \partial x_{m}} \frac{\partial^{2}}{\partial x_{n} \partial x_{n}} \epsilon_{ijk} \frac{\partial f u_{k}}{\partial x_{j}}
	&= \epsilon_{ijk} \left( \frac{\partial^{2}}{\partial x_{m} \partial x_{m}} \frac{\partial^{2}}{\partial x_{n} \partial x_{n}} \frac{\partial f}{\partial x_{j}} \right) u_{k} \\
	&\rightarrow ( \nabla^{2} \nabla^{2} \nabla f ) \times \mathbf{u} 
\end{split}
```
Since $\mathbf{u}$ is non-zero, we obtain the following equation for $f$: 
```{math}
:label: eq:StokesDrag_nonref_16
	\nabla^{2} \nabla^{2} \nabla f = 0
```
The gradient operator can be moved to the left, i.e., 
```{math}
:label: eq:StokesDrag_nonref_17
	\nabla \nabla^{2} \nabla^{2} f = 0
```
and this can be immediately integrated:
```{math}
:label: eq:StokesDrag_nonref_18
	\nabla^{2} \nabla^{2} f = \text{const.}
```
However, $g(r) = df/dr \rightarrow 0$ as $r \rightarrow \infty$, the constant on the R.H.S. should be zero. Therefore, 
```{math}
:label: eq:Stokes_eq_nabla2-nabla2-f
	\nabla^{2} \nabla^{2} f = 0
```
This is the equation we have to solve to obtain the functional form of $f$. 

In the spherical coordinates system (Appendix {ref}`app_nseq_in_polar_sys`), 
```{math}
:label: eq:StokesDrag_nonref_19
	\frac{1}{r^{2}} \frac{d}{dr} \left( r^{2} \frac{d}{dr} \nabla^{2} f \right) = 0
```
Integrating this gives 
```{math}
:label: eq:Stokes_eq_solution-of-nabla2f
	\nabla^{2} f = - \frac{c_{1}}{r} + c_{2}
```
Since $\mathbf{v}' \rightarrow 0$ as $r \rightarrow \infty$, $c_{2} = 0$. 
```{math}
:label: eq:StokesDrag_nonref_20
	\frac{1}{r^{2}} \frac{d}{dr} \left( r^{2} \frac{df}{dr} \right) = - \frac{c_{1}}{r}
```
Solving this equation for $f$ gives 
```{math}
:label: eq:StokesDrag_nonref_21
	f = - \frac{c_{1}}{2} r - \frac{c_{3}}{r} + c_{4}
```
Since $c_{4}$ does not contribute to $\mathbf{v}'$, we choose $c_{4} = 0$. Setting $\alpha = -c_{1}/2$ and $\beta = - c_{3}$, 
```{math}
:label: eq:Stokes_eq_f-solution-Stokes
	f = \alpha r + \frac{\beta}{r}
```
and 
```{math}
:label: eq:Stokes_eq_solution-of-nabla2f-modified
	\nabla^{2} f = \frac{2 \alpha}{r}
```

We are now ready to calculate the functional form of $\mathbf{v}$ by substituting $f$ into Eq. {eq}`eq:Stokes_eq_rot-rot-fu+u`, which can be transformed as 
```{math}
:label: eq:StokesDrag_nonref_22
\begin{split}
	\nabla \times \nabla \times ( f \mathbf{u} ) + \mathbf{u}
	&= \nabla ( \nabla \cdot f \mathbf{u} ) - \nabla^{2} ( f \mathbf{u} ) + \mathbf{u} 
	= \nabla ( \nabla \cdot f \mathbf{u} ) - ( \nabla^{2} f ) \mathbf{u} + \mathbf{u} \\
	&= \nabla ( \nabla \cdot f \mathbf{u} ) - \frac{2 \alpha \mathbf{u}}{r} + \mathbf{u}
\end{split}
```
where Eq. {eq}`eq:Stokes_eq_solution-of-nabla2f-modified` was substituted into the second term in the third equation. In the component form, the right-most equation is 
\begin{equation*}
	\nabla ( \nabla \cdot f \mathbf{u} ) - \frac{2 \alpha \mathbf{u}}{r} + \mathbf{u}
	\rightarrow \frac{\partial}{\partial x_{i}} \frac{\partial f u_{k}}{\partial x_{k}} - \frac{2 \alpha u_{i}}{r} + u_{i}
\end{equation*}
With help of the identity $\nabla r^{n} = n r^{n-1} \mathbf{e}_{r} = n r^{n-2} \mathbf{r}$, the first term can be rewritten as 
```{math}
:label: eq:StokesDrag_nonref_23
\begin{split}
	\frac{\partial}{\partial x_{i}} \frac{\partial f u_{k}}{\partial x_{k}}
	&= u_{k} \frac{\partial}{\partial x_{i}} \left( \frac{d f}{d r} \frac{\partial r}{\partial x_{k}} \right)
	= u_{k} \frac{\partial}{\partial x_{i}} \left( \frac{d f}{d r} \frac{x_{k}}{r} \right)
	= u_{k} \left\{ \frac{d f}{d r} \frac{\partial}{\partial x_{i}} \frac{x_{k}}{r} + \frac{x_{k}}{r} \frac{\partial}{\partial x_{i}} \frac{d f}{d r} \right\} \\
	&= u_{k} \left\{ \frac{d f}{\partial r} \left( \frac{\delta_{ik}}{r} - \frac{x_{i} x_{k}}{r^{3}} \right) + \frac{x_{k}}{r} \frac{\partial r}{\partial x_{i}} \frac{d^{2} f}{d r^{2}} \right\} \\
	&= u_{k} \left\{ \frac{d f}{\partial r} \left( \frac{\delta_{ik}}{r} - \frac{x_{i} x_{k}}{r^{3}} \right) + \frac{x_{i} x_{k}}{r^{2}} \frac{d^{2} f}{d r^{2}} \right\}
\end{split}
```
Using Eq. {eq}`eq:Stokes_eq_f-solution-Stokes` ($df/dr = \alpha - \beta/r^{2}$) gives 
```{math}
:label: eq:StokesDrag_nonref_24
	\frac{\partial}{\partial x_{i}} \frac{\partial f u_{k}}{\partial x_{k}}
	= - \alpha \left( \frac{u_{k} x_{k} x_{i}}{r^{3}} - \frac{u_{i}}{r} \right) + \beta \left( \frac{3 u_{k} x_{k} x_{i}}{r^{5}} - \frac{u_{i}}{r^{3}} \right)
```
Substituting this result into the first term gives
```{math}
:label: eq:StokesDrag_nonref_25
	\frac{\partial}{\partial x_{i}} \frac{\partial f u_{k}}{\partial x_{k}} - \frac{2 \alpha u_{i}}{r} + u_{i}
	= u_{i} - \alpha \left( \frac{u_{k} x_{k} x_{i}}{r^{3}} + \frac{u_{i}}{r} \right) + \beta \left( \frac{3 u_{k} x_{k} x_{i}}{r^{5}} - \frac{u_{i}}{r^{3}} \right) 
```
In the vector form, 
```{math}
:label: eq:StokesDrag_nonref_26
	\mathbf{v} = \mathbf{u} - \alpha \frac{\mathbf{u} + (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r}}{r} + \beta \frac{ 3 (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r} - \mathbf{u}}{r^{3}}
```
We determine the constants, $\alpha$ and $\beta$, by applying the boundary condition at the solid surface: $\mathbf{v} = 0$ at $r = a$. 
```{math}
:label: eq:StokesDrag_nonref_27
	\mathbf{u} - \alpha \frac{\mathbf{u} + (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r}}{a} + \beta \frac{ 3 (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r} - \mathbf{u}}{a^{3}} = 0
```
Factorizing this yields 
```{math}
:label: eq:StokesDrag_nonref_28
	\left( 1 - \frac{\alpha}{a} - \frac{\beta}{a^{3}} \right) \mathbf{u} + \left( - \frac{\alpha}{a} + \frac{3 \beta}{a^{3}} \right) (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r} = 0
```
The coefficients of $\mathbf{u}$ and $(\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r}$ must be zero, yielding the simultaneous equations: 
```{math}
:label: eq:StokesDrag_nonref_29
\begin{split}
	&1 - \alpha/a - \beta/a^{3} = 0 \\
	&- \alpha/a + 3 \beta/a^{3} = 0 	
\end{split}
```
Solving the equations gives $\alpha = 3a/4$ and $\beta = a^{3}/4$. Thus, 
```{math}
:label: eq:StokesDrag_nonref_30
	f = \frac{3a}{4} r + \frac{a^{3}}{4r}
```
The velocity field is then given by 
```{math}
:label: eq:StokesDrag_nonref_31
	\mathbf{v} = \mathbf{u} - \frac{3a}{4} \frac{\mathbf{u} + (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r}}{r} + \frac{a^{3}}{4} \frac{ 3 (\mathbf{u} \cdot \mathbf{e}_{r}) \mathbf{e}_{r} - \mathbf{u}}{r^{3}}
```
The sum of the second and the third terms corresponds to $\nabla \times \mathbf{A}$ and, obviously, $\nabla \times \mathbf{A} \rightarrow 0$ as $r \rightarrow \infty$. 

Let us check the functional form of the vector potential ({numref}`Stokes_Vector potential`). 
```{math}
:label: eq:StokesDrag_nonref_32
	\mathbf{A} 
	= g(r) \mathbf{e}_{r} \times \mathbf{u} 
	= \frac{df}{dr} \mathbf{e}_{r} \times \mathbf{u} 
	= \left( \frac{3a}{4} - \frac{a^{3}}{4r^{2}} \right) \mathbf{e}_{r} \times \mathbf{u}
```
```{figure} ../fig/Stokes-vector-potential.pdf
:name: Stokes_Vector potential
Vector potential: $\mathbf{A}$ on the $y$ axis (left); $\mathbf{A}$ along a circle on a horizontal plane of $z > 0$ (right).
```
For $r \rightarrow \infty$, 
```{math}
:label: eq:StokesDrag_nonref_33
	\mathbf{A} 
	\rightarrow \frac{3a}{4} \mathbf{e}_{r} \times \mathbf{u}
```
At $r = a$, 
```{math}
:label: eq:StokesDrag_nonref_34
	\mathbf{A} 
	= \frac{a}{2} \mathbf{e}_{r} \times \mathbf{u}
```
Therefore, $|\mathbf{A}|$ increases as $r$ increases. The spherical coordinates are taken to have the following base vectors: 
```{math}
:label: eq:StokesDrag_nonref_35
\begin{split}
&\mathbf{e}_{r} = \sin \theta \cos \varphi \mathbf{e}_{x}+\sin \theta \sin \varphi \mathbf{e}_{y}+\cos \theta \mathbf{e}_{z} \\
&\mathbf{e}_{\theta} = \cos \theta \cos \varphi \mathbf{e}_{x} + \cos \theta \sin \varphi \mathbf{e}_{y} - \sin \theta \mathbf{e}_{z} \\
&\mathbf{e}_{\varphi} = - \sin \varphi \mathbf{e}_{x} + \cos \varphi \mathbf{e}_{y}
\end{split}
```
and the uniform velocity $\mathbf{u}$ directs toward $-z$, where $\theta$ is the polar coordinate and $\varphi$ is the azimuthal coordinate. Note that this definition is different from that used in Landau and Lifshitz. On the $y$ axis ($\theta = \pi/2$), $\mathbf{e}_{r} \times \mathbf{u} = - u \mathbf{e}_{x}$ and $|\mathbf{A}|$ increases with increasing $y$, so that $\nabla \times \mathbf{A}$ produces vectors with direction opposite to $\mathbf{u}$. Especially, at $r = a$, $\nabla \times \mathbf{A} = - \mathbf{u}$ and $\mathbf{v} = 0$. Around the $z$ axis ($\theta \sim 0$), $\mathbf{e}_{r} \times \mathbf{u}$ gives vectors along the $\varphi$ coordinate line. The vector field $\mathbf{e}_{r} \times \mathbf{u}$ along the coordinate line looks rotating in the $+\varphi$ direction, so that, roughly speaking, $\nabla \times \mathbf{A}$ gives vectors directing toward $+z$ so as to retard the flow around the sphere. 

The pressure field can be obtained from Eq. {eq}`eq:Stokes_eq_Stokes-equation`: 
```{math}
:label: eq:StokesDrag_nonref_36
	\nabla p = \mu \nabla^{2} \mathbf{v} 
```
By substituting Eq. {eq}`eq:Stokes_eq_rot-rot-fu+u`, we have
```{math}
:label: eq:StokesDrag_nonref_37
	\nabla p 
	= \mu \nabla^{2} ( \nabla \times \nabla \times ( f \mathbf{u} ) + \mathbf{u} )
	= \mu \nabla^{2} \nabla \times \nabla \times ( f \mathbf{u} )
```
where $\nabla^{2} \mathbf{u} = 0$ was used. Using the identity $\nabla \times \nabla \times (\text{any vector}) = \nabla (\nabla \cdot (\text{any vector})) - \nabla^{2} (\text{any vector})$ and making some interchange in the order of the differential operators yields 
```{math}
:label: eq:StokesDrag_nonref_38
	\nabla p 
	= \nabla \mu \nabla^{2} \nabla \cdot f \mathbf{u} - \mu \mathbf{u} \nabla^{2} \nabla^{2} f
```
However, due to Eq. {eq}`eq:Stokes_eq_nabla2-nabla2-f`, 
```{math}
:label: eq:StokesDrag_nonref_39
	\nabla p = \nabla \mu \nabla^{2} \nabla \cdot f \mathbf{u} 
```
Integrating this equation yields 
```{math}
:label: eq:StokesDrag_nonref_40
	p = \mu \nabla^{2} \nabla \cdot f \mathbf{u} + p_{0}
```
where $p_{0}$ is the far field pressure. The first term on the R.H.S. can be rewritten as 
```{math}
:label: eq:StokesDrag_nonref_41
	\mu \nabla^{2} \nabla \cdot f \mathbf{u}
	\rightarrow \mu \frac{\partial^{2}}{\partial x_{k} \partial x_{k}} \frac{\partial f u_{j}}{\partial x_{j}}
	= \mu u_{j} \frac{\partial }{\partial x_{j}} \frac{\partial^{2} f}{\partial x_{k} \partial x_{k}} 
	\rightarrow \mu \mathbf{u} \cdot \nabla ( \nabla^{2} f )
```
Again we use Eq. {eq}`eq:Stokes_eq_solution-of-nabla2f` for the Laplacian of $f$ and we obtain 
```{math}
:label: eq:StokesDrag_nonref_42
	p = 2 \alpha \mu \mathbf{u} \cdot \nabla \frac{1}{r}+ p_{0}
```
Using $\nabla r^{n} = n r^{n-1} \mathbf{e}_{r}$ and $\alpha = 3a/4$, we have 
```{math}
:label: eq:StokesDrag_nonref_43
	p = p_{0} - \frac{3 \mu a ( \mathbf{u} \cdot \mathbf{e}_{r} )}{2 r^{2}}
```

The drag force acting of the sphere is calculated in the following. The velocity components are (refer {numref}`Stokes_Direction cosine` for the calculation of the dot products between the velocity and the base vectors.) 
```{math}
:label: eq:StokesDrag_nonref_44
\begin{split}
	&v_{r} 
	= \mathbf{v} \cdot \mathbf{e}_{r}
	= \mathbf{u} \cdot \mathbf{e}_{r} \left( 1 - \frac{3a}{2r} + \frac{a^{3}}{2 r^{3}} \right)
	= - u \cos \theta \left( 1 - \frac{3a}{2r} + \frac{a^{3}}{2 r^{3}} \right) \\
	&v_{\theta} 
	= \mathbf{v} \cdot \mathbf{e}_{\theta}
	= \mathbf{u} \cdot \mathbf{e}_{\theta} \left( 1 - \frac{3a}{4r} - \frac{a^{3}}{4 r^{3}} \right)
	= u \sin \theta \left( 1 - \frac{3a}{4r} - \frac{a^{3}}{4 r^{3}} \right)
\end{split}
```
```{math}
:label: eq:Stokes_eq_pressure
	p = p_{0} + \frac{3 \mu a u}{2 r^{2}} \cos \theta
```
```{figure} ../fig/Stokes-velocity-component.pdf
:name: Stokes_Direction cosine
Direction cosine for the base vectors and the unit vector $\mathbf{u}/u$.}
```
Some components of the viscous stress tensor are 
```{math}
:label: eq:StokesDrag_nonref_45
	\tau_{rr} 
	= 2 \mu \frac{\partial v_{r}}{\partial r}
	= - 2 \mu u \cos \theta \left( \frac{3 a}{2 r^{2}} - \frac{3 a^{3}}{2 r^{4}} \right)
```
```{math}
:label: eq:StokesDrag_nonref_46
	\tau_{r\theta} 
	= \mu \left( \frac{1}{r} \frac{\partial v_{r}}{\partial \theta} + \frac{\partial v_{\theta}}{\partial r} - \frac{v_{\theta}}{r} \right)
	= \frac{3 \mu u a^{3}}{2 r^{4}} \sin \theta
```
At $r = a$, 
```{math}
:label: eq:Stokes_eq_p_at_a
	\left. p \right|_{r=a} = p_{0} + \frac{3 \mu u}{2 a} \cos \theta
```
```{math}
:label: eq:Stokes_eq_taurr_at_a
	\left. \tau_{rr} \right|_{r=a} = 0
```
```{math}
:label: eq:Stokes_eq_taurt_at_a
	\left. \tau_{r\theta} \right|_{r=a} = \frac{3 \mu u}{2 a} \sin \theta
```
The force acting on the sphere is given by 
```{math}
:label: eq:StokesDrag_nonref_47
	\mathbf{F}
	= \iint_{S} (-p \mathbf{I} + \boldsymbol{\tau}) \cdot \mathbf{n} dS
```
where $\mathbf{n} = \mathbf{e}_{r}$. The drag $F_{D}$ is the component of $\mathbf{F}$ in the $-z$ direction; hence 
```{math}
:label: eq:StokesDrag_nonref_48
	F_{D}
	= -\mathbf{e}_{z} \cdot \mathbf{F}
	= \iint_{S} (p \mathbf{e}_{z} \cdot \mathbf{I} \cdot \mathbf{e}_{r} -\mathbf{e}_{z} \cdot \boldsymbol{\tau} \cdot \mathbf{e}_{r})  dS
	= \iint_{S} (p \mathbf{e}_{z} \cdot \mathbf{e}_{r} - \mathbf{e}_{z} \cdot \boldsymbol{\tau} \cdot \mathbf{e}_{r})  dS
```
For the pressure term, $\mathbf{e}_{z} \cdot \mathbf{e}_{r} = \cos \theta$. By expanding the viscous stress, we obtain 
```{math}
:label: eq:StokesDrag_nonref_49
\begin{split}
	\mathbf{e}_{z} \cdot \boldsymbol{\tau} \cdot \mathbf{e}_{r}
	&= \mathbf{e}_{z} \cdot ( 
	\tau_{rr} \mathbf{e}_{r} \mathbf{e}_{r} + \tau_{r\theta} \mathbf{e}_{r} \mathbf{e}_{\theta} + \tau_{r\varphi} \mathbf{e}_{r} \mathbf{e}_{\varphi}
	+ \tau_{\theta r} \mathbf{e}_{\theta} \mathbf{e}_{r} + \tau_{\theta \theta} \mathbf{e}_{\theta} \mathbf{e}_{\theta} + \tau_{\theta \varphi} \mathbf{e}_{\theta} \mathbf{e}_{\varphi}
	+ \tau_{\varphi r} \mathbf{e}_{\varphi} \mathbf{e}_{r} + \tau_{\varphi \theta} \mathbf{e}_{\varphi} \mathbf{e}_{\theta} + \tau_{\varphi \varphi} \mathbf{e}_{\varphi} \mathbf{e}_{\varphi}
	 ) \cdot \mathbf{e}_{r} \\
	&= \mathbf{e}_{z} \cdot ( \tau_{rr} \mathbf{e}_{r} + \tau_{\theta r} \mathbf{e}_{\theta} + \tau_{\varphi r} \mathbf{e}_{\varphi} )
	= \tau_{rr} \mathbf{e}_{z} \cdot \mathbf{e}_{r} + \tau_{\theta r} \mathbf{e}_{z} \cdot \mathbf{e}_{\theta} \\
	&= \tau_{rr} \cos \theta - \tau_{\theta r} \sin \theta 
\end{split}
```
where $\tau_{\varphi r} = 0$ because of the symmetry of the flow, and $\mathbf{e}_{z} \cdot \mathbf{e}_{r} = \cos \theta$ and $\mathbf{e}_{z} \cdot \mathbf{e}_{\theta} = -\sin \theta$ were used. Putting this result into the integration yields
```{math}
:label: eq:StokesDrag_nonref_50
	F_{D}
	= \iint_{S} (p \cos \theta - \tau_{rr} \cos \theta + \tau_{\theta r} \sin \theta)  dS
```
Substituting Eqs. {eq}`eq:Stokes_eq_p_at_a`, {eq}`eq:Stokes_eq_taurr_at_a` and {eq}`eq:Stokes_eq_taurt_at_a` into this equation gives 
```{math}
:label: eq:StokesDrag_nonref_51
	F_{D} = \int_{0}^{2 \pi} \int_{0}^{\pi} \left( p_{0} \cos \theta + \frac{3 \mu u}{2 a} \cos^{2} \theta + \frac{3 \mu u}{2 a} \sin^{2} \theta \right) a^{2} \sin \theta d \theta d \varphi 
```
It should be noted that the surface integral of any constant vanishes. Hence $p_{0}$ has no contribution to the results. 
```{math}
:label: eq:StokesDrag_nonref_52
\begin{split}
	F_{D} 
	&= \int_{0}^{2 \pi} \int_{0}^{\pi} \left( \frac{3 \mu u}{2 a} \cos^{2} \theta + \frac{3 \mu u}{2 a} \sin^{2} \theta \right) a^{2} \sin \theta d \theta d \varphi 
	= 3 \pi \mu u a \int_{0}^{\pi} \sin \theta d \theta \\
	&= 6 \pi \mu u a
\end{split}
```
The drag coefficient defined by 
```{math}
:label: eq:StokesDrag_nonref_53
	C_{D} = \frac{F_{D}}{\frac{1}{2} \rho u^{2} \pi a^{2}}
```
is then obtained as 
```{math}
:label: eq:StokesDrag_nonref_54
	C_{D} = \frac{24}{Re}
```
where $Re$ is the Reynolds number defined by 
```{math}
:label: eq:StokesDrag_nonref_55
	Re = \frac{2 \rho u a}{\mu}
```
