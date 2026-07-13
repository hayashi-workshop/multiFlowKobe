(bubble_velocity_correlation)=
# Bubble velocity correlations

```{seealso} 
The discussion here is based on order-of-magnitudes of forces relevant to bubble motion {cite:p}`Tomiyama2018-vl`. This approach is simple and easy to follow. However, for readers those who want to see derivation in which the relation with the jump condition is stressed, see also 
- {cite:t}`Legendre2025-si`
- {cite:t}`Iwai2025-ae`
```

In the terminal state of a bubble in still liquid, the force balance, as first order expression, may be written as 
```{math}
:label: eq:eq_ForceBalance_balance_equation
    c_{i} F_{i} + c_{\mu} F_{\mu} - c_{b} F_{b} - c_{\sigma} F_{\sigma} = 0
```
The $c$s are constants. Let us first consider a bubble of very small size. Considering the limiting case of $d \rightarrow 0$, we may also have $V_{T} \rightarrow 0$. Therefore, $F_{\sigma} \gg F_{i}, F_{\mu}, F_{b}$. Because of the strong action of surface tension, the bubble maintain spherical shape. The distribution of surface tension force acting on the spherical surface is symmetric, so that the surface tension force cancels out when integrating the distribution for the entire surface. Thus, for tiny bubbles, the surface tension force keeps their shapes spherical, but plays no role in the rise velocity. Omitting $F_{\sigma}$ from the force balance, we have
```{math}
:label: eq:ForceBalance_nonref_0
    c_{i} F_{i} + c_{\mu} F_{\mu} - c_{b} F_{b} = 0
```
The remaining forces show the dependence: $F_{b} \propto d^{3}$, $F_{\mu} \propto V_{T} d$, and $F_{i} \propto V_{T}^{2} d^{2}$. By a detailed analysis we will discuss later, $V_{T} \propto d^{2}$ for small bubble sizes, so that $F_{\mu} \propto d^{3}$ and $F_{i} \propto d^{4}$. Thus, $F_{b}$ and $F_{\mu}$ are comparable, but $F_{i}$ is smaller than the first two, leading to 
```{math}
:label: eq:ForceBalance_nonref_1
    c_{\mu} F_{\mu} - c_{b} F_{b} = 0
```
from which we obtain 
```{math}
:label: eq:ForceBalance_nonref_2
    c_{\mu} \mu_{L} V_{T} d - c_{b} \Delta \rho g d^{3} = 0
```
The rise velocity is therefore 
```{math}
:label: eq:ForceBalance_nonref_3
     V_{T} = c_{1} \frac{ \Delta \rho g d^{2} }{ \mu_{L} }
```
where $c_{1} = c_{b} / c_{\mu}$. This equation shows that the increase in buoyancy makes a bubble faster, but the viscosity retards the bubble. Dividing this equation with the velocity scale of momentum diffusion, $\mu_{L} / \rho_{L} d$ [m/s], yields the following non-dimensional expression of bubble velocity: 
```{math}
:label: eq:ForceBalance_nonref_4
    Re = c_{1} Ar^{2}
```
Substituting this result into Eq. {eq}`eq:eq_ForceBalance_CD_base` yields
```{math}
:label: eq:ForceBalance_nonref_5
    C_{D} = \frac{c_{St}}{Re}
```
where $c_{St} = 4 c_{1} / 3$. The drag coefficient is therefore inversely proportional to $Re$. The constant, $c_{St}$, can be analytically obtained for $Re \ll 1$ (the Stokes regime) as $c_{St} = 16$. See {ref}`stokes_drag_LL` and {ref}`hadamard_rybczynski_drag` for rigorous derivation. On the other hand, in the limiting case of $Re \rightarrow \infty$ for spherical bubble, the liquid flow can be considered as potential flow, but the work done by drag must have a finite value and balances with the viscous dissipation ({ref}`app_viscous_dissipation`). That is, 
```{math}
:label: eq:ForceBalance_nonref_6
	F_{D} V_{T} 
	= \iiint_{V} 2 \mu_{L} e_{ij} e_{ij} dV
```
where $V$ is the volume of the liquid phase, and $e_{ij}$ is the rate of strain tensor defined by 
```{math}
:label: eq:ForceBalance_nonref_7
    e_{ij} = \frac{1}{2} \left( \frac{\partial v_{i}}{\partial x_{j}} + \frac{\partial v_{j}}{\partial x_{i}} \right)
```
and $v_{i}$ is the $i$th component of the liquid velocity. The order of magnitude of the velocity gradient may be estimated as $V_{T} / d$. Therefore, the order of $e_{ij}$ is $V_{T}/d$. The viscous dissipation may take place in the vicinity of the bubble due to the high $Re$, so that $V$ can be replaced with $d^{3}$. Thus, 
```{math}
:label: eq:ForceBalance_nonref_8
    F_{D} V_{T} \sim \mu_{L} V_{T}^{2} d
```
Substituting $F_{D} = \frac{C_{D}}{2} \rho_{L} V_{T}^{2} \frac{\pi d^{2}}{4}$ into the L.H.S. yields
```{math}
:label: eq:ForceBalance_nonref_9
    \frac{C_{D}}{2} \rho_{L} V_{T}^{3} \frac{\pi d^{2}}{4} \sim \mu_{L} V_{T}^{2} d
```
By putting constants into a single value $c_{L}$, we obtain 
```{math}
:label: eq:ForceBalance_nonref_10
    C_{D} = \frac{c_{L}}{Re}
```
where $c_{L} = 48$. The derivation of this case is given in {ref}`levich_drag`. In summary, for bubbles in the viscous force dominant regime, 
```{math}
:label: eq:ForceBalance_nonref_11
    C_{D} = 
    \left\{
    \begin{array}{ll}
         \frac{16}{Re} &\text{for}~Re \ll 1 \\
         \frac{48}{Re} &\text{for}~Re \rightarrow \infty
    \end{array}
    \right.
```
 
