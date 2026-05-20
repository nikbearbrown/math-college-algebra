# Chapter 9 — Trigonometric Identities and Equations

*The chapter where the same angle, looked at from different directions, turns out to be the same angle.*

---

A radio engineer wants to send two tones simultaneously — one at 440 Hz, one at 660 Hz. The combined signal is:

$$\sin(2\pi \cdot 440\, t) + \sin(2\pi \cdot 660\, t)$$

The receiver needs to decode this. The engineer needs to know: can this sum be written differently? Is there a single sinusoid that captures it? Is there a moment when it equals zero? These are not abstract questions — they determine whether the signal is decodable at all.

Every one of them reduces to the same thing: manipulating trig expressions using *identities* — equations that are true for every angle, not just particular ones. This chapter is about those identities and what you can do with them.

---

## What an identity is, and why it is different from an equation

An *equation* is a condition on an unknown. $2x + 3 = 7$ is true for $x = 2$ and false for everything else. Solving it means finding which values work.

An *identity* is a statement that is true for all valid values of the variable. $\sin^2\theta + \cos^2\theta = 1$ is not a condition on $\theta$ — it holds for every $\theta$, always, without exception. You do not solve it; you use it.

The distinction matters because identities are tools, not problems. When a complicated trig expression appears, you do not solve it — you reach for the right identity and rewrite it into something simpler. The skill is knowing which identity to reach for.

The foundation is one geometric fact: a point on the unit circle has coordinates $(\cos\theta, \sin\theta)$, and every point on the unit circle satisfies $x^2 + y^2 = 1$. Therefore:

$$\sin^2\theta + \cos^2\theta = 1$$

Divide both sides by $\cos^2\theta$:

$$\frac{\sin^2\theta}{\cos^2\theta} + 1 = \frac{1}{\cos^2\theta}$$
$$\tan^2\theta + 1 = \sec^2\theta$$

Divide the original by $\sin^2\theta$ instead:

$$1 + \cot^2\theta = \csc^2\theta$$

Three identities from one geometric fact. This is the pattern throughout the chapter: a single source idea, explored from multiple angles.

There are also the reciprocal identities — $\sec\theta = 1/\cos\theta$, $\csc\theta = 1/\sin\theta$, $\cot\theta = 1/\tan\theta$ — and the quotient identities: $\tan\theta = \sin\theta/\cos\theta$ and $\cot\theta = \cos\theta/\sin\theta$. These are definitions as much as identities. And the even/odd identities: sine and tangent are odd ($\sin(-\theta) = -\sin\theta$, $\tan(-\theta) = -\tan\theta$), cosine is even ($\cos(-\theta) = \cos\theta$). The graph of cosine is symmetric about the vertical axis; the graph of sine is symmetric about the origin.

<!-- → [IMAGE: unit circle with a point at angle θ labeled (cos θ, sin θ), a right triangle drawn from the origin to the point to the x-axis, and the Pythagorean identity written beside it — student should see that sin²θ + cos²θ = 1 is just x² + y² = 1 read in trig notation, not a separate fact to memorize] -->

---

## The sum and difference formulas

Now for the identities that expand the toolkit substantially.

The cosine of a sum is *not* the sum of the cosines. $\cos(A + B) \neq \cos A + \cos B$. You can check: $\cos(60°) = 1/2$, but $\cos(30°) + \cos(30°) = \sqrt{3} \neq 1/2$. The actual formula is:

$$\cos(A + B) = \cos A \cos B - \sin A \sin B$$
$$\cos(A - B) = \cos A \cos B + \sin A \sin B$$

The signs flip between sum and difference — the $\mp$ tracks opposite the $\pm$. For sine:

$$\sin(A + B) = \sin A \cos B + \cos A \sin B$$
$$\sin(A - B) = \sin A \cos B - \cos A \sin B$$

Here the signs track *with* the $\pm$. And for tangent:

$$\tan(A \pm B) = \frac{\tan A \pm \tan B}{1 \mp \tan A \tan B}$$

The denominator's $\mp$ is again opposite the numerator's $\pm$.

These formulas are worth sitting with. They say that the trig of a compound angle is built from the trig of its component angles. This is not obvious — it is a non-trivial geometric fact about how angles combine on the unit circle.

### What you can do with them immediately

Exact values for angles like $75°$, $15°$, $\pi/12$, $5\pi/12$ — angles not on the standard unit circle — become computable by decomposing into angles that are.

