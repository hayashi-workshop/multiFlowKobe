(stokes_drag_GKB)=
# Drag acting on a solid sphere in Stokes flow (GKB)

```{admonition} Summary
* **Subject:** Stokes drag 
* **Main conclusion:** Drag $F_{D} = 6 \pi \mu u a$ in Stokes flow ($Re \ll 1$). 
* **Key idea** $p$ is a harmonic function under the Stokes approximation, which determines the functional form of vorticity $\boldsymbol{\omega}$; then, the velocity field is obtained from Stokes' stream function by solving $\nabla^{2} \Psi = \omega_{\varphi}$.  
* **Reference:** Derivation presented here is given by G. K. Batchelor {cite:p}`Batchelor2000`.
```

Another way to derive the Stokes solution is as follows. The Stokes equations is given by 
```{math}
:label: eq:StokesDrag_nonref_56
    \nabla p = \mu \nabla^{2} \mathbf{v}
```
Due to the symmetry of the flow about the axis and the symmetry for the reversal of the direction of $\mathbf{u}$, we assume that the pressure is a function of $\mathbf{u} \cdot \mathbf{r} / r = \mathbf{u} \cdot \mathbf{e}_{r} = - u \cos \theta$. 
```{toggle}
As can be seen in {numref}`Stokes_Direction cosine`, $( \mathbf{u} \cdot \mathbf{e}_{r} )_{\theta} = - ( \mathbf{u} \cdot \mathbf{e}_{r} )_{\theta + \pi/2}$. This is valid for the change of the direction of $\mathbf{u}$. 
```
In addition, for the $r$ dependence, we assume that the pressure field depends on the distance from the sphere, $F(|\mathbf{r}|^{2}/a^{2})$. Therefore, 
```{math}
:label: eq:StokesDrag_nonref_57
    p = p_{0} + \mu F(|\mathbf{r}|^{2}/a^{2}) \mathbf{u} \cdot \mathbf{e}_{r}
```
Taking $div$ of the Stokes equation, we obtain 
```{math}
:label: eq:StokesDrag_nonref_58
\begin{split}
    &\frac{\partial}{\partial x_{i}} \frac{\partial p}{\partial x_{i}} 
    = \frac{\partial}{\partial x_{i}} \left( \mu \frac{\partial^{2} v_{i}}{\partial x_{j} \partial x_{j}} \right)
    = \mu \frac{\partial^{2}}{\partial x_{j} \partial x_{j}} \left( \frac{\partial v_{i}}{\partial x_{i}} \right)
    = 0 \\
    &\rightarrow \nabla^{2} p = 0
\end{split}
```
where we used the continuity equation $\nabla \cdot \mathbf{v} = 0$. With the spherical coordinates (see Appendix {ref}`app_NSeq_in_polar_sys`), the Laplace equation takes the following form:
```{toggle}
Substituting Eq. {eq}`eq:Stokes_eq_pressure` confirms this equation.
```
```{math}
:label: eq:StokesDrag_nonref_59
\frac{1}{r^{2}}
\frac{\partial}{\partial r}
\left( r^{2} \frac{\partial p}{\partial r} \right)
+
\frac{1}{r^{2} \sin \theta} \frac{\partial }{\partial \theta}
\left( \sin \theta\frac{\partial p}{\partial \theta} \right)
=
0
```
where the $\varphi$ term disappears due to the symmetry. Substituting the functional form of the pressure assumed above into the second term yields
```{math}
:label: eq:StokesDrag_nonref_60
    \frac{1}{r^{2} \sin \theta} \frac{\partial }{\partial \theta} \left( \sin \theta\frac{\partial p}{\partial \theta} \right) 
    = - \mu F u \frac{1}{r^{2} \sin \theta} \frac{\partial }{\partial \theta} \left( \sin \theta\frac{\partial \cos \theta}{\partial \theta} \right)  
    = \mu \frac{u \cos \theta}{r^{2}} 2 F  
```
For the first term, we have 
```{math}
:label: eq:StokesDrag_nonref_61
\frac{1}{r^{2}}
\frac{\partial}{\partial r}
\left( r^{2} \frac{\partial p}{\partial r} \right)
= -\mu \frac{u \cos \theta }{r^{2}}
\frac{\partial}{\partial r}
\left( r^{2} \frac{\partial F}{\partial r} \right)
```
Therefore, to satisfy the Laplace equation, we need to have $F$ such that 
```{math}
:label: eq:StokesDrag_nonref_62
\frac{\partial}{\partial r}
\left( r^{2} \frac{\partial F}{\partial r} \right) = 2F
```
Hence, 
```{math}
:label: eq:StokesDrag_nonref_63
    F = \frac{\alpha'}{r^{2}}
```
and 
```{math}
:label: eq:StokesDrag_nonref_64
    p = p_{0} + \frac{\alpha' \mu ( \mathbf{u} \cdot \mathbf{e}_{r} )}{r^{2}}
```
where $\alpha'$ should be represented in term of $a$. Recalling the identity $\nabla \times \nabla \times (\text{any vector}) = \nabla (\nabla \cdot (\text{any vector})) - \nabla^{2} (\text{any vector})$, we have 
```{math}
:label: eq:StokesDrag_nonref_65
    \nabla \times \nabla \times \mathbf{v} = \nabla (\nabla \cdot \mathbf{v}) - \nabla^{2} \mathbf{v}
    \rightarrow \nabla \times \boldsymbol{\omega} = - \nabla^{2} \mathbf{v}
```
where the continuity equation was used to remove the first term on the R.H.S. The Stokes equation becomes 
```{math}
:label: eq:StokesDrag_nonref_66
    \nabla p = - \mu \nabla \times \boldsymbol{\omega}
```
In the present flow filed symmetrical about the $z$ axis, only non-zero component of the vorticity is the azimuthal one $\omega_{\varphi}$. Therefore, we should have proportionality $\boldsymbol{\omega} \propto \mathbf{u} \times \mathbf{e}_{r}$. Being similar to the case of $p$, we set $\boldsymbol{\omega} = G(|\mathbf{r}|^{2}/a^{2}) \mathbf{u} \times \mathbf{e}_{r}$. Since $\mathbf{u} = - u \cos \theta \mathbf{e}_{r} + u \sin \theta \mathbf{e}_{\theta}$, 
```{toggle}
A geometric consideration shows $\sin \theta \mathbf{e}_{\varphi} = - \frac{\mathbf{u}}{u} \times \mathbf{e}_{r}$. Here, $-\mathbf{u}/u$ is the unit vector directing $+z$. Thus, $\mathbf{u} \times \mathbf{e}_{r} = - u \sin \mathbf{e}_{\varphi}$. 
```

