(bretherton_park)=
# Bretherton problem with surfactant

```{admonition} Summary
* **Subject:** Contaminated long bubble
* **Main conclusion:** Liquid film becomes twice thicker than clean film in fully contaminated situation, while scaling in bubble front is $4^{2/3}$. 
* **Key idea** Surfactant induces Marangoni stress, thereby making thicker liquid film. 
* **References:** 
    - {cite:t}`Park1992-mb`
    - {cite:t}`Magnini2019-jz`
```

Here, we discuss a long bubble contaminated with surfactant, which was discussed by {cite:t}`Park1992-mb`. Same as the Bretherton analysis, the inertial effect in the fluid motion is neglected. First, we shall use the notation by {cite:t}`Magnini2019-jz`. The transport equation of the concentration in the bulk is given by 
```{math}
:label: eq:park_in_magnini_expr_nonref_0
    \nabla \cdot ( C \mathbf{u} ) = D \nabla^{2} C
```
In a thin film, we employ the Cartesian coordinates to simplify the discussion. Thus, 
```{math}
:label: eq:park_in_magnini_expr_nonref_1
    u C_{x} + v C_{y} = D (C_{xx} + C_{yy})
```
Applying the nondimensionalization 
```{math}
:label: eq:park_in_magnini_expr_nonref_2
    \hat{u} = \frac{u}{U_{b}}, \quad
    \hat{v} = \frac{v}{V}, \quad
    \hat{x} = \frac{x}{\ell}, \quad
    \hat{y} = \frac{y}{h_{0}}, \quad
    \hat{p} = \frac{p}{\mu U \ell / h_{0}^{2}}, \quad
    \hat{h} = \frac{h}{h_{0}}, \quad
    \hat{\kappa} = \frac{\kappa}{h_{0} / \ell^{2}}
```
```{math}
:label: eq:park_in_magnini_expr_nonref_3
    \frac{U C_{0}}{\ell} \hat{u} \hat{C}_{\hat{x}} + \frac{\epsilon U C_{0}}{h_{0}} \hat{v} \hat{C}_{\hat{y}} = D \left(\frac{C_{0}}{\ell^{2}} \hat{C}_{\hat{x}\hat{x}} + \frac{C_{0}}{h_{0}^{2}} \hat{C}_{\hat{y}\hat{y}} \right)
```
Rewriting this without putting hat, we have
```{math}
:label: eq:park_in_magnini_expr_nonref_4
    \frac{1}{2} \frac{2 U R}{D} \frac{h_{0}}{\ell} \frac{h_{0}}{R} \left( u C_{x} + \frac{\epsilon}{h_{0}/\ell} v C_{y} \right) = \frac{h_{0}^{2}}{\ell^{2}} C_{xx} + C_{yy} 
```
and then 
```{math}
:label: eq:park_in_magnini_expr_nonref_5
    \frac{1}{2} \epsilon Pe H \left( u C_{x} + v C_{y} \right) = \epsilon^{2} C_{xx} + C_{yy} 
```
where 
```{math}
:label: eq:park_in_magnini_expr_nonref_6
\begin{split}
    Pe = \frac{2 U R}{D},~~~~H = \frac{h_{0}}{R},~~~~\epsilon = h_{0} / \ell
\end{split}
```
If we assume that the factor $\epsilon Pe H$ has a contribution to the leading order, 
```{math}
:label: eq:park_in_magnini_expr_nonref_7
    \frac{1}{2} \epsilon Pe H \left( u C_{x} + v C_{y} \right) = C_{yy} 
```
For the scaling $Ca_{b} \sim O(\epsilon^{3})$, the leading order equation becomes 
```{math}
:label: eq:park_in_magnini_expr_nonref_8
    \frac{1}{2} Ca_{b}^{1/3} Pe H \left( u C_{x} + v C_{y} \right) = C_{yy} 
```
If we write $H \rightarrow Ca^{2/3}$ due to $H \sim O(\epsilon^{2})$, this equation corresponds to Eq. (26a) in Park (1992);
```{math}
:label: eq:park_in_magnini_expr_nonref_9
    u C_{x} + v C_{y} =\frac{2}{Ca_{b} Pe}  C_{yy} 
```
Note that the definition of $Pe$ in Park is $Pe = UR/D$. Up to this result, we have not yet used the scaling of $Pe$. 

