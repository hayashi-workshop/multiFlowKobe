(auton_lift)=
# Lift acting on spherical body in inviscid flow with weak shear

```{admonition} Summary
* **Subject:** Shear-induced lift acting on sphere
* **Main conclusion:** Lift coefficient $C_{L} = 1/2$
* **Key idea** Vortex filament of incident shear flow is deformed and the streamwise vorticity component $\omega_{x}$ is induced, which results in lift. 
* **References:** 
	- {cite:t}`Auton1987-hk`: Founder of $C_{L} = 1/2$
	- {cite:t}`Lighthill1956-ov`: Basis of Auton's theory (drift in weak shear)
	- {cite:t}`Lighthill1956-xl`
    - {cite:t}`Darwin1953-vk`: Drift
    - {cite:t}`Legendre1998-pn`: Established $C_{L}$ of sphere in the whole range of $Re$
```

{cite:t}`Auton1987-hk` derived the following well-known result of the lift coefficient $C_{L}$ for a spherical body experiencing weak shear by an inviscid flow:
```{math}
:label: eq:AutonLift_nonref_0
	C_{L} = \frac{1}{2}
```
where the lift force is defined by 
```{math}
:label: eq:AutonLift_nonref_1
	\mathbf{F}_{L} = - C_{L} \rho \frac{4 \pi a^{3}}{3} \left( \mathbf{U} - \mathbf{u}_{0} \right) \times \boldsymbol{\omega}
```
$\mathbf{U}$ is the velocity of the sphere and $\mathbf{u}_{0}$ is the incident velocity on the center of the sphere. {numref}`Auton_Auton-problem-setting` shows a sphere in a weak shear flow of incompressible fluid, for which the velocity field far upstream is given by 
```{math}
:label: eq:AutonLift_nonref_2
	\mathbf{v} = (v_{x}, v_{y}, v_{z}) = (u_{0} + A y, 0, 0)~~~\text{as}~x \rightarrow -\infty
```
where $A$ is the shear rate of the shear flow and is a positive constant. The vorticity of this oncoming flow is 
```{math}
:label: eq:AutonLift_nonref_3
	\boldsymbol{\omega} = (\omega_{x}, \omega_{y}, \omega_{z}) = (0, 0, -A)~~~\text{as}~x \rightarrow -\infty
```
The sphere is fixed ($\mathbf{U} = 0$), so that, 
```{math}
:label: eq:AutonLift_nonref_4
	\mathbf{F}_{L} = C_{L} \rho \frac{4 \pi a^{3}}{3} \mathbf{u}_{0} \times \boldsymbol{\omega}
	= \left( 0, \frac{2 \pi a^{3}}{3} u_{0} A, 0 \right)
```
This result was obtained by means of numerical integration of the pressure force acting on the sphere; however, a physical argument based on the momentum theorem was also given. It is clear from the  formulae of the lift, knowledge on the vorticity is required to understand the Auton lift. See Appendix {ref}`app_vorticity_equation` for the vorticity equation, Appendix {ref}`app_Helmholtz_law` for Helmholtz's law of vortex motion, and Appendix {ref}`app_Biot_Savart` for the Biot-Savart law, if you need.

```{figure} ../fig/Auton-problem-setting.png
:name: Auton_Auton-problem-setting
Sphere in weak shear flow.
```

