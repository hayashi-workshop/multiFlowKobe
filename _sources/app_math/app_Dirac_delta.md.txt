(app_Dirac_delta)=
# $\nabla^{2} (1/r)$ behaves as Dirac's delta

```{figure} ../fig/Auton-DiracDelta.png
:name: Auton_Auton-DiracDelta
Small sphere $S_{\epsilon}$ surrounded by closed surface $S$.
```

At $\mathbf{r} \neq \mathbf{r}'$, 
```{math}
:label: eq:app_DiracDelta_nonref_0
	\nabla^{2}\frac{1}{r}
	\rightarrow \frac{\partial }{\partial x_{k}} \frac{\partial }{\partial x_{k}} \frac{1}{|\mathbf{r} - \mathbf{r}'|}
	= - \left\{ \frac{\delta_{kk}}{|\mathbf{r} - \mathbf{r}'|^{3}} - \frac{3 (x_{k} - x'_{k})^{2}}{|\mathbf{r} - \mathbf{r}'|^{5}} \right\}
	= 0
```
Let $S_{\epsilon}$ be a small sphere of infinitesimal radius $R$ at $\mathbf{r}'$ and $S$ be a surface surrounding volume $V$, which includes $S_{\epsilon}$ ({numref}`Auton_Auton-DiracDelta`). For the volume $V - V_{\epsilon}$, 
```{math}
:label: eq:Auton_eq_integral-V-Ve
	\iiint_{V - V_{\epsilon}} \nabla^{2} \frac{1}{|\mathbf{r} - \mathbf{r}'|} dV = 0
```
where $V_{\epsilon}$ is the volume of the small sphere. Applying the divergence theorem yields 
```{math}
:label: eq:app_DiracDelta_nonref_1
	\iint_{S + S_{\epsilon}} \mathbf{n} \cdot \nabla \frac{1}{|\mathbf{r} - \mathbf{r}'|} dV 
	= \iint_{S} \mathbf{n} \cdot \nabla \frac{1}{|\mathbf{r} - \mathbf{r}'|} dS + \iint_{S_{\epsilon}} \mathbf{n} \cdot \nabla \frac{1}{|\mathbf{r} - \mathbf{r}'|} dS = 0
```
Note that $\mathbf{n}$ in the second term is the unit normal directing the inside of the small sphere, that is, $\mathbf{n} = - (\mathbf{r} - \mathbf{r}')/|\mathbf{r} - \mathbf{r}'|$. The second term becomes 
```{math}
:label: eq:app_DiracDelta_nonref_2
	\iint_{S_{\epsilon}} \mathbf{n} \cdot \nabla \frac{1}{|\mathbf{r} - \mathbf{r}'|} dS 
	= - \iint_{S_{\epsilon}} \mathbf{n} \cdot \frac{\mathbf{r} - \mathbf{r}'}{|\mathbf{r} - \mathbf{r}'|^{3}} dS 
	= \iint_{S_{\epsilon}} \frac{(\mathbf{r} - \mathbf{r}')\cdot(\mathbf{r} - \mathbf{r}')}{|\mathbf{r} - \mathbf{r}'|^{4}} dS 
	= \iint_{S_{\epsilon}} \frac{dS}{|\mathbf{r} - \mathbf{r}'|^{2}} 
	= 4 \pi
```
Hence, 
```{math}
:label: eq:app_DiracDelta_nonref_3
	\iint_{S} \mathbf{n} \cdot \nabla \frac{1}{|\mathbf{r} - \mathbf{r}'|} dS = - \iint_{S_{\epsilon}} \mathbf{n} \cdot \nabla \frac{1}{|\mathbf{r} - \mathbf{r}'|} dS = - 4 \pi
```
The first equation of the above can however be written as the volume integral for $V$: 
```{math}
:label: eq:Auton_eq_integral-V-4pi
	\iiint_{V} \nabla^{2} \frac{1}{|\mathbf{r} - \mathbf{r}'|} dV = - 4 \pi
```
From Eqs. {eq}`eq:Auton_eq_integral-V-Ve` and {eq}`eq:Auton_eq_integral-V-4pi`, we notice that $- 4 \pi$ comes only from the infinitesimal sphere $V_{\epsilon}$ at $\mathbf{r} - \mathbf{r}'$, leading to 
```{math}
:label: eq:app_DiracDelta_nonref_4
	\iiint_{V} \nabla^{2} \frac{1}{|\mathbf{r} - \mathbf{r}'|} dV = \iiint_{V} - 4 \pi \delta \left( |\mathbf{r} - \mathbf{r}'| \right) dV = - 4 \pi
```
Hence, 
```{math}
:label: eq:app_DiracDelta_nonref_5
	\nabla^{2} \frac{1}{|\mathbf{r} - \mathbf{r}'|} = - 4 \pi \delta \left( |\mathbf{r} - \mathbf{r}'| \right)
```

