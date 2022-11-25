# Plasma-fluid-equations
Work surrounding plasma fluid equations

The plasma fluid equations for the simplest Hermes-3 example, called blob2d, are (here $e=1$)

```math
\dot{n} - \frac{1}{B} \left ( \frac{\partial \phi}{\partial x} \frac{\partial n}{\partial y} - \frac{\partial \phi}{\partial y} \frac{\partial n}{\partial x} \right ) &=& \frac{n \phi}{L};\\
\dot{\omega} - \frac{1}{B} \left ( \frac{\partial \phi}{\partial x} \frac{\partial \omega}{\partial y} - \frac{\partial \phi}{\partial y} \frac{\partial \omega}{\partial x} \right ) &=& \epsilon  \frac{\partial n}{\partial y} \frac{n \phi}{L};\\
\nabla^2 \phi &=& B^2 \omega.
```
