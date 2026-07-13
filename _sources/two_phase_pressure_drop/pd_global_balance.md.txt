(pd_global_balance)=
# Global balance in steady upward flow

Consider an upward two-phase flow in a vertical pipe ({numref}`DriftFlux_two-phase-pressure-drop`(a)). In a steady state the momentum balance is given by 
```{math}
:label: eq:LMcorrelation_nonref_0
\begin{split}
    &( \rho_{G} v_{G}^{2} A_{G} + \rho_{L} v_{L}^{2} A_{L} )_{+} - ( \rho_{G} v_{G}^{2} A_{G} + \rho_{L} v_{L}^{2} A_{L} )_{-} \\
    &=
    ( - p_{G} A_{G} -p_{L} A_{L} )_{+} - ( - p_{G} A_{G} -p_{L} A_{L} )_{-} 
    - \tau_{G} S_{G} - \tau_{L} S_{L}
    - \rho_{G} g V_{G} - \rho_{L} g V_{L}
\end{split}
```
where $A_{k}$ is the cross sectional area occupied by the phase $k$, $S_{k}$ is the area of the wall in contact with the phase $k$, $V_{k}$ is the volume of the phase $k$, and $g$ is the magnitude of the acceleration of gravity. With the volume fractions,  
```{math}
:label: eq:LMcorrelation_nonref_1
\begin{split}
    &( \alpha_{G} \rho_{G} v_{G}^{2} + \alpha_{L} \rho_{L} v_{L}^{2} )_{+} - ( \alpha_{G} \rho_{G} v_{G}^{2} + \alpha_{L} \rho_{L} v_{L}^{2} )_{-} \\
    &=
    ( - p_{G} \alpha_{G} -p_{L} \alpha_{L} )_{+} - ( - p_{G} \alpha_{G} -p_{L} \alpha_{L} )_{-} 
    - \tau_{G} \frac{S_{G}}{A} - \tau_{L} \frac{S_{L}}{A}
    - \rho_{G} g \frac{V_{G}}{A} - \rho_{L} g \frac{V_{L}}{A}
\end{split}
```
By substituting $A = \pi D^{2}/4$, $S_{k} = Pe_{k} \Delta z$ and $V_{k} = \alpha_{k} A \Delta z$, we obtain 
```{math}
:label: eq:LMcorrelation_nonref_2
\begin{split}
    &( \alpha_{G} \rho_{G} v_{G}^{2} + \alpha_{L} \rho_{L} v_{L}^{2} )_{+} - ( \alpha_{G} \rho_{G} v_{G}^{2} + \alpha_{L} \rho_{L} v_{L}^{2} )_{-} \\
    &=
    ( - p_{G} \alpha_{G} -p_{L} \alpha_{L} )_{+} - ( - p_{G} \alpha_{G} -p_{L} \alpha_{L} )_{-}
    - \frac{\tau_{G} Pe_{G} \Delta z}{A} - \frac{\tau_{L} Pe_{L} \Delta z}{A} 
    - ( \alpha_{G} \rho_{G} + \alpha_{L} \rho_{L} ) g \Delta z
\end{split}
```
where $Pe$ is the perimeter. Dividing the both sides by $\Delta z$ and taking a limit of $\Delta z \rightarrow 0$ yield
```{math}
:label: eq:LMcorrelation_nonref_3
\begin{split}
    \frac{\partial \alpha_{G} \rho_{G} v_{G}^{2}}{\partial z} + \frac{\partial \alpha_{L} \rho_{L} v_{L}^{2}}{\partial z} =
    - \frac{\partial \alpha_{G} p_{G}}{\partial z} - \frac{\partial \alpha_{L} p_{L}}{\partial z}
    - \frac{\tau_{G} Pe_{G}}{A} - \frac{\tau_{L} Pe_{L}}{A} 
    - ( \alpha_{G} \rho_{G} + \alpha_{L} \rho_{L} ) g
\end{split}
```
Employing a single-pressure assumption $p_{G} = p_{L} = p$ gives 
```{math}
:label: eq:LMcorrelation_nonref_4
\begin{split}
    - \frac{\partial p}{\partial z} 
    &= \underbrace{\frac{\partial \alpha_{G} \rho_{G} v_{G}^{2}}{\partial z} + \frac{\partial \alpha_{L} \rho_{L} v_{L}^{2}}{\partial z}}_{\text{acceleration}}
    + \underbrace{\frac{\tau_{G} Pe_{G}}{A} + \frac{\tau_{L} Pe_{L}}{A}}_{\text{friction}}
    + \underbrace{( \alpha_{G} \rho_{G} + \alpha_{L} \rho_{L} ) g}_{\text{static}} \\
    &= - \left. \frac{\partial p}{\partial z} \right|_{a}
    - \left. \frac{\partial p}{\partial z} \right|_{f}
    - \left. \frac{\partial p}{\partial z} \right|_{s}
\end{split}
```
where 
```{math}
:label: eq:LMcorrelation_nonref_5
\begin{split}
    &- \left. \frac{\partial p}{\partial z} \right|_{a}
    = \frac{\partial \alpha_{G} \rho_{G} v_{G}^{2}}{\partial z} + \frac{\partial \alpha_{L} \rho_{L} v_{L}^{2}}{\partial z} \\
    &- \left. \frac{\partial p}{\partial z} \right|_{f}
    = \frac{\tau_{G} Pe_{G}}{A} + \frac{\tau_{L} Pe_{L}}{A} \\
    &- \left. \frac{\partial p}{\partial z} \right|_{s}
    = ( \alpha_{G} \rho_{G} + \alpha_{L} \rho_{L} ) g
\end{split}
```

```{figure} ../fig/two-phase-pressure-drop.png
:name: DriftFlux_two-phase-pressure-drop
Vertical and horizontal two-phase pipe flows.
```
