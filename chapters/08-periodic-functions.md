# Chapter 8 — Periodic Functions

*Why the same four numbers describe everything that repeats.*

---

## The thing about tides

Stand at Boston Harbor and watch the water for a day. It rises slowly to a peak — high tide — then falls over several hours to a trough — low tide — then rises again. Two complete cycles in roughly 25 hours. The height of the water at any given moment is a function of time, and that function has a property that almost nothing in Chapter 5 had: it *repeats*. Exactly. The same shape, over and over, indefinitely.

Plot it. What you get is not a parabola or a rational curve with asymptotes. It's a smooth, undulating wave — climbing, peaking, descending, bottoming, climbing again. The technical name for a function that repeats like this is *periodic*. And the remarkable fact, which took mathematicians a long time to fully appreciate, is that virtually every periodic phenomenon in nature is described by the same two functions: sine and cosine.

Not approximately. Exactly, or as close to exactly as you need. The alternating current in the wire powering your desk lamp. The vibration of a guitar string. The seasonal variation in daylight hours. The pressure wave that is sound. The electromagnetic field that is light. All of them are sines and cosines, or sums of sines and cosines. This is not a coincidence — it's a theorem, and it's one of the deepest facts in all of mathematics. This chapter develops the tools you need to work with these functions: how to read their graphs, how to adjust their parameters to fit data, and how to invert them when you need to go backward from a value to an angle.

---

## Part 1 — Sine and cosine: the basic wave

From Chapter 7, $\sin x$ and $\cos x$ are defined for any real number $x$ using the unit circle. The value of $\sin x$ is the $y$-coordinate of the point on the unit circle reached by traveling $x$ radians counterclockwise from $(1, 0)$. The value of $\cos x$ is the $x$-coordinate of that same point.

Because the unit circle has circumference $2\pi$, traveling $2\pi$ radians brings you back exactly where you started. So $\sin(x + 2\pi) = \sin x$ and $\cos(x + 2\pi) = \cos x$ for every $x$. The functions are periodic with period $2\pi$.

Graph $y = \sin x$ from $0$ to $2\pi$. The curve starts at $(0, 0)$, rises to a maximum of $1$ at $x = \pi/2$, returns to zero at $x = \pi$, falls to a minimum of $-1$ at $x = 3\pi/2$, and completes the cycle back at zero at $x = 2\pi$. The graph of $y = \cos x$ has the same shape, starting instead at its maximum: the point $(0, 1)$, falling to zero at $x = \pi/2$, reaching $-1$ at $x = \pi$, returning to zero at $x = 3\pi/2$, and completing the cycle at $(2\pi, 1)$.

Cosine is sine shifted left by $\pi/2$. They're the same wave, out of phase.

<!-- → [IMAGE: $y = \sin x$ and $y = \cos x$ plotted together on the same axes from $-\pi$ to $3\pi$, with key points labeled — $(0,0)$, $(\pi/2, 1)$, $(\pi, 0)$, $(3\pi/2, -1)$, $(2\pi, 0)$ for sine; $(0,1)$, $(\pi/2, 0)$, $(\pi, -1)$ for cosine; the $\pi/2$ horizontal offset between the two curves marked with a bracket; student should see "same shape, different starting point" before the parameter section introduces how to shift deliberately] -->

### The four parameters

Every real-world periodic phenomenon — tides, temperature cycles, sound waves, alternating current — can be modeled by adjusting four parameters of the basic sine or cosine curve. The general sinusoidal function is:

$$y = a\sin(bx - c) + d$$

and the same form for cosine. Each parameter does something geometrically specific.

**Amplitude $|a|$** stretches or compresses the wave vertically. The basic sine oscillates between $-1$ and $1$. Multiply by $a$ and it oscillates between $-|a|$ and $|a|$. If $a < 0$, the wave is also flipped upside down — it starts by going down instead of up.

**Period $\frac{2\pi}{|b|}$** stretches or compresses the wave horizontally. The basic sine completes one cycle in $2\pi$ radians. If $b = 2$, the period is $\pi$ — the wave completes the cycle in half the horizontal distance, so it's compressed. If $b = 1/2$, the period is $4\pi$ — the wave stretches out to twice its normal width. Larger $b$ means faster oscillation; smaller $b$ means slower.