$$\cos 75° = \cos(45° + 30°) = \cos 45° \cos 30° - \sin 45° \sin 30°$$
$$= \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} - \frac{\sqrt{2}}{2} \cdot \frac{1}{2} = \frac{\sqrt{6} - \sqrt{2}}{4}$$

That is an exact value — no approximation, no decimal rounding — derived entirely from the sum formula and the known values at $45°$ and $30°$. The same approach works for $\sin 75°$, $\tan 15°$, any angle that can be expressed as a sum or difference of $30°$, $45°$, and $60°$.

The sum formulas also let you verify identities that would otherwise look like guesswork. To show that $\sin(\pi/2 - \theta) = \cos\theta$, apply the difference formula:

$$\sin\!\left(\frac{\pi}{2} - \theta\right) = \sin\frac{\pi}{2}\cos\theta - \cos\frac{\pi}{2}\sin\theta = 1 \cdot \cos\theta - 0 \cdot \sin\theta = \cos\theta$$

The cofunction identities — sine and cosine are complements, tangent and cotangent are complements, secant and cosecant are complements — all fall out of the sum and difference formulas in exactly this way.

<!-- → [TABLE: two-column reference table — left: sum/difference formula; right: the sign rule in plain English ("cosine: signs flip"; "sine: signs follow"; "tangent: denominator flips") — student should be able to reconstruct the formula from the rule rather than memorizing each line independently] -->

---

## Double angles and half angles

Set $A = B = \theta$ in the sine sum formula:

$$\sin(\theta + \theta) = \sin\theta\cos\theta + \cos\theta\sin\theta = 2\sin\theta\cos\theta$$

So $\sin 2\theta = 2\sin\theta\cos\theta$. The sine of a doubled angle is twice the product of the original sine and cosine. This is one of those results that looks almost too clean. It is clean — and it is exactly right.

For cosine, the same substitution gives:

$$\cos 2\theta = \cos^2\theta - \sin^2\theta$$

Apply $\sin^2\theta = 1 - \cos^2\theta$ to the right side:

$$\cos 2\theta = 2\cos^2\theta - 1$$

Apply $\cos^2\theta = 1 - \sin^2\theta$ instead:

$$\cos 2\theta = 1 - 2\sin^2\theta$$

Three equivalent forms of the cosine double-angle formula. They are all the same identity, just algebraically rearranged. Which form is useful depends on context — in particular, on what you already know about the angle. If you know $\cos\theta$, use the second; if you know $\sin\theta$, use the third.

For tangent: $\tan 2\theta = \frac{2\tan\theta}{1 - \tan^2\theta}$, from the tangent sum formula with $A = B = \theta$.

