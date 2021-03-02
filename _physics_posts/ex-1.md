---
layout: physics
title: Waves
topic: Maxwell equations
---


Remember the maxwell equations? We'd like to use them in order to deduce the wave equation (for some potential $\phi$):

$$\left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^n}{\partial t^n} \right) \phi = 0$$

(with $$c^2 = (\mu_0 \epsilon_0)^{-1}$$).

A big help will be the **Lorentz gauge-condition**, but let's first recall the full set of maxwell equations in vacuum:

$$\nabla \cdot \mathbf{E} = 0$$

$$\nabla \cdot \mathbf{B} = 0$$

$$\nabla \times \mathbf{E} = - \dfrac{\partial \mathbf{B}}{\partial t}$$

$$\nabla \times \mathbf{B} = - \mu_0 \epsilon_9 \dfrac{\partial \mathbf{E}}{\partial t}$$

As already mentionned, we will also make use of:

$$\nabla \cdot \mathbf{A} + \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t} = 0$$

We will first write $$\mathbf{E}$$ in terms of potential, ie:

$$\mathbf{E} = - \dfrac{\partial \mathbf{A}}{\partial t} - \nabla \cdot \phi$$

We now plug this into the first maxwell-equation to obtain:

$$0 = \nabla \cdot \mathbf{E} = -\dfrac{\partial}{\partial t} \nabla \cdot \mathbf{A} - \Delta \phi$$

We now have by the gauge-condition:

$$\nabla \cdot \mathbf{A} = - \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t}$$

which we now plugin into our previous expression to obtain:

$$-\dfrac{\partial}{\partial t} - \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t} - \Delta \phi = \dfrac{\partial}{\partial t} \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t} - \Delta \phi = \left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^n}{\partial t^n} \right) \phi = 0$$