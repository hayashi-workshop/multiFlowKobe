(goldsmith_maison)=
# Lubrication of liquid film

```{admonition} Summary
* **Subject:** Large bubble/drop in vertical pipe
* **Main conclusion:** Velocity profile and liquid film thickness in fully-developed film region as function of two-phase viscosity ratio. 
* **Key idea** Flow in liquid film is uni-directional, and NS eq can be directly solved to obtain velocity field and liquid film thickness.
* **References:** 
    - {cite:t}`Goldsmith1962-pi`
```

{cite:t}`Goldsmith1962-pi` studied the motion of large drops in stagnant liquid confined by a vertical pipe and derived an analytical expression of the terminal velocity in terms of the physical properties of the two fluids, the pipe radius, and the thickness of the liquid film formed between the wall and the liquid-liquid interface. The flow in the developed film is unidirectional, and therefore the inertial term disappears:  
```{math}
:label: eq:TaylorBubbles_nonref_13
    - \frac{\partial p_{k}}{\partial z} + \rho_{k} g + \frac{\mu_{k}}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_{k}}{\partial r} \right) = 0 
```
where $p$ is the pressure, $\rho$ is the density, $g$ is the magnitude of the gravity acceleration, $\mu$ is the viscosity, and the subscript $k$ takes either $i$ (inside) or $o$ (outside the drop). The cylindrical coordinates, $z$ and $r$, are utilized and the $z$ axis corresponds to the pipe axis and is directed vertically downward; therefore, the bubble velocity is negative when a bubble moves upward. The drop shape in the front meniscus develops downward, and the thickness of the liquid film, $h$, far from the front of the drop becomes constant (the film region). In the film region, the drop body is cylindrical, so the interface curvature is given by $\kappa = 1/(R - h)$, where $R$ is the radius of the tube. In addition, the normal momentum balance at the interface is given by 
```{math}
:label: eq:TaylorBubbles_nonref_14
    p_{i} = p_{o} + \frac{\sigma}{R - h}
```
where $\sigma$ is the surface tension. Differentiating this equation with respect to $z$ yields 
```{math}
:label: eq:TaylorBubbles_nonref_15
    \frac{\partial p_{i}}{\partial z} = \frac{\partial p_{o}}{\partial z} = H
```
since the surface tension term is constant, where $H$ is constant. The problem to be solved is therefore the following ODE: 
```{math}
:label: eq:TaylorBubbles_nonref_16
    \frac{\mu_{k}}{r} \frac{d}{d r} \left( r \frac{d v_{k}}{d r} \right) = H - \rho_{k} g
```
By integrating this ODE, we obtain
```{math}
:label: eq:TaylorBubbles_nonref_17
    v_{k} (r) = \frac{r^{2}}{4 \mu_{k}} (H - \rho_{k} g) + \alpha_{k} \ln r + \beta_{k}
```
where $\alpha$ and $\beta$ are integration constants. We need to determine the five constants, i.e. $H$, $\alpha_{i}$, $\alpha_{o}$, $\beta_{i}$ and $\beta_{o}$. We therefore apply the following conditions (C1-C5) to the general solution: 
1. $v_{i}$ must be finite at the axis: $-\infty < v_{i}(0) < \infty$
2. $v_{o}$ is zero (no slip) at the pipe wall ($r = R$): $v_{o}(R) = 0$ 
3. The velocity profiles satisfy the continuity equation: 
```{math}
:label: eq:TaylorBubble_eq_continuity_eq
    2 \pi (R - h)^{2} u = \int_{0}^{R-h} 2 \pi v_{i}(r) rdr = - \int_{R-h}^{R} 2 \pi v_{o}(r) rdr
```
4. The velocities are continuous at the interface: $v_{i}(R-h) = v_{o}(R-h)$
5. The tangential viscous stress is continuous at the interface:
```{math}
:label: eq:TaylorBubbles_nonref_18
    \mu_{i} \left. \frac{\partial v_{i}}{\partial r} \right|_{r=R-h} = \mu_{o} \left. \frac{\partial v_{o}}{\partial r} \right|_{r=R-h}
```
where $u$ is the terminal velocity of drop. 

