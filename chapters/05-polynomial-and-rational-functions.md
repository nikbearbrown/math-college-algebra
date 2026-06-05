# Chapter 5 — Polynomial and Rational Functions


## TL;DR

- What happens when a curve is allowed to bend more than once.
- The chapter moves through The cannonball and the accountant, Part 1 — Quadratic functions: the bend with a name, Finding the vertex two ways, A quadratic optimization problem, and related ideas.
- Read it for the main argument, the vocabulary it introduces, and the practical judgment it asks you to develop.

*What happens when a curve is allowed to bend more than once.*

---

## The cannonball and the accountant

In 1589, Galileo dropped weights from the Tower of Pisa — or so the story goes. What is certain is that he measured falling objects carefully enough to notice something that wasn't obvious: the distance a falling body travels isn't proportional to the time it falls. It grows *faster* than that. In the first second, a ball falls 16 feet. By the second second, it has fallen 64 feet total. By the third, 144 feet. The differences keep growing.

That relationship is $d(t) = 16t^2$. The distance depends on the *square* of the time. Plot it and you get a parabola. The parabola is not linear — it has a bend — and the bend is what captures the physics of acceleration.

![Comparison of $d = 16t$ (linear, straight line)](images/05-polynomial-and-rational-functions-fig-01.png)
*Figure 5.1 — Comparison of $d = 16t$ (linear, straight line)*

Now imagine an accountant keeping revenue records. Quarter one: modest. Quarter two: better. Quarter three: a spike. Quarter four: lower again. One bend isn't enough to describe that curve. Two bends might do it. A cubic polynomial, not a quadratic. If the seasonal pattern is complicated enough, maybe a quartic.

And now imagine a factory where output per worker rises as the team grows, peaks when the team is optimally sized, then falls as coordination problems set in — but output also depends on machine availability, which is a ratio of working machines to total machines, and when that denominator approaches zero, output collapses to nothing. That's a rational function: a polynomial divided by a polynomial, undefined at a point, shooting toward infinity nearby.

This chapter is about all three of these: the quadratic (one bend, the simplest nonlinear case), the general polynomial (as many bends as you need), and the rational function (with the new phenomenon of things going infinite at specific inputs). Three families, increasingly rich, each containing the previous one as a special case.

---

## Part 1 — Quadratic functions: the bend with a name

A *quadratic function* has the form

$$f(x) = ax^2 + bx + c, \quad a \neq 0$$

The graph is a *parabola*. If $a > 0$, it opens upward — like a bowl catching rain. If $a < 0$, downward — like an arch. The single distinguishing feature of a parabola is its *vertex*: the bottom of the bowl or the top of the arch, depending on which way it opens.

![Two parabolas side by side ](images/05-polynomial-and-rational-functions-fig-02.png)
*Figure 5.2 — Two parabolas side by side *

The vertex matters because it is the extreme point — the minimum of the function if $a > 0$, the maximum if $a < 0$. Every optimization problem that leads to a quadratic gets answered at the vertex.

### Finding the vertex two ways

**By formula.** The $x$-coordinate of the vertex of $f(x) = ax^2 + bx + c$ is

$$x = -\frac{b}{2a}$$

Plug that back in to get the $y$-coordinate.

**By completing the square.** Rewrite $f(x)$ in *vertex form*:

$$f(x) = a(x - h)^2 + k$$

The vertex is $(h, k)$. This form makes the vertex obvious by inspection; the formula derivation and the completing-the-square derivation produce the same answer by different routes.

**Example.** Find the vertex of $f(x) = 2x^2 - 8x + 5$.

By formula: $x = -\frac{-8}{2 \cdot 2} = 2$. Then $f(2) = 8 - 16 + 5 = -3$. Vertex: $(2, -3)$.

By completing the square:

$$f(x) = 2(x^2 - 4x) + 5 = 2(x^2 - 4x + 4 - 4) + 5 = 2(x - 2)^2 - 8 + 5 = 2(x - 2)^2 - 3$$

Vertex: $(2, -3)$. Same answer, different route. The vertex form makes it clear that the function is minimized when $(x - 2)^2 = 0$, i.e., when $x = 2$.

### A quadratic optimization problem

A farmer has 100 feet of fencing to enclose a rectangular pen. What dimensions maximize the area?

Let $x$ be one side. The perimeter constraint gives $2x + 2y = 100$, so $y = 50 - x$. The area is:

$$A(x) = x(50 - x) = -x^2 + 50x$$