**Phase shift $\frac{c}{b}$** slides the wave left or right. If $c > 0$, the shift is to the right; if $c < 0$, to the left. The phase shift tells you where the wave starts its cycle relative to the origin.

**Vertical shift $d$** moves the entire wave up or down. The midline of the oscillation — the horizontal center line — is at $y = d$, not at $y = 0$. The wave oscillates between $d - |a|$ and $d + |a|$.

<!-- → [INFOGRAPHIC: four-panel diagram, each panel showing $y = \sin x$ (faint gray baseline) alongside one transformed version — top-left: amplitude doubled ($a = 2$, taller wave); top-right: period halved ($b = 2$, compressed wave); bottom-left: phase shifted right ($c = \pi/2$, same wave slid right); bottom-right: vertical shift up ($d = 2$, wave riding a raised midline); each panel labels only the changed parameter and its geometric effect; student should be able to match each parameter to its visual consequence before reading the worked example] -->

**Example.** Sketch $y = 3\sin\!\left(2x - \frac{\pi}{2}\right) + 1$.

Pull out the four parameters. Amplitude: $|a| = 3$. Period: $\frac{2\pi}{2} = \pi$. Phase shift: $\frac{\pi/2}{2} = \frac{\pi}{4}$ to the right. Vertical shift: $d = 1$.

The midline is $y = 1$. The wave oscillates between $1 - 3 = -2$ and $1 + 3 = 4$. One full cycle runs from $x = \pi/4$ to $x = \pi/4 + \pi = 5\pi/4$. The wave starts at its midline at $x = \pi/4$, reaches its maximum of $4$ at $x = \pi/4 + \pi/4 = \pi/2$, returns to its midline at $x = 3\pi/4$, reaches its minimum of $-2$ at $x = \pi$, and completes the cycle at $x = 5\pi/4$.

<!-- → [IMAGE: sketch of $y = 3\sin(2x - \pi/2) + 1$ over two full cycles, with all five key points of the cycle explicitly labeled: midline crossing at $x = \pi/4$ (start), maximum at $(\pi/2, 4)$, midline crossing at $x = 3\pi/4$, minimum at $(\pi, -2)$, cycle end at $x = 5\pi/4$; dashed horizontal lines at $y = 1$ (midline), $y = 4$ (max), $y = -2$ (min); student should verify each analytical result above against the graph] -->

The four parameters are independent. Change any one and only that geometric feature changes. This is what makes the sinusoidal form powerful for modeling: each parameter corresponds to a measurable property of the phenomenon, and you can read the parameters directly from data.

### Reading parameters from data

If you have a table of periodic data, the four parameters are extractable without any fitting:

The *amplitude* is half the difference between maximum and minimum: $a = \frac{\max - \min}{2}$.

The *vertical shift* is the average of maximum and minimum: $d = \frac{\max + \min}{2}$.

The *period* is the time between two successive maxima (or minima, or any two corresponding points one cycle apart). Then $b = \frac{2\pi}{P}$.

The *phase shift* tells you where the wave starts relative to what a standard sine or cosine would do. If you use cosine (which peaks at $x = 0$), the phase shift is the time at which the maximum occurs.

**Example — daylight in Boston.** The longest day of the year is around June 21 (day 172), with about 15 hours of daylight. The shortest is around December 21 (day 355), with about 9 hours. The period is 365 days.

From the data: amplitude $a = (15 - 9)/2 = 3$. Vertical shift $d = (15 + 9)/2 = 12$. Period $P = 365$, so $b = 2\pi/365$. Use a cosine and note the maximum occurs on day 172:

$$L(t) = 3\cos\!\left(\frac{2\pi}{365}(t - 172)\right) + 12$$

where $t$ is the day of the year. On day 172: $L = 3\cos(0) + 12 = 15$. On day 355: $L = 3\cos(\pi) + 12 = 9$. The model matches.

This is why sinusoidal functions are useful: not because someone declared that daylight varies sinusoidally, but because the actual data is well-approximated by a sinusoidal curve, and the parameters have physical meaning — amplitude is the range, period is the year, phase is the date of longest day.