Let us follow the former analysis by Auton. The pressure distribution at the sphere surface required for calculation the lift can be obtained by Bernoulli's equation once the velocity distribution is known. The perturbation in the velocity field due to weak shear is assumed to be small, i.e., 
```{math}
:label: eq:AutonLift_nonref_5
	\frac{a A}{u_{0}} \ll 1
```
The velocity field is therefore written as the superposition of a primary irrotational flow $\mathbf{V}$ and a small perturbation $\mathbf{v}'$ which is proportional to $a A$:
```{math}
:label: eq:AutonLift_nonref_6
	\mathbf{v} = \mathbf{V} + \mathbf{v}'
```
The primary flow is irrotational. Therefore,  
```{math}
:label: eq:AutonLift_nonref_7
	\nabla \times \mathbf{V} = 0
```
and boundary conditions for $\mathbf{V}$ are given by 
```{math}
:label: eq:AutonLift_nonref_8
	\mathbf{n} \cdot \mathbf{V}  = 0~~~~\text{at}~r = a
```
```{math}
:label: eq:AutonLift_nonref_9
	\mathbf{V} = (u_{0}, 0, 0)~~~\text{as}~r \rightarrow \infty
```
The stream function of the primary flow is given by potential flow theory, i.e., 
```{math}
:label: eq:Auton_eq_psi-primary
	\psi = \frac{1}{2} r^{2} u_{0} \left( 1 - \frac{a^{3}}{r^{3}} \right) \sin^{2} \theta
```
from which we have
```{toggle}
Flows having axial symmetry can be expressed by Stokes' stream function, for which the velocity components are given by 

$v_{r} = \frac{1}{r^{2} \sin \theta} \frac{\partial \psi}{\partial \theta},~~~~v_{\theta} = - \frac{1}{r \sin \theta} \frac{\partial \psi}{\partial r}$
```
```{math}
:label: eq:Auton_eq_Vp-primary
\begin{split}
	&V_{r} = u_{0} \cos \theta \left( 1 - \frac{a^{3}}{r^{3}} \right) 
	&V_{\theta} = - u_{0} \sin \theta \left( 1 + \frac{a^{3}}{2 r^{3}} \right)
	&V_{\varphi} = 0 
\end{split}
```
$\psi = \text{const.}$ represents a streamline. It is convenient to absorb the factor $u_{0}/2$ into the constant, giving 
```{math}
:label: eq:Auton_eq_streamline
	r^{2} \left( 1 - \frac{a^{3}}{r^{3}} \right) \sin^{2} \theta	 = \hat{\rho}_{0}^{2}
```
since $\hat{\rho}_{0}$ represents the distance between the streamline and the $x$ axis in the far upstream of the sphere.
```{toggle}
Taking $a/r \rightarrow 0$ yields $\hat{\rho}_{0} = r \sin \theta$. 
```
Since the flow is steady, the streamline corresponds to the particle path. Therefore, the fluid particle at $\hat{\rho}_{0}$ in the far upstream moves along this streamline. In this context, the initial coordinate $\hat{\rho}_{0}$ can be regarded as a label of fluid particle. 

