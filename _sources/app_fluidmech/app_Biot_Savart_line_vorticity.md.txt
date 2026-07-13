%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
(app_Biot_Savart_line_vorticity)=
# Biot-Savart field by uniform line vorticity

```{admonition} Referred from 
{ref}`auton_lift`
```

```{admonition} References
- {cite:t}`Auton1987-hk`
- {cite:t}`Lighthill1956-ov`
- {cite:t}`Lighthill1956-xl`
```

Let us deduce the Biot-Savart field produced at $\mathbf{r}$ by the uniform line vorticity
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_0
	\boldsymbol{\omega}_{l} = - \frac{\boldsymbol{\omega}_{1}(\mathbf{r}') \cdot \mathbf{e}_{r'}}{a}
```
while referring {ref}`Auton_Auton-line-vorticity`. The line vorticity lies along the position vector $\mathbf{r}'_{i}$, which directs from the origin to the position of the image vorticity for $\boldsymbol{\omega}(\mathbf{r}')$. Since the strength of the line vorticity is uniform, we may write the Biot-Savart integral as 
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_1
	\frac{|\boldsymbol{\omega}_{l}|}{4 \pi} \int_{C} \frac{d\mathbf{s} \times (\mathbf{r} - \mathbf{r}_{l})}{|\mathbf{r} - \mathbf{r}_{l}|^{3}}
```

```{figure} ../fig/Auton-line-vorticity.png
:name: Auton_Auton-line-vorticity
Calculation of Biot-Savart field produced by uniform line vorticity.
```

We first calculate the magnitude of the induced vorticity at $\mathbf{r}$. We take the origin of the coordinate $s$ along the line vorticity as shown in the figure, for which 
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_2
	- s = \frac{R}{\tan \theta} 
```
where $R = |\mathbf{r} - ( \mathbf{r} \cdot \mathbf{e}_{r'} ) \mathbf{e}_{r'}|$
Differentiating this equation yields
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_3
	ds = \frac{R}{ \sin^{2} \theta } d\theta
```
The integration can therefore be carried out as follows:
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_4
	\frac{|\boldsymbol{\omega}_{l}|}{4 \pi} \int_{C} \frac{| d\mathbf{s} \times \tilde{\mathbf{r}} |}{\tilde{r}^{3}}
	= \frac{|\boldsymbol{\omega}_{l}|}{4 \pi} \int_{C} \frac{\tilde{r} ds \sin \theta}{\tilde{r}^{3}}
	= \frac{|\boldsymbol{\omega}_{l}|}{4 \pi} \int_{\alpha}^{\beta} \frac{\sin \theta}{R} d\theta
	= \frac{|\boldsymbol{\omega}_{l}|}{4 \pi R} \left[ - \cos \theta \right]_{\alpha}^{\beta}
	= \frac{|\boldsymbol{\omega}_{l}|}{4 \pi R} \left( \cos \alpha - \cos \beta \right)
```
where $R = \tilde{r} \sin \theta$ was used. Then, the direction of the produced vorticity element at $\mathbf{r}$ is perpendicular to both $\mathbf{r}'_{i}$ and $\mathbf{r}$, and therefore, we can write it as 
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_5
	\mathbf{e}_{r'} \times \frac{\mathbf{r} - ( \mathbf{r} \cdot \mathbf{e}_{r'} ) \mathbf{e}_{r'}}{| \mathbf{r} - ( \mathbf{r} \cdot \mathbf{e}_{r'} ) \mathbf{e}_{r'} |}
	= \frac{ \mathbf{e}_{r'} \times \mathbf{r} }{R}
```
Thus, the produced vorticity at $\mathbf{r}$ is given by
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_6
	\frac{1}{4 \pi} \frac{ |\boldsymbol{\omega}_{l}| \mathbf{e}_{r'} \times \mathbf{r} }{R^{2}} \left( \cos \alpha - \cos \beta \right) 
```
Recall that $\boldsymbol{\omega}_{l} = |\boldsymbol{\omega}_{l}| \mathbf{e}_{r'}$, 
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_7
	\frac{1}{4 \pi} \frac{ \boldsymbol{\omega}_{l} \times \mathbf{r} }{R^{2}} \left( \cos \alpha - \cos \beta \right) 
```
Then, $\cos \alpha$ and $\cos \beta$, can be represented in the following vectorial form: 
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_8
\begin{split}
	&\cos \alpha = \mathbf{e}_{r} \cdot \mathbf{e}_{r'} \\
	&\cos \beta = \frac{(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'}{|(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'|} 
\end{split}
```
Therefore, 
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_9
	\frac{1}{4 \pi} \frac{\boldsymbol{\omega}_{l} \times \mathbf{r}}{|\mathbf{r} - (\mathbf{r} \cdot \mathbf{e}_{r'}) \mathbf{e}_{r'}|^{2}} \left( \mathbf{e}_{r} \cdot \mathbf{e}_{r'} - \frac{(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'}{|(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'|} \right)
```
By integrating all the contributions, we obtain the required result: 
```{math}
:label: eq:app_BiotSavartLineVorticity_nonref_10
	\frac{1}{4 \pi} \iiint_{V'} \frac{\boldsymbol{\omega}_{l} \times \mathbf{r}}{|\mathbf{r} - (\mathbf{r} \cdot \mathbf{e}_{r'}) \mathbf{e}_{r'}|^{2}} \left( \mathbf{e}_{r} \cdot \mathbf{e}_{r'} - \frac{(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'}{|(\mathbf{r} - \mathbf{r}'_{i}) \cdot \mathbf{r}'|} \right) dV'
```

```{seealso}
{cite:t}`Sunagawa1987` for detailed discussion on Biot-Savart law.
```
