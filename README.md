# Plasma-fluid-equations
Work surrounding plasma fluid equations

The plasma fluid equations for the simplest Hermes-3 example, called blob2d, are, in the plane (here $e=1$)

```math
\dot{n} - \frac{1}{B} \left ( \frac{\partial \phi}{\partial x} \frac{\partial n}{\partial y} - \frac{\partial \phi}{\partial y} \frac{\partial n}{\partial x} \right ) = \frac{n \phi}{L};\\
\dot{\omega} - \frac{1}{B} \left ( \frac{\partial \phi}{\partial x} \frac{\partial \omega}{\partial y} - \frac{\partial \phi}{\partial y} \frac{\partial \omega}{\partial x} \right ) = \epsilon  \frac{\partial n}{\partial y} \frac{n \phi}{L};\\
\nabla^2 \phi = B^2 \omega.
```

Expanding about a circularly-symmetric initial solution $n=n_0 + \epsilon n_1$, $\omega = \epsilon \omega_1$, $\phi = epsilon \phi_1$ one has, where all quantities are the first order ones (subscript dropped) except $n_0$, and the prime is radial derivative,

```math
\dot{n} + \frac{n_0'}{Br} = \frac{n_0 \phi}{L};
\dot{\omega} = n_0' \sin \varphi + \frac{n_0 \phi}{L};
\nabla^2 \phi = B^2 \omega.
```

Now inspecting the departure from the initial condition, take all quantities to be Taylor series in time $t$

```math
n = n^{(1)} t + n^{(2)} t^2;
\omega = \omega^{(1)} t + \omega^{(2)} t^2;
\phi = \phi^{(1)} t + \phi^{(2)} t^2.
```
One sees immediately $n^{(1)} = 0$ and the initial time evolution of $n^{(2)}$ can be determined by solving

```math
\omega^{(1)} = n_0' \sin \varphi;
\nabla^2 \phi^{(1)} = B^2 n_0' \sin \varphi;
n^{(2)} = \frac{1}{2} \left ( \frac{n_0 \phi^{(1)}}{L} - \frac{n_0'}{Br} \frac{\partial \phi^{(1)}}{\partial \varphi} \right ).
```

One can work this out for plausible circularly-symmetric blob initial states (now dropping the superscripts, and assuming $\phi \propto \sin \varphi$).  The main step is evaluation of the potential from the Poisson equation

```math
\phi''+\frac{1}{r} \phi' - \frac{1}{r^2} \phi = B^2 n_0'.
```

Note that the complementary function solutions are not promising, being multplies of $\frac{1}{r}$ and $r$, so assume the particular integrals represent the actual perturbation.

1. Gaussian blob $n_0 = e^{-\frac{r^2}{2 r_0^2}}$:

This is a pain because the Poisson equation solves to

```math
\phi = \frac{r_0^2 B^2 e^{-\frac{r^2}{2 r_0^2}}}{r}
```

i.e. singular at the origin!

2. Lorentzian blob $n_0 = \frac{1}{1+\frac{r^2}{r_0^2}}$



3. Poeschl-Teller blob $n_0 = \mathrm{sech}^2 \left ( \frac{r}{r_0} \right )$






