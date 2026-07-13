(af_countercurrent)=
# Counter-current annular flow

When the liquid phase flows downward ({numref}`AnnularFlow_film_model`(b)), the sign of the wall shear stress changes; that is, 
```{math}
:label: eq:annular_eq_momentum_ccfl
\begin{split}
    &- \alpha_{G} \left. \frac{dp}{dz} \right|_{TP} - \tau_{i} \frac{Pe_{i}}{A} - \alpha_{G} \rho_{G} g = 0 \\
    &- \alpha_{L} \left. \frac{dp}{dz} \right|_{TP} + \tau_{i} \frac{Pe_{i}}{A} - \alpha_{L} \rho_{L} g + \tau_{W} \frac{Pe_{W}}{A} = 0
\end{split}
```
Being similar to the case of co-current annular flow, we obtain the relationship between the interfacial and wall shear stresses as 
```{math}
:label: eq:AnnularFlow_nonref_13
    \tau_{i}  + \sqrt{\alpha_{G}} \tau_{W} = \frac{R}{2} \sqrt{\alpha_{G}} \alpha_{L} \Delta \rho g
```
Here, the shear stresses work together to balance with the gravitational force. When $u_{L} = \tau_{W} = 0$, 
```{math}
:label: eq:AnnularFlow_nonref_14
    Fr_{G}^{2} \left(= \frac{u_{G}^{2}}{\Delta \rho g D / \rho_{G}} \right) = \frac{\sqrt{\alpha_{G}} \alpha_{L}}{2 f_{i}} 
```
This relation of the gas Froude number gives a critical gas velocity for suspending the liquid phase (no mean liquid flow rate) by the gas blow only. Substituting the Wallis correlation for $f_{i}$ gives 
```{math}
:label: eq:AnnularFlow_nonref_15
    Fr_{G}^{2} = \frac{\alpha_{L} \sqrt{1 - \alpha_{L}}}{0.01 (1 + 75 \alpha_{L})}
```
The dependence of $Fr_{G}$ on $\alpha_{L}$ is shown in {numref}`AnnularFlow_annular_criticalFrG`.

```{figure} ../python/annular_criticalFrG.pdf
:name: AnnularFlow_annular_criticalFrG
Critical gas Froude number to suspend the liquid phase.
```
