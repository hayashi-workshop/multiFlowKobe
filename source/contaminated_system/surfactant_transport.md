(surfactant_transport)=
# Surfactant transport

```{admonition} Summary
* **Subject:** Transport equations of surfactant in bulk liquid and at interface 
* **Main conclusion:** $\frac{\partial \Gamma}{\partial t} + \nabla_{s} \cdot \Gamma \mathbf{v}_{s} + \Gamma ( \mathbf{v} \cdot \mathbf{n} ) \nabla_{s} \cdot \mathbf{n} = \nabla_{s} \cdot D_{s} \nabla_{s} \Gamma + \dot{S}_{\Gamma}$
* **Key idea** Vectorial fassiion gives a simple derivation. 
* **References:** 
	- {cite:t}`Stone1990-bh`
	- {cite:t}`Levich1962`	
```

Let $S(t)$ be a two-dimensional closed surface embedded in a three dimensional space, like a bubble in liquid. Surfactant accumulates on $S(t)$. The total amount of surfactant on $S(t)$ is written as 
\begin{equation*}
	\iint_{S(t)} \Gamma dS
\end{equation*}
The surfactant transfer between the bulk and molecular diffusion are neglected at this stage and will be considered later. Therefore, by the mass conservation law
```{math}
:label: eq:contami_eq_conservation-of-gamma
	\frac{D}{Dt} \iint_{S(t)} \Gamma dS = 0
```
where 
```{math}
:label: eq:ContaminatedDrop_nonref_4
	\frac{D}{Dt} = \frac{\partial}{\partial t} + \mathbf{v}_{s} \cdot \nabla_{s}
```
is the surface material derivative. The velocity tangential to $dS$ and the surface gradient operator are  
```{math}
:label: eq:ContaminatedDrop_nonref_5
	\mathbf{v}_{s} = \left( \mathbf{I} - \mathbf{n} \mathbf{n} \right) \cdot \mathbf{v}
```
```{math}
:label: eq:ContaminatedDrop_nonref_6
	\nabla_{s} = \left( \mathbf{I} - \mathbf{n} \mathbf{n} \right) \cdot \nabla
```
$\mathbf{n}$ is the unit outward normal to $S(t)$. In Eq. {eq}`eq:contami_eq_conservation-of-gamma`, putting the material derivative inside the integral yields
```{math}
:label: eq:ContaminatedDrop_nonref_7
	\iint_{S(t)} \left\{ \frac{D \Gamma}{Dt} dS + \Gamma \frac{D dS}{Dt} \right\} = 0
	\rightarrow
	\iint_{S(t)} \left\{ \left( \frac{\partial \Gamma}{\partial t} + \mathbf{v}_{s} \cdot \nabla_{s} \Gamma \right) dS + \Gamma \frac{D dS}{Dt} \right\} = 0
```
The rate of change in $dS$ can be rewritten as 
```{math}
:label: eq:ContaminatedDrop_nonref_8
	\frac{1}{dS} \frac{DdS}{Dt}
	= \nabla \cdot \mathbf{v} - ( \mathbf{n} \cdot \nabla ) ( \mathbf{v} \cdot \mathbf{n} )
```
See {cite:t}`Prosperetti1979-lc` for the derivation of this relation. The R.H.S. becomes 
```{math}
:label: eq:ContaminatedDrop_nonref_9
\begin{split}	
	\nabla \cdot \mathbf{v} - ( \mathbf{n} \cdot \nabla ) ( \mathbf{v} \cdot \mathbf{n} )
	\rightarrow \frac{\partial v_{i}}{\partial x_{i}} - n_{j} \frac{\partial v_{i} n_{i}}{\partial x_{j}}
	= \delta_{ij} \frac{\partial v_{i}}{\partial x_{j}} - n_{i} n_{j} \frac{\partial v_{i}}{\partial x_{j}} - v_{i} n_{j} \frac{\partial n_{i}}{\partial x_{j}}
	= \left( \delta_{ij} - n_{i} n_{j} \right) \frac{\partial v_{i}}{\partial x_{j}}
	\rightarrow \nabla_{s} \cdot \mathbf{v}
\end{split}
```
where $\partial \mathbf{n} / \partial n = 0$ was used to eliminate the third term in the third equation. Thus, 
```{math}
:label: eq:ContaminatedDrop_nonref_10
	\iint_{S(t)} \left\{ \frac{\partial \Gamma}{\partial t} + \mathbf{v}_{s} \cdot \nabla_{s} \Gamma + \Gamma \nabla_{s} \cdot \mathbf{v} \right\} dS = 0
```
The second term is transformed as 
```{math}
:label: eq:ContaminatedDrop_nonref_11
	\mathbf{v}_{s} \cdot \nabla_{s} \Gamma 
	= \left\{ (\mathbf{I} - \mathbf{n} \mathbf{n}) \cdot \mathbf{v} \right\} \cdot \nabla_{s} \Gamma 
	= \left\{ \mathbf{v} - \mathbf{n}( \mathbf{v} \cdot \mathbf{n} ) \right\} \cdot \nabla_{s} \Gamma 
	= \mathbf{v} \cdot \nabla_{s} \Gamma - ( \mathbf{v} \cdot \mathbf{n} ) \mathbf{n} \cdot \nabla_{s} \Gamma
	= \mathbf{v} \cdot \nabla_{s} \Gamma
```
since $\mathbf{n} \cdot \nabla_{s} \Gamma = 0$. Therefore, 
```{math}
:label: eq:ContaminatedDrop_nonref_12
	\iint_{S(t)} \left\{ \frac{\partial \Gamma}{\partial t} + \mathbf{v} \cdot \nabla_{s} \Gamma + \Gamma \nabla_{s} \cdot \mathbf{v} \right\} dS = 0
```
and combining the second and third terms 
```{math}
:label: eq:ContaminatedDrop_nonref_13
	\iint_{S(t)} \left\{ \frac{\partial \Gamma}{\partial t} + \nabla_{s} \cdot \Gamma \mathbf{v} \right\} dS = 0
```
Since $S(t)$ is arbitrary, 
```{math}
:label: eq:ContaminatedDrop_nonref_14
	\frac{\partial \Gamma}{\partial t} + \nabla_{s} \cdot \Gamma \mathbf{v} = 0
```
One can rewrite this equation using the interfacial quantities as follows: 
```{math}
:label: eq:ContaminatedDrop_nonref_15
	\nabla_{s} \cdot \Gamma \mathbf{v}
	= \nabla_{s} \cdot \Gamma ( \mathbf{v}_{s} + \mathbf{n} \mathbf{n} \cdot \mathbf{v} )
	= \nabla_{s} \cdot \Gamma \mathbf{v}_{s} + \nabla_{s} \cdot \left \{ \Gamma \mathbf{n} ( \mathbf{v} \cdot \mathbf{n} ) \right\}
	= \nabla_{s} \cdot \Gamma \mathbf{v}_{s} + \Gamma ( \mathbf{v} \cdot \mathbf{n} ) \nabla_{s} \cdot \mathbf{n}  + \mathbf{n} \cdot \nabla_{s} \left\{ \Gamma ( \mathbf{v} \cdot \mathbf{n} ) \right\}
```
However, $\mathbf{n} \cdot \nabla_{s} \left\{ \Gamma  ( \mathbf{v} \cdot \mathbf{n} ) \right\} = 0$, and therefore, 
```{math}
:label: eq:ContaminatedDrop_nonref_16
	\frac{\partial \Gamma}{\partial t} + \nabla_{s} \cdot \Gamma \mathbf{v}_{s} + \Gamma ( \mathbf{v} \cdot \mathbf{n} ) \nabla_{s} \cdot \mathbf{n} = 0
```
$\nabla_{s} \cdot \mathbf{n}$ is the mean curvature of interface. Introducing the interfacial and diffusion fluxes into the above equation yields 
```{math}
:label: eq:contami_eq_gamma-equation
	\frac{\partial \Gamma}{\partial t} + \nabla_{s} \cdot \Gamma \mathbf{v}_{s} + \Gamma ( \mathbf{v} \cdot \mathbf{n} ) \nabla_{s} \cdot \mathbf{n} = \nabla_{s} \cdot D_{s} \nabla_{s} \Gamma + \dot{S}_{\Gamma}
```
where $D_{s}$ is the diffusion coefficient. 

