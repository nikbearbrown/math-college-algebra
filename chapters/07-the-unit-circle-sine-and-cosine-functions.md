# Chapter 7 — The Unit Circle: Sine and Cosine Functions

## TL;DR

- The Wave Is the Shadow of the Circle.
- The chapter moves through Measuring Angles Two Ways, Angles That Share a Terminal Side, The Right-Triangle Definitions, The Unit Circle, and related ideas.
- Read it for the main argument, the vocabulary it introduces, and the practical judgment it asks you to develop.

*The Wave Is the Shadow of the Circle.*

Watch one car on a Ferris wheel.

It rises. It peaks at the top. It falls. It bottoms out near the ground. It rises again. If you plot its height against time, the curve is smooth and perfectly regular — it repeats the same shape over and over, without error, indefinitely. Mathematicians call this curve a *sinusoid*. The same curve describes ocean tides, the voltage in an electrical outlet, the pressure variations in a sound wave, the swing of a pendulum, the seasonal variation in daylight hours. *Anything that returns to where it started, periodically, traces a sinusoid.*

The word *trigonometry* means "triangle measurement" in Greek, and the subject began that way — computing distances using triangles. But the Ferris wheel has no triangle in it. The car just moves in a circle. What connects the circle to the triangle, and both to the wave, is the unit circle. Understanding the unit circle is understanding all three at once.

---

## Measuring Angles Two Ways

Before the unit circle, we need to agree on how to measure the angles that parameterize it.

You know degrees: $360°$ in a full circle. This system traces back to Babylonian astronomy, which divided the sky into units related to the approximate number of days in a year. It is convenient for navigation and everyday geometry. It is awkward for mathematics.

The natural unit for mathematical work is the *radian*. A radian is defined by the circle itself: it is the angle subtended at the center by an arc equal in length to the radius. On a circle of radius $r$, an arc of length $r$ corresponds to exactly 1 radian. Since the full circumference is $2\pi r$, a full revolution corresponds to $2\pi$ radians.

$$\pi \text{ radians} = 180°$$

This single equation converts everything. Multiply degrees by $\frac{\pi}{180}$ to get radians; multiply radians by $\frac{180}{\pi}$ to get degrees.

$$30° = \frac{\pi}{6} \text{ rad}, \quad 45° = \frac{\pi}{4} \text{ rad}, \quad 60° = \frac{\pi}{3} \text{ rad}, \quad 90° = \frac{\pi}{2} \text{ rad}$$

![Circle of radius r with a central angle](images/07-the-unit-circle-sine-and-cosine-functions-fig-01.png)
*Figure 7.1 — Circle of radius r with a central angle*

Why do radians matter? Because with radians, arc length is just $s = r\theta$. There is no conversion factor, no $\frac{\pi}{180}$ lurking in the formula. The formula works because the definition of the radian makes it work — the angle is measured in units of radius-lengths, so multiplying angle by radius gives length. This is not a coincidence; it is the whole point of the definition.

For a central angle $\theta$ (in radians) on a circle of radius $r$, the sector — the pie-slice region — has area

$$A = \frac{1}{2}r^2\theta$$

Again, no conversion factor. Radians are the unit that makes circular geometry clean.

---

## Angles That Share a Terminal Side

An angle is formed by two rays from a common point. Fix one ray pointing right along the positive $x$-axis; that is the *initial side*. Rotate to a *terminal side*. Counterclockwise rotation produces positive angles; clockwise produces negative. The angle is the amount of rotation.

Different amounts of rotation can produce the same terminal side. Rotating $30°$ counterclockwise and rotating $30° + 360° = 390°$ counterclockwise both end up pointing in the same direction. These angles are *coterminal* — they differ by one or more full revolutions. So are $30°$ and $-330°$.

The *reference angle* for any given angle is the acute angle between the terminal side and the nearest part of the $x$-axis. It is always between $0°$ and $90°$, always positive. Its purpose is to reduce any trigonometric calculation — in any quadrant — to a first-quadrant calculation, where all six functions are positive and familiar.

