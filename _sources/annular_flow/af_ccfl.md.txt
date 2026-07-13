(af_ccfl)=
# Counter-current limitation

By eliminating the pressure gradients from Eq. {eq}`eq:annular_eq_momentum_ccfl`, we obtain 
```{math}
:label: eq:AnnularFlow_nonref_16
    \tau_{i} \frac{Pe_{i}}{A \alpha_{L} \alpha_{G}} + \tau_{W} \frac{Pe_{W}}{A \alpha_{L}} = \Delta \rho g
```
We assume $u_{L}/u_{G} \ll 1$; hence, 
```{math}
:label: eq:AnnularFlow_nonref_17
    \tau_{i} \sim f_{i} \frac{\rho_{G}}{2} u_{G}^{2} = f_{i} \frac{\rho_{G}}{2} \frac{j_{G}^{2}}{\alpha_{G}^{2}}
```
The wall shear stress is 
```{math}
:label: eq:AnnularFlow_nonref_18
    \tau_{W} = f_{W} \frac{\rho_{L}}{2} u_{L}^{2} = f_{W} \frac{\rho_{L}}{2} \frac{j_{L}^{2}}{\alpha_{L}^{2}}
```
Substituting the shear stress expressions into the momentum equation gives 
```{math}
:label: eq:AnnularFlow_nonref_19
    \frac{f_{i}}{2} \frac{Pe_{i}}{A \alpha_{L} \alpha_{G}} \frac{u_{G}^{2}}{\Delta \rho g / \rho_{G}} + \frac{f_{W}}{2} \frac{Pe_{W}}{A \alpha_{L}} \frac{u_{L}^{2}}{\Delta \rho g / \rho_{L}} = 1
```
```{math}
:label: eq:AnnularFlow_nonref_20
    \frac{2 f_{i} \sqrt{\alpha_{G}}}{\alpha_{L} \alpha_{G}^{3}} \frac{j_{G}^{2}}{\Delta \rho g D / \rho_{G}} + \frac{2 f_{W} }{\alpha_{L}^{3}} \frac{j_{L}^{2}}{\Delta \rho g D / \rho_{L}} = 1
```
When $\delta / R \ll 1$, $\sqrt{\alpha_{G}} \sim 1$; therefore, 
```{math}
:label: eq:AnnularFlow_nonref_21
    \frac{2 f_{i}}{\alpha_{L} \alpha_{G}^{3}} j_{G}^{*2} + \frac{2 f_{W} }{\alpha_{L}^{3}} j_{L}^{*2} = 1
```
where $j_{k}^{*}$ is the so-called Wallis parameter: 
```{math}
:label: eq:AnnularFlow_nonref_22
\begin{split}
    &j_{G}^{*} = \frac{u_{G}}{\sqrt{\Delta \rho g D / \rho_{G}}} \\
    &j_{L}^{*} = \frac{u_{L}}{\sqrt{\Delta \rho g D / \rho_{L}}} \\
\end{split}
```
We assume the proportionality relation, $f_{i} \propto \alpha_{L}$, and $f_{W} = \text{const.}$ for turbulent film condition, and therefore, 
```{math}
:label: eq:AnnularFlow_nonref_23
    \frac{F}{\alpha_{G}^{3}} j_{G}^{*2} + \frac{G}{\alpha_{L}^{3}} j_{L}^{*2} = 1
```
where $F$ and $G$ are constants. Differentiating this with respect to $\alpha_{L}$ gives 
```{math}
:label: eq:AnnularFlow_nonref_24
    \frac{3 F}{(1-\alpha_{L})^{4}} j_{G}^{*2} - \frac{3 G}{\alpha_{L}^{4}} j_{L}^{*2} = 0
```
and 
```{math}
:label: eq:AnnularFlow_nonref_25
    \frac{\alpha_{L}}{1 - \alpha_{L}} = \left( \frac{G j_{L}^{*2}}{F j_{G}^{*2}} \right)^{1/4}
```

```{math}
:label: eq:AnnularFlow_nonref_26
    F^{1/4} j_{G}^{*1/2} + G^{1/4} j_{L}^{*1/2} = 1
```
One can rewrite this result as 
```{math}
:label: eq:AnnularFlow_nonref_27
    j_{G}^{*1/2} + m j_{L}^{*1/2} = C
```
The $m$ and $C$ are determined by experimental data. This equation was derived by {cite:t}`Wallis1969-kj` and has been used to correlate flooding (flow reversal) condition and counter-current flow limitation. A more detailed analysis can be found in {cite:t}`Goda2018-ht` and a series of works by Murase (e.g., {cite:p}`Murase2017-rf`).