By substituting $\mathbf{v} = \mathbf{V} + \mathbf{v}'$ into the vorticity equation
```{math}
:label: eq:AutonLift_nonref_10
	\mathbf{v} \cdot \nabla \boldsymbol{\omega} = \boldsymbol{\omega} \cdot \nabla \mathbf{v}
```
we have
```{math}
:label: eq:AutonLift_nonref_11
	( \mathbf{V} + \mathbf{v}' ) \cdot \nabla \boldsymbol{\omega} = \boldsymbol{\omega} \cdot \nabla ( \mathbf{V} + \mathbf{v}' )
```
By omitting the second order terms, we obtain
```{toggle}
By scaling the velocities and vorticity as $\mathbf{V}^{*} = \mathbf{V} / u_{0}$, $\mathbf{v}'^{*} = \mathbf{v}' / (aA)$, $\boldsymbol{\omega}^{*} = \boldsymbol{\omega} / A$ and $\nabla^{*} = a \nabla$, we have

$( \mathbf{V} + \mathbf{v}' ) \cdot \nabla \boldsymbol{\omega} = \frac{u_{0}^{2}}{a^{2}} \left\{ \frac{a A}{u_{0}} \mathbf{V}^{*} + \left( \frac{a A}{u_{0}} \right)^{2} \mathbf{v}'^{*} \right\} \cdot \nabla^{*} \boldsymbol{\omega}^{*}$
```
```{math}
:label: eq:Auton_eq_vorticity-eq-linearlized
	\mathbf{V} \cdot \nabla \boldsymbol{\omega} = \boldsymbol{\omega} \cdot \nabla \mathbf{V}
```
This equation represents that *the vorticity is advected by the primary flow while experiencing stretching also by the primary flow*. {cite:t}`Lighthill1956-ov` showed the solution of $\boldsymbol{\omega}$ expressed in terms of the so-called *drift function*, $t$, which is defined by 
```{math}
:label: eq:AutonLift_nonref_12
	dt = \frac{dx}{V_{x}} = \frac{dy}{V_{y}} = \frac{dz}{V_{z}}
```
with 
```{math}
:label: eq:AutonLift_nonref_13
	t - \frac{x}{u_{0}} \rightarrow 0~~~~\text{as}~x \rightarrow -\infty
```
Isosurfaces of $t = \text{const.}$ represent the deformation of material surfaces initially perpendicular to the $x$ axis in the far upstream. In the spherical polar coordinate system, 
```{math}
:label: eq:AutonLift_nonref_14
	dt = \frac{dr}{V_{r}} = \frac{rd\theta}{V_{\theta}} 
```
Using Eq. {eq}`eq:Auton_eq_Vp-primary`, we have
```{math}
:label: eq:Auton_eq_drift-integrand
	u_{0} dt = - \frac{rd\theta}{\sin \theta \left( 1 + \frac{a^{3}}{2 r^{3}} \right)} 
```
By integrating this equation, we can obtain the drift function as $t(\hat{\rho}_{0}, \theta)$.
```{toggle}
The form of Eq. {eq}`eq:Auton_eq_drift-integrand` may meet singularities at $\theta = 0$ and $\pi$, which cause difficulties in numerical integration. Cousins (1970) therefore proposed the following form to avoid the difficulty: 

$u_{0} dt = \left\{ - \frac{\hat{\rho}_{0}}{\sin^{2} \theta} + \left( \frac{\hat{\rho}_{0}}{\sin^{2} \theta} - \frac{r}{\sin \theta \left( 1 + a^{3}/2 r^{3} \right)} \right) \right\} d\theta$

Integrating this equation from $\theta = \pi$~($x \rightarrow -\infty$) to $0$~($x \rightarrow \infty$) gives 

$u_{0} t = \frac{\hat{\rho}_{0}}{\tan \theta} - \int_{\theta}^{\pi} \left( \frac{\hat{\rho}_{0}}{\sin^{2} \theta'} - \frac{r'}{\sin \theta' \left( 1 + a^{3}/2 r'^{3} \right)} \right) d\theta'$

$1 / \sin \theta'$ diverges at $\theta = 0$ and $\pi$, but the sum of the two terms of the integrand approaches zero at these limits, so that the contributions at $\theta = 0$ and $\pi$ can be removed when numerical integration is carried out. The parameter $r'$ also changes during the integration for $\theta'$. By the streamline equation, Eq. {eq}`eq:Auton_eq_streamline`, 

$r'^{2} \left( 1 - \frac{a^{3}}{r'^{3}} \right) = \frac{\hat{\rho}_{0}^{2}}{\sin^{2} \theta'}$

$r'$ can be obtained as the positive root of this equation for given $\theta'$. 
```
Then, the vorticity is given by (see derivation by Lighthill in Appendix {ref}`app_drift_function`)
```{math}
:label: eq:Auton_eq_vorticity_p
\begin{split}
	&\omega_{r} = A \sin \varphi \left( V_{r} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta} - \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{\theta} \right) \\
	&\omega_{\theta} = A \sin \varphi \left( V_{\theta} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta} \right) \\
	&\omega_{\varphi} = - A \cos \varphi \frac{r \sin \theta}{\hat{\rho}_{0}} 
\end{split}
```
It is worth noting that $\omega_{\varphi}$ does not depend on $t$; the factor $r \sin \theta / \hat{\rho}_{0} = \hat{\rho} d \varphi / \hat{\rho}_{0} d\varphi$ represents the stretching rate of vorticity (fluid material) element, so the primary flow causes only stretching of the ring vorticity, $\omega_{\varphi}$. {numref}`Auton_Auton-vortex-line` shows a vortex line coming from upstream stretched by the primary flow while advected toward downstream. 

```{figure} ../fig/Auton-vortex-line.png
:name: Auton_Auton-vortex-line
Vortex line stretched by primary flow. $u_{0} = 1$, $a = 1$, the initial position of the line element $y_{0} = 0.1$.
```

