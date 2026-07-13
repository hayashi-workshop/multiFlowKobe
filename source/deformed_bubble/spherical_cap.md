(spherical_cap)=
# Large bubbles in liquid

```{admonition} Summary
* **Subject:** Rise velocity of spherical-cap bubble 
* **Main conclusion:** A large bubble taking a spherical-cap shape and its velocity is proportional to $\sqrt{g a}$, where $a$ is the cap radius. 
* **Key idea** Potential flow theory can be applied to fluid particles on the front of a spherical-cap bubble of high $Re$ although the flow behind the bubble (wake) may be highly turbulent. 
* **Reference:** 
	- {cite:t}`Davies1950-px`
	- {cite:t}`Batchelor2000`
```

A bubble in a liquid can keep its shape spherical when its size is small. The inertial force becomes stronger as the bubble size increases and the surface tension cannot maintain the sphericity of the bubble shape. In particular, a shape like an umbrella or a slice of a sphere is formed when a bubble is larger than a certain size. They are called *spherical-cap bubbles*. Cap bubbles tend to rise rectilinearly in stagnant liquid. The front shape can be approximated by a sphere of radius $a$ and is stable during the rise motion. On the other hand, the rear shape is flattened and surface waves are formed on the rear surface. The liquid flow may separate at the edge of the cap shape and turbulent stresses play an important role in the wake behind the bubble. The wake angle $\theta_{w}$ is defined as the angle measured from the bubble nose to the edge. The bubble shape is therefore characterized by $a$ and $\theta_{w}$. However, the sphere-volume-equivalent diameter $d$ would be useful when considering the drag coefficient. The volume of the cap bubble is given by 
```{math}
:label: eq:SphericalCap_nonref_0
	V = \frac{4 \pi a^{3}}{3} (2 + \cos \theta_{w}) \left\{ \frac{1}{2} (1 - \cos \theta_{w}) \right\}^{2}
```
where the center of the sphere of $a$ is located at the origin of the spherical coordinates $(r, \theta, \varphi)$ and the bubble nose is set at $z = a$. The bubble volume is also written as $V = \pi d^{3} / 6$. Therefore, 
```{math}
:label: eq:Cap_eq_d-a-ratio
	\left( \frac{d}{a} \right)^{3} = 2 (2 + \cos \theta_{w}) (1 - \cos \theta_{w})^{2}
```
For $Re > 150$, $\theta_{w} \sim 50^{\circ}$ {cite:p}`Clift1978-wa`, so that $d \sim 0.877 a$, where the Reynolds number is defined for $d$ as the length scale:
```{math}
:label: eq:SphericalCap_nonref_1
	Re = \frac{\rho u d}{\mu}
```

```{figure} ../fig/SphericalCap-problem-setting.png
:name: SphericalCap_Spherical cap bubble
Spherical-cap bubble
```