The surfactant transport at bubble surface is written as 
```{math}
:label: eq:park_in_magnini_expr_nonref_10
    \nabla_{S} \cdot (\Gamma \mathbf{u}) = D_{S} \nabla_{S}^{2} \Gamma + j
```
where 
```{math}
:label: eq:park_in_magnini_expr_nonref_11
    j = - D \mathbf{n} \cdot \nabla C
```
For the stationary problem, 
```{math}
:label: eq:park_in_magnini_expr_nonref_12
    \nabla_{S} \cdot (\Gamma \mathbf{u}_{S}) = D \nabla_{S}^{2} \Gamma + j
```
The unit normal to the liquid phase is defined by 
```{math}
:label: eq:park_in_magnini_expr_nonref_13
    \mathbf{n} = \frac{1}{\sqrt{1 + h_{x}^{2}}} \left( -h_{x} , 1 \right)
```
The projection operator is given by 
```{math}
:label: eq:park_in_magnini_expr_nonref_14
    \mathbf{P}
    = \mathbf{I} - \mathbf{n} \mathbf{n} 
    = \frac{1}{1 + h_{x}^{2}} 
    \left( 
    \begin{array}{cc}
    1 &h_{x}\\
    h_{x} &h_{x}^{2}
    \end{array}
    \right)
```
The surface velocity is therefore 
```{math}
:label: eq:park_in_magnini_expr_nonref_15
    \mathbf{u}_{S} 
    = \mathbf{P} \cdot \mathbf{u}
    = \frac{1}{1 + h_{x}^{2}} \left( u + h_{x} v, h_{x} (u + h_{x} v ) \right)
```
The surface gradient operator is 
```{math}
:label: eq:park_in_magnini_expr_nonref_16
    \nabla_{S} 
    = \mathbf{P} \cdot \nabla
    = \frac{1}{1 + h_{x}^{2}} \left( \partial_{x} + h_{x} \partial_{y}, h_{x} (\partial_{x} + h_{x} \partial_{y}) \right)
```
Using these results, one can write the surface divergence term as 
```{math}
:label: eq:park_in_magnini_expr_nonref_17
    \nabla_{S} \cdot ( \Gamma \mathbf{u}_{S} )
    = ( \partial_{x} + h_{x} \partial_{y} ) \left( \Gamma \frac{u + h_{x} v}{1 + h_{x}^{2}} \right) + \frac{h_{x} h_{xx} (u + h_{x} v)}{(1 + h_{x}^{2})^{2}} 
```
Nondimensionalizing this equation gives 
```{math}
:label: eq:park_in_magnini_expr_nonref_18
    \nabla_{S} \cdot ( \Gamma \mathbf{u}_{S} )
    = \frac{U}{\ell} \Gamma_{0} \left[ ( \partial_{x} + h_{x} \partial_{y} ) \left( \Gamma \frac{u + \epsilon^{2} h_{x} v}{1 + \epsilon^{2} h_{x}^{2}} \right) + \frac{\epsilon^{2} h_{x} h_{xx} (u + \epsilon^{2} h_{x} v)}{(1 + \epsilon^{2} h_{x}^{2})^{2}} \right]
```
Here, we eliminated hat, and $\Gamma_{0}$ is the characteristic concentration at bubble surface. The RHS is written as 
```{math}
:label: eq:park_in_magnini_expr_nonref_19
    -D \mathbf{n} \cdot \nabla C
    = - \frac{D C_{0}}{h_{0}} \frac{1}{\sqrt{1 + \epsilon^{2} h_{x}^{2}}} \left( - \epsilon^{2} h_{x} C_{x} + C_{y} \right)
```
Combining the reuslts and neglecting the surface diffusion, which is usually much smaller than advection, yields 
```{math}
:label: eq:park_in_magnini_expr_nonref_20
    \frac{h_{0}}{\ell} \frac{U}{D} \frac{\Gamma_{0}}{C_{0}} \left[ ( \partial_{x} + h_{x} \partial_{y} ) \left( \Gamma \frac{u + \epsilon^{2} h_{x} v}{1 + \epsilon^{2} h_{x}^{2}} \right) + \frac{\epsilon^{2} h_{x} h_{xx} (u + \epsilon^{2} h_{x} v)}{(1 + \epsilon^{2} h_{x}^{2})^{2}} \right]
    =
    - \frac{1}{\sqrt{1 + \epsilon^{2} h_{x}^{2}}} \left( - \epsilon^{2} h_{x} C_{x} + C_{y} \right)
```
One may rewrite this as 
```{math}
:label: eq:park_in_magnini_expr_nonref_21
    \frac{1}{2} \epsilon Pe K \left[ ( \partial_{x} + h_{x} \partial_{y} ) \left( \Gamma \frac{u + \epsilon^{2} h_{x} v}{1 + \epsilon^{2} h_{x}^{2}} \right) + \frac{\epsilon^{2} h_{x} h_{xx} (u + \epsilon^{2} h_{x} v)}{(1 + \epsilon^{2} h_{x}^{2})^{2}} \right]
    =
    - \frac{1}{\sqrt{1 + \epsilon^{2} h_{x}^{2}}} \left( - \epsilon^{2} h_{x} C_{x} + C_{y} \right)
```
where 
```{math}
:label: eq:park_in_magnini_expr_nonref_22
    K = \frac{\Gamma_{0}}{C_{0} R}
```
Neglecting small contributions, we have 
```{math}
:label: eq:park_in_magnini_expr_nonref_23
    \frac{1}{2} \epsilon Pe K (\Gamma u)_{x} 
    =
    \epsilon^{2} h_{x} C_{x} - C_{y} 
```
{cite:t}`Park1992-mb` mentioned that $C_{y} = 0$ at the tube wall, and therefore the transport equation of $C$ offers that $C$ is a function of $x$ only. Hence, $C_{y}$ on the RHS of the $\Gamma$ equation was omitted. 
```{math}
:label: eq:park_in_magnini_expr_nonref_24
    \frac{1}{2} \epsilon Pe K (\Gamma u)_{x} 
    =
    \epsilon^{2} h_{x} C_{x}
```
Although some scaling in Park 1992 is not fully understood, if we assume $K \sim O(\epsilon^{2})$, this scale cancels out together with $\epsilon^{2}$ on the RHS; therefore, 
```{math}
:label: eq:park_in_magnini_expr_nonref_25
    (\Gamma u)_{x} 
    =
    \frac{2}{Pe Ca_{b}^{1/3}} h_{x} C_{x}
```
{cite:t}`Park1992-mb` mentioned that $K \sim O(Ca^{2/3})$. 