```{math}
:label: eq:StokesDrag_nonref_68
    \mathbf{u} \times \mathbf{e}_{r}
    = ( - u \cos \theta \mathbf{e}_{r} + u \sin \theta \mathbf{e}_{\theta} ) \times \mathbf{e}_{r}
    = - u \sin \theta \mathbf{e}_{\varphi}
```
For $\boldsymbol{\omega} = (0, 0, \omega_{\varphi}) = (0, 0, -G u \sin \theta)$, the rotation of the vorticity is calculated as 
```{math}
:label: eq:StokesDrag_nonref_69
\begin{split}
\nabla \times \boldsymbol{\omega}
&=
\frac{1}{r \sin \theta} 
\left( \frac{\partial \omega_{\varphi} \sin \theta}{\partial \theta} \right) \mathbf{e}_{r} - \frac{1}{r} \left( \frac{\partial r \omega_{\varphi}}{\partial r} \right) \mathbf{e}_{\theta} \\
&=
\frac{-G u}{r \sin \theta} 
\left( \frac{\partial \sin^{2} \theta}{\partial \theta} \right) \mathbf{e}_{r} 
+ \frac{u \sin \theta}{r} \left( \frac{\partial r G}{\partial r} \right) \mathbf{e}_{\theta}\\
&= 
\frac{- 2 G u \cos \theta}{r} \mathbf{e}_{r} 
+ 
u \sin \theta \left( \frac{G}{r} + \frac{\partial G}{\partial r} \right) \mathbf{e}_{\theta}
\end{split}
```
We compare this with the pressure gradient term given by 
```{math}
:label: eq:StokesDrag_nonref_70
\begin{split}
    - \frac{\nabla p}{\mu}
    &= - \nabla \left( \frac{\alpha' \mathbf{u} \cdot \mathbf{e}_{r}}{r^{2}} \right)
    = \alpha' u \nabla \frac{\cos \theta}{r^{2}}
    = \alpha' u \left\{ \frac{\partial}{\partial r} \left( \frac{\cos \theta}{r^{2}} \right) \mathbf{e}_{r} + \frac{1}{r} \frac{\partial }{\partial \theta} \left( \frac{\cos \theta}{r^{2}} \right) \mathbf{e}_{\theta} \right\} \\
    &= - \frac{2 \alpha' u \cos \theta}{r^{3}} \mathbf{e}_{r} - \frac{\alpha' u \sin \theta}{r^{3}} \mathbf{e}_{\theta}
\end{split}
```
Hence, 
```{math}
:label: eq:StokesDrag_nonref_71
    G = \frac{\alpha'}{r^{2}}
```
and therefore 
```{toggle}
$\boldsymbol{\omega} = - \alpha' \frac{u \sin \theta}{r^{2}} \mathbf{e}_{\varphi}$
```
```{math}
:label: eq:StokesDrag_nonref_73
    \boldsymbol{\omega} = \frac{\alpha' \mathbf{u} \times \mathbf{e}_{r}}{r^{2}}
```
We need to determine $\alpha'$ by considering the velocity field. 

