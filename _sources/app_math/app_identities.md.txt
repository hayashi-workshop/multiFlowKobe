(app_identities)=
# Some useful identities

```{admonition} Referred from 
{ref}`stokes_drag_LL`
```

For a scalar field $\phi$, 
```{math}
:label: eq:app_identities_nonref_0
	\nabla \times \nabla \phi 
	\rightarrow 
	\epsilon_{ijk} \frac{\partial }{\partial x_{j}} \frac{\partial \phi}{\partial x_{k}} = \epsilon_{ijk} \frac{\partial^{2} \phi}{\partial x_{j} \partial x_{k}}
```
Since $\epsilon_{ijk} = - \epsilon_{ikj}$, 
```{math}
:label: eq:app_identities_nonref_1
	\epsilon_{ijk} \frac{\partial^{2} \phi}{\partial x_{j} \partial x_{k}}
	= - \epsilon_{ikj} \frac{\partial^{2} \phi}{\partial x_{j} \partial x_{k}}
```
However, the differentiation with respect to $x$ is free to exchange, so that  
```{math}
:label: eq:app_identities_nonref_2
	- \epsilon_{ikj} \frac{\partial^{2} \phi}{\partial x_{j} \partial x_{k}}
	= - \epsilon_{ikj} \frac{\partial^{2} \phi}{\partial x_{k} \partial x_{j}}
```
The indices $j$ and $k$ in the last equation are dummy; therefore rewriting $j \rightarrow k$ and $k \rightarrow j$ gives 
```{math}
:label: eq:app_identities_nonref_3
	- \epsilon_{ikj} \frac{\partial^{2} \phi}{\partial x_{k} \partial x_{j}}
	= - \epsilon_{ijk} \frac{\partial^{2} \phi}{\partial x_{j} \partial x_{k}}
```
Adding this result to the first equation yields 
```{math}
:label: eq:app_identities_nonref_4
	2 \nabla \times \nabla \phi 	
	\rightarrow 
	\epsilon_{ijk} \frac{\partial }{\partial x_{j}} \frac{\partial \phi}{\partial x_{k}} = \epsilon_{ijk} \frac{\partial^{2} \phi}{\partial x_{j} \partial x_{k}}
	- \epsilon_{ijk} \frac{\partial^{2} \phi}{\partial x_{j} \partial x_{k}}
	= 0
```
Therefore, the rotation of the gradient of a scalar field is identically zero: 
```{math}
:label: eq:app_identities_nonref_5
	\nabla \times \nabla \phi = 0
```

For a vector field $\mathbf{f}$, 
```{math}
:label: eq:app_identities_nonref_6
	\nabla \cdot \nabla \times \mathbf{f}
	\rightarrow \frac{\partial }{\partial x_{i}} \epsilon_{ijk} \frac{\partial f_{k}}{\partial x_{j}}
	= \epsilon_{ijk} \frac{\partial^{2} f_{k}}{\partial x_{i} \partial x_{j}}	
```
With the same manner we used above, it can be shown that 
```{math}
:label: eq:app_identities_nonref_7
	\nabla \cdot \nabla \times \mathbf{f} = 0 
```

When we have $\times$ twice, we often use 
```{math}
:label: eq:app_identities_nonref_8
	\epsilon_{kij} \epsilon_{kmn}
	= \delta_{im} \delta_{jn} - \delta_{in} \delta_{jm} 
```

We often meet \textit{rotation of rotation}, $\nabla \times \nabla \times \mathbf{f}$, in vector calculus for fluid mechanics. This can be rewritten in a form expressed in terms of $grad$ and $div$ as follows: 
```{math}
:label: eq:app_identities_nonref_9
\begin{split}	
	\nabla \times \nabla \times \mathbf{f}
	&\rightarrow \epsilon_{ijk} \frac{\partial }{\partial x_{j}} \epsilon_{kmn}  \frac{\partial f_{n}}{\partial x_{m}}
	= \epsilon_{ijk} \epsilon_{kmn} \frac{\partial }{\partial x_{j}}  \frac{\partial f_{n}}{\partial x_{m}}
	= ( \delta_{im} \delta_{jn} - \delta_{in} \delta_{jm} ) \frac{\partial }{\partial x_{j}}  \frac{\partial f_{n}}{\partial x_{m}}
	= \frac{\partial }{\partial x_{j}} \frac{\partial f_{j}}{\partial x_{i}} - \frac{\partial }{\partial x_{j}} \frac{\partial f_{i}}{\partial x_{j}} \\
	&= \frac{\partial }{\partial x_{i}} \frac{\partial f_{j}}{\partial x_{j}} - \frac{\partial^{2} f_{i}}{\partial x_{j} \partial x_{j}} 
\end{split}
```
Therefore,
```{math}
:label: eq:app_identities_nonref_10
	\nabla \times \nabla \times \mathbf{f}
	= \nabla \nabla \cdot \mathbf{f} - \nabla^{2} \mathbf{f}
```