{numref}`fig_H-and-Gs-in-Park1992` shows numerical results, where (a) shows the film shape (not displayed in {cite:t}`Park1992-mb`) and (b) shows the normalized surfactant concentration (Fig. 5 in {cite:p}`Park1992-mb`). The variables here are normalized as follows: 
```{math}
:label: eq:park_in_magnini_expr_nonref_26
H = \frac{\overline{h}}{\overline{h}_s},~~
X = \frac{\overline{x} + s}{\overline{h}_s},~~
G = \frac{\overline{\Gamma}}{\overline{\Gamma}_f},~~
G_s = \frac{\overline{\Gamma}_s}{\overline{\Gamma}_f},~~
\overline{M} = \overline{\Gamma}_{f} M
```
Here, the overline means variables scaled with 
```{math}
:label: eq:park_in_magnini_expr_nonref_27
x \sim Ca^{1/3},~~
h \sim Ca^{2/3},~~
\Gamma \sim Ca^{2/3}
```
and
```{math} 
:label: eq:park_in_magnini_expr_nonref_28
\overline{M} = - \frac{\Gamma_f}{\mathrm{Ca}^{2/3} \, \sigma_f} \left( \frac{\partial \sigma}{\partial \Gamma} \right)_{\Gamma_f}
```
The subscript $s$ denotes the stationary film. The subscript $f$ denotes the front tip. The ODEs of liquid film thickness and surfactant concentration are therefore 
```{math}
:label: eq:park_in_magnini_expr_nonref_29
    H_{XXX} = \frac{3(H-1)}{H^3} + \frac{3\overline{M} G_X}{2H}
```
```{math}
:label: eq:park_in_magnini_expr_nonref_30
    G_{X} = \frac{2(H-3)G + 4HG_s}{\overline{M} H^2 G}
```
In order to reproduce the problem with our code for the full curvature expression, we used a very small value for $Ca_{b}$ since {cite:t}`Park1992-mb` used a simplified curvature expression ($H_{XXX}$). Therefore, we utilized $Ca_{b} = 1 \times 10^{-6}$ although Park did not mention the actual value. Due to the small $Ca_{b}$, the film thickness is extremely thin (the Bretherton scaling: $\propto Ca_{b}^{2/3}$). The surfactant concentration decreases from the nose toward the film because of the expansion of the surface area in the meniscus, and then it becomes constant in the film. {cite:t}`Park1992-mb` found that the film thicknening by Marangoni stress is scaled by factor of $4^{2/3}$ at large $\overline{M}$ {cite:p}`Ratulowski1990-eo`. 

```{figure} ../python/Fig_h_g_Park.png
:name: fig_H-and-Gs-in-Park1992
Profiles of film $H$ and surfactant concentration $G_{s}$. This verification corresponds to Fig. 5 in {cite:t}`Park1992-mb`.