Suppose that a spherical cap bubble rises rectilinearly through the liquid at a constant speed $u$. Let us use the spherical coordinate system fixed at the bubble center, so that the liquid motion in the far field is $\mathbf{u} = - u \mathbf{e}_{z}$ as we considered for the Stokes drag. At the bubble nose $(z = a)$, the liquid flow is stagnant and the liquid stagnation pressure is denoted by $p_{s}$. Bernoulli's theorem for the bubble nose and a point on the $\varphi$ coordinate line of $z = a - h$ gives 
```{math}
:label: eq:Cap_eq_cap-Bernoulli
	p_{s} = p + \frac{\rho v^{2}}{2} - \rho g h = p + \frac{\rho v^{2}}{2} - \rho g a (1 - \cos \theta)
```
The gas pressure $p_{g}$ at the stagnant point balances with the sum of the liquid pressure and the surface tension, i.e.,
```{math}
:label: eq:Cap_eq_normal-stress-balance
	p_{g} = p_{s} + \frac{2 \sigma}{a}~~~~\text{at}~~z = a
```
where $\sigma$ is the surface tension. The gas density is negligibly small compared to $\rho$, and therefore the gas pressure at $z = a - h$ can also be considered as $p_{g}$. Hence, 
```{math}
:label: eq:SphericalCap_nonref_2
	p_{g} = p + \frac{2 \sigma}{a}~~~~\text{at}~~z = a - h
```
Therefore, 
```{math}
:label: eq:SphericalCap_nonref_3
	p = p_{s}
```
Substituting this relation into Eq. {eq}`eq:Cap_eq_cap-Bernoulli` yields
```{math}
:label: eq:SphericalCap_nonref_4
	v^{2} = 2 g a (1 - \cos \theta)
```
The flow filed is not irrotational. However, because of large $Re$ and the slip boundary condition at the bubble surface, the velocity of the surface flow on the front cap can be approximated with the potential flow theory, that is, 
```{math}
:label: eq:SphericalCap_nonref_5
	v = \left. v_{\theta} \right|_{r=a} = \frac{3}{2} u \sin \theta
```
Thus 
```{math}
:label: eq:SphericalCap_nonref_6
	\frac{9}{4} u^{2} \sin^{2} \theta = 2 g a (1 - \cos \theta)
```
By taking the limit $\theta \rightarrow 0$, we may write $\sin^{2} \theta \sim \theta^{2}$ and $1 - \cos \theta = 2 \sin^{2} (\theta/2) \sim \theta^{2} / 2$. As a result, 
```{math}
:label: eq:SphericalCap_nonref_7
	u = \frac{2}{3} \sqrt{ g a }
```
Let us consider a more general situation that the gas density $\rho_{g}$ has some effect on the gravitational term, but the gas dynamic pressure is negligible. In this case, 
```{math}
:label: eq:SphericalCap_nonref_8
	p_{g} = \left( p + \frac{2 \sigma}{a} \right) - \rho_{g} g h ~~~~\text{at}~~z = a - h
```
The first term is the normal stress balance and the second term is due to the potential energy with non-negligible $\rho_{g}$. Subtracting this from Eq. {eq}`eq:Cap_eq_normal-stress-balance` yields
```{math}
:label: eq:SphericalCap_nonref_9
	p_{s} - p =  - \rho_{g} g h
```
Combining this result with the Bernoulli equation for the liquid gives 
```{math}
:label: eq:SphericalCap_nonref_10
	\frac{\rho v^{2}}{2} = ( \rho - \rho_{g} ) g h
```
and 
```{math}
:label: eq:Cap_eq_cap-bubble-velocity
	u = \frac{2}{3} \sqrt{ \frac{\Delta \rho g a}{\rho} }
```
where $\Delta \rho = \rho - \rho_{g}$. 

The force balance between the buoyancy and the drag is given by 
```{math}
:label: eq:SphericalCap_nonref_11
	C_{D} \frac{\rho u^{2}}{2} \frac{\pi d^{2}}{4}
	= \Delta \rho g \frac{\pi d^{3}}{6}
```
It should be noted that $C_{D}$ is defined as $C_{D} = F_{D} / (\frac{1}{2} \rho u^{2} \frac{\pi d^{2}}{4})$. Solving this for $C_{D}$ gives
```{math}
:label: eq:SphericalCap_nonref_12
	C_{D} = \frac{4}{3}  \frac{\Delta \rho g d}{\rho u^{2}}
```
By substituting Eq. {eq}`eq:Cap_eq_cap-bubble-velocity` into this expression, we have 
```{math}
:label: eq:SphericalCap_nonref_13
	C_{D} = \frac{3 d}{a}
```
With help of the geometric relationship Eq. {eq}`eq:Cap_eq_d-a-ratio` we obtain 
```{math}
:label: eq:SphericalCap_nonref_14
	C_{D} = 3 \left\{ 2 (2 + \cos \theta_{w}) (1 - \cos \theta_{w})^{2} \right\}^{1/3} \sim 2.63
```
This is comparable to the following well-known drag correlation {cite:p}`Ishii1979-sx`:
```{math}
:label: eq:SphericalCap_nonref_15
	C_{D} = \frac{8}{3}
```
