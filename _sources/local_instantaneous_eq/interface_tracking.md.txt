(interface_tracking)=
# Interface tracking

As we found in Eq. {eq}`eq:Introduction_eq_continuity_of_velocity`, the interface moves with the fluids. The interface can be written with a scalar function $S(\mathbf{x}, t)$ as $S(\mathbf{x}, t) = 0$. The fluid particle on the interface always stay on it, so that, 
```{math}
:label: eq:LocalInstantaneousEq_nonref_27
    \frac{DS}{Dt} = 0,~~~~\frac{\partial S}{\partial t} + \mathbf{v}_{int} \cdot \nabla S = 0
```
By using the definition $\mathbf{n} = \nabla S / |\nabla S|$, we may rewrite the second expression as 
```{math}
:label: eq:LocalInstantaneousEq_nonref_28
    \frac{1}{| \nabla S |} \frac{\partial S}{\partial t} = -  \mathbf{v}_{int} \cdot \mathbf{n}
```
This form clearly shows that the interface shape is evolved by the normal velocity component; consider a rotating sphere with a finite rotational (tangential) velocity. The fluid particles are moving along the interface, but the interface shape does not change. 