For $210°$: the terminal side lies in the third quadrant, $30°$ past the negative $x$-axis. Reference angle: $30°$.

For $315°$: the terminal side lies in the fourth quadrant, $45°$ short of a full revolution. Reference angle: $45°$.

![Coordinate plane showing all four quadrants](images/07-the-unit-circle-sine-and-cosine-functions-fig-02.png)
*Figure 7.2 — Coordinate plane showing all four quadrants*

Reference angles are a shortcut that the whole chapter depends on.

---

## The Right-Triangle Definitions

For an acute angle $\theta$ inside a right triangle, label the sides relative to $\theta$: the side opposite $\theta$, the side adjacent to $\theta$, and the hypotenuse. The six trigonometric functions are ratios of these sides:

$$\sin\theta = \frac{\text{opp}}{\text{hyp}}, \quad \cos\theta = \frac{\text{adj}}{\text{hyp}}, \quad \tan\theta = \frac{\text{opp}}{\text{adj}}$$

$$\csc\theta = \frac{\text{hyp}}{\text{opp}}, \quad \sec\theta = \frac{\text{hyp}}{\text{adj}}, \quad \cot\theta = \frac{\text{adj}}{\text{opp}}$$

The mnemonic *SOH-CAH-TOA* names the first three. The reciprocal functions are the last three, each the flip of a primary function: $\csc$ is the reciprocal of $\sin$, $\sec$ of $\cos$, $\cot$ of $\tan$.

These ratios are well-defined because all right triangles containing the same angle are *similar*: they have the same shape, different sizes. Similar triangles have proportional sides, so the ratio opposite/hypotenuse is the same regardless of how large or small the triangle is. That is the geometric content behind the trig functions — they measure a shape property of a triangle, not a size property.

Two right triangles are worth memorizing because they produce exact values.

**The 45-45-90 triangle.** Both legs equal; if each is 1, the hypotenuse is $\sqrt{2}$. So:

$$\sin 45° = \cos 45° = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}, \quad \tan 45° = 1$$

**The 30-60-90 triangle.** If the short leg (opposite $30°$) is 1, the long leg (opposite $60°$) is $\sqrt{3}$, and the hypotenuse is 2. So:

$$\sin 30° = \cos 60° = \frac{1}{2}, \quad \sin 60° = \cos 30° = \frac{\sqrt{3}}{2}$$
$$\tan 30° = \frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}, \quad \tan 60° = \sqrt{3}$$

Notice the symmetry: $\sin 30° = \cos 60°$ and $\sin 60° = \cos 30°$. This is not a coincidence. In a right triangle, the two non-right angles are complementary — they sum to $90°$. The sine of one is the cosine of the other. This is why they are called *co*-functions: cosine is the sine of the *co*mplementary angle. The same relationship holds for tangent/cotangent and secant/cosecant.

$$\sin(90° - \theta) = \cos\theta, \quad \cos(90° - \theta) = \sin\theta$$

![Two labeled right triangles side by side ](images/07-the-unit-circle-sine-and-cosine-functions-fig-03.png)
*Figure 7.3 — Two labeled right triangles side by side *

---

## The Unit Circle

The right-triangle definitions work for acute angles — angles between $0°$ and $90°$. The Ferris wheel car needs angles beyond $90°$. When the car is above and to the left of center, the angle to its position is between $90°$ and $180°$. When it is below and to the left, the angle is between $180°$ and $270°$. The right-triangle definition breaks down there — you cannot have a triangle with an obtuse angle as one of the three.

The unit circle fixes this.

Draw the circle $x^2 + y^2 = 1$ — radius 1, centered at the origin. For any angle $\theta$ measured counterclockwise from the positive $x$-axis, draw the terminal ray. Where it intersects the unit circle, label the point $(x, y)$. *Define*:

$$\cos\theta = x, \quad \sin\theta = y$$

That is the whole definition. The cosine of an angle is the $x$-coordinate of the corresponding point on the unit circle. The sine is the $y$-coordinate.

