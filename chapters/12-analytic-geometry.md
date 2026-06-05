# Chapter 12 — Analytic Geometry


## TL;DR

- The chapter where a cone, sliced four different ways, explains satellite orbits, whispering galleries, and parabolic headlights.
- The chapter moves through A distance condition is a curve, The ellipse, Eccentricity, Where the focus matters physically, and related ideas.
- Read it for the main argument, the vocabulary it introduces, and the practical judgment it asks you to develop.

*The chapter where a cone, sliced four different ways, explains satellite orbits, whispering galleries, and parabolic headlights.*

---

Here is something that deserves more amazement than it usually gets. A satellite orbiting Earth traces an ellipse. A parabolic mirror in a telescope focuses starlight to a single point. The cooling towers of a nuclear plant have hyperbolic cross-sections. These are not metaphors for each other — they are literally the same curves, the same equations, appearing in completely unrelated physical contexts.

The reason is that all three shapes are sections of a cone. Take a double cone — two cones joined at the tip — and pass a plane through it. Depending on how you tilt the plane, the intersection is a circle, an ellipse, a parabola, or a hyperbola. Tilt it one way and you get one shape. Tilt it another and you get another. Four shapes from one operation.

This chapter is about the algebra of those shapes: how to write their equations, how to read their geometry from the equations, and why the same curve keeps appearing in optics, acoustics, and orbital mechanics.

