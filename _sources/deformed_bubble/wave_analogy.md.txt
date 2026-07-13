(wave_analogy)=
# Wave analogy for bubble rise velocity

```{admonition} Reffered from 
{ref}`void_fraction` 
```

```{admonition} Summary
* **Subject:** Rise velocity in ellipsoidal bubble regime 
* **Main conclusion:** $u^{2} = \frac{2 \sigma}{\rho d} \left( 1 + \frac{\Delta \rho g d^{2}}{4 \sigma} \right)$ 
* **Key idea** Potential theory of one-dimensional water wave describes the bubble rise velocity. 
* **Reference:** 
    - {cite:t}`Mendelson1967-od`
    - {cite:t}`Tomiyama1998-lv`
```

The phase velocity of deep-water gravitational wave is given by 
```{math}
:label: eq:Mendelson_eq_cp-gravitational-wave
	c_{p} = \sqrt{ \frac{g \lambda}{2 \pi} }
```
where $\lambda$ is the wavelength. The rise velocity of a spherical-cap bubble was derived as (see {ref}`spherical_cap`)
```{math}
:label: eq:WaveAnalogy_nonref_0
	u = \frac{2}{3} \sqrt{ g a } \sim \sqrt{ \frac{g d}{2} }
```
where $d \sim 0.877 a$ was used. By setting $\lambda = \pi d$, the phase velocity in Eq. {eq}`eq:Mendelson_eq_cp-gravitational-wave` gives the velocity of spherical-cap bubble, that is,
```{math}
:label: eq:WaveAnalogy_nonref_1
	c_{p} \xrightarrow[\lambda = \pi d]{} u
```
This relation is called *wave analogy*, in which the rise motion of a bubble is regarded as the propagation of disturbance as water wave. It is clear from Eq. {eq}`eq:Mendelson_eq_cp-gravitational-wave` that the deep-water wave is dispersive. However, the spherical-cap bubble rises at a constant speed while maintaining its shape. This fact suggests that the bubble rise motion should be regarded as the water wave with the principal mode of $\lambda = \pi d$. 

The phase velocity of capillary-gravitational wave is given by (see Appendix {ref}`app_water_wave`)
```{math}
:label: eq:Mendelson_eq_cp-capillary-gravitational-wave
	c_{p} = \sqrt{ \frac{2 \pi \sigma}{\rho \lambda} + \frac{g \lambda}{2 \pi} }
```
{cite:t}`Mendelson1967-od` proposed the following velocity correlation for deformed bubbles by assuming the wave analogy: 
```{math}
:label: eq:WaveAnalogy_nonref_2
	u = \sqrt{ \frac{2 \sigma}{\rho d} + \frac{g d}{2} }
```
{cite:t}`Tomiyama1998-lv` gave a physical interpretation of the wave analogy and replaced $g$ with $\Delta \rho g / \rho$ to make clear the buoyancy effect, i.e., 
```{math}
:label: eq:Mendelson_eq_u-wave-analogy
	u = \sqrt{ \frac{2 \sigma}{\rho d} + \frac{\Delta \rho g d}{2 \rho} }
```
Factorizing the R.H.S. by the factor $2 \sigma / \rho d$ yields
```{math}
:label: eq:WaveAnalogy_nonref_3
	u^{2} = \frac{2 \sigma}{\rho d} \left( 1 + \frac{\Delta \rho g d^{2}}{4 \sigma} \right)
```
Substituting this result into the force balance 
```{math}
:label: eq:WaveAnalogy_nonref_4
	C_{D} = \frac{4}{3} \frac{\Delta \rho g d}{\rho u^{2}}
```
gives
```{math}
:label: eq:WaveAnalogy_nonref_5
	C_{D} = \frac{8}{3} \frac{\frac{\Delta \rho g d^{2}}{\sigma}}{\frac{\Delta \rho g d^{2}}{\sigma} + 4}
```
By defining the Eötvös number as 
```{math}
:label: eq:WaveAnalogy_nonref_6
	Eo = \frac{\Delta \rho g d^{2}}{\sigma}
```
we have 
```{math}
:label: eq:WaveAnalogy_nonref_7
	C_{D} = \frac{8}{3} \frac{Eo}{Eo + 4}
```
This drag correlation is applicable to a wide range of the bubble diameter, e.g. for air bubbles in water $d$ larger than about 1 mm.  

As can be seen in Eq. {eq}`eq:Mendelson_eq_u-wave-analogy` the gravitational wave becomes dominant as $d$ increases. For the limiting case of $Eo \rightarrow \infty$, $C_{D}$ becomes 
```{math}
:label: eq:WaveAnalogy_nonref_8
	C_{D} = \frac{8}{3}
```
which corresponds to the drag coefficient of spherical-cap bubble and the velocity of spherical-cap bubble recovers 
```{math}
:label: eq:Mendelson_eq_u-gravitational
	u = \sqrt{ \frac{\Delta \rho g d}{2 \rho} }
```
For small $Eo$, the capillary wave is dominant and 
```{math}
:label: eq:WaveAnalogy_nonref_9
	C_{D} = \frac{2}{3} Eo \left( 1 + \frac{Eo}{4} \right)^{-1}
```
can be approximated with the condition $Eo/4 \ll 1$ as 
```{math}
:label: eq:WaveAnalogy_nonref_10
	C_{D} = \frac{2}{3} Eo 
```
In the velocity form, this is of course 
```{math}
:label: eq:Mendelson_eq_u-capillary
	u = \sqrt{ \frac{2 \sigma}{\rho d} }
```
This represents that the rise velocity decreases with increasing bubble size, which agrees with experimental facts. The decreasing and increasing trends in Eqs. {eq}`eq:Mendelson_eq_u-capillary` and {eq}`eq:Mendelson_eq_u-gravitational`, respectively, indicate that there is a minimum velocity for a certain critical diameter, at which the dominant force changes. Differentiating Eq. {eq}`eq:Mendelson_eq_u-wave-analogy` with respect to $d$ and setting $du/dd = 0$ yield the critical diameter
```{math}
:label: eq:WaveAnalogy_nonref_11
	d_{c} = 2 \sqrt{ \frac{\sigma}{\Delta \rho g} }
```
The critical diameter is twice longer than the capillary length ($l = \sqrt{\sigma / \Delta \rho g}$). By substituting $d_{c}$ into the velocity equation, we obtain 
```{math}
:label: eq:WaveAnalogy_nonref_12
	u_{c} = \sqrt{2} \left[ \frac{\Delta \rho g \sigma}{\rho^{2}} \right]^{1/4}
```
This velocity corresponds to that obtained with the Ishii-Chawla drag correlation {cite:p}`Ishii1979-sx`: 
```{math}
:label: eq:WaveAnalogy_nonref_13
	C_{D} = \frac{2}{3} \sqrt{Eo}
```
For an air-water system, $d_{c}$ and $u_{c}$ are about 5.5 mm and 0.23 m/s, respectively. 
