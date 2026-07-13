(pd_lockhart)=
# Frictional pressure drop: Lockhart-Martinelli correlation

## Separate flow model

Following {cite:t}`Lockhart1949`, we assume that the two-phase pressure drop can be expressed by 
```{math}
:label: eq:LMcorrelation_nonref_16
\begin{split}
    - \left. \frac{dp}{dz} \right|_{TP} = \lambda_{k} \frac{\rho_{k} v_{k}^{2}}{2D}
\end{split}
```
where the friction factors of both phases are given in the Blasius form: 
```{math}
:label: eq:LMcorrelation_nonref_17
    \lambda_{k} = C_{k} Re_{k}^{n_{k}} 
```
The Reynolds number of the phase $k$ is defined by 
```{math}
:label: eq:LMcorrelation_nonref_18
    Re_{k} = \frac{\rho_{k} j_{k} D}{\mu_{k}}
```
If the phase $k$ flows alone at the mass flux $G_{k} = \alpha_{k} \rho_{k} v_{k} = \rho_{k} j_{k}$, the pressure drop may be expressed as 
```{math}
:label: eq:LMcorrelation_nonref_19
\begin{split}
    - \left. \frac{dp}{dz} \right|_{k} = \lambda_{k} \frac{\rho_{k} j_{k}^{2}}{2D}
\end{split}
```
since the mean velocity is given by $G_{k} / \rho_{k} = j_{k}$. 
```{note}
$- | dp/dz |_{L}$ and $- | dp/dz |_{L0}$ are different quantities!
```
The square root of the ratio of the liquid-phase pressure drop to the gas-phase pressure drop is the Lockhart-Martinelli parameter: 
```{math}
:label: eq:LMcorrelation_nonref_20
    X^{2} 
    = \frac{\left. dp/dz \right|_{L}}{\left. dp/dz \right|_{G}}
    = \frac{\lambda_{L} \rho_{L} j_{L}^{2}/2D}{\lambda_{G} \rho_{G} j_{G}^{2}/2D}
    = \frac{C_{L}}{C_{G}} \frac{\mu_{G}^{n_{G}}}{\mu_{L}^{n_{L}}} \frac{\rho_{L}^{1+n_{L}}}{\rho_{G}^{1+n_{G}}} \frac{j_{L}^{2+n_{L}}}{j_{G}^{2+n_{G}}} \frac{D^{n_{L}}}{D^{n_{G}}}
```
The last expression seems complex, but if we take $n_{L} = n_{G} = 0$ and $C_{L} = C_{G}$ under an assumption that both phases are in fully turbulent conditions we obtain 
```{math}
:label: eq:PressureDrop_eq_X-turbulent
    X^{2} = \frac{\rho_{L} j_{L}^{2}}{\rho_{G} j_{G}^{2}} 
    = \frac{\rho_{G} G_{L}}{\rho_{L} G_{G}} 
    = \frac{\rho_{G}}{\rho_{L}} \frac{1 - x}{x}
```
Writing the two-phase pressure drop as a product of the pressure drop of the phase $k$ and a two-phase multiplier $\phi_{k}$, we have 
```{math}
:label: eq:LMcorrelation_nonref_21
\begin{split}
    - \left. \frac{dp}{dz} \right|_{TP} = - \left. \frac{dp}{dz} \right|_{k} \phi_{k}^{2}
\end{split}
```
Therefore, 
```{math}
:label: eq:LMcorrelation_nonref_22
    \frac{\phi_{G}^{2}}{\phi_{L}^{2}}
    = \frac{\left. dp/dz \right|_{L}}{\left. dp/dz \right|_{G}} = X^{2}
```
By obtaining $\phi$ as a function of $X$, we can calculate the two-phase pressure drop since $X$ is determined by the flow condition. 

## Theoretical basis

