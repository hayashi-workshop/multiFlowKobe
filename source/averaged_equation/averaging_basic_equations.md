(averaging_basic_equations)=

# Averaging basic equations 

When we consider practical problems in engineering applications, we may not be able to resolve all the interfaces present in the system since numerous bubbles, drops, and particles are usually present there. In such cases, it is neither possible nor reasonable to deal with the motion of each interface. Instead, we shall consider solving only the macro/mesoscopic dynamics of the system by making use of appropriate models for the interaction between those scales and the microscopic scale. For this purpose we apply an averaging technique to the governing equations to filter out the microscopic nature. 

The continuity equation is given by 
```{math}
:label: eq:AveragedEquation_nonref_0
    \frac{\partial \rho}{\partial t} + \nabla \cdot \rho \mathbf{v} = 0
```
By multiplying the phase indicator, $X_{k}$ (Eq. {eq}`eq:VoidFraction_eq_phase_indicator`), we have 
```{math}
:label: eq:AveragedEquation_nonref_1
    X_{k} \frac{\partial \rho}{\partial t} + X_{k} \nabla \cdot \rho \mathbf{v} = 0
```
where $k = G$ or $L$ for gas-liquid two-phase flows. One can rewrite this equation as 
```{math}
:label: eq:AveragedEquation_nonref_2
    \frac{\partial X_{k} \rho}{\partial t} + \nabla \cdot X_{k} \rho \mathbf{v} = \rho \left( \frac{\partial X_{k}}{\partial t} + \mathbf{v} \cdot \nabla X_{k} \right)
```
However, since $X_{k}$ changes its value due to the interface motion, the transport equation of $X_{k}$ is given by 
```{math}
:label: eq:AveragedEquation_nonref_3
    \frac{\partial X_{k}}{\partial t} + \mathbf{v}_{int} \cdot \nabla X_{k} = 0
```
Hence, 
```{math}
:label: eq:AveragedEquations_eq_continuity_naive
    \frac{\partial X_{k} \rho}{\partial t} + \nabla \cdot X_{k} \rho \mathbf{v} = \rho \left( \mathbf{v} - \mathbf{v}_{int} \right) \cdot \nabla X_{k}
```
This equation reduces to the continuity equation of the phase $k$ when $\mathbf{x} \in k$. The R.H.S. is non-zero only at the interface. As can be seen in its unit [kg/m$^{2}\cdot$s], $\rho \mathbf{v}$ represents the flux of mass. The R.H.S. is the local mass flux from one phase to the other through the interface, that is, the mass flux of phase change. 

Here, we define some averaging: 
```{math}
:label: eq:AveragedEquation_nonref_4
    \begin{array}{ll}
    \overline{\phi_{k}} = \frac{1}{M} \int_{M} \phi_{k} dm &\text{$m$-averaging} \\
    \overline{\overline{\phi_{k}}} = \frac{\overline{X_{k} \phi}}{\overline{X_{k}}} &\text{phase-weighted} \\
    \widetilde{\phi_{k}} = \frac{\overline{X_{k} \rho \phi}}{\overline{X_{k} \rho}} &\text{phase-density-weighted}
    \end{array}
```
The time-, volume-, and ensemble-averaging can be used for $m$. Averaging $X_{k}$ gives the volume fraction: 
```{math}
:label: eq:AveragedEquation_nonref_5
    \overline{X_{k}} = \alpha_{k}
```
Therefore, 
```{math}
:label: eq:AveragedEquation_nonref_6
    \overline{X_{k} \phi} = \alpha_{k} \overline{\overline{\phi_{k}}}
```
```{math}
:label: eq:AveragedEquation_nonref_7
    \overline{X_{k} \rho \phi} = 
    \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\phi_{k}} 
```
We list the characteristics of the averaging for some fundamental operations as follows: 
```{math}
:label: eq:AveragedEquation_nonref_8
    \overline{\phi_{k} + \psi_{k}} = \overline{\phi_{k}} + \overline{\psi_{k}},~~~~
    \overline{\frac{\partial \phi_{k}}{\partial t}} = \frac{\partial \overline{\phi_{k}}}{\partial t},~~~~
    \overline{\nabla \phi_{k}} = \nabla \overline{\phi_{k}}
```

Let us apply the averaging to Eq. {eq}`eq:AveragedEquations_eq_continuity_naive`. 
```{math}
:label: eq:AveragedEquation_nonref_9
    \overline{ \frac{\partial X_{k} \rho}{\partial t} + \nabla \cdot X_{k} \rho \mathbf{v} } = \overline{\rho \left( \mathbf{v} - \mathbf{v}_{int} \right) \cdot \nabla X_{k}}
```
With the definitions given above, we obtain 
```{math}
:label: eq:AveragedEquations_eq_continuity_averaged
    \frac{\partial \alpha_{k} \overline{\overline{\rho_{k}}}}{\partial t} + \nabla \cdot \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\mathbf{v}_{k}} = \Gamma_{k}
```
where
```{math}
:label: eq:AveragedEquation_nonref_10
\begin{split}
    &\Gamma_{k} = \overline{\rho \left( \mathbf{v} - \mathbf{v}_{int} \right) \cdot \nabla X_{k}} \\
\end{split}
```
It should be noted that 
```{math}
:label: eq:AveragedEquation_nonref_11
    \Gamma_{G} + \Gamma_{L} = 0
```

