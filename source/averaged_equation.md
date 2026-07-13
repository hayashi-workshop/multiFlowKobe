(averaged_equation)=
# Averaged equations

```{admonition} Summary
* **Subject:** How to deal with numerous bubbles, drops, and particles in practical systems. 
* **Main conclusions** Averaged equations and closture relationships
* **Key idea** Averaged equations of the two phases are solved with interfacial mass/momentum transfer. 
* **References** 
    - {cite:t}`Drew1999`
    - {cite:t}`Tomiyama2018-vl`
```


```{toctree}
:maxdepth: 1

averaged_equation/averaging_basic_equations
averaged_equation/interfacial_momentum_transfer
```

```{figure} fig/euler_lagrange.jpg
:name: euler_lagrange
Euler-Lagrange simulation example. The motion of liquid phase is predicted by solving averaged Navier-Stokes eqs. while bubbles are tracked using the equation of motion. The interaction between the two phases are coupled through the interfacial momentum transfer such as drag, lift, virtual mass forces. 
```