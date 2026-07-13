% % % % % % % % % % % % % % % % % % % % % 
(app_viscous_dissipation)=
# Viscous dissipation

```{admonition} Referred from 
{ref}`levich_drag`
```

```{admonition} Reference
{cite:t}`Aris1990`
```

The work done by the stress $T_{ij}$ on a surface element $dS$ is given by $(v_{j} \delta t) T_{ji} n_{j} dS$. The total power for the whole surface $S$ enclosing volume $V$ is therefore given by $\iint_{S} v_{i} T_{ji} n_{j} dS$. Applying the divergence theorem yields 
```{math}
:label: eq:app_ViscousDissipation_nonref_0
\begin{split}
	\iint_{S} v_{i} T_{ji} n_{j} dS
	&= \iiint_{V} \frac{\partial v_{i} T_{ji}}{\partial x_{j}} dV
	= \iiint_{V} \left\{ v_{i} \frac{\partial T_{ji}}{\partial x_{j}} +  \frac{\partial v_{i}}{\partial x_{j}} T_{ji}\right\} dV \\
	&= \iiint_{V} \left\{ v_{i} \left[ \rho \frac{D v_{i}}{Dt} - \rho f_{i} \right] +  \frac{\partial v_{i}}{\partial x_{j}} T_{ji}\right\} dV
\end{split}
```
where the equation of motion was used. $v_{i} D v_{i}/Dt = D/Dt (v^{2}/2)$. Therefore, the rate of change in the kinetic energy of the fluid is written as 
```{math}
:label: eq:app_ViscousDissipation_nonref_1
\begin{split}
	\iiint_{V} \rho \frac{D}{Dt}\left( \frac{v^{2}}{2} \right) dV
	&=
	\frac{D}{Dt} \iiint_{V} \frac{\rho v^{2}}{2} dV \\
	&=
	\iiint_{V} \rho f_{i} v_{i} dV
	+ \iint_{S} v_{i} T_{ji} n_{j} dS
	- \iiint_{V} \frac{\partial v_{i}}{\partial x_{j}} T_{ji} dV
\end{split}
```
The terms on the R.H.S. are the rate of change in the kinetic energy due to the external forces, the surface stresses, and the internal stresses. For the last one we may write
```{math}
:label: eq:app_ViscousDissipation_nonref_2
\begin{split}
	\iiint_{V} \frac{\partial v_{i}}{\partial x_{j}} T_{ji} dV	
	&= \iiint_{V} e_{ij} T_{ji} dV	
	= \iiint_{V} e_{ij} \left( -p \delta_{ji} + 2 \mu e_{ji} - \frac{2}{3} \mu e_{kk} \delta_{ji} \right) dV \\
	&= \iiint_{V}  \left\{ -p e_{kk} + 2 \mu \left( e_{ji} - \frac{1}{3} e_{kk} \delta_{ji} \right) e_{ij} \right\} dV	
\end{split}
```
The pressure term $-p e_{kk} \rightarrow -p \nabla \cdot \mathbf{v}$ corresponds to the reversible work associated with the volume change. The second term can be rewritten as 
```{math}
:label: eq:app_ViscousDissipation_nonref_3
	\iiint_{V}  2 \mu \left( e_{ji} - \frac{1}{3} e_{kk} \delta_{ji} \right) e_{ij} dV	
	= \iiint_{V}  2 \mu \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} dV	
```
It is obvious that this term is always negative, so that the kinetic energy decreases in the irreversible manner due to the viscous nature. For incompressible fluids, the rate of the viscous dissipation is 
```{math}
:label: eq:app_ViscousDissipation_nonref_4
	\iiint_{V}  2 \mu e_{ij} e_{ij} dV	
```
Let us confirm the fact that the kinetic energy dissipated changes into the internal energy $i$. The conservation of the total energy $\rho i + \rho v^{2}/2$ is given by  
```{math}
:label: eq:app_ViscousDissipation_nonref_5
	\frac{D}{Dt} \iiint_{V} \left( \rho i + \frac{\rho v^{2}}{2} \right) dV
	=
	\iiint_{V} \rho f_{i} v_{i} dV
	+ \iint_{S} v_{i} T_{ji} n_{j} dS
	- \iint_{S} q_{j} n_{j} dS
```
Subtracting the kinetic energy equation from the total energy equation yields 
```{math}
:label: eq:app_ViscousDissipation_nonref_6
\begin{split}
	\frac{D}{Dt} \iiint_{V} \rho i dV
	&=
	- \iint_{S} q_{j} n_{j} dS
	+ \iiint_{V} \frac{\partial v_{i}}{\partial x_{j}} T_{ji} dV \\
	&=
	- \iint_{S} q_{j} n_{j} dS
	- \iiint_{V} p \frac{\partial v_{j}}{\partial x_{j}} dV	
	+ \iiint_{V}  2 \mu \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} dV		
\end{split}
```
This is the equation corresponding to the first law of thermodynamics, $di \leq \delta q + \delta w$. With help of the divergence theorem, 
```{math}
:label: eq:app_ViscousDissipation_nonref_7
	\iiint_{V} 
	\left(
		\rho \frac{D i}{Dt} 
	+ \frac{\partial q_{j}}{\partial x_{j}} 
	+ p \frac{\partial v_{j}}{\partial x_{j}} 
	- 2 \mu \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} 
	\right)
	dV
	= 0
```
Since $V$ is arbitrary, 
```{math} 
:label: eq:app_ViscousDissipation_nonref_8
	\rho \frac{D i}{Dt} 
	=
	- \frac{\partial q_{j}}{\partial x_{j}} 
	- p \frac{\partial v_{j}}{\partial x_{j}} 
	+ 2 \mu \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} 
```
The laws of thermodynamics holds within each fluid particle (*hypothesis of local equilibrium*), we rewrite the first law of thermodynamics
```{math} 
:label: eq:app_ViscousDissipation_nonref_9
T ds = di + p d \left( \frac{1}{\rho} \right)
```
into the following form: 
```{math} 
:label: eq:app_ViscousDissipation_nonref_10
T \frac{Ds}{Dt} 
= \frac{Di}{Dt} + p \frac{D}{Dt} \left( \frac{1}{\rho} \right)
= \frac{Di}{Dt} - \frac{p}{\rho^{2}} \frac{D \rho}{Dt}
```
where $s$ is the entropy. By substituting this equation into Eq. {eq}`eq:app_ViscousDissipation_nonref_8` becomes we obtain 
```{math} 
:label: eq:app_ViscousDissipation_nonref_11
	\rho T \frac{Ds}{Dt} 
	=
	- \frac{\partial q_{j}}{\partial x_{j}} 
	+ 2 \mu \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} 
```
This is comparable to $ds \ge \delta q/T$ in thermodynamics. For more clarity we shall observe the entropy generation within a system of $V$. 
```{math} 
:label: eq:app_ViscousDissipation_nonref_12
	\frac{D}{Dt} \iiint_{V} \rho s dV
	=
	\iiint_{V} \left( 
	- T^{-1} \frac{\partial q_{j}}{\partial x_{j}} 
	+ 2 T^{-1} \mu \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} 
	\right) dV
```
Using Fourie's law
```{math} 
:label: eq:app_ViscousDissipation_nonref_13
q_{j} = - k \frac{\partial T}{\partial x_{j}}
```
```{math} 
:label: eq:app_ViscousDissipation_nonref_14
	\frac{D}{Dt} \iiint_{V} \rho s dV
	=
	\iiint_{V} \left( 
	T^{-1} \frac{\partial}{\partial x_{j}} \left( k \frac{\partial T}{\partial x_{j}} \right)
	+ 2 T^{-1} \mu \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} 
	\right) dV
```

```{math} 
:label: eq:app_ViscousDissipation_nonref_15
	\frac{D}{Dt} \iiint_{V} \rho s dV
	=
	\iint_{S} \frac{k}{T} \frac{\partial T}{\partial x_{j}} n_{j} dS
	+ \iiint_{V} \left\{ 
	  \left( \frac{k}{T^{2}} \left( \frac{\partial T}{\partial x_{j}} \right)^{2} \right)
	+ \frac{2 \mu}{T} \left( e_{ij} - \frac{1}{3} e_{kk} \delta_{ij} \right)^{2} 
	\right\} dV
```
The first term on the R.H.S. is entropy transfer with the neighbors of $V$; while the second term represents *irreversible* entropy generation within $V$, the origin of which is the heat conduction (temperature gradient) and viscous stress (velocity gradient). 
