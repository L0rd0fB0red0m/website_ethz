---
layout: physics
title: Waves
topic: Maxwell equations
---


Remember the maxwell equations? We'd like to use them in order to deduce the wave equation (for some potential $$\phi$$):

$$\left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^n}{\partial t^n} \right) \phi = 0$$

(with $$c^2 = (\mu_0 \epsilon_0)^{-1}$$).

We will make use of the **Lorentz gauge-condition**, but let's first recall the full set of maxwell equations in vacuum:

> $$\nabla \cdot \mathbf{E} = 0$$
> 
> $$\nabla \cdot \mathbf{B} = 0$$
> 
> $$\nabla \times \mathbf{E} = - \dfrac{\partial \mathbf{B}}{\partial t}$$
> 
> $$\nabla \times \mathbf{B} = - \mu_0 \epsilon_0 \dfrac{\partial \mathbf{E}}{\partial t}$$

As already mentioned, we will also make use of:

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

This usually is only a matter of plugging in the expression and verifying the outcome (remember, we expect $$0$$). 

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

We need to make another consideration, namely the chain rule for the gradient:

$$\nabla \cdot (\mathbf{k} \alpha) = \mathbf{k} \cdot (\nabla \alpha) + (\nabla \cdot \mathbf{k}) \alpha$$

And we also have $$\nabla f (\mathbf{k \cdot r}) = \mathbf{k} \cdot f'(\mathbf{k \cdot r})$$. (This can be seen by applying $$\nabla$$ in cartesian coordinates and the fact that $$\mathbf{k \cdot r} = k_x x + k_y y + k_z z$$)

Let's get going then:

$$
\begin{align}
    \left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^2}{\partial t^2} \right) f_{\pm} (\mathbf{k \cdot r} \pm \omega t)
    & = \nabla \cdot \nabla f_{\pm} (\mathbf{k \cdot r} \pm \omega t) - \dfrac{1}{c^2} \dfrac{\partial^2}{\partial t^2} f_{\pm} (\mathbf{k \cdot r} \pm \omega t) \\
    & = \nabla \cdot ( \mathbf{k} f'_{\pm} (\mathbf{k \cdot r} \pm \omega t)) \mp \dfrac{\omega}{c^2} \dfrac{\partial}{\partial t} f_{\pm} (\mathbf{k \cdot r} \pm \omega t) \\
    & = \mathbf{k} \cdot \mathbf{k} f''_{\pm} (\mathbf{k \cdot r} \pm \omega t)) - \dfrac{\omega^2}{c^2} f_{\pm} (\mathbf{k \cdot r} \pm \omega t) \\
    & = \left( |\mathbf{k}|^2 - \dfrac{\omega^2}{c^2} \right) f_{\pm}
\end{align}
$$

which equals $$0$$ if $$\omega^2 = c^2 k^2$$. (not too unexpected, huh?)

For the spherical wave there isn't any angular dependence, so the laplacian reduces to

$$\Delta_r = \dfrac{1}{r} \dfrac{\partial^2}{\partial r^2}$$

and we then simply apply as above:

$$
\begin{align}
    \left( \Delta - \dfrac{1}{c^2} \dfrac{\partial^2}{\partial t^2} \right) \dfrac{1}{r} g_{\pm} (\mathbf{k \cdot r} \pm \omega t)
    & = \left( \dfrac{1}{r}\dfrac{\partial^2}{\partial r^2} - \dfrac{1}{c^2} \dfrac{\partial^2}{\partial t^2} \right) \dfrac{1}{r} g_{\pm} \\
    & = \left(k^2 - \dfrac{(\pm \omega)^2}{c^2} \right) \dfrac{1}{r} g''_{\pm}
\end{align}
$$

which reevaluates to $$0$$ when $$\omega^2 = c^2 k^2$$.

Let's now take a look at a special wave-constellation. The Gaussian wave packet is described by

$$\phi_G (z,t) = \dfrac{2}{\Delta k_0 \cdot \sqrt{\pi}} \int_{-\infty}^\infty dk \, \exp \left( - \dfrac{4 (k - k_0)^2}{(\Delta k_0)^2} \right) \cdot e^{i(kz -wt)}$$

So what exactly is this? First and foremost it is a (weighted) linear combination of plane waves. Effectively this is centered around $$k_0$$ with a width of $$\Delta k_0$$. 

We can still extract even more information and show that this is aperiodic. We'll also compute the phase velocity and the group velocity. In the end we are going to determine whether dispersion occurs here.

We first show that $$\phi_G$$ is aperiodic and that its amplitude is actually gaussianly distributed. In order to do just that we actually compute the integral. A good idea would be to substitute $$x = k - k_0$$ and to remember that $$\omega = ck$$ which is also dependent of $$k$$.

$$
\begin{align}
    \phi_G (z,t)
    & = \frac{2}{(\Delta k_0) \sqrt{\pi}} \int_{-\infty}^\infty dk \, \exp \left( - \dfrac{4 (k - k_0)^2}{(\Delta k_0)^2} \right) \cdot e^{i (k - k_0) (z - ct) + ik_0 (z-ct)} \\
    & = \frac{2}{(\Delta k_0) \sqrt{\pi}} \int_{-\infty}^\infty dx \exp \left[ - \frac{4}{(\Delta k_0)^2} x^2 \right] \cdot e^{ix (z - ct)} \cdot e^{ik_0 (z - ct)} \\
    & = \frac{2 e^{i k_0 (z - ct)}}{(\Delta k_0) \sqrt{\pi}} \int_{-\infty}^\infty dx \exp \left[ - \frac{4}{(\Delta k_0)^2} x^2 + x (z - ct) \right] \\
    & \text{we have the identity: } \int_{-\infty}^\infty dx e^{ax^2 + bx} = \sqrt{\frac{\pi}{a}} e^{b^2 / 4a} \\
    & = \frac{2 e^{i k_0 (z - ct)}}{(\Delta k_0) \sqrt{\pi}} \cdot \sqrt{\pi} \cdot \frac{\Delta k_0}{2} \exp \left[ \frac{(z-ct)^2 \cdot (\Delta k_0)^2}{4 \cdot 4}\right] \\
    & =  e^{i k_0 (z - ct)} \cdot \exp \left[ \frac{1}{4} \cdot (z-ct) \cdot \Delta k_0 \right]^2 \\
\end{align}
$$

What we obtain is a plane wave travelling at a velocity $$c$$ with a wavelength $$2\pi / k_0$$ (first term). The second term is the gaussian envelope which distributes the amplitudes of the wave (whole expression). The gaussian has a width of $$1 / \Delta k_0$$ and is centered around the point $$z - ct$$. Both travel at a speed of $$c$$ so the waves phase velocity and the envelopes group velocity coincide.

This last point allows us to say that the medium is non-dispersive, which is what we expect from the vacuum.
