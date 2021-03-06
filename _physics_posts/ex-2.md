---
layout: physics
title: Astronomical Interferometry
topic: Fraunhoffer diffraction, lenses
---

Consider a distant star, at a distance of $$550$$ lightyears, whose $$790$$ nm light we observe. It has a diameter of around $$10^9$$ km.

If we want to observe it, there are a few things to note already:

*   The angular width of the star, here on earth turns out to be given by:

    $$\sin (\vartheta_{res}) = \frac{d_{star}}{dist} \Leftrightarrow \vartheta_{res} = \sin^{-1} \frac{d_{star}}{dist} = \frac{10^9 \text{km}}{3 \cdot 10^5 \text{km}/s \cdot 365 * 24 * 3600} = 16.3 \text{arcsec}$$

*   The imaging resolution of our eye, given by the Rayleigh criterion is

    $$\sin(\vartheta_{min,eye}) = \frac{\lambda}{D} \Leftrightarrow \vartheta_{min,eye} = 0.04 \text{arcsec}$$

    if we consider the lens of our eye to have a diameter of $$D = 10$$ mm. Even though this is an approximiation this is far too small to resolve the star.

*   Similarly we can compute the resolution of a telescope with a lens of diameter $$D = 1$$ m:

    $$\sin(\vartheta_{min,telescope}) = \frac{\lambda}{D} \Leftrightarrow \vartheta_{min,telescope} = 0.16 \text{arcsec}$$

    which still is too small.

We will therefore take a look at another method, interferometry. If we set up two telescopes of diameter $$d = 10$$ cm, distanced by $$B = 50$$ m. If we think of them as a special aperture we can compute how their combined input will behave. We can model this special aperture by the one-dimensional function

$$a(x) = \left\{ \begin{array}{c c c}
    1 & \text{ if } & -B/2 - d/2 \leq x \leq -B/2 + d/2 \\
    & \text{ or } & B/2 - d/2 \leq x \leq B/2 + d/2 \\
    0 & \text{ else } & 
\end{array}\right.$$

The resulting signal can be expressed through the fourier transform of this aperture. Namely through

$$\begin{align}
    U(P) & = \int a(x) e^{-ikXx} dx \\
    & = \int_{-B/2 -d/2}^{-B/2 + d/2} e^{-ikXx} dx + \int_{B/2 -d/2}^{B/2 + d/2} e^{-ikXx} dx \\
    & \vdots \\
    & \propto \text{sinc}(kXd/2) \cdot \frac{\sin(kXB)}{\sin(kXB/2)}
\end{align}$$

where $$P$$ depends on $$X$$ and the distance to the screen where we measure the incoming light. More on that later.

We can now apply the Rayleigh criterion for Fraunhoffer diffraction: Two objects are resolved if their extrema overlay. (The one's maximum overlays the other's minimum).

First a little simplification is due: if we use that $$d << B$$ we can rewrite the above expression as
$$\begin{align}
    U(P) & \propto \text{sinc}(kXd/2) \cdot \frac{\sin(2 \cdot kXB/2)}{\sin(kXB/2)} \\
    & = \text{sinc}(kXd/2) \cdot \frac{2 \cdot \sin(kXB/2) \cdot \cos(kXB/2)}{\sin(kXB/2)} \\
    \Rightarrow I(P) & \propto U(P)^2 \\
    & \propto \text{sinc}^2(kXd/2) \cdot \cos^2(kXB/2) \\
    & \text{expand into powers of } d/B << 1 \text{ (this follows from the series representation of the sine)} \\
    & = \text{sinc}^2(kXB/2 \cdot d/B) \cdot \cos^2(kXB/2) \\
    & \approx \left(1 - \frac{(kXB/2)^2}{6} \cdot \frac{d}{B}^2 + O((d/B)^4) \right) \cdot \cos^2(kXB/2) \\
    & \approx \cos^2(kXB/2)
\end{align}$$

Our star now lies on $$X_1 = \frac{0}{dist}$$ and $$X_2 = \frac{d_{star}}{dist}$$, as we take the resulting interference pattern at the receptor directly. So $$X_1$$ has its maximum at the center and $$X_2$$ is the displacement of the second signal. To satisfy Rayleigh the displaced minimum should lie on the maximum, which we have if $$k X_2 B/2 = \pm \pi/2$$. This gives us that

$$X_2 = \frac{\pi}{kB} = \frac{\lambda}{2B}$$

If we recall that $$X_2 = \frac{d_{star}}{dist} = \sin(\vartheta_{min, interferometer})$$ so for the wavelength of our star we have

$$\vartheta_{min, interferometer} = \sin^{-1} \left(\frac{\lambda}{2B}\right) = 0.163 \text{arcsec}$$

which finally allows us to resolve the star.

As a comparison, to achieve this resolution with a conventional lens, we would need a diameter of 

$$d_{lens} = \frac{\lambda}{\sin(\vartheta_{min, interferometer})} = 39.3 \text{m}$$
