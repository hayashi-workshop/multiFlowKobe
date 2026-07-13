(af_upward_cocurrent)=
# Upward co-current annular flow

Suppose that the gas and liquid phases flow upward in a vertical pipe of radius $R~(=D/2)$ as shown in {numref}`AnnularFlow_film_model`(a). The momentum balance in the two phases can be written as 
```{math}
:label: eq:annular_eq_momentum
\begin{split}
    &- \alpha_{G} \left. \frac{dp}{dz} \right|_{TP} - \tau_{i} \frac{Pe_{i}}{A} - \alpha_{G} \rho_{G} g = 0 \\
    &- \left. \frac{dp}{dz} \right|_{TP} A_{L} + \tau_{i} Pe_{i} - \rho_{L} g A_{L}  - \tau_{W} Pe_{W} = 0
\end{split}
```
where 
```{math}
:label: eq:AnnularFlow_nonref_0
\begin{split}
    &A = \pi R^{2} \\
    &A_{G} = \pi ( R - \delta )^{2} \\
    &A_{L} = A - A_{G} \\
    &Pe_{W} = 2 \pi R \\
    &Pe_{i} = 2 \pi (R - \delta) = 2 \pi R \sqrt{\alpha_{G}}
\end{split}
```
and $\delta$ is the mean liquid film thickness. We employ the following expressions for the interfacial and wall frictions: 
```{math}
:label: eq:AnnularFlow_nonref_1
\begin{split}
    &\tau_{i} = f_{i} \frac{\rho_{G}}{2} (u_{G} - u_{L})^{2} \\
    &\tau_{W} = f_{W} \frac{\rho_{L}}{2} u_{L}^{2}
\end{split}
```
Thus, 
```{math}
:label: eq:AnnularFlow_nonref_2
\begin{split}
    &- \alpha_{G} \left. \frac{dp}{dz} \right|_{TP} - f_{i} \frac{\rho_{G}}{2} (u_{G} - u_{L})^{2} \frac{2 \pi R \sqrt{\alpha_{G}}}{A} - \alpha_{G} \rho_{G} g = 0 \\
    &- \alpha_{L} \left. \frac{dp}{dz} \right|_{TP} + f_{i} \frac{\rho_{G}}{2} (u_{G} - u_{L})^{2} \frac{2 \pi R \sqrt{\alpha_{G}}}{A} - \alpha_{L} \rho_{L} g  - f_{W} \frac{\rho_{L}}{2} u_{L}^{2} \frac{Pe_{W}}{A} = 0
\end{split}
```
For a given set of the volume flow rates, 
```{math}
:label: eq:AnnularFlow_nonref_3
\begin{split}
    &u_{G} = \frac{Q_{G}}{A_{G}} \\
    &u_{L} = \frac{Q_{L}}{A_{L}} \\
\end{split}
```
Therefore, we can obtain $- \left. dp/dz \right|_{TP}$ and $\alpha_{G}$ by solving the momentum equations, provided that the friction factors are given. 

```{figure} ../fig/AnnularFlow.png
:name: AnnularFlow_film_model
Simple model of annular flow.
```

Being similar to single-phase flows, the wall friction factor is often given by the following functional form: 
```{math}
:label: eq:AnnularFlow_nonref_4
    f_{W} = \frac{a}{Re_{L}^{n}}
```
where $Re_{L}$ is the liquid Reynolds number defined by 
```{math}
:label: eq:AnnularFlow_nonref_5
    Re_{L} = \frac{\rho_{L} j_{L} D}{\mu_{L}}
```
For example, {cite:t}`Wallis1970` used the following expression:
```{math}
:label: eq:AnnularFlow_nonref_6
    f_{W} = 
    \left\{
    \begin{array}{ll}
         \frac{16}{Re_{L}} &\text{for}~Re_{L} \le 2300  \\
         \frac{0.079}{Re_{L}} & \text{otherwise}
    \end{array}
    \right.
```
The interfacial friction factor is considered to be a function of $\delta$, e.g., {cite:p}`Wallis1969-kj`
```{math}
:label: eq:AnnularFlow_nonref_7
    f_{i} = 0.005 \left( 1 + 150 \frac{\delta}{R} \right)
```
When $\delta \ll R$, $\alpha \sim 1 - 2 \delta / R$; therefore, 
```{math}
:label: eq:AnnularFlow_nonref_8
    f_{i} = 0.005 \left( 1 + 75 (1 - \alpha_{G}) \right)
```

From Eq. {eq}`eq:annular_eq_momentum`, 
```{math}
:label: eq:AnnularFlow_nonref_9
    \tau_{i} = \frac{R}{2} \sqrt{\alpha_{G}} \left(  - \left. \frac{dp}{dz} \right|_{TP} - \rho_{G} g  \right)
```
By summing the two in Eq. {eq}`eq:annular_eq_momentum`, we obtain the global balance equation: 
```{math}
:label: eq:AnnularFlow_nonref_10
    \tau_{W} = \frac{R}{2} \left( - \left. \frac{dp}{dz} \right|_{TP} - \rho_{m} g \right)
```
where $\rho_{m} = \alpha_{G} \rho_{G} + \alpha_{L} \rho_{L}$. Eliminating the pressure drop yields
```{math}
:label: eq:AnnularFlow_nonref_11
    \tau_{i}  = \sqrt{\alpha_{G}} \tau_{W} + \frac{R}{2} \sqrt{\alpha_{G}} \left( \rho_{m} - \rho_{G} \right) g
```
or 
```{math}
:label: eq:AnnularFlow_nonref_12
    \tau_{i}  = \sqrt{\alpha_{G}} \tau_{W} + \frac{R}{2} \sqrt{\alpha_{G}} \alpha_{L} \Delta \rho g
```
where $\Delta \rho = \rho_{L} - \rho_{G}$. The liquid film is, thus, suspended by the interfacial friction. Using {eq}`eq:AnnularFlow_nonref_1` and evaluating $\tau_{W} \sim \mu_{L} u_{L} / \delta$ give 
```{math}
:label: eq:AnnularFlow_nonref_12_expand
    f_{i} \frac{\rho_{G}}{2} (u_{G} - u_{L})^{2}  = \sqrt{\alpha_{G}} \mu_{L} \frac{u_{L}}{\delta} + \frac{R}{2} \sqrt{\alpha_{G}} \alpha_{L} \Delta \rho g
```
```{math}
:label: eq:AnnularFlow_nonref_12_expand_mod
    u_{G} - j = \left[ 
        \frac{2 D \sqrt{\alpha_{G}}}{\alpha_{L} \delta f_{i}} \left( 
        1 + \alpha_{L}^{2} \frac{\Delta \rho g D \delta}{4 \mu_{L} j_{L}} \right)
        \right]^{1/2} \left( \frac{\mu_{L} j_{L}}{\rho_{G} D} \right)^{1/2}
        + ( u_{L} - j )
```
This can be the basis of the drift velocity as shown in {numref}`Introduction_eq_drift_flux_parameters`. 