In the first quadrant, where the angle is acute, this agrees with the right-triangle definition: if you drop a perpendicular from the point $(x, y)$ to the $x$-axis, you form a right triangle with hypotenuse 1 (the radius), adjacent side $x$, and opposite side $y$. So $\cos\theta = x/1 = x$ and $\sin\theta = y/1 = y$. The unit circle extends the definition; it does not contradict it.

What does the extension buy you? Everything in the other three quadrants.

In the second quadrant ($90° < \theta < 180°$), the point $(x, y)$ has negative $x$ and positive $y$. So cosine is negative and sine is positive.

In the third quadrant ($180° < \theta < 270°$), both $x$ and $y$ are negative. Both cosine and sine are negative.

In the fourth quadrant ($270° < \theta < 360°$), $x$ is positive and $y$ is negative. Cosine positive, sine negative.

The mnemonic *All Students Take Calculus* names which functions are positive in each quadrant: All in Q I, Sine only in Q II, Tangent only in Q III, Cosine only in Q IV.

Here is the full table of standard values, which the unit circle encodes geometrically:

| $\theta$ (rad) | $\theta$ (deg) | $\cos\theta$ | $\sin\theta$ |
|---|---|---|---|
| $0$ | $0°$ | $1$ | $0$ |
| $\pi/6$ | $30°$ | $\sqrt{3}/2$ | $1/2$ |
| $\pi/4$ | $45°$ | $\sqrt{2}/2$ | $\sqrt{2}/2$ |
| $\pi/3$ | $60°$ | $1/2$ | $\sqrt{3}/2$ |
| $\pi/2$ | $90°$ | $0$ | $1$ |
| $\pi$ | $180°$ | $-1$ | $0$ |
| $3\pi/2$ | $270°$ | $0$ | $-1$ |
| $2\pi$ | $360°$ | $1$ | $0$ |

You do not memorize the table as a table. You derive each entry on demand from two things: the reference angle values from the special triangles, and the sign rule for the quadrant.

Here is the technique applied. What is $\sin(150°)$?

The terminal side of $150°$ lies in the second quadrant. The reference angle is $180° - 150° = 30°$. The magnitude is therefore $|\sin(30°)| = \frac{1}{2}$. In the second quadrant, sine is positive. So $\sin(150°) = \frac{1}{2}$.

What is $\cos(225°)$?

Third quadrant. Reference angle: $225° - 180° = 45°$. Magnitude: $\frac{\sqrt{2}}{2}$. In the third quadrant, cosine is negative. So $\cos(225°) = -\frac{\sqrt{2}}{2}$.

Four steps every time: find the quadrant, find the reference angle, look up the magnitude from the special triangles, apply the sign.

![Full unit circle diagram with all sixteen standard-angle](images/07-the-unit-circle-sine-and-cosine-functions-fig-04.png)
*Figure 7.4 — Full unit circle diagram with all sixteen standard-angle*

---

## The Identity That Comes for Free

The unit circle's equation is $x^2 + y^2 = 1$. Substitute $x = \cos\theta$ and $y = \sin\theta$:

$$\cos^2\theta + \sin^2\theta = 1$$

This is the *Pythagorean identity*. It holds for every real $\theta$ — every point on the unit circle satisfies the equation of the unit circle. The identity is not derived; it is read off directly from the definition.

It is also the most useful single equation in trigonometry. If you know $\sin\theta$, you can find $|\cos\theta|$ (the sign requires the quadrant). If you know $\cos\theta$, you can find $|\sin\theta|$. The identity connects them.

Two more identities follow from dividing through. Divide both sides by $\cos^2\theta$:

$$1 + \tan^2\theta = \sec^2\theta$$

Divide both sides by $\sin^2\theta$:

$$\cot^2\theta + 1 = \csc^2\theta$$

All three Pythagorean identities come from one equation: $x^2 + y^2 = 1$.

The unit circle also makes visible a geometric fact about sine and cosine. Rotating counterclockwise by $\theta$ gives a point $(x, y)$. Rotating clockwise by $\theta$ — that is, by angle $-\theta$ — gives the reflection across the $x$-axis: the point $(x, -y)$. So $\cos(-\theta) = x = \cos\theta$ and $\sin(-\theta) = -y = -\sin\theta$. Cosine is an *even* function (symmetric across the vertical axis); sine is an *odd* function (antisymmetric). These properties are not memorized — they are read off the symmetry of the circle.

