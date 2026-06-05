# Chapter 10 — Further Applications of Trigonometry

## TL;DR

- How Angles Measured from a Hundred Miles Away Revealed the Height of the World.
- The chapter moves through Oblique Triangles, The Law of Sines, The Law of Cosines, Polar Coordinates, and related ideas.
- Read it for the main argument, the vocabulary it introduces, and the practical judgment it asks you to develop.

*How Angles Measured from a Hundred Miles Away Revealed the Height of the World.*

In 1852, a mathematician in Calcutta named Radhanath Sikdar noticed something unusual in the survey data streaming in from the Himalayan foothills. For years, the Great Trigonometric Survey of India had been triangulating its way northward — measuring angles, computing distances, tying station to station across the subcontinent with extraordinary care. One peak, designated Peak XV, kept coming out taller than every other measurement in the record. Sikdar walked into the office of Superintendent Andrew Waugh and is said to have reported: "Sir, I have discovered the highest mountain in the world."

The height they computed — $29{,}002$ feet — was derived entirely from angles measured at stations more than a hundred miles from the mountain, stations so distant that the peak was not even visible from ground level; they worked from elevated platforms. No surveyor set foot on the mountain. No rope was dropped from the summit. The height of Everest was computed from trigonometry: angles observed through theodolites, distances measured along baselines, and the laws that govern how angles and sides relate inside oblique triangles.

This chapter is about the tools those surveyors used — and the surprising reach of the same tools into coordinates, complex numbers, curves in time, and the direction of forces.

---

## Oblique Triangles

In a right triangle, one angle is $90°$ and the structure is simple: one formula (SOH-CAH-TOA) relates the sides and angles, and the Pythagorean theorem connects the three sides directly. The Himalayas contain no convenient right triangles. The triangle formed by two survey stations and the summit of Everest has three angles that are all, in general, something other than $90°$. Such a triangle is *oblique*, and it requires two laws the right-triangle setting doesn't need.

### The Law of Sines

Label the triangle's vertices $A$, $B$, $C$ and their opposite sides $a$, $b$, $c$. The Law of Sines states that the ratio of any side to the sine of its opposite angle is the same for all three:

$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C}$$

Why should this be true? Drop a perpendicular from $C$ to side $c$, creating a height $h$. In the left sub-triangle, $h = b\sin A$. In the right sub-triangle, $h = a\sin B$. Setting these equal: $b\sin A = a\sin B$, which rearranges to $\frac{a}{\sin A} = \frac{b}{\sin B}$. The same construction with a perpendicular from $A$ gives the third ratio. The law follows from the definition of sine, applied twice inside the same triangle.

![Oblique triangle ABC with a perpendicular h dropped](images/10-further-applications-of-trigonometry-fig-01.png)
*Figure 10.1 — Oblique triangle ABC with a perpendicular h dropped*

The Law of Sines is the tool to reach for when you know two angles and one side — because two angles immediately give you the third ($A + B + C = 180°$), and then you have a complete ratio to work with. It also applies when you know two sides and a non-included angle, though that case — called the *ambiguous case* — can produce zero, one, or two valid triangles. The ambiguity arises because $\sin\theta = \sin(180° - \theta)$: two different angles have the same sine, so the calculation may have two legitimate solutions.

Here is the Law of Sines working. In triangle $ABC$: $A = 50°$, $B = 60°$, $a = 10$. Find $b$.

$$\frac{b}{\sin 60°} = \frac{10}{\sin 50°}$$

$$b = \frac{10 \sin 60°}{\sin 50°} \approx \frac{10 \cdot 0.866}{0.766} \approx 11.30$$

Two angles, one side, one unknown side. The whole calculation is one ratio set equal to another.

### The Law of Cosines

The Law of Sines requires knowing an angle opposite a known side. When you know three sides and want an angle, or two sides and the angle *between* them, the Law of Sines has nothing to grip. The Law of Cosines fills that gap.

For a triangle with sides $a$, $b$, $c$ and angle $C$ opposite side $c$:

$$c^2 = a^2 + b^2 - 2ab\cos C$$