<!-- → [INFOGRAPHIC: derivation tree showing the sum formulas at the top, with arrows branching down — one branch: set A = B to get double-angle formulas; second branch: solve double-angle for θ/2 to get half-angle formulas; third branch: add sum and difference formulas to get product-to-sum formulas — student should see the entire chapter's identity catalog as a single derivation tree with two source formulas at the root] -->

### Half angles

Take the double-angle formula $\cos 2\theta = 1 - 2\sin^2\theta$ and solve for $\sin\theta$:

$$\sin^2\theta = \frac{1 - \cos 2\theta}{2}$$

$$\sin\theta = \pm\sqrt{\frac{1 - \cos 2\theta}{2}}$$

Now substitute $\theta \to \theta/2$ — let the doubled angle be $\theta$ instead:

$$\sin\frac{\theta}{2} = \pm\sqrt{\frac{1 - \cos\theta}{2}}$$

The sign is chosen based on the quadrant that $\theta/2$ falls in. Similarly:

$$\cos\frac{\theta}{2} = \pm\sqrt{\frac{1 + \cos\theta}{2}}$$

$$\tan\frac{\theta}{2} = \frac{1 - \cos\theta}{\sin\theta} = \frac{\sin\theta}{1 + \cos\theta}$$

The tangent half-angle formulas have no $\pm$ ambiguity — both forms are always defined when the right side is, and both give the correct sign automatically. This makes them the preferred form when working with tangent.

The half-angle formulas extend the reach of exact computation. $\sin 22.5°$ is not on the unit circle, but $22.5° = 45°/2$ is, so:

$$\sin 22.5° = \sqrt{\frac{1 - \cos 45°}{2}} = \sqrt{\frac{1 - \sqrt{2}/2}{2}} = \frac{\sqrt{2 - \sqrt{2}}}{2}$$

Exact.

### Power-reducing forms

The half-angle derivation also produces what are called *power-reducing* identities:

$$\sin^2\theta = \frac{1 - \cos 2\theta}{2}, \qquad \cos^2\theta = \frac{1 + \cos 2\theta}{2}$$

These rewrite squared trig functions in terms of cosine of a doubled angle. The immediate use here is verification and simplification; in calculus, they are the standard tool for integrating $\sin^2$ and $\cos^2$ — a fact worth knowing even if calculus is ahead rather than behind you.

---

## Products and sums

There is a family of identities that convert *products* of trig functions into *sums*, and vice versa.

Add the cosine sum and difference formulas:

$$\cos(A - B) + \cos(A + B) = 2\cos A \cos B$$

So: $\cos A \cos B = \frac{1}{2}[\cos(A-B) + \cos(A+B)]$.

Similarly:

$$\sin A \cos B = \frac{1}{2}[\sin(A+B) + \sin(A-B)]$$
$$\sin A \sin B = \frac{1}{2}[\cos(A-B) - \cos(A+B)]$$

Running these in reverse — from sums to products — requires a substitution. Let $A = \frac{u+v}{2}$ and $B = \frac{u-v}{2}$, so $A + B = u$ and $A - B = v$. Then:

$$\sin u + \sin v = 2\sin\frac{u+v}{2}\cos\frac{u-v}{2}$$
$$\cos u + \cos v = 2\cos\frac{u+v}{2}\cos\frac{u-v}{2}$$

This is where the engineer's signal problem lives. Adding two sinusoids of different frequencies produces a *beating* pattern — the amplitude rises and falls at the difference frequency while oscillating at the average frequency. Physically: two guitar strings slightly out of tune produce a sound that pulses at the difference in their frequencies. Mathematically: that pulsing is exactly the product-to-sum formula at work.

<!-- → [IMAGE: graph showing sin(2π·440t) + sin(2π·660t) over a short time window — the rapid oscillation at the average frequency (550 Hz) is visibly modulated by a slower envelope at the difference frequency (220 Hz / 2 = 110 Hz); student should see the beating pattern and connect it to the sum-to-product formula that produces a product of a fast oscillation and a slow amplitude envelope] -->

---

## Verifying identities

The task: given a trig equation that claims to hold for all $\theta$, prove it.

The method: start with one side — usually the more complicated one — and rewrite it using identities until it matches the other side. Do not treat this like solving an equation. Do not work on both sides simultaneously and meet in the middle. Work on one side only.

Strategy guide:

- Express everything in terms of sine and cosine first. Secants, cosecants, and cotangents usually simplify once converted.
- Look for Pythagorean opportunities: $1 - \sin^2\theta = \cos^2\theta$, $\sec^2\theta - 1 = \tan^2\theta$.
- If products appear, try converting to sums; if sums appear, try factoring.
- A common denominator often clarifies a sum of fractions.

A worked verification: show that $\frac{\sin 2\theta}{1 + \cos 2\theta} = \tan\theta$.

Start with the left side. Substitute the double-angle formulas $\sin 2\theta = 2\sin\theta\cos\theta$ and $\cos 2\theta = 2\cos^2\theta - 1$:

$$\frac{2\sin\theta\cos\theta}{1 + (2\cos^2\theta - 1)} = \frac{2\sin\theta\cos\theta}{2\cos^2\theta} = \frac{\sin\theta}{\cos\theta} = \tan\theta \quad \checkmark$$

Notice the choice of which form of $\cos 2\theta$ to use. The denominator is $1 + \cos 2\theta$, so the form $2\cos^2\theta - 1$ is the right pick — it makes the $1 + (\ldots - 1)$ collapse cleanly to $2\cos^2\theta$. That kind of pattern recognition is what gets better with practice.

---

## Solving trigonometric equations

An identity holds for all $\theta$. A *trig equation* — $\sin\theta = 1/2$, or $2\cos^2\theta - \cos\theta = 0$ — is true for some values of $\theta$ and false for others. Solving it means finding all values.

### The inverse function and the symmetry

To solve $\sin\theta = c$ for $c \in [-1, 1]$:

- The inverse sine function $\sin^{-1}(c)$ returns one value, in $[-\pi/2, \pi/2]$.
- Sine's symmetry about $\pi/2$ means there is a second solution in $[0, 2\pi)$: $\pi - \sin^{-1}(c)$.
- The general solution extends periodically: $\theta = \sin^{-1}(c) + 2\pi n$ and $\theta = \pi - \sin^{-1}(c) + 2\pi n$ for integer $n$.

For cosine: solutions come in a $\pm$ pair. $\cos\theta = c$ gives $\theta = \pm\cos^{-1}(c) + 2\pi n$.

For tangent: period is $\pi$, not $2\pi$. $\tan\theta = c$ gives $\theta = \tan^{-1}(c) + \pi n$.

The pattern to internalize: use the inverse function to get one solution, then use the symmetry of the function to find the rest within one period, then append the periodic repetition.

<!-- → [IMAGE: three unit-circle diagrams side by side — one for sine showing the two solutions θ and π − θ that share the same sine value; one for cosine showing the two solutions θ and −θ; one for tangent showing the single solution per π-period — student should see that the symmetry rules for finding the second solution come directly from the geometry of the circle, not from a formula to memorize] -->

### Quadratic form

Sometimes the equation is quadratic in a trig function. Factor or apply the quadratic formula to the algebraic variable, then solve the resulting trig equations separately.

$2\sin^2\theta - 3\sin\theta + 1 = 0$ on $[0, 2\pi)$.

Let $u = \sin\theta$. Then $2u^2 - 3u + 1 = 0$, which factors as $(2u-1)(u-1) = 0$. So $u = 1/2$ or $u = 1$.

$\sin\theta = 1/2$: $\theta = \pi/6$ or $5\pi/6$.

$\sin\theta = 1$: $\theta = \pi/2$.

Three solutions: $\pi/6, \, \pi/2, \, 5\pi/6$.

### Using identities to simplify first

Some equations are not directly solvable until an identity converts them into a solvable form.

$\sin 2\theta = \cos\theta$ on $[0, 2\pi)$.

The equation mixes $2\theta$ and $\theta$. Substitute $\sin 2\theta = 2\sin\theta\cos\theta$:

$$2\sin\theta\cos\theta = \cos\theta$$
$$\cos\theta(2\sin\theta - 1) = 0$$

Now the equation is factored. Either $\cos\theta = 0$ or $2\sin\theta - 1 = 0$.

$\cos\theta = 0$: $\theta = \pi/2$ or $3\pi/2$.

$\sin\theta = 1/2$: $\theta = \pi/6$ or $5\pi/6$.

Four solutions: $\pi/6, \, \pi/2, \, 5\pi/6, \, 3\pi/2$.

The key step was recognizing that $\cos\theta$ appeared on the right and could be factored out of the left after applying the double-angle formula. Factoring is often the right instinct once identities have reduced everything to a common variable.

### The structure of the solution set

One more thing worth understanding: trig equations typically have infinitely many solutions (because trig functions are periodic), and the restriction to $[0, 2\pi)$ is a choice — a way of listing one full period's worth. The *general* solution uses integer multiples of the period to capture everything. Whether you need the general solution or the solution on a given interval depends on the context; know which one you are being asked for before you start.

---

## One function, combined two ways

A pendulum's angular displacement from vertical is:

$$\theta(t) = 0.2\cos(2t) + 0.05\sin(2t)$$

This is not obviously a single sinusoid. But the sum formula — run backward — says that any expression of the form $a\cos\omega t + b\sin\omega t$ can be written as $R\cos(\omega t - \phi)$ for some amplitude $R$ and phase shift $\phi$.

Expand $R\cos(2t - \phi)$ using the cosine difference formula:

$$R\cos(2t - \phi) = R\cos\phi\cos 2t + R\sin\phi\sin 2t$$

Match coefficients: $R\cos\phi = 0.2$ and $R\sin\phi = 0.05$. Then:

$$R = \sqrt{0.2^2 + 0.05^2} = \sqrt{0.04 + 0.0025} = \sqrt{0.0425} \approx 0.206$$

$$\tan\phi = \frac{0.05}{0.2} = 0.25 \implies \phi \approx 0.245 \text{ rad}$$

So $\theta(t) \approx 0.206\cos(2t - 0.245)$.

The maximum displacement is $R \approx 0.206$ radians, or about $11.8°$. The first zero occurs when $\cos(2t - 0.245) = 0$, i.e., when $2t - 0.245 = \pi/2$, giving $t \approx 0.908$ seconds.

A sum of two trig terms became one. The maximum, the phase, and the zeros all became readable from the single-function form. This is what the sum formulas are for in practice: not just computing $\cos 75°$, but combining oscillations into a manageable form.

<!-- → [IMAGE: graph of θ(t) = 0.2·cos(2t) + 0.05·sin(2t) over t ∈ [0, 3] with the equivalent 0.206·cos(2t − 0.245) overlaid as a dashed curve (the two are identical — student should see they coincide), the maximum at t ≈ 0.123 labeled with R ≈ 0.206, and the first zero at t ≈ 0.908 labeled; a small right-triangle inset shows how R and φ are computed from the coefficients 0.2 and 0.05] -->

---

## What you can do now

You can apply the fundamental Pythagorean, reciprocal, and quotient identities to simplify any trig expression. You can use the sum and difference formulas to compute exact values at non-standard angles and to verify identities by rewriting one side. You can apply the double-angle formulas — all three forms of $\cos 2\theta$, the single form of $\sin 2\theta$ — and derive the half-angle and power-reducing formulas from them. You can convert products of trig functions to sums, and sums to products.

You can solve any trig equation that reduces to a single trig function equal to a constant, by using the appropriate inverse function and the symmetry of the function over one period. You can handle quadratic-form equations by treating the trig function as an algebraic variable, and you can handle mixed-angle equations by applying identities to unify the angles before solving.

The catalog of identities is not large. The Pythagorean identity is one geometric fact. The sum formulas are two — for sine and cosine — from which everything else follows by substitution. The double-angle formulas come from setting $A = B$. The half-angle formulas come from solving the double-angle formula for $\theta/2$. The product-to-sum and sum-to-product formulas come from adding and subtracting the sum and difference formulas.

It is a small, interconnected structure. Every identity in the chapter either is one of two or three source identities, or follows from them by straightforward algebra. Once you see the structure, the catalog is not a list to memorize — it is a web of consequences from a few starting points.

---

## Exercises

### Warm-up

**Exercise 9.1.** *Tests the Pythagorean identity and its derived forms.* Given $\sin\theta = 3/5$ and $\theta$ is in Quadrant II, find $\cos\theta$, $\tan\theta$, $\sec\theta$, and $\csc\theta$ exactly. Do not use a calculator — use the Pythagorean identity and the signs appropriate to Quadrant II. Difficulty: low.

**Exercise 9.2.** *Tests the sum and difference formulas.* Use a sum or difference formula to find the exact value of each. (a) $\sin 75°$. (b) $\cos 15°$. (c) $\tan(7\pi/12)$. Difficulty: low.

**Exercise 9.3.** *Tests the double-angle formulas.* If $\cos\theta = -4/5$ and $\theta$ is in Quadrant III, find $\sin 2\theta$, $\cos 2\theta$, and $\tan 2\theta$ exactly. State which form of the $\cos 2\theta$ formula you are using and why. Difficulty: low.

### Application

**Exercise 9.4.** *Tests identity verification.* Verify the identity $\frac{\cos^2\theta - \sin^2\theta}{1 - \tan^2\theta} = \cos^2\theta$. Work on one side only. Difficulty: medium.

**Exercise 9.5.** *Tests solving a basic trig equation with the full solution set.* Solve $\sqrt{3}\tan\theta + 1 = 0$. (a) Give all solutions in $[0, 2\pi)$. (b) Give the general solution. Difficulty: medium.

**Exercise 9.6.** *Tests solving by factoring after applying an identity.* Solve $\cos 2\theta + \cos\theta = 0$ on $[0, 2\pi)$. Use the double-angle formula to express everything in terms of $\cos\theta$ first. Difficulty: medium.

### Synthesis

**Exercise 9.7.** *Tests quadratic-form equation with identity simplification.* Solve $2\sin^2\theta + 3\sin\theta - 2 = 0$ on $[0, 2\pi)$. Show the substitution, the factoring, and check that no candidate is extraneous. Difficulty: medium-high.

**Exercise 9.8.** *Tests combining two sinusoids into one.* A signal has the form $f(t) = 3\cos(5t) - 4\sin(5t)$. (a) Write this as $R\cos(5t - \phi)$, finding $R$ and $\phi$ exactly (or to four decimal places). (b) What is the maximum value of the signal? (c) Find the first positive time $t$ at which the signal equals zero. Difficulty: medium-high.

### Challenge

**Exercise 9.9.** *Tests the structure of the identity catalog.* Starting only from the sum formulas for $\sin(A + B)$ and $\cos(A + B)$, derive the following in order, showing each step: (a) $\sin 2\theta$ and $\cos 2\theta$; (b) the power-reducing formula for $\sin^2\theta$; (c) the half-angle formula for $\sin(\theta/2)$; (d) the product-to-sum formula $\sin A \cos B = \frac{1}{2}[\sin(A+B) + \sin(A-B)]$. Each derivation should take no more than three lines. The goal is to see the entire chapter as four steps from two starting points. Difficulty: high.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 9.1 — Identity vs. equation.** Tell an LLM: "I claim that $\sin^2\theta + \cos^2\theta = 1$ is an *identity*, not an equation. What does that distinction actually mean — what would change if I called it an equation?" Push it to articulate that an identity is true for *every* value in its domain (no solution set; the whole domain is the solution set), while an equation typically has a finite or restricted solution set. Then ask: "How would I prove a proposed identity is *not* an identity?" The answer: find one counterexample. One value where the two sides disagree is enough.

**LLM Exercise 9.2 — Why the sum formula is what it is.** Ask an LLM: "Derive $\sin(A + B) = \sin A \cos B + \cos A \sin B$ geometrically." Don't accept algebraic manipulation — push for the geometric construction (typically a unit-circle picture or a stack of triangles). Then ask: "Why doesn't $\sin(A+B) = \sin A + \sin B$ work?" Try it on $A = B = \pi/2$: $\sin\pi = 0$, but $\sin(\pi/2) + \sin(\pi/2) = 2$. The LLM should give a clear geometric reason for the failure of additivity.

**LLM Exercise 9.3 — Half-angle ambiguity.** Ask an LLM: "The half-angle formula $\sin(\theta/2) = \pm\sqrt{(1 - \cos\theta)/2}$ has a $\pm$ sign. Why is that ambiguity necessary?" Force the explanation: $\theta$ pins down a unique sine value, but $\theta/2$ can land in different quadrants depending on which "version" of $\theta$ you mean (e.g., $\theta + 2\pi$ has half-angle $\theta/2 + \pi$, in a different quadrant). Then ask: "Given a specific $\theta$, how do I decide which sign to use?" The answer requires knowing which quadrant $\theta/2$ is in.

**LLM Exercise 9.4 — How many solutions?** Tell an LLM: "Solve $2\sin\theta = 1$ for $\theta$ in radians. How many solutions does this have?" The answer: infinitely many ($\theta = \pi/6 + 2\pi k$ and $\theta = 5\pi/6 + 2\pi k$ for any integer $k$). Then ask: "Now restrict to $\theta \in [0, 2\pi)$." Two solutions. Then: "Now restrict further to $\theta \in [0, \pi/2]$." One solution. Probe: "What general rule determines how many solutions a trig equation has on a given interval?" Force the LLM to articulate the rule: count the periods that fit in the interval and how many times the equation is satisfied per period.

**LLM Exercise 9.5 — Why some identities verify from one side, others need both.** Ask an LLM: "When verifying a trig identity, sometimes you can manipulate just one side until it matches the other. Other times you have to manipulate both sides until they meet in the middle. What determines which approach is needed?" Push it to articulate that the choice depends on which side has more structure to work with — typically you start from the more complex side. Then ask: "Why is it generally bad practice to multiply both sides of a proposed identity by a non-zero expression as a verification step?" The answer: that move is valid for equations (preserves solution sets) but invalid for identities (would let you "verify" things that aren't actually identities, by introducing the assumption you're trying to prove).

---

## AI Wayback Machine

**Hipparchus of Nicaea** compiled the first known trigonometric table around 130 BCE — establishing trig as a discipline. Most of the identities we still teach today have a continuous lineage back to his calculations.

**Run this:**

```
Who was Hipparchus, and how does his trigonometric work connect to the identities and equations we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Hipparchus"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through how Hipparchus used trigonometric ratios to compute astronomical distances.
- Ask it about Hipparchus's discovery of the precession of the equinoxes.

What changes? What gets better? What gets worse?