{cite:t}`Lighthill1956-xl` pointed out that the Biot-Savart field should be constructed by the vorticity change
```{math}
:label: eq:AutonLift_nonref_16
	\boldsymbol{\omega}_{1}	= \boldsymbol{\omega} - \boldsymbol{\omega}_{0}
```
and the Biot-Savart integral does not converge if the uniform oncoming vorticity $\boldsymbol{\omega}_{0} = (0, 0, -A)$ is not subtracted. The orthogonal matrix 
```{math}
:label: eq:AutonLift_nonref_17
	\mathbf{M}^{-1}
	=
	\left(
	\begin{array}{c}
		\mathbf{e}_{r} \\
		\mathbf{e}_{\theta} \\
		\mathbf{e}_{\varphi} \\
	\end{array}
	\right)
	=
	\left(
	\begin{array}{rrr}
		\sin \theta \cos \varphi &\sin \theta \sin \varphi &\cos \theta \\
		\cos \theta \cos \varphi &\cos \theta \sin \varphi &-\sin \theta \\
		-\sin \varphi &\cos \varphi &0
	\end{array}
	\right)
```
transforms the Cartesian components to the components in the spherical polar coordinate system. With this matrix, 
```{math}
:label: eq:AutonLift_nonref_18
	\boldsymbol{\omega}_{0} \rightarrow 
	\left( 
		\begin{array}{c}
			\omega_{0r} \\
			\omega_{0\theta} \\
			\omega_{0\varphi} 
		\end{array}
	\right)
	=
	\mathbf{M}^{-1}
	\left( 
		\begin{array}{c}
			\omega_{0y} \\
			\omega_{0z} \\
			\omega_{0x} 
		\end{array}
	\right)
	=
	\mathbf{M}^{-1}
	\left( 
		\begin{array}{r}
			0 \\
			-A \\
			0 
		\end{array}
	\right)
	=
	\left( 
		\begin{array}{c}
			-A \sin \varphi \sin \theta \\
			-A \sin \varphi \cos \theta \\
			-A \cos \varphi
		\end{array}
	\right)
```
Thus, 
```{math}
:label: eq:Auton_eq_vorticity_1p
\begin{split}
	&\omega_{1r} = A \sin \varphi \left\{ \left( V_{r} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta} - \left( \frac{\partial r}{\partial \hat{\rho}_{0}} \right)_{\theta} \right) + \sin \theta \right\} \\
	&\omega_{1\theta} = A \sin \varphi \left\{ \left( V_{\theta} \left( \frac{\partial t}{\partial \hat{\rho}_{0}} \right)_{\theta} \right) + \cos \theta \right\} \\
	&\omega_{1\varphi} = A \cos \varphi \left\{ - \frac{r \sin \theta}{\hat{\rho}_{0}} + 1 \right\}
\end{split}
```

The secondary velocity field $\mathbf{v}'$ can then be constructed from four parts: 
\begin{itemize}
	\item the uniform shear flow perturbation $\mathbf{v}_{0}^{e} = (Ay, 0, 0)$, 
	\item an irrotational flow field, $\mathbf{v}_{0}^{i}$, enforcing $\mathbf{v}_{0}~(=\mathbf{v}_{0}^{e} + \mathbf{v}_{0}^{i})$ so as to satisfy the boundary condition $\mathbf{n} \cdot \mathbf{v}_{0} = \mathbf{n} \cdot ( \mathbf{v}_{0}^{e} + \mathbf{v}_{0}^{i} ) = 0$ at $r = a$, 
	\item the Biot-Savart field, $\mathbf{v}_{1}^{e}$, by $\boldsymbol{\omega}_{1}$, 
	\item an irrotational flow field, $\mathbf{v}_{1}^{i}$, enforcing $\mathbf{v}_{1}~(=\mathbf{v}_{1}^{e} + \mathbf{v}_{1}^{i})$ so as to satisfy the boundary condition $\mathbf{n} \cdot \mathbf{v}_{1} = \mathbf{n} \cdot ( \mathbf{v}_{1}^{e} + \mathbf{v}_{1}^{i} ) = 0$ at $r = a$. 