When $C = 90°$, $\cos C = 0$ and this reduces to $c^2 = a^2 + b^2$ — the Pythagorean theorem. The Law of Cosines is a generalization of Pythagoras: the correction term $-2ab\cos C$ accounts for the fact that the angle is not $90°$. If $C < 90°$, the cosine is positive and the correction is negative — $c$ is shorter than Pythagoras would predict. If $C > 90°$, the cosine is negative and the correction becomes positive — $c$ is longer.

The law can also be rearranged to find an angle from three sides:

$$\cos C = \frac{a^2 + b^2 - c^2}{2ab}$$

Given all three sides, substitute and solve for $\cos C$, then take the inverse cosine.

Together, the Law of Sines and the Law of Cosines cover every triangle that can be solved:

- Two angles and any side → Law of Sines.
- Two sides and the included angle → Law of Cosines.
- Three sides → Law of Cosines (for an angle), then Law of Sines for the rest.
- Two sides and a non-included angle → Law of Sines, with ambiguity.

| What You Know | What You Want | Which Law | Caveat |
| --- | --- | --- | --- |
| AAS | ASA) two angles + one side → Law of Sines → none | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| SAS) two sides + included angle → Law of Cosines → none | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| SSS) three sides → Law of Cosines for first angle then Law of Sines → none | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| SSA) two sides + non-included angle → Law of Sines → ambiguous case (0, 1, or 2 solutions | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| student should be able to look at what they are given and immediately identify the correct tool without trial and error | The pattern becomes easy to misuse or overlook. | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |

When all three sides are known but no angles, there is also Heron's formula for area directly:

$$\text{Area} = \sqrt{s(s-a)(s-b)(s-c)}, \quad s = \frac{a+b+c}{2}$$

where $s$ is the *semiperimeter*. No angles required at all.

---

## Polar Coordinates

Rectangular coordinates describe a point in the plane by its horizontal and vertical distances from the origin: $(x, y)$. This is the natural system when motion is along horizontal and vertical axes — walking city blocks, say.

But for a boat on the ocean, or a radar dish sweeping the sky, or a planet orbiting the sun, the natural description is different: how far from a center, and in what direction. This is the polar coordinate system: $(r, \theta)$, where $r$ is the distance from the origin and $\theta$ is the angle from the positive $x$-axis.

The conversion between the two is just the unit-circle definition of sine and cosine, applied at radius $r$:

$$x = r\cos\theta, \quad y = r\sin\theta$$
$$r = \sqrt{x^2 + y^2}, \quad \tan\theta = \frac{y}{x}$$

The second pair inverts the first. To find $\theta$ from $x$ and $y$, use $\tan^{-1}(y/x)$ but check the quadrant — the arctangent function only returns values in $(-90°, 90°)$, and the actual angle might be in the second or third quadrant.

Why does polar form matter? Because some curves that are complicated in rectangular coordinates are simple in polar. The circle $x^2 + y^2 = a^2$ has a complicated implicit equation in $x$ and $y$; in polar it is simply $r = a$ — the set of all points at distance $a$ from the origin. The cardioid — a heart-shaped curve that appears in optics and antenna design — has the polar equation $r = a(1 + \cos\theta)$ and a rectangular equation that fills several lines. The Archimedean spiral, where successive loops are evenly spaced, is $r = a\theta$ in polar and has no clean rectangular form at all.

The choice of coordinate system is a design decision. Use the system that makes your curve or your calculation simple.

![Four polar curves plotted side by side ](images/10-further-applications-of-trigonometry-fig-02.png)
*Figure 10.2 — Four polar curves plotted side by side *

---

## Complex Numbers as Rotations

A complex number $z = x + yi$ corresponds to the point $(x, y)$ in the plane. In rectangular form, addition is easy: you add real parts and imaginary parts separately, just like vector addition. But multiplication is not obvious — it mixes real and imaginary parts in a way that looks complicated:

$$(x_1 + y_1 i)(x_2 + y_2 i) = (x_1 x_2 - y_1 y_2) + (x_1 y_2 + y_1 x_2)i$$

In polar form, multiplication becomes transparent.

Write $z = r(\cos\theta + i\sin\theta)$, where $r = \sqrt{x^2 + y^2}$ is the *modulus* and $\theta$ is the *argument* — exactly the polar coordinates of the point $(x, y)$. Now multiply two complex numbers in this form:

$$r_1(\cos\theta_1 + i\sin\theta_1) \cdot r_2(\cos\theta_2 + i\sin\theta_2) = r_1 r_2 [\cos(\theta_1 + \theta_2) + i\sin(\theta_1 + \theta_2)]$$

The identity $\cos(\theta_1 + \theta_2) + i\sin(\theta_1 + \theta_2)$ follows from the angle addition formulas for cosine and sine. But the result is remarkable: to multiply two complex numbers, *multiply their moduli and add their arguments*. Multiplication in the complex plane is simultaneously a scaling (by $r_1 r_2$) and a rotation (by $\theta_1 + \theta_2$). Every complex multiplication is a rotation and a rescaling. The complicated formula in rectangular form was hiding something simple.

From this, De Moivre's theorem follows immediately by repeated multiplication:

$$(r(\cos\theta + i\sin\theta))^n = r^n(\cos n\theta + i\sin n\theta)$$

Raise to the $n$th power: raise the modulus to $n$, multiply the argument by $n$.

Here it is working. What is $(1 + i)^4$?

Convert to polar: $|1 + i| = \sqrt{1^2 + 1^2} = \sqrt{2}$, and the argument is $\theta = 45° = \pi/4$ (the point $(1,1)$ is at $45°$). So $1 + i = \sqrt{2}(\cos 45° + i\sin 45°)$.

Apply De Moivre: $(1+i)^4 = (\sqrt{2})^4(\cos(4 \cdot 45°) + i\sin(4 \cdot 45°)) = 4(\cos 180° + i\sin 180°) = 4(-1 + 0 \cdot i) = -4$.

Verify directly: $(1+i)^2 = 1 + 2i + i^2 = 2i$. Then $(2i)^2 = 4i^2 = -4$. The two paths agree.

The power of polar form is that it makes repeated multiplication geometrical. Raising to the $n$th power is spinning around the origin $n$ times while scaling the distance from the origin. Nothing mysterious.

![Complex plane showing the successive powers of (1+i)](images/10-further-applications-of-trigonometry-fig-03.png)
*Figure 10.3 — Complex plane showing the successive powers of (1+i)*

---

## Parametric Equations: Curves with Memory

A line in the plane is a set of points. A trajectory in the plane is a *path* — points traced in a specific order at specific times. The equation $y = 2x + 1$ describes the same line whether you walk it left to right, right to left, or jump around. It carries no information about when you were where.

Parametric equations restore that information. Instead of one equation relating $x$ and $y$, you write two equations relating $x$ and $y$ each to a parameter $t$ — typically time:

$$x = f(t), \quad y = g(t)$$

As $t$ varies, the point $(x(t), y(t))$ traces a path with direction and timing.

The classic example is projectile motion. A ball thrown at speed $v_0$ at angle $\alpha$ above horizontal travels as:

$$x(t) = v_0 t \cos\alpha, \quad y(t) = v_0 t \sin\alpha - \tfrac{1}{2}gt^2$$

The parameter $t$ is time in seconds. The path is a parabola — you can verify this by solving $t = x/(v_0\cos\alpha)$ from the first equation and substituting into the second:

$$y = x\tan\alpha - \frac{g}{2v_0^2\cos^2\alpha}x^2$$

This is indeed a parabola in $x$ and $y$. But the parametric form is more informative: it tells you not just where the ball goes, but when it gets there, how fast it's moving at each point, and where it is at any specific moment. Eliminating the parameter collapses the time information; the parametric form preserves it.

Other parameterizations: a circle of radius $r$ can be written $x = r\cos t$, $y = r\sin t$. Eliminating $t$: $x^2 + y^2 = r^2\cos^2 t + r^2\sin^2 t = r^2$. The Pythagorean identity does the work. An ellipse is $x = a\cos t$, $y = b\sin t$ — eliminating $t$ gives $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$.

The key insight: a curve is a geometric object (a set of points); a parametric curve is a dynamic object (a path with timing). The same geometry can have infinitely many parameterizations, each describing a different way of traversing it.

---

## Vectors: Magnitude and Direction Together

Temperature is a number. It tells you how hot. Velocity is not a number — it tells you how fast *and in what direction*. Force is not a number either. Quantities that have both magnitude and direction are *vectors*, and combining them requires different arithmetic than combining numbers.

A vector in the plane is written as a pair of components $\langle a, b \rangle$ — the horizontal and vertical displacements from tail to tip. The magnitude (length) of the vector is

$$|\vec{v}| = \sqrt{a^2 + b^2}$$

the Pythagorean theorem applied to the components.

Addition of vectors is component-wise:

$$\langle a_1, b_1 \rangle + \langle a_2, b_2 \rangle = \langle a_1 + a_2, b_1 + b_2 \rangle$$

Geometrically, vector addition is the *tip-to-tail* rule: place the tail of the second vector at the tip of the first; the sum goes from the original tail to the final tip. This is how forces combine, how velocities compound, how displacements accumulate.

A vector with magnitude $r$ and direction $\theta$ has components $\langle r\cos\theta, r\sin\theta \rangle$ — again, the unit circle at work. This conversion between magnitude-and-direction and component form is the bridge between the geometric and algebraic descriptions of vectors.

Here is the canonical application. A plane has an airspeed of $500$ mph on a heading of $60°$ from the positive $x$-axis (roughly northeast). The wind is blowing from the west at $50$ mph, meaning it pushes in the positive $x$-direction.

Plane's vector (relative to air): $\vec{p} = \langle 500\cos 60°, 500\sin 60°\rangle = \langle 250, 433\rangle$.

Wind vector (ground to air): $\vec{w} = \langle 50, 0\rangle$.

The plane's ground velocity is the vector sum:

$$\vec{r} = \vec{p} + \vec{w} = \langle 300, 433\rangle$$

Magnitude: $|\vec{r}| = \sqrt{300^2 + 433^2} = \sqrt{90{,}000 + 187{,}489} \approx 526$ mph.

Direction: $\theta = \tan^{-1}(433/300) \approx 55.3°$ — slightly farther east than the original $60°$ heading.

The wind adds $50$ mph of eastward push. The plane ends up moving faster than its airspeed but in a slightly shifted direction. Both the speed and direction of the ground track are different from what the pilot set — a practical reality that every navigator accounts for.

![Vector diagram showing the plane-wind problem ](images/10-further-applications-of-trigonometry-fig-04.png)
*Figure 10.4 — Vector diagram showing the plane-wind problem *

---

## A Worked Problem: The Fire Lookout

Two ranger stations are 12 miles apart along an east-west line. Call them $A$ (west) and $B$ (east). A fire is spotted to the north. From $A$, the bearing to the fire is N 35° E — that is, $35°$ east of due north. From $B$, the bearing is N 60° W — $60°$ west of due north. How far is the fire from each station?

**Translate bearings to angles.** Bearings are measured clockwise from north. To convert to standard mathematical angles (counterclockwise from positive $x$-axis): the line from $A$ to the fire, at bearing N 35° E, makes an angle of $90° - 35° = 55°$ with the east direction. The line from $B$ to the fire, at bearing N 60° W, makes an angle of $90° + 60° = 150°$ with east.

**Find the triangle's angles.** The baseline $AB$ points east. At vertex $A$, the sight line to the fire rises at $55°$ from the baseline. At vertex $B$, the sight line points at $150°$ from east — which is $180° - 150° = 30°$ from the baseline (since the baseline from $B$ toward $A$ points west, at $180°$). The angle at the fire is $180° - 55° - 30° = 95°$.

**Apply the Law of Sines.** The side opposite the $95°$ angle is the baseline $AB = 12$ miles.

$$\frac{12}{\sin 95°} = \frac{AF}{\sin 30°} = \frac{BF}{\sin 55°}$$

$$AF = \frac{12\sin 30°}{\sin 95°} \approx \frac{6}{0.9962} \approx 6.02 \text{ miles}$$

$$BF = \frac{12\sin 55°}{\sin 95°} \approx \frac{9.83}{0.9962} \approx 9.87 \text{ miles}$$

The fire is about 6 miles from station A and about 9.9 miles from station B.

This problem used nothing that the surveyors of Everest did not also use. The geometry is the same: known baseline, observed angles, unknown distances, one application of the Law of Sines. The only difference is scale.

![Diagram of the fire lookout problem ](images/10-further-applications-of-trigonometry-fig-05.png)
*Figure 10.5 — Diagram of the fire lookout problem *

---

## The Unity Beneath Five Topics

This chapter listed five separate subjects — oblique triangles, polar coordinates, complex numbers, parametric equations, vectors — and it would be easy to finish it feeling you have learned five unrelated tricks. But look at what connects them.

All five are about dealing with quantities that have *both magnitude and direction*. The oblique triangle is solved by relating magnitudes (sides) to directions (angles). Polar coordinates describe a point by its distance and angle from a reference. Complex numbers in polar form encode a number as a magnitude and a rotation. Parametric equations describe a path by tracking position in two directions simultaneously over time. Vectors are the direct representation of magnitude-and-direction as an algebraic object.

Rectangular coordinates are natural when the world is organized along perpendicular axes — when north and east are the relevant directions. Angles, distances, rotations, and paths are all more naturally expressed in ways that carry both pieces of information at once. Every topic in this chapter is a different mathematical formalism for doing that.

The surveyors mapping the Himalayas had no GPS, no satellite imagery, no way to go and measure directly. What they had was angles, careful measurement, and the laws that govern how angles and distances are related in triangles. They computed the height of the world's highest mountain from measurements taken more than a hundred miles away. That is what trigonometry can do when its tools are used with care.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 10.1 — Law of sines vs. law of cosines.** Tell an LLM: "I have a triangle. When should I use the Law of Sines and when should I use the Law of Cosines?" Force a precise answer that maps to the four standard cases (SSS, SAS, ASA, SSA). Then ask: "What is the *ambiguous case* and why does it arise specifically with SSA?" The LLM should explain that two angles can produce the same opposite side length, so two valid triangles can match the given data — or one, or none. Probe with a specific SSA example and have the LLM enumerate the possibilities.

**LLM Exercise 10.2 — Why $r$ can be negative.** Ask an LLM: "In polar coordinates, the radius $r$ is sometimes allowed to be negative. What does that even mean geometrically?" Push for the explanation: $(r, \theta)$ with negative $r$ refers to the point you'd reach by going $|r|$ in the *opposite* direction from $\theta$. Then ask: "Couldn't I always rewrite $(-r, \theta)$ as $(r, \theta + \pi)$ instead, and avoid negative radii entirely?" Yes — but then ask why mathematicians keep the negative-$r$ convention anyway. The answer involves convenience for plotting and for certain polar-equation simplifications.

**LLM Exercise 10.3 — Multiplication by $i$ as rotation.** Ask an LLM: "Why does multiplying a complex number by $i$ rotate it 90° counterclockwise?" Force the geometric derivation: $i = 0 + 1i$ has magnitude 1 and angle $\pi/2$, so multiplication by $i$ rotates by $\pi/2$ and scales by 1. Then ask: "Why does multiplying by $i$ twice equal multiplication by $-1$?" The answer: two 90° rotations equal a 180° rotation. The lesson: complex multiplication is rotation-and-scaling, geometrically.

**LLM Exercise 10.4 — Parametric equations have memory.** Tell an LLM: "Why can a parametric curve $x = f(t), y = g(t)$ trace the same set of points twice, while $y = f(x)$ cannot?" Push for the explanation that parametric equations encode *time* — the path matters, not just the set of points. Then ask: "Give me a parametric equation that traces a circle clockwise, and one that traces the same circle counterclockwise." The LLM should produce both. Verify that the underlying point set is identical.

**LLM Exercise 10.5 — What does the dot product compute?** Ask an LLM: "If $\vec{u} \cdot \vec{v} = 0$, what does that say geometrically?" The expected answer: the vectors are perpendicular. Then ask: "If $\vec{u} \cdot \vec{v} > 0$, what does *that* say?" Push it past "they point in similar directions" to a precise answer: the angle between them is less than 90°. Then ask: "Why does the dot product equal $|\vec{u}||\vec{v}|\cos\theta$ — what is $\cos\theta$ doing in this formula?" Force the geometric argument: $\cos\theta$ measures how much $\vec{v}$ projects onto $\vec{u}$.

---

##  AI Wayback Machine

**Run this:**

```
Who was Bhāskara II, and how does his work connect to the further applications of trigonometry we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Bhāskara II"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to solve one specific problem from the *Līlāvatī* using modern notation.
- Ask it about the legend of the *Līlāvatī* being written for Bhāskara's daughter — and whether it's likely true.

What changes? What gets better? What gets worse?