This is a downward-opening parabola ($a = -1$). The maximum is at the vertex:

$$x = -\frac{50}{2 \cdot (-1)} = 25$$

So $y = 25$ as well, and the maximum area is $625$ ft². The pen is a square. This turns out to be a general fact: for a fixed perimeter, the rectangle with maximum area is always a square. The quadratic structure reveals it.

The quadratic is a powerful model precisely because it has exactly one bend. That's enough to capture acceleration in physics, maximization in economics, and the geometry of parabolic mirrors. When one bend isn't enough, you need more.

---

## Part 2 — Polynomial functions: bending as many times as needed

A *polynomial function* of degree $n$ has the form

$$f(x) = a_n x^n + a_{n-1} x^{n-1} + \ldots + a_1 x + a_0, \quad a_n \neq 0$$

Degree 2 is the quadratic we just finished. Degree 3 is cubic — it can have two bends. Degree 4 is quartic — three possible bends. In general, a polynomial of degree $n$ has at most $n - 1$ turning points. Adding degree adds flexibility.

The graph of a polynomial is smooth (no corners) and continuous (no breaks). The shapes it can take on are constrained by its degree, its leading coefficient, and where it crosses zero.

### End behavior: the long-run story

As $x$ goes to $\pm\infty$, the behavior of the whole polynomial is determined entirely by the *leading term* $a_n x^n$. The lower-degree terms get dominated.

Four cases:

| Degree | Leading coefficient | Left end ($x \to -\infty$) | Right end ($x \to +\infty$) |
|---|---|---|---|
| Even | Positive | $+\infty$ | $+\infty$ |
| Even | Negative | $-\infty$ | $-\infty$ |
| Odd | Positive | $-\infty$ | $+\infty$ |
| Odd | Negative | $+\infty$ | $-\infty$ |

Even-degree polynomials have both ends going the same direction (both up or both down). Odd-degree polynomials have the ends going opposite directions. The leading coefficient determines which direction.

![Four small polynomial sketches arranged in a 2×2](images/05-polynomial-and-rational-functions-fig-03.png)
*Figure 5.3 — Four small polynomial sketches arranged in a 2×2*

So $f(x) = -2x^4 + 7x^2 - 3$ goes to $-\infty$ on both ends (even degree, negative leading coefficient). And $f(x) = x^3 + 5x - 2$ goes from $-\infty$ on the left to $+\infty$ on the right (odd degree, positive leading coefficient).

### Zeros and the factor theorem

A *zero* of $f$ is any $x$ where $f(x) = 0$. The *factor theorem* says: $r$ is a zero if and only if $(x - r)$ is a factor of $f(x)$.

This is the key connection between the algebra (finding roots of an equation) and the geometry (where the graph crosses the $x$-axis). Every zero is a crossing point or a touch point.

The *multiplicity* of a zero is how many times the corresponding factor appears. If $f(x) = (x - 2)^3(x + 1)$, the zero $x = 2$ has multiplicity 3 and $x = -1$ has multiplicity 1.

Multiplicity controls what the graph does at that zero:

- **Odd multiplicity:** the graph crosses the $x$-axis. It comes from one side and exits the other.
- **Even multiplicity:** the graph touches the $x$-axis but turns around without crossing. It "bounces" off.

A zero of multiplicity 1 crosses cleanly. A zero of multiplicity 2 bounces off, like a ball touching the floor and rebounding. A zero of multiplicity 3 crosses but with an S-shaped inflection — it flattens out as it passes through.

![Three close-up sketches of a curve near a](images/05-polynomial-and-rational-functions-fig-04.png)
*Figure 5.4 — Three close-up sketches of a curve near a*

### Finding zeros

When the polynomial doesn't factor by inspection, two tools help.

**The rational zero theorem.** If a polynomial with integer coefficients has a rational zero $p/q$ (fully reduced), then $p$ divides the constant term and $q$ divides the leading coefficient. This gives a finite list of candidates to test — not a proof that any of them work, but a finite search space instead of an infinite one.

**Example.** Find the zeros of $f(x) = 2x^3 - 5x^2 - 4x + 3$.

The constant term is 3, the leading coefficient is 2. Candidates: $\pm 1, \pm 3, \pm \frac{1}{2}, \pm \frac{3}{2}$.

Test $x = 3$: $f(3) = 54 - 45 - 12 + 3 = 0$. Hit. So $(x - 3)$ is a factor.