---

## The Ferris Wheel, Revisited

Return to the car on the Ferris wheel. Suppose the wheel has radius $r$ and the car starts at the three o'clock position — that is, at the rightmost point of the wheel, at the height of the center. The car moves counterclockwise. After it has rotated through angle $\theta$:

$$x(\theta) = r\cos\theta, \quad y(\theta) = r\sin\theta$$

where $x$ is horizontal displacement from the center and $y$ is vertical displacement. As $\theta$ increases from $0$ to $2\pi$ (one full revolution), $\cos\theta$ traces from 1 down to $-1$ and back to 1; $\sin\theta$ traces from 0 up to 1, back down to $-1$, and back to 0.

Now convert to time. If the wheel completes one revolution in $T$ seconds, then $\theta = \frac{2\pi t}{T}$. The height of the car as a function of time is:

$$y(t) = r\sin\left(\frac{2\pi t}{T}\right)$$

This is a sinusoidal function of time — the wave we mentioned at the beginning. The unit circle did not just define sine and cosine; it explained *why* circular motion produces wave-shaped graphs when plotted against time. The wave is the shadow of the circle.

![Figure ](images/07-the-unit-circle-sine-and-cosine-functions-fig-05.png)
*Figure 7.5 — Figure *

The same logic applies everywhere sinusoids appear. A sound wave is the variation in air pressure as molecules oscillate back and forth — circular-ish motion in the molecular bonds projected onto a single dimension. Alternating current is the voltage produced by a generator whose coil rotates in a magnetic field — literally circular motion, with the sine function measuring the projection onto one axis. Ocean tides are driven partly by the rotation of the Earth and Moon — more circular motion. In every case, the sinusoidal shape of the graph is the direct consequence of something moving in a circle and being observed from one direction.

---

## A Worked Problem That Uses Everything

A clock's minute hand is 5 inches long. In 20 minutes, what arc does the tip trace? What area does the hand sweep? And where is the tip, as a coordinate pair, at $t$ minutes past 12?

**Angle swept.** A full revolution is 60 minutes. In 20 minutes, the hand sweeps $\frac{20}{60} = \frac{1}{3}$ of a revolution, which is $\frac{1}{3} \cdot 2\pi = \frac{2\pi}{3}$ radians.

**Arc length.** $s = r\theta = 5 \cdot \frac{2\pi}{3} = \frac{10\pi}{3} \approx 10.47$ inches.

**Sector area.** $A = \frac{1}{2}r^2\theta = \frac{1}{2}(25)\left(\frac{2\pi}{3}\right) = \frac{25\pi}{3} \approx 26.18$ square inches.

**Position at time $t$.** The minute hand starts at 12 o'clock — pointing straight up, the positive $y$-direction. It moves *clockwise* (the standard direction for clock hands), which is the negative-angle direction in standard mathematical convention.

After $t$ minutes, the hand has rotated clockwise through $\frac{2\pi t}{60} = \frac{\pi t}{30}$ radians. Working from the 12 o'clock position:

$$x(t) = 5\sin\left(\frac{\pi t}{30}\right), \quad y(t) = 5\cos\left(\frac{\pi t}{30}\right)$$