```{figure} ../fig/Contaminated-Levich.pdf
:name: Contami_Contaminated-Levich 
Fully-contaminated drop/bubble in uniform flow
```

In the following, it is assumed that the surfactant is present only in the continuous phase (see {numref}`Contami_Contaminated-Levich`). The conservation law of the surfactant molecules in a moving volume $V(t)$ of the continuous phase is given by 
```{math}
:label: eq:ContaminatedDrop_nonref_17
	\frac{D}{Dt} \iiint_{V(t)} C dV = 0
```
without diffusion. Here, $C$ is the concentration of surfactant in the continuous phase and the material derivative is for the bulk fluid, that is, $D/Dt = \partial / \partial t + \mathbf{v} \cdot \nabla$. Having the material derivative inside the integral, we have
```{math}
:label: eq:ContaminatedDrop_nonref_18
	\iiint_{V(t)} \left\{ \frac{DC}{Dt} dV + C \frac{DdV}{Dt} \right\} = 0
```
The rate of change in $dV$ is expressed as 
```{math}
:label: eq:ContaminatedDrop_nonref_19
	\frac{1}{dV} \frac{DdV}{Dt} = \nabla \cdot \mathbf{v}
```
Therefore, 
```{math}
:label: eq:ContaminatedDrop_nonref_20
	\iiint_{V(t)} \left\{ \frac{DC}{Dt} + C \nabla \cdot \mathbf{v} \right\} dV = 0
```
Thus, we obtain 
```{math}
:label: eq:ContaminatedDrop_nonref_21
	\frac{DC}{Dt} + C \nabla \cdot \mathbf{v} = 0
	~~~~\text{or}~~~~
	\frac{\partial C}{\partial t} + \nabla \cdot C \mathbf{v} = 0
```
By introducing the diffusive flux, the transport equation of $C$ is given by 
```{math}
:label: eq:contami_eq_c-equation
	\frac{\partial C}{\partial t} + \nabla \cdot C \mathbf{v} = \nabla \cdot D \nabla C
```
where $D$ is the diffusion coefficient for $C$. The diffusive flux balances with the adsorption-desorption flux at the interface, i.e., 
```{math}
:label: eq:ContaminatedDrop_nonref_22
	- D \nabla C = \dot{S}_{\Gamma}~~~~\text{on}~S
```