For C1, $\alpha_{i} = 0$, and C2 gives the relation between $\alpha_{o}$ and $\beta_{o}$: 
```{math}
:label: eq:TaylorBubble_eq_BC_for_external
    \frac{R^{2}}{4 \mu_{o}} (H - \rho_{o} g) + \alpha_{o} \ln R + \beta_{o} = 0
    \rightarrow 
    \alpha_{o} \ln r + \beta_{o} = - \frac{R^{2}}{4 \mu_{o}} (H - \rho_{o} g) - \alpha_{o} \ln \frac{R}{r}
```
Substituting the expression of $v_{i}(r)$ into the second equation of Eq. {eq}`eq:TaylorBubble_eq_continuity_eq` (C3) gives 
```{math}
:label: eq:TaylorBubbles_nonref_19
    \pi (R - h)^{2} u
    = 2 \pi \left\{ \frac{(R - h)^{4}}{16 \mu_{i}} (H - \rho_{i} g) + \beta_{i} \frac{(R - h)^{2}}{2} \right\}
```
Therefore, the constant $\beta_{i}$ is given as 
```{math}
:label: eq:TaylorBubbles_nonref_20
    \beta_{i} = u - \frac{(R - h)^{2}}{8 \mu_{i}} (H - \rho_{i} g)
```
Thus, the internal velocity profile is 
```{math}
:label: eq:TaylorBubble_eq_internal_velocity_field
    v_{i}(r)
    = \frac{H - \rho_{i} g}{8 \mu_{i}} \left\{ 2 r^{2} - (R - h)^{2} \right\} + u
```

The external velocity profile is 
```{math}
:label: eq:TaylorBubbles_nonref_21
    v_{o} (r) = \frac{r^{2}}{4 \mu_{o}} (H - \rho_{o} g) + \alpha_{o} \ln r + \beta_{o}
```
Using Eq. {eq}`eq:TaylorBubble_eq_BC_for_external` for the constants yields 
```{math}
:label: eq:TaylorBubbles_nonref_22
    v_{o} (r) = - \frac{R^{2} - r^{2}}{4 \mu_{o}} (H - \rho_{o} g) - \alpha_{o} \ln \frac{R}{r}
```
In order to obtain $\alpha_{o}$, we consider the continuity of the tangential stress (C5). The velocity gradients are 
```{math}
:label: eq:TaylorBubbles_nonref_23
\begin{split}
    &\frac{d v_{o}}{dr} = \frac{r}{2 \mu_{o}} (H - \rho_{o} g) + \frac{\alpha_{o}}{r} \\
    &\frac{d v_{i}}{dr} = \left( \frac{H - \rho_{i} g}{2 \mu_{i}} \right) r
\end{split}
```
At $r = R - h$, the viscous stresses balance, so 
```{math}
:label: eq:TaylorBubbles_nonref_24
    \frac{R - h}{2} (H - \rho_{o} g) + \frac{\mu_{o} \alpha_{o}}{R - h} = \left( \frac{H - \rho_{i} g}{2} \right) (R - h)
```
Rearranging this yields $\alpha_{o}$
```{math}
:label: eq:TaylorBubbles_nonref_25
    \alpha_{o}
    = - \frac{(R - h)^{2}}{2 \mu_{o}} \Delta \rho g
```
where $\Delta \rho = \rho_{i} - \rho_{o}$. Note that for rising drop $\rho_{i} < \rho_{o}$, so that $\Delta \rho < 0$. Thus, the external velocity profile is 
```{math}
:label: eq:TaylorBubble_eq_external_velocity_field
    v_{o} (r) = - \frac{R^{2} - r^{2}}{4 \mu_{o}} (H - \rho_{o} g) + \frac{\Delta \rho g (R - h)^{2}}{2 \mu_{o}} \ln \frac{R}{r}
```
C3 for the external velocity field becomes 
```{math}
:label: eq:TaylorBubble_eq_continuity_external
    u = \frac{H - \rho_{o} g}{\mu_{o}} \left\{ \frac{R^{4}}{8 (R - h)^{2}} - \frac{R^{2}}{4} + \frac{(R - h)^{2}}{8} \right\} + \frac{\Delta \rho g (R - h)^{2}}{2 \mu_{o}} \left\{ \ln \frac{R}{R - h} - \frac{R^{2} - (R - h)^{2}}{2 (R - h)^{2}} \right\}
```

