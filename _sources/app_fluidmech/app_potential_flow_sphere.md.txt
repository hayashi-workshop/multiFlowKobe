(app_potential_flow_sphere)=
# Potential flow about sphere

```{admonition} Referred from 
- {ref}`analysis_bubble_motion`
- {ref}`levich_drag`
```

```{figure} ../fig/Levich-PotentialFlowSphere.png
:name: Levich_Levich-PotentialFlowSphere
Potential flow about sphere
```

Suppose that a fluid is uniformly flow in $-z$ direction: $\mathbf{v} = -u \mathbf{e}_{z}$. In the spherical polar system, $\mathbf{v} = (- u \cos \theta, u \sin \theta, 0)$. The velocity potential for this is $\phi = - u r \cos \theta$. $\phi = - m / r~(m > 0)$ represents a flow having only the radial velocity component: $\mathbf{v} = (m/r^{2}, 0, 0)$. This flow is the so-called *source* and $m$ is the strength of source since $m$ determines the volume flow rate passing through an arbitrary sphere set at the origin, i.e., $\iint_{S} \mathbf{v} \cdot \mathbf{n} dS = 4 \pi m$. The velocity potential $\phi = m/r$ gives a velocity field of *sink* of the strength $m$. Let us consider a situation that the uniform flow is coming from the far field, the sink is set at the origin, and the source is placed on the $z$ axis with a small distance $\delta z$. The sum of these velocity potentials also satisfies the Laplace equation, $\nabla^{2} \phi = 0$, because of the linearity of the equation. Therefore, we make 
```{math}
:label: eq:app_PotentialFlowSphere_nonref_0
	\phi = - u r \cos \theta + \frac{m}{r} - \frac{m}{r_{s}}
```
where $r_{s} = r + \delta z$. Applying Taylor series expansion to the third term, we have 
```{math}
:label: eq:app_PotentialFlowSphere_nonref_1
	\phi = - u r \cos \theta - \frac{m \delta z }{r^{3}} z
```
By taking the limit $\delta z$, which means the source is approaching the sink, while keeping $\lambda = m \delta z = \text{const.}$, we obtain
```{math}
:label: eq:app_PotentialFlowSphere_nonref_2
	\phi = - \left( u r + \frac{\lambda}{r^{2}} \right) \cos \theta
```
where $z = r \cos \theta$ was used. The radial velocity component is given by 
```{math}
:label: eq:app_PotentialFlowSphere_nonref_3
	v_{r} = - \left( u - \frac{2 \lambda}{r^{3}} \right) \cos \theta
```
Given the boundary condition $v_{r} = 0$ at $r = a$, we get $\lambda = u a^{3} / 2$. Hence, 
```{math}
:label: eq:app_PotentialFlowSphere_nonref_4
	\phi = - \left( u r + \frac{u a^{3}}{2 r^{2}} \right) \cos \theta~~~~\text{for sphere fixed in uniform flow}
```
There is no flow passing through the sphere of radius $a$. Therefore, the velocity field can be regarded as a uniform flow past a sphere. By removing the velocity potential for the uniform flow, we can have a potential for the flow about a sphere moving along the $z$ axis at $u$: 
```{math}
:label: eq:app_PotentialFlowSphere_nonref_5
	\phi = - \frac{u a^{3}}{2 r^{2}} \cos \theta~~~~\text{for sphere moving in stagnant fluid}
```