\end{itemize}
The first one in the spherical polar coordinate system is written as 
```{math}
:label: eq:AutonLift_nonref_19
	\mathbf{v}_{0}^{e} \rightarrow 
	\left( 
		\begin{array}{c}
			v_{0r}^{e} \\
			v_{0\theta}^{e} \\
			v_{0\varphi}^{e} 
		\end{array}
	\right)
	=
	\mathbf{M}^{-1}
	\left( 
		\begin{array}{c}
			v_{0y} \\
			v_{0z} \\
			v_{0x} 
		\end{array}
	\right)
	=
	\mathbf{M}^{-1}
	\left( 
		\begin{array}{c}
			0 \\
			0 \\
			A r \sin \theta \cos \varphi 
		\end{array}
	\right)
	=
	\left( 
		\begin{array}{c}
			A r \sin \theta \cos \theta \cos \varphi \\
			-A r \sin^{2} \theta \cos \varphi \\
			0
		\end{array}
	\right)
```
$\mathbf{v}_{0}^{i}$ is deduced from the following velocity potential:
```{math}
:label: eq:AutonLift_nonref_20
	\phi_{0}^{i} = \frac{A a^{5}}{3 r^{3}} \sin \theta \cos \theta \cos \varphi
```
from which
```{math}
:label: eq:AutonLift_nonref_21
	\mathbf{v}_{0}^{i}
	= \nabla \phi_{0}^{i}
	= \frac{\partial \phi}{\partial r} \mathbf{e}_{r}
	+ \frac{1}{r} \frac{\partial \phi}{\partial \theta} \mathbf{e}_{\theta}
	+ \frac{1}{r \sin \theta} \frac{\partial \phi}{\partial \varphi} \mathbf{e}_{\varphi}
```
and 
```{math}
:label: eq:AutonLift_nonref_22
\begin{split}
	&v_{0r}^{i} = - \frac{A a^{5}}{r^{4}} \sin \theta \cos \theta \cos \varphi \\
	&v_{0\theta}^{i} = \frac{A a^{5}}{3 r^{4}} \cos \varphi \cos 2 \theta \\
	&v_{0\varphi}^{i} = - \frac{A a^{5}}{3 r^{4}} \cos \theta \sin \varphi 
\end{split}
```
Hence, 
```{math}
:label: eq:AutonLift_nonref_23
\begin{split}
	&v_{0r} = A r \sin \theta \cos \theta \cos \varphi \left( 1 - \frac{a^{5}}{r^{5}} \right) \\
	&v_{0\theta} = A r \cos \varphi \left( -\sin^{2} \theta + \frac{a^{5}}{3 r^{5}} \cos 2 \theta \right) \\
	&v_{0\varphi} = - \frac{A a^{5}}{3 r^{4}} \cos \theta \sin \varphi 
\end{split}
```
It is obvious that $v_{0r} = 0$ at $r = a$. 

```{figure} ../fig/Auton-image-system.png
:name: Auton_Auton-image-system
Image system of vorticity

The Biot-Savart field $\mathbf{v}_{1}^{e}$ induced by $\boldsymbol{\omega}_{1}$ is given as
```{math}
:label: eq:AutonLift_nonref_24
	\mathbf{v}_{1}^{e} (\mathbf{r}) = \frac{1}{4 \pi} \iiint_{V'} \frac{\boldsymbol{\omega}_{1}(\mathbf{r}') \times (\mathbf{r} - \mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|^{3}} dV'
```
{cite:t}`Lighthill1956-xl` showed that $\mathbf{v}_{1}^{i}$ is given as the Biot-Savart field of a system of image vorticity *inside* the sphere, that is, for $\boldsymbol{\omega_{1}} dV$ at $(r, \theta, \varphi)$ external to the sphere, an image system of vorticity at the image point $(a^{2}/r, \theta, \varphi)$
```{math}
:label: eq:AutonLift_nonref_25
	\boldsymbol{\omega}_{i} dV = \left( \frac{a}{r} \omega_{1r}, - \frac{a}{r} \omega_{1\theta}, - \frac{a}{r} \omega_{1\varphi} \right) dV