![Diagram of a double cone (two cones joined](images/12-analytic-geometry-fig-01.png)
*Figure 12.1 — Diagram of a double cone (two cones joined*

---

## A distance condition is a curve

Every conic section can be defined by a distance condition — a rule specifying which points qualify.

A *circle* is the set of points at a fixed distance from one fixed point (the center). One point, one distance, one equation.

An *ellipse* generalizes this: instead of one fixed point, two — the *foci*. The rule is that the *sum* of a point's distances from the two foci is constant. Pick any point on the ellipse, measure its distance to focus 1 and its distance to focus 2, add them: you always get the same number. Every point on the curve satisfies this; every point off the curve does not.

A *hyperbola* replaces the sum with a *difference*: the absolute difference of distances from the two foci is constant.

A *parabola* replaces the second focus with a line — the *directrix*. The rule is that every point on the parabola is equidistant from the focus and the directrix.

Four curves, four distance conditions. The algebra translates each condition into an equation in $x$ and $y$.

| conic | fixed elements | distance condition | equation form — |
| --- | --- | --- | --- |
| circle (one point, fixed distance, x² + y² = r² | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| ellipse (two foci, sum = 2a, x² | a² + y² | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| hyperbola (two foci, /difference/ = 2a, x² | a² − y² | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| parabola (one focus + directrix, equal distances, y² = 4px) | student should see the entire chapter's logic in one row per conic before any algebra appears | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |

---

## The ellipse

Start with two foci at $(-c, 0)$ and $(c, 0)$. The defining condition: for any point $(x, y)$ on the ellipse, the sum of the distances to the two foci equals some constant $2a$.

Work out the algebra — square twice to eliminate the square roots — and the condition becomes:

$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$

where $b^2 = a^2 - c^2$. The parameter $a$ is half the total width along the major axis; $b$ is half the height along the minor axis; $c$ is the distance from the center to each focus. The three are linked: $a^2 = b^2 + c^2$. Always.

Read the geometry from the equation: the ellipse crosses the $x$-axis at $x = \pm a$ (the *vertices*) and the $y$-axis at $y = \pm b$ (the *co-vertices*). The foci sit inside the ellipse at $(\pm c, 0)$. When $a = b$, the foci collapse to the center, $c = 0$, and the ellipse is a circle.

For a vertical major axis, the roles of $a$ and $b$ swap: $\frac{x^2}{b^2} + \frac{y^2}{a^2} = 1$, where $a > b$ and the vertices are at $(0, \pm a)$. The rule for recognizing orientation: whichever denominator is larger, that is the major axis.

For an ellipse centered at $(h, k)$:

$$\frac{(x-h)^2}{a^2} + \frac{(y-k)^2}{b^2} = 1$$

### Eccentricity

The ratio $e = c/a$ is the *eccentricity*. It measures elongation. At $e = 0$, the ellipse is a circle. As $e$ approaches 1, the ellipse stretches into an increasingly narrow sliver.

Earth's orbit has $e \approx 0.017$ — nearly circular, which is why seasons are driven by axial tilt rather than distance from the Sun. Halley's Comet has $e \approx 0.967$ — at perihelion it passes inside the orbit of Venus; at aphelion it reaches beyond Neptune. Same kind of curve, radically different eccentricity.

### Where the focus matters physically

Place a light source at one focus of an elliptical mirror. Every ray bounces off the mirror and converges at the other focus — because the reflection law and the equal-sum distance condition combine to guarantee it. This is why elliptical mirrors concentrate light, and why elliptical ceilings concentrate sound.

Statuary Hall in the U.S. Capitol has an elliptical floor plan. John Quincy Adams, serving as a congressman after his presidency, reportedly positioned his desk at one focus — so he could hear conversations at the other focus across the room. Whether the story is exact, the geometry is.

### Finding the equation from the geometry

An ellipse has vertices at $(\pm 5, 0)$ and foci at $(\pm 3, 0)$.

$a = 5$ and $c = 3$, so $b^2 = a^2 - c^2 = 25 - 9 = 16$.

$$\frac{x^2}{25} + \frac{y^2}{16} = 1$$

That is it. The entire geometry of the ellipse — its width, its height, the locations of both foci — is packed into two numbers in the denominators.

![Labeled ellipse diagram showing the equation x²/25 +](images/12-analytic-geometry-fig-02.png)
*Figure 12.2 — Labeled ellipse diagram showing the equation x²/25 +*

---

## The hyperbola

Change the sum in the ellipse definition to a difference. Now we want all points where the *absolute difference* of distances to two foci equals a constant $2a$.

The algebra produces:

$$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$$

where now $c^2 = a^2 + b^2$ — addition, not subtraction. This is the critical sign change relative to the ellipse. For the ellipse, $c < a$ because $c^2 = a^2 - b^2$. For the hyperbola, $c > a$ because $c^2 = a^2 + b^2$. The foci of a hyperbola lie *outside* the curve; the foci of an ellipse lie *inside* it.

The hyperbola has two separate branches, opening left and right. The vertices are at $(\pm a, 0)$ — the points on the curve closest to the center. The curve never reaches the $y$-axis; any point on the $y$-axis would be equidistant from both foci, giving a difference of zero, which satisfies the condition only if $a = 0$.

### The asymptotes

As you move far from the center along a hyperbola, the curve approaches but never reaches the lines $y = \pm \frac{b}{a} x$. These are the *asymptotes*. No point on the hyperbola lies on an asymptote, but they describe the hyperbola's long-run behavior exactly.

A useful construction: draw the rectangle with corners at $(\pm a, \pm b)$. The asymptotes are its diagonals, extended. This rectangle is the key to sketching a hyperbola — draw the rectangle, extend the diagonals, and the branches hug those diagonals as they fly outward from the vertices.

For a vertical transverse axis: $\frac{y^2}{a^2} - \frac{x^2}{b^2} = 1$. The vertices move to $(0, \pm a)$, the asymptotes become $y = \pm \frac{a}{b} x$. The sign of the leading positive term tells you the orientation: positive $x^2$ term means horizontal, positive $y^2$ term means vertical.

### An example read directly from the equation

$\frac{x^2}{16} - \frac{y^2}{9} = 1$.

$a^2 = 16$, $b^2 = 9$, so $a = 4$, $b = 3$. $c^2 = 16 + 9 = 25$, $c = 5$.

Vertices: $(\pm 4, 0)$. Foci: $(\pm 5, 0)$. Asymptotes: $y = \pm \frac{3}{4} x$. Branches open left and right.

Draw the rectangle from $(-4, -3)$ to $(4, 3)$. Extend its diagonals. The two branches pass through the vertices, curl outward, and approach the diagonal lines.

![Graph of x²/16 − y²/9 = 1 with](images/12-analytic-geometry-fig-03.png)
*Figure 12.3 — Graph of x²/16 − y²/9 = 1 with*

### Where hyperbolas appear

The LORAN navigation system, used before GPS, fixed a ship's position by measuring the *difference* in arrival times of radio signals from two fixed stations. Equal time differences placed the ship on a hyperbola with the two stations as foci. A second pair of stations gave a second hyperbola. The intersection of the two curves gave the position. This is the distance-difference condition converted into a navigation instrument — and it worked for decades.

---

## The parabola

The parabola has one focus and no second focus. The defining condition: a point on the parabola is equidistant from the focus and from a fixed line, the directrix.

With focus at $(p, 0)$ and directrix $x = -p$, the condition $\sqrt{(x-p)^2 + y^2} = x + p$ — distance to focus equals distance to directrix — squares and simplifies to:

$$y^2 = 4px$$

This is the standard form for a parabola opening right with vertex at the origin. The parameter $p$ is the distance from the vertex to the focus (and also from the vertex to the directrix — they are always equal, by the definition of the vertex as the midpoint between the two).

For $p > 0$ the parabola opens right; for $p < 0$ it opens left. The upward-opening version is $x^2 = 4py$, with focus at $(0, p)$ and directrix $y = -p$.

With vertex at $(h, k)$: $(y-k)^2 = 4p(x-h)$ opens horizontally; $(x-h)^2 = 4p(y-k)$ opens vertically.

Large $p$ gives a wide, shallow parabola; small $p$ gives a narrow, steep one. All parabolas are geometrically similar — they are the same shape, merely scaled — but $p$ sets the scale.

### Why the parabola appears in optics

Parallel rays traveling horizontally toward a parabolic mirror all reflect to the focus — exactly, not approximately. This follows from the reflection law and the equal-distance defining condition: the geometry enforces it.

Run it in reverse: a light source at the focus sends rays outward in all directions, but after reflecting off the parabolic mirror, every ray travels parallel to the axis — a focused beam. This is why flashlights, car headlights, and spotlights use parabolic reflectors. And it is why radio telescopes and satellite dishes are parabolic: incoming parallel signals converge to a single point where the receiver sits.

The parabola is the unique curve with this property. No other shape converts parallel rays to a focus without aberration. The definition — equal distances to focus and directrix — turns out to be exactly the condition that guarantees perfect focusing.

![Two side-by-side diagrams of a parabolic mirror ](images/12-analytic-geometry-fig-04.png)
*Figure 12.4 — Two side-by-side diagrams of a parabolic mirror *

---

## Reading any conic from its equation

In practice you encounter equations like $4x^2 - 9y^2 + 16x + 18y - 29 = 0$ — mixed terms, no obvious structure. The technique for recovering standard form is completing the square on the $x$ terms and $y$ terms separately. Rearrange, group, complete, and the equation reveals its type and its key features.

Before doing that work, you can classify the conic from the equation's structure alone. The general second-degree equation is:

$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

The *discriminant* $B^2 - 4AC$ classifies the conic without any algebraic manipulation:

- $B^2 - 4AC < 0$: ellipse (or circle if $A = C$ and $B = 0$).
- $B^2 - 4AC = 0$: parabola.
- $B^2 - 4AC > 0$: hyperbola.

The $Bxy$ term appears when the conic is rotated relative to the coordinate axes — when the major axis does not align with $x$ or $y$. The discriminant is invariant under rotation, which is why it classifies the conic even in the rotated case.

For equations with $B = 0$ — no cross-term, so no rotation — the test simplifies even further: look at the signs and magnitudes of the $x^2$ and $y^2$ coefficients.

- Same sign, unequal: ellipse.
- Same sign, equal: circle.
- One coefficient is zero: parabola.
- Opposite signs: hyperbola.

This is usually the faster check. The discriminant is the test that works when cross-terms are present.

---

## One formula for all three: polar form

The most elegant unification comes from polar coordinates. Place one focus at the origin. Then all three conics share a single equation:

$$r = \frac{ed}{1 \pm e\cos\theta}$$

(or with $\sin\theta$ for conics whose axis of symmetry is vertical), where $e$ is the eccentricity and $d$ is the distance from the focus at the origin to the directrix.

The value of $e$ classifies the conic:

- $e < 1$: ellipse.
- $e = 1$: parabola.
- $e > 1$: hyperbola.

One formula, one parameter, three curves. The parabola is the boundary — it is what an ellipse becomes as it stretches toward $e = 1$, and what a hyperbola becomes as it compresses toward $e = 1$ from above. The three families are not separate shapes: they are a continuum parameterized by eccentricity, with the parabola sitting exactly at the transition.

This polar form is the natural language of orbital mechanics. Kepler's first law — planets orbit the Sun in ellipses, with the Sun at one focus — is the statement that a planet's polar coordinates satisfy the formula above with $e < 1$. Comets on hyperbolic trajectories, passing through the solar system only once, satisfy the same formula with $e > 1$. A body that arrives from infinity, swings around the Sun, and departs on a path exactly mirroring its arrival has $e = 1$ — a parabolic orbit. Same formula throughout, physics choosing the eccentricity.

![A sequence of four polar curves plotted using](images/12-analytic-geometry-fig-05.png)
*Figure 12.5 — A sequence of four polar curves plotted using*

---

## A satellite orbit from two measurements

A satellite is placed in elliptical orbit around Earth. At perigee — closest approach — it is 200 km above the surface. At apogee — farthest point — it is 2,000 km above. Earth's radius is about 6,371 km.

Distance from Earth's center at perigee: $6371 + 200 = 6571$ km. At apogee: $6371 + 2000 = 8371$ km.

For an ellipse with Earth at one focus, the perigee is the short end of the major axis and the apogee is the far end. The distances from the focus to the two vertices are:

$$a - c = 6571 \qquad a + c = 8371$$

Add the two equations: $2a = 14942$, so $a = 7471$ km. Subtract: $2c = 1800$, so $c = 900$ km.

Then $b^2 = a^2 - c^2 = 7471^2 - 900^2 = 55{,}815{,}841 - 810{,}000 = 55{,}005{,}841$, giving $b \approx 7416.6$ km.

The orbit equation:

$$\frac{x^2}{7471^2} + \frac{y^2}{7416.6^2} = 1$$

Eccentricity: $e = 900/7471 \approx 0.12$. This is mildly elliptical — more stretched than Earth's own nearly circular orbit ($e \approx 0.017$), far less extreme than Halley's Comet ($e \approx 0.967$).

Two observable measurements — the two altitudes — determined the entire orbital geometry. The semi-major axis, the semi-minor axis, the location of Earth relative to the ellipse's center, the eccentricity: all of it follows from the two numbers 200 and 2,000.

![Diagram of the satellite orbit ellipse with Earth](images/12-analytic-geometry-fig-06.png)
*Figure 12.6 — Diagram of the satellite orbit ellipse with Earth*

---

## What you can do now

You can write the standard-form equation of any ellipse, hyperbola, or parabola from geometric data — vertices, foci, directrix, eccentricity — and you can extract all of those features from the equation. You can sketch each curve by locating the center, the vertices, and for hyperbolas, the asymptote rectangle. You can complete the square to convert a general second-degree equation to standard form.

You can classify a conic from its general equation using the discriminant, before doing any algebraic work. You can write conics in polar form with one focus at the origin and read the type directly from the eccentricity.

The single organizing idea: **all four conic sections are sets of points satisfying a distance condition involving one focus, two foci, or one focus and a directrix.** The circle, the ellipse, the hyperbola, and the parabola are not four separate inventions — they are four cases of one idea, distinguished by whether you use a sum, a difference, or an equal distance, and whether you have one fixed point or two.

The same curves appear in optics because light bouncing off a mirror obeys a reflection law that interacts with distance conditions in exactly the way the conic definitions require. They appear in orbital mechanics because gravity produces an inverse-square force whose trajectories happen to be conic sections. The mathematics did not chase the physics — it had already described the pattern before anyone knew the physics was there.

---

## Exercises

### Warm-up

**Exercise 12.1.** *Tests reading an ellipse from its equation.* For the ellipse $\frac{x^2}{49} + \frac{y^2}{25} = 1$, identify (a) the orientation of the major axis, (b) the values of $a$, $b$, and $c$, (c) the coordinates of the vertices, co-vertices, and foci. Do not use a calculator. Difficulty: low.

**Exercise 12.2.** *Tests reading a hyperbola from its equation.* For the hyperbola $\frac{y^2}{9} - \frac{x^2}{16} = 1$, identify (a) the orientation of the transverse axis, (b) the values of $a$, $b$, and $c$, (c) the vertices, foci, and asymptote equations. Difficulty: low.

**Exercise 12.3.** *Tests reading a parabola from its equation.* Write $x^2 = -12y$ in the form $x^2 = 4py$. Identify $p$, the direction of opening, the coordinates of the focus, and the equation of the directrix. Difficulty: low.

### Application

**Exercise 12.4.** *Tests writing an equation from geometric data.* Find the equation of the ellipse with foci at $(\pm 4, 0)$ and vertices at $(\pm 7, 0)$. Then find the eccentricity and state whether the ellipse is closer to circular or highly elongated. Difficulty: medium.

**Exercise 12.5.** *Tests completing the square to identify a conic.* Identify the conic and find its key features: $9x^2 - 4y^2 - 36x + 8y - 4 = 0$. Complete the square on both variables and write the result in standard form. Difficulty: medium.

**Exercise 12.6.** *Tests the discriminant classification.* Use the discriminant $B^2 - 4AC$ to classify each conic without further algebra. (a) $3x^2 + 5xy + 2y^2 - 6 = 0$. (b) $x^2 - 4xy + 4y^2 + 2x - y = 0$. (c) $2x^2 + 3y^2 - 12 = 0$. Difficulty: medium.

### Synthesis

**Exercise 12.7.** *Tests building an ellipse equation from a physical setup.* A whispering gallery has an elliptical ceiling. The foci are 40 ft apart and the ceiling is 25 ft high at its center (directly above the midpoint between the foci). (a) Find the equation of the ellipse, with the center at the origin. (b) How wide is the gallery at floor level? (c) A person stands at one focus. How far are they from the nearest wall along the major axis? Difficulty: medium-high.

**Exercise 12.8.** *Tests the polar form and eccentricity continuum.* A comet follows the path $r = \frac{3}{1 - 1.2\cos\theta}$ (distances in AU, with the Sun at the origin). (a) Identify the type of conic. (b) Find the eccentricity and the distance from the focus to the directrix. (c) Find the closest the comet comes to the Sun (perihelion distance). (d) Does this comet return, or does it pass through the solar system only once? Justify your answer using the eccentricity. Difficulty: medium-high.

### Challenge

**Exercise 12.9.** *Tests integration of all three conics.* A reflecting telescope has a parabolic primary mirror with focus at point $F_1$, and a small hyperbolic secondary mirror whose nearer focus also sits at $F_1$ and whose farther focus $F_2$ is behind the primary mirror (where the eyepiece is). (a) Explain in terms of the distance conditions why a ray parallel to the telescope axis, after reflecting off the parabolic mirror toward $F_1$, will then reflect off the hyperbolic mirror toward $F_2$. (b) If the parabolic mirror has equation $x^2 = 200y$ (in mm) and the hyperbolic secondary has $a = 30$ mm and $c = 110$ mm, write the equation of the hyperbola centered at the origin with transverse axis along the $y$-axis. (c) Verify that the shared focus condition is physically consistent given the mirror geometry. Difficulty: high.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 12.1 — Eccentricity unifies the conics.** Ask an LLM: "Eccentricity $e = 0$ gives a circle, $0 < e < 1$ gives an ellipse, $e = 1$ gives a parabola, and $e > 1$ gives a hyperbola. Why does a single number control all four shapes?" Force the geometric explanation: each conic is defined by a fixed ratio between the distance to a focus and the distance to a directrix; that ratio is exactly $e$. Then ask: "What is the eccentricity of Earth's orbit?" The LLM should give approximately $0.0167$ — extremely close to a circle. Probe: "If the eccentricity were $0.5$, what would Earth's climate look like?"

**LLM Exercise 12.2 — Why an ellipse has two foci.** Tell an LLM: "An ellipse is defined by the property that the sum of distances from a point on the curve to two fixed foci is constant. Why two foci, not one?" Push it to explain that one fixed-distance condition gives a circle (radius = constant); two fixed points with sum-of-distances constant gives an ellipse. Then ask: "What's the optical consequence of the two-focus property?" The answer: light or sound emitted from one focus reflects off the ellipse and converges at the other focus — the basis of whispering galleries.

**LLM Exercise 12.3 — Parabolic reflection.** Ask an LLM: "Why do all parallel rays striking a parabolic dish converge at the focus?" Push for the geometric proof — every point on the parabola is equidistant from the focus and the directrix; that geometric symmetry forces the reflection angle to send incoming parallel rays through the focus. Then ask: "What real technologies depend on this property, and what would happen if we used a sphere or an ellipse instead?" The LLM should mention satellite dishes, headlights, and solar collectors, and explain why a sphere produces spherical aberration.

**LLM Exercise 12.4 — The hyperbola's asymptotes.** Tell an LLM: "Why does a hyperbola have asymptotes — why does the curve approach two straight lines as $x$ grows large?" Push for the algebraic argument: as $x \to \infty$, the hyperbola's equation $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$ effectively becomes $\frac{x^2}{a^2} = \frac{y^2}{b^2}$, giving $y = \pm(b/a)x$. Then ask: "Why don't ellipses have asymptotes?" Force the explanation that ellipses are bounded; hyperbolas extend to infinity, and unbounded curves often acquire asymptotic behavior.

**LLM Exercise 12.5 — Polar form's price.** Ask an LLM: "The polar form $r = \frac{ed}{1 - e\cos\theta}$ describes all conics with one formula. What's the price of this unification?" Push for the trade-off: simplicity and unification, at the cost of obscuring the conic-specific parameters that the Cartesian forms make obvious (semi-major / semi-minor axis lengths, exact vertex locations, asymptote slopes). Then ask: "When would I actually prefer the polar form to the Cartesian form?" The answer: when working with orbital mechanics (satellites and planets), where the focus is the natural origin.

---

##  AI Wayback Machine
**Pierre de Fermat** developed analytic geometry independently of (and slightly before) Descartes — though Descartes published first. Fermat's *Ad Locos Planos et Solidos Isagoge* showed how algebraic equations could describe curves.

**Run this:**

```
Who was Pierre de Fermat, and how does his analytic geometry work connect to what we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Pierre de Fermat"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to compare Fermat's and Descartes's versions of analytic geometry — what each got right.
- Ask it about Fermat's day job as a magistrate, and how mathematics fit into a working lawyer's life.

What changes? What gets better? What gets worse?
