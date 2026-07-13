(pd_homogeneous)=
# Frictional pressure drop: Homogeneous model

The homogeneous model is the simplest model to calculate the frictional pressure drop in two-phase flows. We assume that the two phases are completely mixed and have the same velocity. The total mass flux of the mixture is given by 
```{math}
:label: eq:LMcorrelation_nonref_6
    G = G_{G} + G_{L} = \alpha_{G} \rho_{G} v_{G} + \alpha_{L} \rho_{L} v_{L} = \rho_{G} j_{G} + \rho_{L} j_{L}
```
(it is a custom to use $G$ for mass flux {cite:p}`Chisholm1983-wy`.) The two-phase pressure drop for this flux is given by
```{math}
:label: eq:LMcorrelation_nonref_7
    - \left. \frac{dp}{dz} \right|_{TP} = \frac{\lambda_{H} G^{2}}{2 \rho_{H} D}
```
where $D$ is the pipe diameter, and $\lambda_{H}$ is the two-phase friction factor, which may be given in the Blasius form like
```{math}
:label: eq:LMcorrelation_nonref_8
    \lambda_{H} = C Re_{H}^{n}
```
The density of the homogeneous mixture is given by the harmonic mean: 
```{math}
:label: eq:LMcorrelation_nonref_9
\begin{split}
    \frac{1}{\rho_{H}} = \frac{x}{\rho_{G}} + \frac{1 - x}{\rho_{L}}
\end{split}
```
where $x$ is the flow quality defined by 
```{math}
:label: eq:LMcorrelation_nonref_10
    x = \frac{G_{G}}{G},~~~~1 - x = \frac{G_{L}}{G}
```
There are several options for the viscosity in the Reynolds number. If we take $\mu_{L}$, 
```{math}
:label: eq:LMcorrelation_nonref_11
    Re_{H} = \frac{G D}{\mu_{L}}
```
and 
```{math}
:label: eq:LMcorrelation_nonref_12
    - \left. \frac{dp}{dz} \right|_{TP} = \frac{C \mu_{L} G^{2-n}}{2 \rho_{H} D^{1+n}}
```
Suppose a situation that the liquid phase flows with the total mass flux $G$; we have 
```{math}
:label: eq:LMcorrelation_nonref_13
    - \left. \frac{dp}{dz} \right|_{L0} 
    = \frac{\lambda_{L} G^{2}}{2 \rho_{L} D}
    = \frac{C \mu_{L} G^{2-n}}{2 \rho_{L} D^{1+n}}
```
The square of the ratio of these pressure drops is termed the two-phase multiplier $\phi_{L0}$:
```{math}
:label: eq:LMcorrelation_nonref_14
    \phi_{L0}^{2} = \frac{\left. dp /dz \right|_{TP}}{\left. dp / dz \right|_{L0}}
```
and for the homogeneous flow model with $\mu_{H} = \mu_{L}$, we obtain 
```{math}
:label: eq:LMcorrelation_nonref_15
    \phi_{L0}^{2} = \frac{\rho_{L}}{\rho_{H}} = 1 + \left\{ \frac{\rho_{L}}{\rho_{G}} - 1 \right\} x
```
