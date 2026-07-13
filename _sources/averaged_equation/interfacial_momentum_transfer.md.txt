(interfacial_momentum_transfer)=
# Interfacial momentum transfer

Hereafter, we omit $\overline{( ~~ )}$ for simplicity. 

## Drag 

```{seealso} 
- {ref}`drag_sphere`
- {ref}`deformed_bubble`
```

The drag force acting on a bubble in liquid is given by 
```{math}
:label: eq:eq_int_mom_trans_1
\mathbf{F}_{D} = - C_{D} \frac{\rho_{L}}{2} \left| \mathbf{v}_{G} - \mathbf{v}_{L} \right| \left( \mathbf{v}_{G} - \mathbf{v}_{L} \right) \frac{\pi d^{2}}{4}
```
where $d$ is the sphere-volume equivalent bubble diameter, and $C_{D}$ is the drag coefficient. Suppose that $N$ bubbles are in the averaging volume $V$. The total momentum transfer from $L$ to $G$ due to drag is therefore written as 
```{math}
:label: eq:eq_int_mom_trans_2
\mathbf{M}_{D}^{l \rightarrow g} = 
\frac{N \mathbf{F}_{D}}{V} = 
- \frac{3}{4} \alpha_{G}  C_{D} \rho_{L} \left| \mathbf{v}_{G} - \mathbf{v}_{L} \right| \left( \mathbf{v}_{G} - \mathbf{v}_{L} \right) 
```
The reaction: 
```{math}
:label: eq:eq_int_mom_trans_3
\mathbf{M}_{D}^{l \rightarrow g} = - \mathbf{M}_{D}^{g \rightarrow l}
```
For poly-dispersed bubbly flows, the interface area concentration and Sauter mean diameter are more suitable for considering the momentum transfer through bubble surfaces. Let $P(d)$ be the probability density of bubbles within $d(d)$ (a small fraction of diameter range). The mean diameter is defined by 
```{math}
:label: eq:eq_int_mom_trans_4
\overline{d} = \int_{0}^{\infty} P(d) d d(d)
```
while Sauter mean diameter is defined by 
```{math}
:label: eq:eq_int_mom_trans_5
d_{S} = 
\frac{\int_{0}^{\infty} P(d) d^{3} d(d)}{\int_{0}^{\infty} P(d) d^{2} d(d)
}
```
The interface area concentration, $a_{\text{int}}$, is given by 
```{math}
:label: eq:eq_int_mom_trans_6
a_{\text{int}} 
= \frac{6 \alpha_{G}}{d_{S}}
```
Thus, 
```{math}
:label: eq:eq_int_mom_trans_10
\mathbf{M}_{D}^{l \rightarrow g} 
= - \frac{a_{\text{int}}}{8} C_{D} \rho_{L} \left| \mathbf{v}_{G} - \mathbf{v}_{L} \right| \left( \mathbf{v}_{G} - \mathbf{v}_{L} \right)
```


## Lift

```{seealso} 
- {ref}`auton_lift`
- {ref}`negative_lift`
```

The lift force acting on a bubble is given by 
```{math}
:label: eq:eq_int_mom_trans_11
\mathbf{F}_{L} = - C_{L} \rho_{L} \frac{\pi d^{3}}{6} \left| \mathbf{v}_{G} - \mathbf{v}_{L} \right| \times \nabla \times \mathbf{v}_{L}
```
Being similar to the drag the momentum transfer is given by 
```{math}
:label: eq:eq_int_mom_trans_12
\mathbf{M}_{L}^{l \rightarrow g} = 
- \alpha _{G} C_{L} \rho_{L} \left| \mathbf{v}_{G} - \mathbf{v}_{L} \right| \times \nabla \times \mathbf{v}_{L}
```


## Virtual mass

```{seealso} 
{ref}`virtual_mass`
```

```{math}
:label: eq:eq_int_mom_trans_13
\mathbf{M}_{VM}^{l \rightarrow g} = 
\alpha_{G} C_{VM} \rho_{L} \left( \frac{D \mathbf{v}_{L}}{Dt} - \frac{D \mathbf{v}_{G}}{Dt} \right) 
```

## Another closures

- Turbulent dispersion force
- Wall lubrication force