The swap of sine and cosine — sine for $x$, cosine for $y$ — comes from the clock starting at the top rather than the right. At $t = 0$: $x = 0$, $y = 5$ (straight up, correct). At $t = 15$ minutes (3 o'clock position): $x = 5\sin(\pi/2) = 5$, $y = 5\cos(\pi/2) = 0$ (pointing right, correct). The parameterization checks out.

Notice what the problem required: radians for arc length and sector area (Concept 1), the right-triangle-derived lengths for evaluating at specific angles (Concept 2), and the unit-circle coordinates for the position function (Concept 3). These are not three separate tools. They are three aspects of one construction.

![Clock face diagram with the minute hand shown](images/07-the-unit-circle-sine-and-cosine-functions-fig-06.png)
*Figure 7.6 — Clock face diagram with the minute hand shown*

---

## What the Unit Circle Actually Is

The unit circle is often presented as a memorization device — a chart of $(x, y)$ coordinates at standard angles that students are expected to reproduce on demand. That misses the point.

The unit circle is the natural domain of periodicity. Any quantity that repeats with a fixed period — any phenomenon that returns to its starting state after a fixed interval — is described by functions defined on the circle. The circle's circumference is $2\pi$ radians; after $2\pi$, you are back where you started. So the period of sine and cosine is $2\pi$:

$$\sin(\theta + 2\pi) = \sin\theta, \quad \cos(\theta + 2\pi) = \cos\theta$$

This is not a coincidence. It is the definition of the unit circle. Periodicity is built in.

This is why a single chapter on the unit circle is worth spending time on, even before we graph the wave shapes in Chapter 8. The wave shapes are the display; the unit circle is the machinery. And the machinery is simple: one circle, one radius, two coordinates. Sine is the height. Cosine is the horizontal displacement. Everything else — the identities, the special values, the reference angle technique, the connection to circular motion — is a consequence of where those two coordinates live.

The Ferris wheel car was always there. The unit circle is just how we describe its position precisely.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 7.1 — Why radians?** Ask an LLM: "Why do mathematicians prefer radians over degrees? What goes wrong if I just use degrees everywhere?" Push it past "convention" to the actual mathematical reason — the arc length formula $s = r\theta$ requires radians; the derivative of $\sin x$ equals $\cos x$ only in radians. Then ask: "If degrees are unnatural, why did humans invent them in the first place?" Probe the historical answer (360 has many divisors; Babylonian base 60).

**LLM Exercise 7.2 — Why $\sin^2\theta + \cos^2\theta = 1$.** Ask an LLM to prove the Pythagorean identity in two different ways — first using the unit circle and the Pythagorean theorem, then using the right-triangle definitions and the same theorem. They should reach the same conclusion. Then ask: "Are these really two different proofs, or two presentations of the same proof?" The answer should clarify that the unit circle definition extends the right-triangle definition to all real angles, but both rely on Pythagoras.

**LLM Exercise 7.3 — What does a negative angle mean?** Ask an LLM: "What is the difference between an angle of $-30°$ and an angle of $330°$?" The expected answer: they have the same terminal side (they're coterminal), so all trig values agree. Then ask: "Then why bother with negative angles at all?" Force it to explain that negative angles encode *direction* of rotation (clockwise vs. counterclockwise), which matters when an angle represents motion or change.

**LLM Exercise 7.4 — Coterminal angles share trig values.** Tell an LLM: "I claim that $\sin(\theta + 360°) = \sin(\theta)$ for every $\theta$. Why?" Push it to explain via the unit circle — same terminal point, same coordinates, same sine value. Then ask: "Is the same true for $\sin(\theta + 180°)$?" The answer is no — the terminal side is opposite, the $y$-coordinate flips sign, so $\sin(\theta + 180°) = -\sin(\theta)$. Probe the geometric reason.

**LLM Exercise 7.5 — When the right-triangle definition stops working.** Tell an LLM: "I'm on a Ferris wheel that rotates from the 3 o'clock position. After 270° of rotation, what is my $y$-coordinate relative to the center?" The answer involves $\sin(270°) = -1$. Then ask: "What right triangle is being used to compute this? It can't be a right triangle in the traditional sense — there's no triangle when the angle is 270°." Force the LLM to explain that the unit-circle definition is necessary precisely because right triangles only handle acute angles in the first quadrant.

---

##  AI Wayback Machine

**Run this:**

```
Who was Madhava of Sangamagrama, and how does his work on trigonometric series connect to the unit-circle sine and cosine functions we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Madhava of Sangamagrama"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Madhava's series for sin(x) and how it converges.
- Ask it about the Kerala school of astronomy and mathematics — and why its work was unknown to Europe for centuries.

What changes? What gets better? What gets worse?
