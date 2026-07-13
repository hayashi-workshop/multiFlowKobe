(negative_lift)=
# Lift reversal

```{admonition} Summary
* **Subject:** Reversal of direction of lift acting on an elliosoidal bubble
* **Main conclusion:** Shape deformation induces negative lift, thereby changing the sign of lift coefficient. 
* **Key idea** Surface vorticity gets stronger with shape defomation and interacts with the incident vorcitiy so as to make the role of *secondary trailing vorticity* {cite:p}`Lighthill1956-ov`. 
* **References:** 
	- {cite:t}`Tomiyama2002-yo`: Most widely used lift correlation 
	- {cite:t}`Adoua2009-sc`: Description of lift reversal in terms of vorticity
	- {cite:t}`Hessenkemper2021-hc`: Lift correlation for bubbles in low viscosity system
	- {cite:t}`Hayashi2021-tl`: Vorticity-based lift correlation for bubbles in low viscosity system
```


As shown in {numref}`Auton_Auton-vortex-line`, the stretched vortex line in the wake of the sphere causes vortex threads counterrotating each other (secondary trailing vorticity). The flow by the rotation directs toward the negative $y$, which results in the lift directs the positive $y$ as reaction. This is referred to as the Lighthill mechanism of the lift on sphere under weak shear {cite:p}`Adoua2009-sc`. {cite:t}`Adoua2009-sc` gave a simple picture of this mechanism as follows. The vorticity equation of the streamwise component without diffusion is given by 
```{math} 
:label: eq:negative_lift_1
\frac{D \omega_{x}}{Dt} = \boldsymbol{\omega} \cdot \nabla V_{x}
```
In the lighthill mechanism, the incident vorticity 
```{math}
:label: eq:negative_lift_2
\boldsymbol{\omega}_{-\infty} = - A \mathbf{e}_{z}
```
is dominant, and therefore, 
```{math} 
:label: eq:negative_lift_3
\boldsymbol{\omega} \cdot \nabla V_{x} \sim
- A \frac{\partial V_{x}}{\partial z}
```
Since $\partial V_{x} / \partial z \substack{> \\ <} 0$ for $z \substack{> \\ <} 0$. Therefore, $D \omega_{x} / Dt \substack{< \\ >} 0$ for $z \substack{> \\ <} 0$, which explains the formation of the counter-rotating motion in the trailing voricity observed in {numref}`Auton_Auton-vortex-line`. 


Interestingly, deformation of a bubble, which means the bubble takes ellipsoidal shape, induces vorticity threads having the opposite direction of rotation and the bubble exhibits a negative sign in $C_{L}$ in a certain range of the bubble Reynolds number. This can happen when the vorticity produced at the bubble surface plays a dominant role in the lift. According to {cite:p}`Magnaudet2007-eh`, the magnitude of surface vorticity becomes stronger as $\omega_{s} a / u_{0} \propto \chi^{3}$. When the surface vorticity is dominant rather than the oncoming vorticity, 
```{math} 
:label: eq:negative_lift_4
\boldsymbol{\omega} \cdot \nabla V_{x} \sim
\omega_{s\varphi} \frac{\partial V_{x}}{\partial \varphi}
```
where the ring vorticity $\omega_{s\varphi} < 0$, while $\partial V_{x} / \partial \varphi \substack{< \\ >}$ for $z \substack{> \\ <} 0$. This contribution is opposite to that in the Lighthill mechanism, and reversal of the sign of trailing vorticity threads can take place in this case. 

Modeling of the lift reversal has been attempted in the last three dacades. {cite:t}`Tomiyama2002-yo` proposed a correlation most widely used in bubbly flow simulations. Their correlation is expressed in terms of a modified Eötvös number, which is based on the major axis of a bubble to take into account the deformation effect. The modified-$Eo$-based approach has been employed, and {cite:t}`Hessenkemper2021-hc` developed a $C_{L}$ correlation for bubbles in water. Those correlations are however purely empirical. Lift correlations accounting for the relation with surface vorticity were given by {cite:p}`Hayashi2020-sk` and {cite:p}`Hayashi2021-tl`. For bubbles in low viscosity system, 
```{math} 
:label: eq:negative_lift_5
C_{L} = C_{LS} - \gamma \omega_{\text{max}}^{*\infty} \left[ \frac{8 Eo}{3 \left( Eo + 16 (\chi^{2} - 1) / \chi^{8/3} \right)} \right]
```
where $C_{LS}$ is given by {eq}`eq:AutonLift_nonref_50` and $\gamma = 0.048$, and $\omega_{\text{max}}^{*\infty}$ is the maximum surface vorticity given by {cite:p}`Magnaudet2007-eh`
```{math} 
:label: eq:negative_lift_6
\omega_{\text{max}}^{*\infty} = \frac{2 \chi^{5/3} (\chi^2 - 1)^{3/2}}{\chi^2 \sec^{-1} \chi - (\chi^2 - 1)^{1/2}}
```

```{figure} ../python/lift_data_Re_integrated_for_ln.pdf
:name: lift_data_Re_integrated_for_ln
Lift coefficient correlations {cite:p}`Hayashi2021-ux`
```