{cite:t}`Chisholm1967-zs` gave a theoretical basis for an empirical fit of $\phi (X)$ as follows. The force balance in each phase is given by 
```{math}
:label: eq:LMcorrelation_nonref_23
\begin{split}
    &- \left. \frac{dp}{dz} \right|_{TP} A_{G} - \tau_{G} Pe_{G} - \tau_{i} Pe_{i} = 0 \\
    &- \left. \frac{dp}{dz} \right|_{TP} A_{L} - \tau_{L} Pe_{L} + \tau_{i} Pe_{i} = 0
\end{split}
```
where $Pe_{k}$ is the perimeter of the phase $k$ ($Pe_{G} + Pe_{L} = \pi D$), $Pe_{i}$ is the perimeter of the gas-liquid interface, $A_{k}$ is the cross sectional area of the phase $k$,  $\tau_{k}$ is the wall shear stress at the contact between the phase $k$ and the pipe wall, and $\tau_{i}$ is the interfacial shear stress.
```{toggle}
Summing the two equations yields 

$- \left. \frac{dP}{dz} \right|_{TP} 
    = \tau_{G} \frac{Pe_{G}}{A} + \tau_{L} \frac{Pe_{L}}{A} 
    = \frac{4 \tau_{G}}{4A/Pe_{G}} + \frac{4 \tau_{L}}{4A/Pe_{L}}
    = \frac{4 \tau_{G}}{D_{G}} + \frac{4 \tau_{L}}{D_{L}}$
    
where $D_{k}$ is the hydraulic equivalent diameter.
```
Factorizing the pressure gradient and interfacial friction terms gives
```{math}
:label: eq:LMcorrelation_nonref_24
\begin{split}
    &- \left. \frac{dp}{dz} \right|_{TP} \left\{ 1 - \frac{\tau_{i} Pe_{i}}{- A_{G} \left. dp/dz \right|_{TP} } \right\} = \frac{\tau_{G} Pe_{G}}{A_{G}} \\
    &- \left. \frac{dp}{dz} \right|_{TP} \left\{ 1 + \frac{\tau_{i} Pe_{i}}{- A_{L} \left. dp/dz \right|_{TP}} \right\} = \frac{\tau_{L} Pe_{L}}{A_{L}}
\end{split}
```
The ratio of the interfacial friction to the pressure drop is denoted by 
```{math}
:label: eq:LMcorrelation_nonref_25
    S_{R} = \frac{\tau_{i} Pe_{i}}{- A_{G} \left. dp/dz \right|_{TP}}
```
and the wall shear stresses are given by the following constitutive equations: 
```{math}
:label: eq:LMcorrelation_nonref_26
    \tau_{k} = \frac{f_{k} \rho_{k} v_{k}^{2}}{2}
```
where $f_{k}$ is Fanning's friction coefficient for the phase $k$. Therefore, 
```{math}
:label: eq:PressureDrop_eq_dpdzTP-LM
\begin{split}
    &- \left. \frac{dp}{dz} \right|_{TP} \left\{ 1 - S_{R} \right\} = f_{G} \frac{Pe_{G}}{A_{G}} \frac{\rho_{G} v_{G}^{2}}{2} \\
    &- \left. \frac{dp}{dz} \right|_{TP} \left\{ 1 + \frac{A_{G}}{A_{L}} S_{R} \right\} = f_{L} \frac{Pe_{L}}{A_{L}} \frac{\rho_{L} v_{L}^{2}}{2}
\end{split}
```
Dividing the second equation with the first one and using the definition  
```{math}
:label: eq:LMcorrelation_nonref_27
    Z^{2} = \frac{1 + S_{R} A_{G} / A_{L}}{1 - S_{R}}
```
yield 
```{math}
:label: eq:LMcorrelation_nonref_28
    Z^{2} = \frac{f_{L}}{f_{G}} \frac{Pe_{L} A_{G}}{Pe_{G} A_{L}} \frac{\rho_{L} v_{L}^{2}}{\rho_{G} v_{G}^{2}}
```
Therefore, the velocity ratio is given by
```{math}
:label: eq:LMcorrelation_nonref_29
    K = \frac{v_{G}}{v_{L}}
    = \frac{1}{Z} \sqrt{ \frac{f_{L}}{f_{G}} \frac{Pe_{L} A_{G}}{Pe_{G} A_{L}} \frac{\rho_{L}}{\rho_{G}} }
```
For the cases in which the two phases flow alone, the liquid pressure drop can be written as 
```{math}
:label: eq:LMcorrelation_nonref_30
    - \left. \frac{dp}{dz} \right|_{L} = Pe_{L}' f_{L}' \frac{\rho_{L} j_{L}^{2}}{2} = Pe_{L}' f'_{L} \frac{A_{L}^{2}}{A^{2}} \frac{\rho_{L} v_{L}^{2}}{2}
```
where $f'_{L}$ is the friction factor for the liquid phase flowing alone and $D = 4 A_{L} / Pe'$. The two-phase multiplier is calculated from this equation and Eq. {eq}`eq:PressureDrop_eq_dpdzTP-LM` as 
```{math}
:label: eq:LMcorrelation_nonref_31
    \phi_{L}^{2} 
    = \frac{\left. dp/dz \right|_{TP}}{\left. dp/dz \right|_{L}}
    = \frac{( 1 + A_{G}/A_{L} )^{2}}{ 1 + S_{R} A_{G} / A_{L}  } \frac{f_{L}}{f'_{L}} \frac{Pe_{L}}{Pe'} 
```
Rearranging the first factor in the third equation yields 
```{math}
:label: eq:LMcorrelation_nonref_32
    \phi_{L}^{2} 
    = \frac{f_{L}}{f'_{L}} \frac{Pe_{L}}{Pe'} \left(1 + \frac{A_{G}}{A_{L}} \right) \left( 1 + \frac{A_{G}}{A_{L} Z^{2}} \right)
```

Consider the limiting case where both phases are in turbulent conditions; the friction factors are the same constant and the phase distributions are uniform, and there is no velocity slip, yielding 
```{math}
:label: eq:LMcorrelation_nonref_33
    Z^{2} = \frac{\rho_{L}}{\rho_{G}}
```
Using Eq. {eq}`eq:PressureDrop_eq_X-turbulent`, we obtain 
```{math}
:label: eq:LMcorrelation_nonref_34
    \frac{X}{Z} = \frac{1 - x}{x} = \frac{A_{L}}{A_{G}} 
```
Thus, 
```{math}
:label: eq:LMcorrelation_nonref_35
    \phi_{L}^{2} = 1 + \frac{C}{X} + \frac{1}{X^{2}}
```
where the coefficient $C$ depends on the flow state as shown in {numref}`DriftFlux_tab_Chisholm`, and {numref}`DriftFlux_Chisholm-LM` shows the model for each flow conditions. 


```{table} Chisholm parameter
:name: DriftFlux_tab_Chisholm
:widths: 20 20 20 20 20

| Liquid/Gas | Turbulent/Turbulent | Laminar/Turbulent | Turbulent/Laminar | Laminar/Laminar |
| :--- | :---: | :---: | :---: | :---: |
| $C$ | 20 | 12 | 10 | 5 |
```

```{figure} ../python/Lockhart-Martinelli.pdf
:name: DriftFlux_Chisholm-LM
Chisholm model for two-phase multiplier. solid line: $\phi_{L}$, broken line: $\phi_{G}$. 
```