Bubbles cannot maintain their spherical shape as $d$ increases. The shape of a large bubble may be no longer neither spherical nor ellipsoidal, but a slice of a sphere called a spherical cap. Because of its large size, the inertial and buoyancy forces are dominant rather than the viscous and surface tension forces. Therefore, 
```{math}
:label: eq:ForceBalance_nonref_12
    c_{i} F_{i} - c_{b} F_{b} = 0 \rightarrow c_{i} \rho_{L} V_{T}^{2} d^{2} - c_{b} \Delta \rho g d^{3}
```
Hence, 
```{math}
    V_{T} = \sqrt{ \frac{ c_{b} \Delta \rho g d }{ c_{i} \rho_{L} } }
```
This functional form is similar to that of the phase velocity of gravitational water wave. In dimensionless form, the bubble velocity can be written as 
```{math}
    Fr = c_{T}
```
where $c_{T} = \sqrt{c_{b}/c_{i}}$. Hence, the drag coefficient is given by 
```{math}
:label: eq:ForceBalance_nonref_13
    C_{D} = \frac{4}{3 c_{T}^{2}}
```
The Bernoulli theorem (see {ref}`spherical_cap`) gives $c_{T} = 1/\sqrt{2}$, so that $C_{D} = 8/3$. Using the relationship $Fr^{2} = We/ Eo$ gives an alternative dimensionless form: 
```{math}
:label: eq:eq_ForceBalance_gravitational
    We = c_{T}^{2} Eo
```

Consider bubbles of intermediate sizes. They cannot maintain spherical shape but may be ellipsoidal or distorted ellipsoidal. Assuming that the viscous contribution to the drag is negligible compared to the other forces, we have
```{math}
:label: eq:ForceBalance_nonref_14
    c_{i} F_{i} - c_{b} F_{b} - c_{\sigma} F_{\sigma} = 0
```
First, we assume that the bubble rise motion is governed by the inertial and surface tension forces. In this case, 
```{math}
:label: eq:ForceBalance_nonref_15
    c_{i} F_{i} - c_{\sigma} F_{\sigma} = 0 \rightarrow c_{i} \rho_{L} V_{T}^{2} d^{2} - c_{b} \sigma d = 0
```
Hence, 
```{math}
:label: eq:ForceBalance_nonref_16
    V_{T} = \sqrt{ \frac{c_{\sigma}}{c_{i}} \frac{ \sigma }{ \rho_{L} d } }
```
The phase velocity of capillary water wave has a similar functional form. Interestingly, in this limiting case, the bubble rise velocity decreases with increasing bubble size. Nondimensionalizing this equation yields 
```{math}
:label: eq:eq_ForceBalance_capillary_dimensionless
    We = c_{M}
```
where $c_{M} = c_{\sigma} / c_{i}$ and $c_{M}$ will be found to be $2$ in {ref}`wave_analogy`. If the inertial and buoyancy forces are competitive, we combine Eqs. {eq}`eq:eq_ForceBalance_gravitational` and {eq}`eq:eq_ForceBalance_capillary` to obtain 
```{math}
:label: eq:ForceBalance_nonref_17
    We = \frac{1}{2} Eo + 2
```
With help of Eq. {eq}`eq:eq_ForceBalance_CD_base` (the most right equation), 
```{math}
:label: eq:ForceBalance_nonref_18
    C_{D} = \frac{8}{3} \frac{Eo}{Eo + 4}
```
This is valid for bubbles in the surface-tension and inertial force dominant regime. 