**Synthetic division.** Once one zero $r$ is found, divide $f(x)$ by $(x - r)$ using synthetic division to get the remaining factor. For $f(x) = 2x^3 - 5x^2 - 4x + 3$ divided by $(x - 3)$:

$$2x^3 - 5x^2 - 4x + 3 = (x - 3)(2x^2 + x - 1)$$

Factor $2x^2 + x - 1 = (2x - 1)(x + 1)$. All three zeros: $x = 3$, $x = \frac{1}{2}$, $x = -1$.

### Sketching a polynomial from its features

**Example.** Sketch $f(x) = (x + 2)(x - 1)^2(x - 3)$.

Zeros: $-2$ (multiplicity 1), $1$ (multiplicity 2), $3$ (multiplicity 1).

Behavior at zeros: multiplicity 1 → cross at $-2$ and $3$; multiplicity 2 → bounce at $1$.

Degree: $1 + 2 + 1 = 4$. Even degree.

Leading coefficient: positive (multiplying the highest-degree terms gives $x^4$).

End behavior: even degree, positive leading → both ends go to $+\infty$.

$y$-intercept: $f(0) = (2)(1)(-3) = -6$.

Now assemble: the graph starts at $+\infty$ on the left, comes down, crosses at $-2$, continues down to $-6$ at $x = 0$, bounces at $x = 1$ (touching but not crossing), comes back down, crosses at $x = 3$, then rises to $+\infty$. No guessing about crossings or bounces — the multiplicities determine them entirely.

![Complete sketch of $f(x) = (x+2)(x-1)^2(x-3)$ on the](images/05-polynomial-and-rational-functions-fig-05.png)
*Figure 5.5 — Complete sketch of $f(x) = (x+2)(x-1)^2(x-3)$ on the*

### The fundamental theorem of algebra

A polynomial of degree $n$ has exactly $n$ zeros, counted with multiplicity and including complex zeros. This is the fundamental theorem of algebra. A cubic has 3 zeros, a quartic has 4, and so on. Some may be repeated; some may be complex. If the polynomial has real coefficients and a complex zero $a + bi$, then its conjugate $a - bi$ is also a zero — complex zeros of real-coefficient polynomials come in pairs.

The theorem guarantees that the zero-finding process terminates: there are exactly $n$ things to find, no more and no fewer.

---

## Part 3 — Rational functions: when a denominator can be zero

A *rational function* is a ratio of two polynomials:

$$f(x) = \frac{p(x)}{q(x)}, \quad q(x) \not\equiv 0$$

Division by zero is not defined. So wherever $q(x) = 0$, the function is undefined. That fact — which sounds like a technicality — is what gives rational functions their most interesting behavior.