The continuity equation in the spherical coordinates system is given by 
```{math}
:label: eq:StokesDrag_nonref_74
\begin{split}
\frac{1}{r^{2}} \frac{\partial r^{2} v_{r}}{\partial r}
+ \frac{1}{r \sin \theta} \frac{\partial v_{\theta} \sin \theta}{\partial \theta}
= 0
\end{split}
```
where we omit the $\varphi$ component. The Stokes' stream function $\Psi$ defined by the following equation satisfies the continuity equation:  
```{math}
:label: eq:Stokes_eq_Stokes_streamfunction_definition
    v_{r} = \frac{1}{r^{2} \sin \theta} \frac{\partial \Psi}{\partial \theta},~~~~v_{\theta} = - \frac{1}{r \sin \theta} \frac{\partial \Psi}{\partial r}
```
Using the stream function, the azimuthal component of vorticity becomes 
```{math}
:label: eq:StokesDrag_nonref_75
\omega_{\varphi}
=
\frac{1}{r} \left( \frac{\partial r v_{\theta}}{\partial r} - \frac{\partial v_{r}}{\partial \theta} \right)
= 
- \frac{1}{r} \left\{ \frac{1}{\sin \theta} \frac{\partial^{2} \Psi}{\partial r^{2}} + \frac{1}{r^{2}} \frac{\partial}{\partial \theta} \left( \frac{1}{\sin \theta} \frac{\partial \Psi}{\partial \theta} \right) \right\}
```
Thus, 
```{math}
:label: eq:StokesDrag_nonref_76
    \frac{\partial^{2} \Psi}{\partial r^{2}} + \frac{\sin \theta}{r^{2}} \frac{\partial}{\partial \theta} \left( \frac{1}{\sin \theta} \frac{\partial \Psi}{\partial \theta} \right)
    = \frac{\alpha' u \sin^{2} \theta}{r}
```
Comparing the first term on the L.H.S. and the R.H.S. indicates that $\Psi$ should be proportional to $\sin^{2} \theta$, and therefore we assume 
```{math}
:label: eq:Stoles_eq_Stokes_streamfunction
    \Psi = f(r) u \sin^{2} \theta
```
Substituting this form into the P.D.E. yields the following O.D.E.: 
```{math}
:label: eq:Stokes_eq_f_ODE_Batchelor
    r^{2} \frac{d^{2}f}{dr^{2}} - 2f = \alpha' r
```
Consider the solution in the following form: 
```{math}
:label: eq:StokesDrag_nonref_77
    f(r) = c_{0} + \sum_{n=1}^{\infty} \left( c_{n} r^{n} + \frac{\tilde{c}_{n}}{r^{n}} \right)
```
Differentiating this with respect to $r$ gives 
```{math}
:label: eq:StokesDrag_nonref_78
\begin{split}
    &\frac{df}{dr} = \sum_{n=1}^{\infty} \left( n c_{n} r^{n-1} - n \frac{\tilde{c}_{n}}{r^{n+1}} \right) \\
    &\frac{d^{2}f}{dr^{2}} = \sum_{n=2}^{\infty} n (n - 1) c_{n} r^{n-2} + \sum_{n=1}^{\infty} n (n+1) \frac{\tilde{c}_{n}}{r^{n+2}} 
\end{split}
```
Shifting the index of the first term of the second equation, we have 
```{math}
:label: eq:StokesDrag_nonref_79
    \frac{d^{2}f}{dr^{2}} = \sum_{n=1}^{\infty} n (n + 1) c_{n+1} r^{n-1} + \sum_{n=1}^{\infty} n (n+1) \frac{\tilde{c}_{n}}{r^{n+2}} 
```
Substituting these expressions into Eq. {eq}`eq:Stokes_eq_f_ODE_Batchelor` yields
```{math}
:label: eq:StokesDrag_nonref_80
    \sum_{n=1}^{\infty} \left\{ [ n (n + 1) c_{n+1} r - 2 c_{n} ] r^{n} +  [ n (n+1) - 2 ] \frac{\tilde{c}_{n}}{r^{n}} \right\} - 2 c_{0} = \alpha' r
```
Comparing the L.H.S. and the R.H.S., obviously $c_{0} = 0$. The terms of $\tilde{c}_{n}/r^{n}$ must vanish by themselves; for this $n(n + 1) - 2 = 0$. The roots are $n = 1, -2$. However, $n = -2$ is outside the range of summation and must be discarded. For the first term, 
```{math}
:label: eq:StokesDrag_nonref_81
\begin{split}
    &n=1:~~(2c_{2} r - 2c_{1}) r \\
    &n=2:~~(6c_{3}r - 2c_{2}) r^{2} \\
    &n=3:~~(12c_{4}r - 2c_{3}) r^{3} \\
    &~~~~\vdots
\end{split}
```
For $n = 1$, we find $c_{1} = - \alpha'/2$ from the second term, and the first term cancels out with the second term of $n = 2$. Then, $c_{n} = 0$ for $n > 2$. Thus, we obtain 
```{math}
:label: eq:StokesDrag_nonref_82
    f(r) = - \frac{\alpha'}{2} r + c_{2} r^{2} + \frac{\tilde{c}_{1}}{r}
```