The momentum equation is given by 
```{math}
:label: eq:AveragedEquation_nonref_12
    \frac{\partial \rho \mathbf{v}}{\partial t} + \nabla \cdot \rho \mathbf{v} \mathbf{v} = \nabla \cdot \mathbf{T} + \rho \mathbf{g}
```
where 
```{math}
:label: eq:AveragedEquation_nonref_13
    \mathbf{T} = - p \mathbf{I} + \boldsymbol{\tau}
```
Applying the averaging to the momentum equation gives 
```{math}
:label: eq:AveragedEquation_nonref_14
    \frac{\partial \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\mathbf{v}_{k}}}{\partial t} + \nabla \cdot \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\mathbf{v}_{k} \mathbf{v}_{k}} = \nabla \cdot \alpha_{k} \overline{\overline{\mathbf{T}_{k}}} + \alpha_{k} \overline{\overline{\rho_{k}}} \mathbf{g}
    + \mathbf{v}_{k,int}^{m} \Gamma_{k}
    - \overline{ \mathbf{T} \cdot \nabla X_{k}}
```
where
```{math}
:label: eq:AveragedEquation_nonref_15
    \mathbf{v}_{k,int}^{m} \Gamma_{k}
    = \overline{\mathbf{v} \rho (\mathbf{v} - \mathbf{v}_{int}) \cdot \nabla X_{k}}
```
This term represents the interfacial momentum transfer due to phase change. 

The last term on the R.H.S. needs further discussion. 
```{math}
:label: eq:AveragedEquation_nonref_16
\begin{split}
    - \overline{ \mathbf{T} \cdot \nabla X_{k}} 
    &= \overline{ (\overline{p_{int}} + p'_{int}) \nabla X_{k} - \boldsymbol{\tau} \cdot \nabla X_{k}} \\
    &= \overline{p_{int}} \nabla \alpha_{k} + \overline{ ( p'_{int} \mathbf{I} - \boldsymbol{\tau} ) \cdot \nabla X_{k}} 
\end{split}
```
Here, the interface pressure is decomposed into the mean and fluctuation. This is reasonalbe due to the identity that $\iint_{S} \mathbf{n} dS = 0$; constatns have no contributions. Thus, 
```{math}
:label: eq:AveragedEquation_nonref_17
\begin{split}
    \frac{\partial \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\mathbf{v}_{k}}}{\partial t} + \nabla \cdot \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\mathbf{v}_{k} \mathbf{v}_{k}} 
    = 
    &- \alpha_{k} \nabla \overline{\overline{p_{k}}} 
    + \left( \overline{p_{int}} - \overline{\overline{p_{k}}} \right) \nabla \alpha_{k} \\
    &+ \nabla \cdot \alpha_{k} \overline{\overline{\boldsymbol{\tau}_{k}}} 
    + \alpha_{k} \overline{\overline{\rho_{k}}} \mathbf{g}
    + \mathbf{v}_{k,int}^{m} \Gamma_{k}
    + \mathbf{M}_{k}
\end{split}
```
where 
```{math} 
:label: eq:AveragedEquation_nonref_18
\mathbf{M}_{k} =
\overline{ ( p'_{int} \mathbf{I} - \boldsymbol{\tau} ) \cdot \nabla X_{k}} 
```
It is often assumed that (single-pressure assumption)
```{math}
:label: eq:AveragedEquation_nonref_19
\left( \overline{p_{int}} - \overline{\overline{p_{k}}} \right) \nabla \alpha_{k} = 0
```
Hence, 
```{math}
:label: eq:AveragedEquation_nonref_20
    \frac{\partial \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\mathbf{v}_{k}}}{\partial t} + \nabla \cdot \alpha_{k} \overline{\overline{\rho_{k}}} \widetilde{\mathbf{v}_{k} \mathbf{v}_{k}} 
    = 
    - \alpha_{k} \nabla \overline{\overline{p_{k}}} 
    + \nabla \cdot \alpha_{k} \overline{\overline{\boldsymbol{\tau}_{k}}} 
    + \alpha_{k} \overline{\overline{\rho_{k}}} \mathbf{g}
    + \mathbf{v}_{k,int}^{m} \Gamma_{k}
    + \mathbf{M}_{k}
```

We need expressions for the interfacial mass and momentum transfers $\mathbf{M}_{k}$. For the dispersed phases, the drag, lift, virtual mass forces etc. are representative and will be discussed in the following sections. 

```{note} 
The Reynolds decomposition is usually applied to the advection term, which results in the Reynolds stress term. We do not go into detail of this treatment here. See the literature cited in the front page of this section. 
```