<!-- → [CHART: $L(t) = 3\cos(2\pi(t-172)/365) + 12$ plotted over one full year ($t = 0$ to $365$), with the actual Boston daylight data points overlaid as dots for the solstices and equinoxes; horizontal dashed lines at $L = 15$ (summer max), $L = 9$ (winter min), $L = 12$ (midline); vertical dashed lines at $t = 172$ (June 21) and $t = 355$ (Dec 21); student should see that the formula and the data aren't just numerically close — the curve's shape matches the physical phenomenon] -->

---

## Part 2 — Tangent and its relatives: when division by zero is the interesting part

Sine and cosine are bounded. They never exceed 1 or go below $-1$. Tangent is different.

$\tan x = \frac{\sin x}{\cos x}$

Wherever $\cos x = 0$, the tangent is undefined. The cosine is zero at $x = \pm\pi/2, \pm 3\pi/2, \ldots$ — every odd multiple of $\pi/2$. At each of these points, the tangent has a vertical asymptote: the function shoots to $+\infty$ from one side and to $-\infty$ from the other.

Between consecutive asymptotes — say between $x = -\pi/2$ and $x = \pi/2$ — the tangent is continuous and increasing. It starts at $-\infty$ on the left, passes through $(0, 0)$ where $\sin 0 = 0$, and goes to $+\infty$ on the right. Then the pattern repeats on the next interval $(\pi/2, 3\pi/2)$, and so on.

The period of tangent is $\pi$, not $2\pi$. The tangent function completes a full cycle in half the interval that sine or cosine requires.

Why $\pi$ and not $2\pi$? Because $\tan(x + \pi) = \frac{\sin(x + \pi)}{\cos(x + \pi)} = \frac{-\sin x}{-\cos x} = \frac{\sin x}{\cos x} = \tan x$. The negatives cancel. Shifting by $\pi$ returns the same value.

<!-- → [IMAGE: $y = \tan x$ plotted from $-3\pi/2$ to $3\pi/2$, showing three complete branches; vertical asymptotes at $x = \pm\pi/2, \pm 3\pi/2$ drawn as dashed lines; zero crossings at $x = 0, \pm\pi$ marked; one branch annotated with "increases from $-\infty$ to $+\infty$ on $(-\pi/2, \pi/2)$"; period $\pi$ marked with a horizontal bracket between two successive zero crossings; student should see why the period is $\pi$ rather than $2\pi$ before encountering cotangent] -->

The three other functions — cotangent, secant, cosecant — are defined analogously:

$$\cot x = \frac{\cos x}{\sin x}, \qquad \sec x = \frac{1}{\cos x}, \qquad \csc x = \frac{1}{\sin x}$$

**Cotangent** is undefined where $\sin x = 0$ — at $x = 0, \pi, 2\pi, \ldots$ It has the same period as tangent ($\pi$) but decreases on each branch rather than increasing.

**Secant** is the reciprocal of cosine. Where cosine is large, secant is small; where cosine is near zero, secant blows up. The graph of secant is a series of U-shaped arcs: opening upward above the $x$-axis (where $\cos x > 0$) and opening downward below it (where $\cos x < 0$). The period is $2\pi$, the same as cosine.

**Cosecant** behaves the same way, relative to sine. Asymptotes where $\sin x = 0$; period $2\pi$.

The useful mental picture: the graphs of $\sec x$ and $\csc x$ are the graphs of $\cos x$ and $\sin x$ *inverted* — stretched to infinity near the zeros, compressed toward $\pm 1$ at the peaks.

<!-- → [IMAGE: two-panel figure — left panel: $y = \cos x$ (light gray, full wave) and $y = \sec x$ (dark, U-shaped arcs) plotted together from $-\pi$ to $3\pi$; right panel: $y = \sin x$ and $y = \csc x$ plotted together the same way; in each panel, asymptotes shown as dashed verticals, the parent function's zeros align exactly with the asymptotes of the reciprocal, and the reciprocal's arcs touch the parent function at $y = \pm 1$; student should see the reciprocal relationship geometrically — where the parent is small, the reciprocal is large, and vice versa] -->

### Transformations of tangent

The same parameter logic applies. For $y = a\tan(bx - c) + d$:

The period is $\frac{\pi}{|b|}$ (since tangent's natural period is $\pi$, not $2\pi$). The vertical asymptotes occur wherever the argument $bx - c$ equals $\pm\pi/2 + n\pi$ — that is, wherever the underlying cosine is zero. The vertical shift $d$ moves the midpoint of each branch up or down. The parameter $a$ stretches the branch vertically.

**Example.** $y = \tan(2x)$.

Period: $\pi/2$. Vertical asymptotes where $2x = \pm\pi/2$, i.e. $x = \pm\pi/4$. Then the pattern repeats every $\pi/2$.

---

## Part 3 — Inverse trig functions: going backward

Here is a question: if $\sin x = 0.5$, what is $x$?

The problem is that infinitely many values of $x$ satisfy this. In the interval $[0, 2\pi]$ alone, there are two: $x = \pi/6$ and $x = 5\pi/6$. Add any multiple of $2\pi$ to either and you get another. Sine is not one-to-one on the real line — the same output is achieved by infinitely many inputs. A function that isn't one-to-one doesn't have an inverse.

The solution is to *restrict the domain* to a piece of the real line where sine is one-to-one, and define the inverse only on that piece.

For sine, the standard choice is the interval $[-\pi/2, \pi/2]$. On this interval, sine is strictly increasing from $-1$ to $1$, so every value in $[-1, 1]$ is achieved exactly once. The *inverse sine* (written $\sin^{-1}$ or $\arcsin$) is the function that reverses this: given a value $y \in [-1, 1]$, it returns the unique $x \in [-\pi/2, \pi/2]$ with $\sin x = y$.

$$\sin^{-1}(1/2) = \pi/6, \quad \sin^{-1}(-1) = -\pi/2, \quad \sin^{-1}(0) = 0$$

For cosine, the standard restriction is $[0, \pi]$. On this interval, cosine is strictly decreasing from $1$ to $-1$. The *inverse cosine* $\cos^{-1}$ returns the unique $x \in [0, \pi]$ with $\cos x = y$.

$$\cos^{-1}(1/2) = \pi/3, \quad \cos^{-1}(-1) = \pi, \quad \cos^{-1}(0) = \pi/2$$

For tangent, the restriction is $(-\pi/2, \pi/2)$ — open because the asymptotes at the endpoints are not in the domain. Tangent on this interval runs from $-\infty$ to $+\infty$, strictly increasing, so every real number is achieved exactly once. The *inverse tangent* $\tan^{-1}$ returns the unique $x \in (-\pi/2, \pi/2)$ with $\tan x = y$.

$$\tan^{-1}(1) = \pi/4, \quad \tan^{-1}(0) = 0, \quad \tan^{-1}(-\sqrt{3}) = -\pi/3$$

<!-- → [IMAGE: three panels side by side, one per inverse function — left: $y = \sin x$ with the restricted segment $[-\pi/2, \pi/2]$ highlighted and all other periods faded, below it the graph of $y = \sin^{-1} x$ on $[-1,1]$; center: same treatment for $\cos x$ on $[0, \pi]$ and $\cos^{-1} x$; right: same for $\tan x$ on $(-\pi/2, \pi/2)$ and $\tan^{-1} x$; in each panel, the restricted segment of the original and the inverse function are visually mirror images across $y = x$; student should see that the inverse is literally the original function reflected — the range of the inverse is exactly the restricted domain of the original] -->

### The composition trap

A natural question: does $\sin^{-1}(\sin x) = x$?

Sometimes. If $x \in [-\pi/2, \pi/2]$ — in the restricted range — then yes. But if $x = 3\pi/4$, then $\sin(3\pi/4) = \sin(\pi/4) = \sqrt{2}/2$, and $\sin^{-1}(\sqrt{2}/2) = \pi/4$, not $3\pi/4$. The inverse sine returns the equivalent angle *in the restricted range*, not the original angle.

$\sin^{-1}(\sin(3\pi/4)) = \pi/4$, not $3\pi/4$.

The other direction is cleaner: $\sin(\sin^{-1}(x)) = x$ for all $x \in [-1, 1]$. Always.

This asymmetry is not a flaw. It's a consequence of the fact that we had to restrict the domain to create an inverse at all. The inverse sine knows about angles in $[-\pi/2, \pi/2]$; for angles outside that range, it can only return the equivalent angle inside it.

### Solving equations with inverse trig

To solve $\sin x = 0.6$:

Step one: $x = \sin^{-1}(0.6) \approx 0.6435$ radians. This is one solution — the one in $[-\pi/2, \pi/2]$.

Step two: sine is positive in quadrants I and II. The other solution in $[0, 2\pi)$ is $\pi - 0.6435 \approx 2.498$ radians.

Step three: every multiple of $2\pi$ added to either gives another solution. The general solution:

$$x = 0.6435 + 2\pi n \quad \text{or} \quad x = 2.498 + 2\pi n, \quad n \in \mathbb{Z}$$

The inverse function gives you one solution. The symmetry of the circle — and the knowledge of which quadrants give positive or negative values — gives you the rest.

---

## Putting it together: building a tide model

A coastal city's tide table for one day: high tide at 6 AM, water height 14 ft; low tide at 12 PM, water height 2 ft; high tide again at 6 PM.

**Extract the parameters.** The period is 12 hours (from high to high). The amplitude is $(14 - 2)/2 = 6$ ft. The vertical shift (midline) is $(14 + 2)/2 = 8$ ft.

**Choose the form.** The tide is at maximum at $t = 6$ AM. Cosine is at its maximum at $t = 0$, so use cosine shifted 6 hours to the right. With $b = 2\pi/12 = \pi/6$:

$$h(t) = 6\cos\!\left(\frac{\pi}{6}(t - 6)\right) + 8$$

where $t$ is hours since midnight.

**Verify.** At $t = 6$: $h = 6\cos(0) + 8 = 14$. ✓ At $t = 12$: $h = 6\cos(\pi) + 8 = -6 + 8 = 2$. ✓ At $t = 18$: $h = 6\cos(2\pi) + 8 = 14$. ✓

**Use the model.** A fishing boat needs at least 11 feet of water to leave the harbor. During what hours is the water level at least 11 ft?

$$6\cos\!\left(\frac{\pi}{6}(t - 6)\right) + 8 \geq 11$$

$$\cos\!\left(\frac{\pi}{6}(t - 6)\right) \geq \frac{1}{2}$$

Cosine is at least $1/2$ when its argument is in $[-\pi/3, \pi/3]$. So:

$$-\frac{\pi}{3} \leq \frac{\pi}{6}(t - 6) \leq \frac{\pi}{3}$$

Multiply through by $6/\pi$:

$$-2 \leq t - 6 \leq 2$$

$$4 \leq t \leq 8$$

The water is at least 11 feet from 4 AM to 8 AM — a four-hour window. By the symmetry of the cosine, the same window holds in the next cycle: 4 PM to 8 PM.

<!-- → [CHART: $h(t) = 6\cos(\pi(t-6)/6) + 8$ plotted over 24 hours ($t = 0$ to $24$), showing two complete tide cycles; horizontal dashed lines at $h = 14$ (high tide), $h = 2$ (low tide), $h = 8$ (midline), $h = 11$ (boat threshold); the two intervals $[4, 8]$ and $[16, 20]$ shaded in a distinct color to show when $h \geq 11$; vertical tick marks at $t = 6, 12, 18$ (high tide, low tide, high tide); student should verify the shaded windows correspond exactly to the algebraic solution above] -->

This problem uses all three parts of the chapter. Part 1 built the sinusoidal model from four parameters. Part 3 solved the resulting inequality using the inverse cosine. The answer is concrete and checkable: plug $t = 4$ and $t = 8$ back in and confirm $h = 11$ at both.

The deeper point is about what kind of object a sinusoidal model is. It isn't a curve that happens to fit the data. It's a curve whose *structure* corresponds to the physics: amplitude is the tidal range, period is the time between high tides, phase is when the high tide occurs. The four parameters aren't free dials to twist until the curve fits — they're physical quantities that you measure first and translate directly into the formula. The model is the physics, written in the language of functions.

---

## What makes these functions special

Polynomials can be made to fit any smooth curve, but they do it by brute force — increasing degree until the fit is acceptable. A periodic function breaks any polynomial: no polynomial repeats, ever. Rational functions can blow up and have asymptotes, but they don't oscillate.

Sine and cosine are the only smooth, bounded, periodic functions that satisfy a simple differential equation: $y'' = -y$. That equation says the rate of change of the rate of change equals the negative of the value itself. This is the equation of a restoring force — the mathematical signature of anything that gets pushed back toward equilibrium harder the farther it strays. Springs. Pendulums. Electric circuits. Sound vibrations.

That's why these functions are everywhere. Not because mathematicians decided to study them, but because the physical world is full of systems with restoring forces, and sine and cosine are what restoring-force systems *do*.

The four parameters — amplitude, period, phase, vertical shift — encode everything about the wave. Amplitude is how far the system strays from equilibrium. Period is how long one oscillation takes. Phase is when in the cycle we start the clock. Vertical shift is where equilibrium sits on the scale we're measuring. Change the physical system, and these four numbers change. The functional form stays the same.

That is the design philosophy of periodic functions: four numbers, infinite variety, and every repeating thing in the physical world described by a sum of them.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 8.1 — The four parameters specify everything.** Ask an LLM: "Any sinusoid can be written as $y = A\sin(B(x - C)) + D$. Why are exactly *four* parameters needed — no more, no fewer?" Push it to identify what each parameter controls (amplitude, period via $B$, phase shift, vertical shift) and why no other transformation of a sinusoid is independent of these four. Then ask: "What about reflection across the $x$-axis — isn't that a fifth degree of freedom?" The answer should explain that reflection is captured by the sign of $A$.

**LLM Exercise 8.2 — Why tangent has vertical asymptotes.** Tell an LLM: "Tangent has vertical asymptotes at $\theta = \pi/2 + k\pi$. Sine and cosine never have asymptotes. What's different?" Force the explanation to connect to Chapter 5's rational-function asymptotes — tangent is $\sin\theta / \cos\theta$, and the denominator hits zero precisely at $\pi/2 + k\pi$ where the numerator does not. Then ask: "Are these asymptotes 'holes' or true vertical asymptotes?" Push the LLM to apply the Chapter 5 distinction.

**LLM Exercise 8.3 — Why $\arcsin$ has a restricted range.** Ask an LLM: "If $\sin(30°) = 0.5$ and $\sin(150°) = 0.5$, then $\arcsin(0.5)$ should equal both $30°$ and $150°$. Why is it defined to equal only $30°$?" The answer requires understanding that an inverse function must be a function — single-valued. Then ask: "Why was the range $[-\pi/2, \pi/2]$ chosen, rather than $[0, \pi]$ or some other interval?" Probe the answer: this interval covers all output values exactly once and includes the natural "small angle" reference cases.

**LLM Exercise 8.4 — When tides aren't sinusoidal.** Give an LLM this: "A pure sinusoidal tide model has equal high tides and equal low tides, equally spaced. But real tides at many locations show *two unequal high tides per day* (mixed semidiurnal tides) and seasonal variation. Why does the simple sinusoid fail there?" Force it to explain the limitation of a single sinusoid and what additional sinusoids (the moon's, the sun's, with different periods and amplitudes summed) are needed to model the real signal. The lesson: real periodic phenomena are often *sums* of sinusoids, not single ones.

**LLM Exercise 8.5 — Tangent as slope.** Ask an LLM: "Why does $\tan\theta$ equal the slope of the radius drawn at angle $\theta$ from the origin?" Push it to derive — slope = rise/run = $y/x = \sin\theta/\cos\theta = \tan\theta$. Then ask: "What does the asymptote of the tangent function correspond to, geometrically, in terms of the radius?" The answer: a vertical radius has undefined slope (vertical line), corresponding to the vertical asymptote. The geometry and algebra agree exactly.

---

## AI Wayback Machine

**Joseph Fourier** showed in 1822 that any periodic function can be decomposed into a sum of sines and cosines — Fourier series. The result reshaped not only mathematics but also physics, signal processing, and modern audio compression.

**Run this:**

```
Who was Joseph Fourier, and how does Fourier analysis connect to the periodic functions we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Joseph Fourier"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through how a square wave decomposes into a Fourier series — which sine and cosine terms add up to it?
- Ask it about Fourier's parallel role as governor of Egypt under Napoleon — and how that work shaped his physics.

What changes? What gets better? What gets worse?