Substituting Eq. {eq}`eq:Stoles_eq_Stokes_streamfunction` into Eq. {eq}`eq:Stokes_eq_Stokes_streamfunction_definition` yields 
```{math}
:label: eq:StokesDrag_nonref_83
\begin{split}
    &v_{r} = \frac{2 u \cos \theta}{r^{2}} f = \frac{2 u \cos \theta}{r^{2}} \left( - \frac{\alpha'}{2} r + c_{2} r^{2} + \frac{\tilde{c}_{1}}{r} \right)  \\
    &v_{\theta} = - \frac{u \sin \theta}{r} \frac{df}{dr} = - \frac{u \sin \theta}{r} \left( - \frac{\alpha'}{2} + 2 c_{2} r - \frac{\tilde{c}_{1}}{r^{2}} \right)
\end{split}
```
$c_{2} = -1/2$ to recover $\mathbf{v} = (-u\cos \theta, u \sin \theta,0)$ in the far field. Then, the noslip condition on the sphere $v_{r} = v_{\theta} = 0$ at $r = a$ gives
```{math}
:label: eq:StokesDrag_nonref_84
    \begin{split}
    &\tilde{c}_{1} = \frac{a^{2}}{2} \alpha' + \frac{a^{3}}{2} \\
    &\tilde{c}_{1} = - \frac{a^{2}}{2} \alpha' - a^{3}
    \end{split}
```
Solving the set of equations, we obtain $\tilde{c}_{1} = -a^{3}/4$ and $\alpha' = -3a/2$. Hence, 
```{math}
:label: eq:StokesDrag_nonref_85
    f(r) = \frac{3a}{4} r - \frac{r^{2}}{2} - \frac{a^{3}}{4 r},~~\frac{df}{dr} = \frac{3a}{4} - r + \frac{a^{3}}{4 r^{2}}
```
and 
```{math}
:label: eq:StokesDrag_nonref_86
\begin{split}
	&v_{r}	= - u \cos \theta \left( 1 - \frac{3a}{2r} + \frac{a^{3}}{2 r^{3}} \right) \\
	&v_{\theta} = u \sin \theta \left( 1 - \frac{3a}{4r} - \frac{a^{3}}{4 r^{3}} \right) \\
    &p = p_{0} + \frac{3 \mu a u}{2 r^{2}} \cos \theta \\
    &\omega_{\varphi} = \frac{3a }{2} \frac{u \sin \theta}{r^{2}}
\end{split}
```
These are, of course, the same as those we obtained previously. 

```{seealso} 
{ref}`drag_vorticity`
```