C4, the continuity of the velocity filed at the interface, can be expressed using Eqs. {eq}`eq:TaylorBubble_eq_internal_velocity_field` and {eq}`eq:TaylorBubble_eq_external_velocity_field`: 
```{math}
:label: eq:TaylorBubbles_nonref_26
    \frac{H - \rho_{i} g}{8 \mu_{i}} (R - h)^{2} + u
    = - \frac{R^{2} - (R - h)^{2}}{4 \mu_{o}} (H - \rho_{o} g) + \frac{\Delta \rho g (R - h)^{2}}{2 \mu_{o}} \ln \frac{R}{R - h}
```
The pressure gradient $H$ can be obtained from this equation as 
```{math}
:label: eq:TaylorBubble_eq_H
    H = \frac{ M + \left\{ 1 + ( \rho_{o} / \rho_{i} ) L \right\} \rho_{i} g }{1 + L}
```
where 
```{math}
:label: eq:TaylorBubbles_nonref_27
    L = 2 \frac{\mu_{i}}{\mu_{o}} \left\{ \frac{R^{2}}{(R - h)^{2}} - 1 \right\}
```
and 
```{math}
:label: eq:TaylorBubbles_nonref_28
    M = 4 \frac{\mu_{i}}{\mu_{o}} \Delta \rho g \ln \frac{R}{R - h} - \frac{8 \mu_{i}}{(R - h)^{2}} u
```

An example of the calculation procedure is as follows:
- For a given $u$, compute $h$ from Eq. {eq}`eq:TaylorBubble_eq_continuity_external`. 
- Update $h$ by an iterative manner until $h$ satisfies the continuity equation {eq}`eq:TaylorBubble_eq_continuity_external`.  
- Draw velocity profiles using Eqs. {eq}`eq:TaylorBubble_eq_internal_velocity_field` and {eq}`eq:TaylorBubble_eq_external_velocity_field`. 
{numref}`TaylorBubble_fig_velocity_profile` shows an example of the velocity profiles inside and outside a drop (system 11 in the literature). 

```{figure} ../python/GoldsmithTaylor.png
:name: TaylorBubble_fig_velocity_profile
Velocity profile. $\Delta \rho = -0.214$ g/cm$^{3}$, $\mu_{o} = 0.1224$ Pa s, $\mu_{i}/\mu_{o} = 1.1$, $R = 4$ mm, $u = -0.183$ cm/s. The calculated $h$ is 1.07 mm.
```

A limiting case of special interest is of gas bubbles. In this case, $\mu_{i} / \mu_{o} \ll 1$, and therefore we may neglect $\mu_{i}$ in the derivation. Eq. {eq}`eq:TaylorBubble_eq_H` reduces to 
```{math}
:label: eq:TaylorBubbles_nonref_29
    H = \rho_{i} g
```
Since the internal viscous stress does not play a role, C5 becomes 
```{math}
:label: eq:TaylorBubbles_nonref_30
    \mu_{o} \left. \frac{\partial v_{o}}{\partial r} \right|_{r=R-h} = 0
```
Hence, 
```{math}
:label: eq:TaylorBubbles_nonref_31
    \alpha_{o} = - \frac{(R - h)^{2}}{2 \mu_{o}} \Delta \rho g
```
With this coefficient, the continuity equation, C3, gives 
```{math}
:label: eq:TaylorBubbles_nonref_32
    u = \frac{\Delta \rho g}{2 \mu_{o}} \left[ \frac{R^{4}}{4 (R - h)^{2}} - R^{2} + \frac{3}{4} (R - h)^{2} + (R - h)^{2} \ln \frac{R}{R - h} \right]
```
The velocity profile is 
```{math}
:label: eq:TaylorBubbles_nonref_33
    v_{o}(r) = - \frac{\Delta \rho g}{4 \mu_{o}} \left\{ (R^{2} - r^{2}) - 2(R - h)^{2} \ln \frac{R}{r} \right\}
```
{numref}`TaylorBubble_fig_velocity_profile_gas_bubble` shows an example of the external velocity profile. The zero-shear stress condition can be seen, that is, the velocity gradient is zero at the bubble surface. 

```{figure} ../python/GoldsmithTaylor_gas_bubble.png
:name: TaylorBubble_fig_velocity_profile_gas_bubble
Velocity profile. $\Delta \rho = -0.985$ g/cm$^{3}$, $\mu_{o} = 0.13$ Pa s, $R = 4$ mm, $u = -2.15$ cm/s. The calculated $h$ is 1.08 mm.
```
