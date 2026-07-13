(isotherm)=
# Isotherm and surfactant kinetics

```{admonition} Summary
* **Subject:** Isotherm 
* **Main conclusion:** $\sigma = \sigma_{0} + n R T \Gamma_{max} \ln \left( 1 - \frac{\Gamma}{\Gamma_{max}} \right)$
* **Key idea** Thermodynamic analysis derives surface tension as a function of surfactant concentration. 
* **References:** 
	- {cite:t}`Chang1995-oa`
```

Surface-active agents are generally referred to as surfactant. They have hydrophilic and hydrophobic groups in their molecular structure. When soluble surfactants are present in water, their hydrophobic group feels frustrated to be inside the water, so the surfactant molecules migrate toward gas-liquid interfaces to put the hydrophobic group in the gas phase and to keep the hydrophilic group inside the water. The surface tension $\sigma$ of a gas-liquid interface reduces its value by accumulation of surfactant. 

The following Gibbs adsorption equation gives an estimate of the amount of surfactant from the characteristics of the surface tension reduction: 
```{math}
:label: eq:contami_Gibbs-adsorption-eq
	\Gamma = - \frac{1}{n R T} \left( \frac{\partial \sigma}{\partial \ln C_{0}} \right)_{T}
```
where $\Gamma$ is the interfacial surfactant concentration (mol per unit area), $C_{0}$ is the surfactant concentration in the bulk liquid (mol per cubic meter), $R$ is the gas constant, and $T$ is the temperature. Generally, $n = 1$ for a non-ionic surfactant, while $n = 2$ for an ionic surfactant. The following relation between $\Gamma$ and $C_{0}$ is known as Henry's isotherm: 
```{math}
:label: eq:contami_isotherm-henry
	\Gamma = K_{H} C_{0}
```
where $K_{H}$ is the adsorption length (m). By integrating Eq. {eq}`eq:contami_Gibbs-adsorption-eq` with Eq. {eq}`eq:contami_isotherm-henry` for $\Gamma$, we obtain
```{toggle}
Substituting Eq. {eq}`eq:contami_isotherm-henry` into Eq. {eq}`eq:contami_Gibbs-adsorption-eq` gives $- n R T K_{H} e^{\ln C_{0}} = \frac{\partial \sigma}{\partial \ln C_{0}}$, where we replaced $C_{0}$ in the L.H.S. with $e^{\ln C_{0}}$. 

$\sigma = c - n R T K_{H} e^{\ln C_{0}} = c - n R T K_{H} C_{0} = c - n R T \Gamma$

The surface tension in the absence of surfactants is denoted by $\sigma_{0}$. Integrating this gives Eq. {eq}`eq:contami_surface-equation-henry`. 
```
```{math}
:label: eq:contami_surface-equation-henry
	\sigma = \sigma_{0} - n R T \Gamma
```
where $\sigma_{0}$ is the surface tension in the absence of surfactants. It is obvious that $\Gamma$ obeying Henry's isotherm has no upper limit in its amount. The Langumuir isotherm is an extension of Henry's isotherm by accounting for the upper limit, $\Gamma_{max}$, which is the maximum interfacial concentration: 
```{math}
:label: eq:contami_isotherm-langmuir
	\Gamma = \frac{K_{L} C_{0}}{1 + K_{L} C_{0}} \Gamma_{max} 
```
where $K_{L}$ is the Langmuir equilibrium adsorption constant (cubic meters per mol). Using this isotherm and the Gibbs equation yields the Szyszkowski equation:
```{toggle}
By substituting the Langmuir isotherm into the Gibbs equation we have 

$\frac{\partial \sigma}{\partial \ln C_{0}} = - n R T \Gamma_{max} \frac{K_{L} C_{0}}{1 + K_{L} C_{0}}$ 

Using the chain rule $\partial \sigma / \partial \ln C_{0} = (\partial \sigma / \partial C_{0}) (\partial C_{0} / \partial \ln C_{0}) = C_{0} \partial \sigma / \partial C_{0}$ we have 

$\frac{\partial \sigma}{\partial C_{0}} = - n R T \Gamma_{max} \frac{K_{L}}{1 + K_{L} C_{0}}$

Integrating this gives Eq. {eq}`eq:contami_surface-equation-langmuir`. 
```
```{math}
:label: eq:contami_surface-equation-langmuir
	\sigma = \sigma_{0} - n R T \Gamma_{max} \ln (1 + K_{L} C_{0})
```
Since $\Gamma/\Gamma_{max} - 1 = 1/(1 + K_{L} C_{0})$, the above equation can be rewritten in the form of the Frumkin surface equation: 
```{math}
:label: eq:contami_surface-equation-frumkin
	\sigma = \sigma_{0} + n R T \Gamma_{max} \ln \left( 1 - \frac{\Gamma}{\Gamma_{max}} \right)
```

The net surfactant flux $\dot{S}_{\Gamma}$ is often expressed as a superposition of the adsorption and desorption fluxes: 
```{math}
:label: eq:contami_surfactant-flux
	\dot{S}_{\Gamma} = Q(C_{S}, \Gamma) - P(\Gamma)
```
where $Q$ is the adsorption flux and $P$ is the desorption flux. The former is a function of the bulk surfactant concentration $C_{S}$ at the interface and $\Gamma$, while the latter depends only on $\Gamma$. A linear model is given by the Langmuir-Hinshelwood equation: 
```{math}
:label: eq:contami_frumkin-levich
	\dot{S}_{\Gamma} = k_{a} C_{S} \left( \Gamma_{max} - \Gamma \right) - k_{d} \Gamma
```
$k_{a}$ and $k_{d}$ are the adsorption and desorption rate constants, respectively. For the adsorption-desorption equilibrium, $\dot{S}_{\Gamma} = 0$, the equilibrium concentration $\Gamma_{eq}$ is given by 
```{math}
:label: eq:ContaminatedDrop_nonref_0
	\Gamma_{eq} = \frac{k_{a} C_{S}}{k_{d} + k_{a} C_{S}} \Gamma_{max}
```
It is assumed that, for surfactant transfer from the bulk to the interface faster than the adsorption time scale, $C_{S} \sim C_{0}$, for which $\Gamma_{eq}$ corresponds to $\Gamma$ in the Langmuir isotherm, that is, 
```{math}
:label: eq:contami_frumkin-levich-c0
	\dot{S}_{\Gamma} = k_{a} C_{0} \left( \Gamma_{max} - \Gamma \right) - k_{d} \Gamma
```
and 
```{math}
:label: eq:ContaminatedDrop_nonref_1
	\Gamma_{eq} 
	= \frac{k_{a} C_{0}}{k_{d} + k_{a} C_{0}} \Gamma_{max}
	= \frac{K_{L} C_{0}}{1 + K_{L} C_{0}} \Gamma_{max}
	= \frac{La}{1 + La} \Gamma_{max}
```
where 
```{math}
:label: eq:ContaminatedDrop_nonref_2
	K_{L} = \frac{k_{a}}{k_{d}}
```
and the Langmuir number 
```{math}
:label: eq:ContaminatedDrop_nonref_3
	La = \frac{k_{a} C_{0}}{k_{d}}
```
