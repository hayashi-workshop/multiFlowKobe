(taylor_order_of_magnitude)=
# Order-of-magnitude analysis for bubble velocity

```{admonition} Reffered from 
{ref}`void_fraction` 
```

```{admonition} Summary
* **Subject:** Large bubble in vertical pipe
* **Main conclusion:** Froude number as a function of Reynolds and Eötvös numbers. 
* **Key idea** Application of simple order-of-magnitude analysis yields valid functional form of $Fr$. 
* **References:** 
    - {cite:t}`White1962-fp`
    - {cite:t}`Hayashi2011-kw`
```

When bubbles and drops of large size flow in a circular conduit, they may take a bullet-like shape due to the constraint of the wall. Due to pioneered work by {cite:t}`Davies1950-px`, bullet-shaped bubbles are termed *Taylor bubbles*. 

An order of magnitude analysis is applied to a Taylor bubble in the following to obtain an velocity expression. The Navier-Stokes equations of the two phases are given by
```{math}
:label: eq:TaylorBubbles_nonref_0
    \rho_{k} \mathbf{v}_{k} \cdot \nabla \mathbf{v}_{k} = - \nabla p_{k} + \nabla \cdot \boldsymbol{\tau}_{k} + \rho_{k} \mathbf{g} 
```
Evaluating each term in a sense of *magnitude*, we obtain 
```{math}
:label: eq:TaylorBubbles_nonref_1
\begin{split}
    \rho_{L} \frac{u^{2}}{D} &\sim - \frac{p_{L}}{D} + \frac{1}{D} \left( \mu_{L} \frac{u}{R - h} \right) + \rho_{L} g \\
    0 &\sim - \frac{p_{G}}{D} + \rho_{G} g 
\end{split}
```
Therefore, the pressures are 
```{math}
:label: eq:TaylorBubbles_nonref_2
\begin{split}
    &p_{L} \sim c_{i} \rho_{L} u^{2} + c_{\mu} \mu_{L} \frac{u}{h} + c_{g} \rho_{L} g D \\
    &p_{G} \sim c_{g} \rho_{G} g D
\end{split}
```
The jump condition in of the momentum in the normal direction is given by 
```{math}
:label: eq:TaylorBubbles_nonref_3
    p_{G} 
    =
    p_{L} + \mathbf{n}_{L} \cdot \boldsymbol{\tau}_{L} \cdot \mathbf{n}_{L}
    + \sigma \kappa
```
where the curvature in the film region can be evaluated as 
```{math}
:label: eq:TaylorBubbles_nonref_4
    \kappa \sim \frac{1}{R - h}
```
Substituting the orders of pressure into the jump condition yields 
```{math}
:label: eq:TaylorBubbles_nonref_5
    c_{g} \rho_{G} g D 
    =
    c_{i} \rho_{L} u^{2} + c_{\mu} \mu_{L} \frac{u}{h} + c_{g} \rho_{L} g D  + c_{\sigma} \frac{\sigma}{R - h} 
```
In a dimensionless form, 
```{math}
:label: eq:TaylorBubbles_nonref_6
    0
    =
    c_{i} Fr^{2} + c_{\mu} \frac{D}{h} \frac{Fr^{2}}{Re} + c_{g}  + c_{\sigma} \frac{D}{(R - h) Eo}
```
where
```{math}
:label: eq:TaylorBubbles_nonref_7
    Fr = \frac{u}{\sqrt{ \Delta \rho g D / \rho_{L} }}
```
```{math}
:label: eq:TaylorBubbles_nonref_8
    Re = \frac{\rho_{L} u D}{\mu_{L}}
```
```{math}
:label: eq:TaylorBubbles_nonref_9
    Eo = \frac{\Delta \rho g D^{2}}{\sigma}
```
Solving the dimensionless form for the Froude number, we have a Froude number correlation of Taylor bubble: 
```{math}
:label: eq:TaylorBubbles_nonref_10
    Fr = \sqrt{ \frac{c_{1} + c_{3} \frac{D}{R - h} \frac{1}{Eo}}{1 + c_{2} \frac{D}{h} \frac{1}{Re}} }
```
In the limiting case of $Re \rightarrow \infty$ and $Eo \rightarrow \infty$, 
```{math}
:label: eq:TaylorBubbles_nonref_11
\begin{split}
    &Fr = \sqrt{ \frac{c_{1}}{1 + c_{2} \frac{D}{h} \frac{1}{Re}} } &Eo \rightarrow \infty \\
    &Fr = \sqrt{ c_{1} + c_{3} \frac{D}{R - h} \frac{1}{Eo} } &Re \rightarrow \infty \\
    &Fr = c_{1}^{1/2} &Eo, Re \rightarrow \infty
\end{split}
```
Experiments found that $c_{1}^{1/2} = 0.35$ and $\Delta \rho / \rho_{L} \ll 1$, so
```{math}
:label: eq:TaylorBubbles_nonref_12
    u = 0.35 \sqrt{g D}
```
for gas bubbles rising through a low viscosity liquid in a large pipe. A graphical correlation of Taylor bubbles in the entire range of relevant relevant dimensionless groups was given by {cite:t}`White1962-fp`. Readers those who are interested in analytical method on the rise velocity of Taylor bubble, see {cite:t}`Funada2005-dk`.

```{figure} ../fig/TaylorDrop.pdf
:name: TaylorBubble_TaylorBubble
Taylor drop ({cite:p}`Hayashi2011-kw`)
```
