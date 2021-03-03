---
layout: physics
title: Waves
topic: Maxwell equations
---


Remember the maxwell equations? We'd like to use them in order to deduce the wave equation (for some potential $\phi$):

$$\left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^n}{\partial t^n} \right) \phi = 0$$

(with $$c^2 = (\mu_0 \epsilon_0)^{-1}$$).

A big help will be the **Lorentz gauge-condition**, but let's first recall the full set of maxwell equations in vacuum:

> $$\nabla \cdot \mathbf{E} = 0$$
> 
> $$\nabla \cdot \mathbf{B} = 0$$
> 
> $$\nabla \times \mathbf{E} = - \dfrac{\partial \mathbf{B}}{\partial t}$$
> 
> $$\nabla \times \mathbf{B} = - \mu_0 \epsilon_0 \dfrac{\partial \mathbf{E}}> {\partial t}$$

As already mentionned, we will also make use of:

$$\nabla \cdot \mathbf{A} + \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t} = 0$$

We will first write $$\mathbf{E}$$ in terms of potential, ie:

$$\mathbf{E} = - \dfrac{\partial \mathbf{A}}{\partial t} - \nabla \cdot \phi$$

We now plug this into the first maxwell-equation to obtain:

$$0 = \nabla \cdot \mathbf{E} = -\dfrac{\partial}{\partial t} \nabla \cdot \mathbf{A} - \Delta \phi$$

We now have by the gauge-condition:

$$\nabla \cdot \mathbf{A} = - \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t}$$

which we now plugin into our previous expression to obtain:

$$
\begin{align}
    -\dfrac{\partial}{\partial t} - \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t} - \Delta \phi & = \dfrac{\partial}{\partial t} \dfrac{1}{c^2}\dfrac{\partial \phi}{\partial t} - \Delta \phi \\
    & = \left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^n}{\partial t^n} \right) \phi = 0
\end{align}
$$

which is just what we wanted. It's just a reminder to see that those wave equations don't come out of nowhere.

We can now consider two well-known types of vawes and show that they do actually fulfill the wave equation. Namely we'll see this for

$$\phi_p (\mathbf{r}, t) = f_{+} (\mathbf{k \cdot r} + \omega t) + f_{-} (\mathbf{k \cdot r} - \omega t)$$

(a planar wave) and

$$\phi_s (\mathbf{r}, t) = \dfrac{1}{r} \cdot \left[ g_{+} (\mathbf{k \cdot r} + \omega t) + g_{-} (\mathbf{k \cdot r} - \omega t) \right] $$

(a spherical wave).

This usually is only a matter of plugging in the expression and verifying the outcome (remember, we expect $0$). 

So let's do just that, and start by recalling the laplacian in cartesian and spherical coordinates:

> In cartesian coordinates we have: 
>
> $$\Delta = \dfrac{\partial^2}{\partial x^2} + \dfrac{\partial^2}{\partial y^2} + \dfrac{\partial^2}{\partial z^2}$$
>
> In spherical coordinates, things heat up a bit:
> 
> $$\Delta = \frac{1}{r^2} \frac{\partial}{\partial r} \cdot \left(r^2 \frac{\partial}{\partial r} \right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{\partial}{\partial \theta} \right) + \frac{1}{r^2 \sin^2 \theta} \frac{\partial^2}{\partial \varphi^2}$$
>
> These are operators and we **apply them to functions**, in this case our expressions of $$\phi$$.

Let's get going then:

$$
\begin{align}
    \left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^n}{\partial t^n} \right) \phi_p
    & = 
\end{align}
$$