```
and a uniform line vortex of strength 
```{math}
:label: eq:AutonLift_nonref_26
	\boldsymbol{\omega}_{l} dV = \left( - \frac{1}{a} \omega_{1r}, 0, 0 \right) dV
```
between the center of the sphere and the position of the image vorticity (see {numref}`Auton_Auton-image-system`). The position, $\mathbf{r}'_{i}$, of the image system for $\mathbf{r}'$ can be written in the vectorial form as 
\begin{equation*}
	\mathbf{r}'_{i} = \frac{a^{2}}{r'} \mathbf{e}_{r'}
\end{equation*}
where 
```{math}
:label: eq:AutonLift_nonref_27
	\mathbf{e}_{r'} = \frac{\mathbf{r}'}{r'}
```
At $\mathbf{r}'_{i}$, the image vorticity can be written as 
```{math}
:label: eq:AutonLift_nonref_28
	\boldsymbol{\omega}_{i}
	= - \frac{a}{r'} \left\{ \boldsymbol{\omega}_{1}(\mathbf{r}') - 2 ( \boldsymbol{\omega}_{1}(\mathbf{r}') \cdot \mathbf{e}_{r'} ) \mathbf{e}_{r'} \right\}
```
Therefore, the contribution of $\boldsymbol{\omega}_{i}$ to the Biot-Savart integral is expressed by (Appendix {ref}`app_Biot_Savart_line_vorticity`)
```{math}
:label: eq:AutonLift_nonref_29
	\frac{1}{4 \pi} \iiint_{V'} \frac{\boldsymbol{\omega}_{i} \times (\mathbf{r} - \mathbf{r}'_{i})}{|\mathbf{r} - \mathbf{r}'_{i}|^{3}} dV'	
```
Then the uniform line vortex is expressed as 
```{math}
:label: eq:AutonLift_nonref_30
	\boldsymbol{\omega}_{l} = - \frac{\boldsymbol{\omega}_{1}(\mathbf{r}') \cdot \mathbf{e}_{r'}}{a}
```
It should be noted that the line vorticity is the strength of vorticity per unit length. Being similar to the Biot-Savart integral for a line current, we can write the Biot-Savart integral for the uniform line vortex as (see {ref}`app_Biot_Savart_line_vorticity`)
```{math}
:label: eq:AutonLift_nonref_31
	\frac{1}{4 \pi} \iiint_{V'} \frac{\boldsymbol{\omega}_{l} \times \mathbf{r}}{|\mathbf{r} - (\mathbf{r} \cdot \mathbf{e}_{r'}) \mathbf{e}_{r'}|^{2}} \left( \mathbf{e}_{r} \cdot \mathbf{e}_{r'} - \frac{(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'}{|(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'|} \right) dV'		
```
Thus, 
```{math}
:label: eq:AutonLift_nonref_32
	\mathbf{v}_{1}^{i} (\mathbf{r}) =
	\frac{1}{4 \pi} \iiint_{V'} \left\{ \frac{\boldsymbol{\omega}_{i} \times (\mathbf{r} - \mathbf{r}'_{i})}{|\mathbf{r} - \mathbf{r}'_{i}|^{3}} 
	+ \frac{\boldsymbol{\omega}_{l} \times \mathbf{r}}{|\mathbf{r} - (\mathbf{r} \cdot \mathbf{e}_{r'}) \mathbf{e}_{r'}|^{2}} \left( \mathbf{e}_{r} \cdot \mathbf{e}_{r'} - \frac{(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'}{|(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'|} \right) \right\} dV'
```
and 
```{math}
:label: eq:AutonLift_nonref_33
	\mathbf{v}_{1} (\mathbf{r}) =
	\frac{1}{4 \pi} \iiint_{V'} \left\{ \frac{\boldsymbol{\omega}_{1}(\mathbf{r}') \times (\mathbf{r} - \mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|^{3}} + \frac{\boldsymbol{\omega}_{i} \times (\mathbf{r} - \mathbf{r}'_{i})}{|\mathbf{r} - \mathbf{r}'_{i}|^{3}} 
	+ \frac{\boldsymbol{\omega}_{l} \times \mathbf{r}}{|\mathbf{r} - (\mathbf{r} \cdot \mathbf{e}_{r'}) \mathbf{e}_{r'}|^{2}} \left( \mathbf{e}_{r} \cdot \mathbf{e}_{r'} - \frac{(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'}{|(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'|} \right) \right\} dV'
```

Auton obtained the Biot-Savart field by means of numerical integration, in which some elaborative variable transformation were used to avoid singularities and sharp behaviors of the integrand. Once $\mathbf{v}_{1}$ is obtained, the secondary velocity field can be obtained as 
```{math}
:label: eq:AutonLift_nonref_34
	\mathbf{v}' = \mathbf{v}_{0} + \mathbf{v}_{1}
```
{numref}`Auton_AutonTable5` shows the velocity components of the secondary flow given by Auton. 

```{figure} ../python/AutonTable5.png
:name: Auton_AutonTable5
Secondary velocity at sphere surface produced by vorticity, $v'_{\theta}(a, \theta, 0)$ and $v'_{\varphi}(a, \theta, \pi/2)$.
```

The lift force acting on the sphere is calculated by
```{math}
:label: eq:AutonLift_nonref_35
	\mathbf{F} = \iint_{S} - p \mathbf{n} dS
```
Bernoulli's theorem shows that 
```{math}
:label: eq:AutonLift_nonref_36
	p = p_{0} + \frac{1}{2} \rho u_{0}^{2} - \frac{1}{2} \rho \mathbf{v} \cdot \mathbf{v}
```
where $p_{0}$ is the pressure in the far upstream on the stagnation streamline. For the velocity square, 
```{math}
:label: eq:AutonLift_nonref_37
	\mathbf{v} \cdot \mathbf{v}
	= ( \mathbf{V} + \mathbf{v}' ) \cdot ( \mathbf{V} + \mathbf{v}' )
	= ( V_{r} + v'_{r} )^{2} + ( V_{\theta} + v'_{\theta} )^{2} + ( V_{\varphi} + v'_{\varphi} )^{2}
```
Since $V_{r} = v_{r} = 0$ at $r = a$ and $V_{\varphi} = 0$ due to symmetry this reduces to 
```{math}
:label: eq:AutonLift_nonref_38
	\mathbf{v} \cdot \mathbf{v}
	= V_{\theta}^{2} + 2 V_{\theta} v'_{\theta} + O((aA)^{2})
```
Therefore, to the first order, 
```{math}
:label: eq:AutonLift_nonref_39
	p = p_{0} + \frac{1}{2} \rho u_{0}^{2} - \frac{1}{2} \rho V_{\theta}^{2} - \rho V_{\theta} v'_{\theta} 
```
However, the first two terms are constant and have no contributions to the integral.
```{toggle}
Indenticaly, $\iint_{S} (~\text{const.}~) \mathbf{n} dS = 0$ for the closed surfaces. 
```
In addition, the potential component, $V_{\theta}$, is symmetric, and therefore, the integral vanishes for this. Hence, only the fourth term in the pressure survives after integration. 
```{math}
:label: eq:AutonLift_nonref_40
	\mathbf{F} = \iint_{S} \rho V_{\theta} v'_{\theta} \mathbf{n} dS
```
From Eq. {eq}`eq:Auton_eq_Vp-primary`, 
```{math}
:label: eq:AutonLift_nonref_41
	V_{\theta} = - \frac{3}{2} u_{0} \sin \theta~~~~\text{at}~r = a
```
According to the dependence of Eq. {eq}`eq:Auton_eq_vorticity_1p` on $\varphi$, we can write 
```{math}
:label: eq:AutonLift_nonref_42
	\boldsymbol{\omega}_{1}(\hat{\rho}'_{0}, \theta', \varphi')
	= \boldsymbol{\omega}_{1}(\hat{\rho}'_{0}, \theta', 0) \cos \varphi' +\boldsymbol{\omega}_{1}(\hat{\rho}'_{0}, \theta', \pi/2) \sin \varphi'
```
This dependence on $\varphi$ results in a similar form of the perturbed velocity field: 
```{math}
:label: eq:AutonLift_nonref_43
	\mathbf{v}_{1}(r, \theta, \varphi)
	= \mathbf{v}_{1}(r, \theta, 0) \cos \varphi + \mathbf{v}_{1}(r, \theta, \pi/2) \sin \varphi
```
In particular, for the $\theta$ component, 
```{math}
:label: eq:AutonLift_nonref_44
	v'_{\theta}(a, \theta, \varphi) = v'_{\theta}(a, \theta, 0) \cos \varphi
```
The $y$ component of the lift is therefore given by 
```{math}
:label: eq:AutonLift_nonref_45
	F_{y}
	= \iint_{S} \rho V_{\theta} v'_{\theta} \mathbf{n} dS
	= - \rho \frac{3}{2} u_{0} a^{2} \int_{0}^{2\pi} \int_{0}^{\pi} v'_{\theta}(a, \theta, 0) \sin^{2} \theta \cos \varphi \mathbf{n} d \theta d\varphi
```
The Cartesian components of the unit normal are 
```{math}
:label: eq:AutonLift_nonref_46
	\mathbf{n} 
	=
	\left( 
		\begin{array}{c}
			n_{x}\\
			n_{y}\\
			n_{z}
		\end{array}
	\right)
	=
	\left( 
		\begin{array}{c}
			\cos \theta\\
			\sin \theta \cos \varphi\\
			\sin \theta \sin \varphi
		\end{array}
	\right)
```
Substituting this expression into the lift equation yields
```{toggle}
For the integration for $\varphi$, $\int_{0}^{2\pi} \cos^{2} \varphi d\varphi = \pi$. A numerical integration for the $\theta$ term gives $\int_{0}^{\theta} v'_{\theta} (a, \theta, 0) \sin^{2} \theta d\theta \sim -0.44456$
```
```{math}
:label: eq:AutonLift_nonref_47
	F_{y}
	= - \frac{3}{2} \rho u_{0} a^{2} \int_{0}^{2\pi} \cos^{2} \varphi d\varphi \int_{0}^{\pi} v'_{\theta}(a, \theta, 0) \sin^{3} \theta d\theta
	= - \frac{3}{2} \rho u_{0} \pi a^{2} \int_{0}^{\pi} v'_{\theta}(a, \theta, 0) \sin^{3} \theta d\theta
```
Auton prepared a lookup table of $v'_{\theta}(a, \theta, 0) / a A$ for integrating $F_{y}$ and obtained 
```{math}
:label: eq:AutonLift_nonref_48
	F_{y} \sim 2.09454 \rho a^{3} u_{0} A = 0.500035 \cdot \rho \frac{4 \pi a^{3}}{3} u_{0} A
```
The value of the lift coefficient was confirmed to be exactly $1/2$ by means of the momentum-integral theory. 

{cite:t}`Legendre1997-ev` derived the following lift coefficient of sphere in the Stokes regime: 
```{math} 
:label: eq:AutonLift_nonref_49
C_{L} = 
\frac{6}{\pi^{2}} \frac{2.255}{\sqrt{Sr Re} \left[ 1 + 0.2 Re/Sr \right]^{3/2}}
```
where $Sr~(= 2 a A / u_{0})$ is the dimensionless shear rate of the incident flow. Then, they carried out numerical simulation of a weak shear flow past a spherical bubble at various Reynolds numbers and showed that the lift coefficient approaches Auton's result at high Reynolds numbers {cite:t}`Legendre1998-pn`. The numerical results were used to connect Eq. {eq}`eq:negative_lift_1` and the Auton lift, that is, 
```{math} 
:label: eq:AutonLift_nonref_50
C_{L} = 
\left( 
\left[ \frac{6}{\pi^{2}} \frac{2.255}{\sqrt{Sr Re} \left[ 1 + 0.2 Re/Sr \right]^{3/2}} \right]^{2}
+
\left[ \frac{1}{2} \left( \frac{1 + 16/Re}{1 + 29/Re} \right) \right]^{2} 
\right)^{1/2}
```
