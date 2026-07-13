(drift_flux)=
# Drift-flux model

```{admonition} References
- {cite:t}`Zuber1965-nm`: Drift-flux model
```

Consider a two-phase flow in a vertical pipe and the pipe axis is taken as the $z$ coordinate. The area-averaged volume fraction for the cross-sectional area $A$ on the $xy$ plane is calculated as 
```{math}
:label: eq:DriftFlux_nonref_6
    \langle \alpha_{k} \rangle (z, t) = \frac{1}{A} \iint_{A} X_{k} (\mathbf{x}, t) dA
```
The area average of the phase-averaged local velocity is defined by 
```{math}
:label: eq:DriftFlux_nonref_7
    \langle\langle v_{k} \rangle\rangle 
    = \frac{\frac{1}{A} \iint X_{k} \mathbf{v} dA}{\frac{1}{A} \iint X_{k} dA}
    = \frac{\langle j_{k} \rangle}{\langle \alpha_{k} \rangle}
```
For the phase $k = 2$ (we may use this for the gas phase), 
```{math}
:label: eq:Introduction_eq_area_phase_averaged_velocity
    \langle\langle v_{2} \rangle\rangle 
    = \frac{\langle j_{2} \rangle}{\langle \alpha_{2} \rangle}
```
However, from Eq. {eq}`eq:Introduction_eq_local_volumetric_flux`, 
```{math}
:label: eq:DriftFlux_nonref_8
    j_{2} = \alpha_{2} v_{2}
```
and Eq. {eq}`eq:Introduction_eq_local_drift_velocity` becomes 
```{math}
:label: eq:DriftFlux_nonref_9
    v_{2} = j + v_{2j}
```
so that 
```{math}
:label: eq:DriftFlux_nonref_10
    \langle\langle v_{2} \rangle\rangle 
    = \frac{\langle \alpha_{2} j + \alpha_{2} v_{2j} \rangle}{\langle \alpha_{2} \rangle}
    = \frac{\langle \alpha_{2} j \rangle}{\langle \alpha_{2} \rangle}
    + \frac{\langle \alpha_{2} v_{2j} \rangle}{\langle \alpha_{2} \rangle}
```
Rewriting the last equation gives 
```{math}
:label: eq:DriftFlux_nonref_11
    \langle\langle v_{2} \rangle\rangle 
    = \frac{\langle \alpha_{2} j \rangle}{\langle \alpha_{2} \rangle \langle j \rangle} \langle j \rangle
    + \frac{\langle \alpha_{2} v_{2j} \rangle}{\langle \alpha_{2} \rangle}
```
Using Eq. {eq}`eq:Introduction_eq_area_phase_averaged_velocity` we have 
```{math}
:label: eq:DriftFlux_nonref_12
    \frac{\langle j_{2} \rangle}{\langle \alpha_{2} \rangle} 
    = \frac{\langle \alpha_{2} j \rangle}{\langle \alpha_{2} \rangle \langle j \rangle} \langle j \rangle
    + \frac{\langle \alpha_{2} v_{2j} \rangle}{\langle \alpha_{2} \rangle}
```
We may write 
```{math}
:label: eq:DriftFlux_eq_drift_flux_model
    \frac{\langle j_{2} \rangle}{\langle \alpha_{2} \rangle} 
    = C_{0} \langle j \rangle
    + V_{2j}
```
where 
```{math}
:label: eq:DriftFlux_nonref_13
    C_{0} = \frac{\langle \alpha_{2} j \rangle}{\langle \alpha_{2} \rangle \langle j \rangle}
```
and 
```{math}
:label: eq:DriftFlux_nonref_14
    V_{2j} = \frac{\langle \alpha_{2} v_{2j} \rangle}{\langle \alpha_{2} \rangle}
```
Since $\langle j_{2} \rangle = Q_{2} / A$ and $\langle j \rangle = (Q_{1} + Q_{2})/A$, where $Q$ is the volume flow rate, are known as the inlet condition, we can calculate the volume fraction by solving the above equation for $\alpha_{2}$:
```{math}
:label: eq:DriftFlux_nonref_15
    \langle \alpha_{2} \rangle
    =
    \frac{\langle j_{2} \rangle}{C_{0} \langle j \rangle
    + V_{2j}}, 
```
provided that $C_{0}$ and $V_{2j}$ are given. They are referred to as the distribution parameter and the drift velocity, respectively. Alternatively, we can write Eq. {eq}`eq:DriftFlux_eq_drift_flux_model` in the following dimensionless form: 
```{math}
:label: eq:DriftFlux_eq_drift_flux_model_beta_form
    \frac{\langle \beta_{2} \rangle}{\langle \alpha_{2} \rangle} 
    = C_{0}
    + \frac{V_{2j}}{ \langle j \rangle}
```
where 
```{math}
:label: eq:DriftFlux_nonref_16
    \langle \beta_{2} \rangle = \frac{Q_{2}}{Q_{1} + Q_{2}}
```
If the two phases flow as a complete mixture and $v_{1} = v_{2}$, we have $\langle \alpha_{2} \rangle = \langle \beta_{2} \rangle$. Therefore, the drift-flux model reduces to the homogeneous model when $C_{0} = 1$ and $V_{2j} = 0$, and the R.H.S. of Eq. {eq}`eq:DriftFlux_eq_drift_flux_model_beta_form` represents how the flow is far from the homogeneous state. 

In the following, we choose the liquid phase $L$ for $1$ and the gas phase $G$ for $2$, so $\alpha_{2}$ is the void fraction and will be simply written as $\alpha$. The distribution parameter depends on the profile of $\alpha$. When $\alpha$ is uniform in the cross section of a pipe, $C_{0}$ takes a value close to unity. On the other hand, $C_{0}$ is larger than $1$ when the void fraction in the core region is large, e.g., a parabolic profile. $C_{0}$ may be less than $1$ when the void fraction accumulates in the near-wall region. 

The values of $C_{0}$ and $V_{Gj}$ depend of the flow pattern. Some examples of drift flux parameters are given in {numref}`Introduction_eq_drift_flux_parameters` {cite:p}`JSMEhb2006`. The drift velocities of the bubbly and slug flow regimes will be found, respectively, in {ref}`wave_analogy` and {ref}`taylor_order_of_magnitude`. As can be understood from its definition, the drift velocity represents how fast the gas phase is compared to the mixture. In bubbly flows and slug flows in a vertical pipe, the drift velocity is therefore tightly related with the bubble rise velocity in still liquid. In the annular flow pattern, the cross-sectional area is almost occupaied by the gas phase, and therefore $C_{0}$ is close to unity. The fucntional form of drift velocity will be briefly discussed in {ref}`annular_flow`.


```{table} Drift flux parameters (quoted from Two-Phase Flow Handbook (JSME))
:name: Introduction_eq_drift_flux_parameters
:widths: 20 30 50

| Flow regime | $C_{0}$ | $V_{Gj}$ |
| :--- | :--- | :--- |
| Bubbly flow | $1.2 - 0.2 \sqrt{\rho_{G}/\rho_{L}}$ | $\sqrt{2} [\sigma \Delta \rho g / \rho_{L}^{2}]^{1/4}$ |
| Slug flow | $1.2$ | $0.35 [\Delta \rho g D / \rho_{L}]^{1/2}$ |
| Annular flow | $1.0$ | $23[\mu_{L} \langle j_{L} \rangle / \rho_{G} D]^{1/2} \Delta \rho/\rho_{L}$ |
```
