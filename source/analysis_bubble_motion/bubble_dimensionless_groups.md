(bubble_dimensionless_groups)=
# Dimensionless groups

```{admonition} References
- {cite:t}`Clift1978-wa`
- {cite:t}`Moore1959-wo`
- {cite:t}`Tomiyama2018-vl`
```

The rise velocity of a gas bubble in still liquid is determined by the balance between four forces, i.e., the buoyancy, the inertial force, the viscous force and the surface tension force. Let $d$ be the sphere-volume-equivalent bubble diameter, $V_{T}$ is the terminal velocity, $\rho$ is the density, $\mu$ is the viscosity, $\sigma$ the surface tension, $g$ is the magnitude of gravitational acceleration, the subscripts $L$ and $G$ denote the liquid and gas phases, respectively ({numref}`ForceBalance_bubble`). The orders of the four forces can be estimated as follows: 
```{math}
:label: eq:eq_ForceBalance_surface_tension
\begin{split}
    &F_{b} = \Delta \rho g d^{3} \\
    &F_{i} = \rho_{L} V_{T}^{2} d^{2} \\
    &F_{\mu} = \mu_{L} V_{T} d \\
    &F_{\sigma} = \sigma d 
\end{split}
```
where $\Delta \rho = \rho_{L} - \rho_{G}$. The ratio of the inertial force to the viscous force gives the bubble Reynolds number: 
```{math}
:label: eq:eq_ForceBalance_Reynolds
    Re = \frac{F_{i}}{F_{\mu}} = \frac{\rho_{L} V_{T} d}{\mu_{L}}
```
Other dimensionless groups relevant to the bubble rise motion can also be defined by combining these forces, e.g., 
```{math}
:label: eq:eq_ForceBalance_Eotvos
    Eo = \frac{F_{b}}{F_{\sigma}} = \frac{\Delta \rho g d^{2}}{\sigma}~~~\text{(Eötvös number)}
```
```{math}
:label: eq:eq_ForceBalance_Weber
    We = \frac{F_{i}}{F_{\sigma}} = \frac{\rho_{L} V_{T}^{2} d}{\sigma}~~~\text{(Weber number)}
```
```{math}
:label: eq:eq_ForceBalance_capillary
    Ca = \frac{F_{\mu}}{F_{\sigma}} = \frac{\mu_{L} V_{T}}{\sigma}~~~\text{(capillary number)}
```
```{math}
:label: eq:eq_ForceBalance_Morton
    M = \frac{F_{\mu}^{4} F_{b}}{F_{i}^{2} F_{\sigma}^{3}} = \frac{\mu_{L}^{4} \Delta \rho g}{\rho_{L}^{2} \sigma^{3}}~~~\text{(Morton number)}
```
```{math}
:label: eq:eq_ForceBalance_Archimedes
    Ar = \frac{\sqrt{F_{i} F_{b}}}{F_{\mu}} = \frac{\sqrt{\rho_{L} \Delta \rho g d^{3}}}{\mu_{L}}~~~\text{(Archimedes number)}
```
```{math}
:label: eq:eq_ForceBalance_Froude
    Fr = \sqrt{\frac{F_{i}}{F_{b}}} = \frac{V_{T}}{\sqrt{\Delta \rho g d / \rho_{L}}}~~~\text{(Froude number)}
```
Some useful relationships between the dimensionless groups can be found; for example,  
```{math}
:label: eq:eq_ForceBalance_relations
    Ar^{4} = Eo^{3} / M,~~~~We = Re Ca,~~~~Fr^{2} = We / Eo = Re^{2} / Ar^{2}
```
The drag force, $F_{D}$, acting on a bubble balances with the buoyancy in the terminal state, so that
```{math}
:label: eq:eq_ForceBalance_ForceBalance
    \Delta \rho g \frac{\pi d^{3}}{6} = \frac{C_{D}}{2} \rho_{L} V_{T}^{2} \frac{\pi d^{2}}{4}
```
Arranging this equation using the dimensionless groups defined above yield
```{math}
:label: eq:eq_ForceBalance_Re_form
    Re^{2} = \frac{4}{3 C_{D}} \sqrt{\frac{Eo^{3}}{M}}
```
which shows that correlating the bubble velocity on the $Re$-$Eo$ map as a function, $Re = f(Eo, M)$ drawing $Re$ curves depending on $M$ ({numref}`ForceBalance_gracemap`). It is obvious that the characteristics of the $Re$ curve are determined by the drag coefficient, $C_{D}$, which also depends on dimensionless groups as discussed in the following sections. By making use of Eq. {eq}`eq:eq_ForceBalance_relations`, Eq. {eq}`eq:eq_ForceBalance_Re_form` can be rewritten as 
```{math}
:label: eq:eq_ForceBalance_CD_base
    C_{D} = \frac{4}{3} \frac{Ar^{2}}{Re^{2}} = \frac{4}{3 Fr^{2}} = \frac{4 Eo}{3 We}
```

```{figure} ../fig/ForceBalance_bubble.pdf
:name: ForceBalance_bubble
Rising bubble in liquid
```

```{figure} ../python/gracemap.pdf
:name: ForceBalance_gracemap
Grace map: $Re$ plotted as a function of $Eo$ and $M$. The values for each line represent $\log M$. The curves are drawn by using a drag correlation proposed by {cite:t}`Tomiyama1998-lv`.
```