Near a point where the denominator goes to zero (and the numerator doesn't), the function doesn't just get large. It gets *arbitrarily* large, positively or negatively, depending on which side you approach from. The graph shoots off toward infinity. The function has a *vertical asymptote* there.

### Domain and vertical asymptotes

The domain of a rational function excludes all $x$ where $q(x) = 0$.

A *vertical asymptote* is a vertical line $x = c$ that the graph approaches but never crosses. It occurs at each zero of the denominator that does not cancel with a zero of the numerator.

**Example.** $f(x) = \frac{x + 1}{(x - 2)(x + 2)}$.

Domain: all real numbers except $x = 2$ and $x = -2$.

Vertical asymptotes: $x = 2$ and $x = -2$ (the numerator $x + 1$ is nonzero at both points, so neither cancels).

### Holes

When a factor cancels between numerator and denominator, something subtler happens.

$f(x) = \frac{x^2 - 4}{x - 2} = \frac{(x-2)(x+2)}{x-2} = x + 2$ for $x \neq 2$.

The function equals the line $y = x + 2$ everywhere except $x = 2$, where it is undefined. The graph is a straight line with a single point missing — a *hole* at $(2, 4)$. Not a vertical asymptote; not a crossing; a single missing point. Factor cancellation is how you detect holes.

![Two side-by-side graphs ](images/05-polynomial-and-rational-functions-fig-06.png)
*Figure 5.6 — Two side-by-side graphs *

### Horizontal asymptotes: the long-run behavior

As $x \to \pm\infty$, the lower-degree terms in numerator and denominator get dominated by the highest-degree terms. Three cases, determined by comparing degrees:

Let $n = \deg(p)$ and $m = \deg(q)$.

- **$n < m$:** the denominator dominates. $f(x) \to 0$. Horizontal asymptote $y = 0$.
- **$n = m$:** numerator and denominator grow at the same rate. Horizontal asymptote $y = \frac{a_n}{b_m}$, the ratio of leading coefficients.
- **$n > m$:** the numerator dominates. No horizontal asymptote. If $n = m + 1$, there is a *slant asymptote* — a non-horizontal line the graph approaches at the ends.

**Example.** $f(x) = \frac{2x^2 + 3}{x^2 - 4}$. Degrees equal. Leading coefficients $2$ and $1$. Horizontal asymptote $y = \frac{2}{1} = 2$.

The graph approaches $y = 2$ from above or below as $x$ gets large, but never reaches it on either side.

### A full worked example

Graph $f(x) = \frac{x - 1}{x + 2}$.

**Domain:** $x \neq -2$.

**Vertical asymptote:** $x = -2$ (denominator zero, numerator nonzero at that point).

**Horizontal asymptote:** Degrees equal, leading coefficients both 1. $y = 1$.

**$x$-intercept:** Numerator zero at $x = 1$. Point: $(1, 0)$.

**$y$-intercept:** $f(0) = \frac{-1}{2}$. Point: $(0, -\frac{1}{2})$.

Now think about where the graph lives in each region. For $x > -2$: the function passes through $(0, -\frac{1}{2})$ and $(1, 0)$, then approaches $y = 1$ from below as $x \to +\infty$. For $x < -2$: as $x \to -2^-$, the denominator approaches zero from below, so $f$ goes to $+\infty$; as $x \to -\infty$, $f$ approaches $y = 1$ from above.

The function never equals 1 (the horizontal asymptote), because that would require $\frac{x-1}{x+2} = 1 \Rightarrow x - 1 = x + 2 \Rightarrow -1 = 2$, a contradiction.

![Complete graph of $f(x) = \frac{x-1}{x+2}$, showing both](images/05-polynomial-and-rational-functions-fig-07.png)
*Figure 5.7 — Complete graph of $f(x) = \frac{x-1}{x+2}$, showing both*

### Variation: rational structure in disguise

Several applied relationships are rational functions in simple forms.

**Inverse variation:** $y = \frac{k}{x}$. The output halves when the input doubles. Pressure and volume in a gas at constant temperature. Time and speed for a fixed distance.

**Inverse-square variation:** $y = \frac{k}{x^2}$. Light intensity falls off with the square of distance from the source. So does gravitational force.

**Example.** Light intensity $I$ varies inversely with the square of distance $r$: $I = \frac{k}{r^2}$. At $r = 5$ m, $I = 100$ lux. Find $I$ at $r = 10$ m.

$100 = \frac{k}{25}$, so $k = 2500$. At $r = 10$: $I = \frac{2500}{100} = 25$ lux.

Doubling the distance reduces intensity to one-quarter. This is the inverse-square law, and it governs light, gravity, electrostatic force, and sound in open air. The rational structure of $y = k/x^2$ encodes it exactly.

---

## Putting it together: a box from a flat sheet

A rectangular sheet of cardboard is 30 inches long and 20 inches wide. Cut equal squares of side $x$ from each corner, fold up the flaps, and you have a box.

**Building the volume function.** After cutting, the length of the box is $30 - 2x$, the width is $20 - 2x$, and the height is $x$. The volume is:

$$V(x) = x(30 - 2x)(20 - 2x) = x(600 - 100x + 4x^2) = 4x^3 - 100x^2 + 600x$$

This is a cubic polynomial in $x$.

**Domain.** The cut size must be positive ($x > 0$), and the width must remain positive ($20 - 2x > 0$, so $x < 10$). The domain is $(0, 10)$.

**Shape of the function on the domain.** At $x = 0$: $V = 0$ (no box). At $x = 10$: $V = 0$ again (the width disappears, no box). On the interval $(0, 10)$, the volume is positive — it rises from zero, reaches a peak, and falls back to zero. The maximum is somewhere in the interior.

The cubic $V(x) = 4x^3 - 100x^2 + 600x$ factors as $V(x) = 4x(x^2 - 25x + 150)$. The zeros of the quadratic factor are at $x = \frac{25 \pm \sqrt{625 - 600}}{2} = \frac{25 \pm 5}{2}$, giving $x = 10$ and $x = 15$. So on $(0, 10)$, the only zero is at the boundary.

Finding the interior maximum precisely requires calculus — setting the derivative to zero. The answer is $x \approx 3.92$ in, giving a maximum volume of about 1056 in³. For now, the polynomial structure tells us the shape: starts and ends at zero, has exactly one peak, and the location of that peak is determined by the algebra.

The whole problem is a study in what polynomial structure reveals. The volume formula came from a geometric construction. Its zeros came from the physical constraints. The existence of a maximum came from the end behavior (zero at both boundaries, positive in between). The polynomial didn't just represent the answer — it told us where to look.

![Figure ](images/05-polynomial-and-rational-functions-fig-08.png)
*Figure 5.8 — Figure *

---

## The design philosophy of the three families

Polynomial functions are smooth and continuous. They can bend as many times as their degree permits, no more. They are unbounded — as $x$ grows, a polynomial grows too, without limit. They cannot have asymptotes, holes, or discontinuities. Their values at large $x$ are dominated by the leading term.

Rational functions inherit polynomials' smoothness wherever the denominator is nonzero, then add the new feature: points where the function is undefined, with asymptotic behavior nearby. The domain is no longer all real numbers. Rationals can model bounded outputs (horizontal asymptotes tell you what the function approaches, and it actually approaches it), and they can model blowups (vertical asymptotes tell you where the function escapes to infinity).

The quadratic is a special case of the polynomial, which is a special case of the rational (with denominator 1). Each generalization adds expressiveness at the cost of one more set of features to track. Polynomials require monitoring degree, leading coefficient, and zeros. Rationals require all of that plus domain, asymptotes, and holes.

The through-line is the same idea from Chapter 2: an equation is a relationship written in symbols. A function is a rule for turning inputs into outputs. A graph is a picture of that rule. The polynomial and rational function chapters add new rules — more complicated, more expressive — but the translation between words, symbols, and pictures works the same way it always did. Set up the relationship. Identify the features. Draw the picture. Answer the question.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 5.1 — How many roots can a polynomial have?** Tell an LLM: "A degree-5 polynomial can have at most 5 real roots. Why exactly 5, and not more?" Ask it to explain the Fundamental Theorem of Algebra and the distinction between *real* roots and *complex* roots. Then ask: "Can a degree-5 polynomial have *zero* real roots? If yes, give me an example. If no, prove it." What does it say?

**LLM Exercise 5.2 — End behavior, in plain reasoning.** Give an LLM the polynomial $-3x^4 + 2x^3 - x + 7$ and ask: "Why does end behavior depend only on the leading term, and not on any of the others?" Push it to explain *why* — at very large $|x|$, why does $-3x^4$ swamp $2x^3 - x + 7$? Then ask: "At what value of $x$ does the leading term start dominating, in this specific polynomial?" The answer requires comparing magnitudes — see if the LLM gives a number or hand-waves.

**LLM Exercise 5.3 — Vertical asymptote vs. hole.** Ask an LLM: "If the numerator and denominator of a rational function both equal zero at $x = a$, do you get a vertical asymptote or a hole — or could it be either?" Push for the precise condition: a hole occurs when a factor cancels; an asymptote occurs when it doesn't. Then ask: "Construct a rational function with a hole at $x = 2$ and a vertical asymptote at $x = -3$, and graph it." Verify the construction.

**LLM Exercise 5.4 — When the function "doesn't exist."** Give an LLM the rational function $f(x) = \frac{x^2 - 9}{x^2 - 9}$ and ask what its graph looks like. The expected answer is *the horizontal line $y = 1$ with holes at $x = \pm 3$*. If the LLM says simply $y = 1$, push back: "But what is $f(3)$? What is $0/0$?" Force it to distinguish *the function* from *the simplified expression*. The two are not the same object.

**LLM Exercise 5.5 — Optimization and the bend.** Tell an LLM: "I'm building an open-top box from a 12-by-12 inch sheet by cutting equal squares from each corner and folding up the sides. Why does this problem have a maximum volume — why can't the volume just keep increasing?" Push it to explain the trade-off between base area (shrinks as cut size grows) and height (grows). Then ask it to find the optimum by setting up $V(x)$ and explain *why* this curve must have an interior maximum rather than maximizing at an endpoint.

---

##  AI Wayback Machine
**Évariste Galois** developed the theory connecting polynomial roots to group symmetries between 1828 and his death at age 20 in a duel — work that founded modern algebra. The night before the duel he wrote out as much of the theory as he could.

**Run this:**

```
Who was Évariste Galois, and how does his work on polynomials connect to what we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Évariste Galois"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to explain why fifth-degree polynomials have no general formula in terms of radicals — Galois's central result.
- Ask it about the duel — what we know and don't know about its cause.

What changes? What gets better? What gets worse?
