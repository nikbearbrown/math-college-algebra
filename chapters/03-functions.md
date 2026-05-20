# Chapter 3 — Functions
*One rule, one output — and why that constraint unlocks everything else.*

---

There is a weather station in Anchorage that records the outdoor temperature at noon every day. Day 1: 42°F. Day 2: 38°F. Day 3: 41°F. Day 4: 35°F.

Notice what is rigid about that pairing. Each day produces exactly one temperature. Not two, not zero — one. You never look at the record and see "Day 3: 41°F and also 52°F." And you never look at a day and find it blank. Every input in the list pairs with exactly one output.

That rigidity is not a quirk of weather stations. It is the central feature of an enormous class of relationships, and mathematicians gave it a name: a *function*. The goal of this chapter is to understand what that name means, why it matters, and what you can do with it.

---

## What a function actually is

The formal definition sounds tidy: a function is a rule that assigns to each input exactly one output. But definitions do not make things clear — examples do. So let us look at some.

A car's odometer reads 12,847 miles at 9 a.m. on a Tuesday. Every moment after that, it reads something. At each moment in time there is exactly one odometer value. Time is the input. Mileage is the output. That is a function.

The price of a share of stock at any given second is a function of time. One price per second. (The price might change violently — that is fine. What matters is that at each second there is one price, not several.)

Now consider the reverse: given an odometer reading, what time does it correspond to? Here the relationship breaks down. If the car sat in a parking lot for six hours, the odometer read 12,847 from 9 a.m. until 3 p.m. That one value corresponds to many different times. Reverse it, and the rule is *not* a function.

The distinction is exactly this: a function is a rule where each input produces one output. The *same* input always produces the *same* output. Two different inputs are allowed to produce the same output — that is fine. What is not allowed is one input producing two different outputs.

<!-- → [IMAGE: side-by-side diagram contrasting a valid function (arrows from each input to exactly one output) with a non-function (one input with two arrows pointing to two different outputs) — student should immediately see why the odometer-in-reverse example fails] -->

### The notation

Mathematicians write $f(x)$ to mean "the output that rule $f$ produces when given input $x$." This is read "f of x." The symbol $f$ names the rule. The symbol $f(4)$ names the specific value the rule produces at input 4.

If $f(x) = 2x + 3$, then:

$$f(4) = 2(4) + 3 = 11$$
$$f(0) = 2(0) + 3 = 3$$
$$f(-2) = 2(-2) + 3 = -1$$

The rule is a machine. You put a number in. A number comes out. The formula tells you how the machine transforms the input.

One subtlety worth naming: $f$ and $f(x)$ are different things. $f$ is the rule itself — the machine. $f(x)$ is the output of the machine when it receives input $x$. Confusing the two causes trouble when we start composing and inverting functions, so notice the distinction now.

### The domain and the range

The *domain* is the set of all allowed inputs. The *range* is the set of all actual outputs — not the set of all possible outputs, the set of all outputs that actually occur.

For most functions defined by formulas, the domain is "all real numbers except the ones that break the formula." Two things break formulas:

**Division by zero.** The expression $\frac{1}{x-2}$ is undefined when $x = 2$. So the domain of $f(x) = \frac{1}{x-2}$ is all real numbers except $x = 2$.

**Even roots of negative numbers.** The expression $\sqrt{x-5}$ requires $x - 5 \geq 0$, so $x \geq 5$. The domain is $[5, \infty)$.

If neither constraint applies — no fractions, no even roots — the domain is all real numbers.

The range is harder to pin down from a formula alone. It helps to know the basic shapes. Here are the toolkit functions, the building blocks from which most college-algebra functions are assembled:

<!-- → [TABLE: toolkit functions with columns — name, rule, graph shape (described briefly), domain, range — the graph-shape column is what makes this table earn its place; a student who can picture each shape can derive the domain and range rather than memorizing them] -->

| Function | Rule | Domain | Range |
|---|---|---|---|
| Constant | $f(x) = c$ | all reals | $\{c\}$ |
| Identity | $f(x) = x$ | all reals | all reals |
| Quadratic | $f(x) = x^2$ | all reals | $[0, \infty)$ |
| Square root | $f(x) = \sqrt{x}$ | $[0, \infty)$ | $[0, \infty)$ |
| Reciprocal | $f(x) = 1/x$ | all reals except 0 | all reals except 0 |
| Absolute value | $f(x) = \|x\|$ | all reals | $[0, \infty)$ |

These are worth memorizing, not as arbitrary facts, but because every function in the next several chapters is one of these, modified.

<!-- → [IMAGE: a single figure showing all six toolkit function graphs on labeled axes, arranged in a 2×3 grid — student should see the family resemblance and be able to read domain and range directly from the shape of each curve] -->

### Testing a graph

If a relation is given as a graph rather than a formula, there is a simple visual test: does any vertical line cross the graph more than once?

A vertical line at $x = a$ is asking: "What output does the input $a$ produce?" If the line hits the graph twice, the input $a$ has two outputs — which violates the function rule. One crossing or none: function. Two crossings: not a function.

The parabola $y = x^2$ passes this test. Draw a vertical line anywhere; it hits the parabola once. The circle $x^2 + y^2 = 25$ fails. A vertical line at $x = 3$ hits the circle at $y = 4$ and at $y = -4$.

<!-- → [IMAGE: two side-by-side graphs — left: parabola y = x² with a vertical line touching it once (labeled "function"); right: circle x² + y² = 25 with a vertical line at x = 3 crossing it at y = 4 and y = −4 (labeled "not a function") — student should see the test in action on both cases] -->

---

## How functions behave

Knowing that a relationship is a function is the beginning. The next questions are more interesting: does the output grow as the input grows? Where does it peak? How fast does it change?

### Increasing and decreasing

A function is *increasing* on an interval if larger inputs produce larger outputs throughout that interval. Formally:

$$x_1 < x_2 \implies f(x_1) < f(x_2) \quad \text{for all } x_1, x_2 \text{ in the interval}$$

It is *decreasing* on an interval if larger inputs produce smaller outputs. The direction reverses, the logic stays the same.

The function $f(x) = x^2$ is decreasing on $(-\infty, 0)$ — as $x$ goes from $-3$ to $-2$ to $-1$, the output drops from 9 to 4 to 1. On $(0, \infty)$ it is increasing — as $x$ goes from 1 to 2 to 3, the output climbs from 1 to 4 to 9. The point $x = 0$ is where the function turns around.

That turning-around point — where the function stops decreasing and starts increasing, or vice versa — is a *local extremum*. A *local maximum* at $x = c$ means $f(c) \geq f(x)$ for all $x$ near $c$ (not necessarily everywhere, just nearby). A *local minimum* is the reverse.

An *absolute maximum* is the highest value the function achieves over its entire domain. An absolute minimum is the lowest. The parabola $f(x) = x^2$ has an absolute minimum at $(0, 0)$ — no other input produces a smaller output. It has no absolute maximum; the outputs grow without bound as $x$ gets large.

The distinction between local and absolute matters. A function might have several local maxima — several peaks — while only one of them is the highest point overall. Hiking: you can stand at the summit of a small hill (local maximum) while a taller mountain nearby is the absolute maximum of the terrain.

<!-- → [IMAGE: graph of a function with two local maxima and one local minimum marked, with the higher local maximum also labeled as the absolute maximum — the student should see that "local" and "absolute" are different concepts on the same curve] -->

### Average rate of change

Here is a question that sounds like physics but is pure algebra: how fast does the output change as the input changes?

The answer at any particular moment requires calculus — that is the derivative. But over an interval, we can answer it now. The *average rate of change* of $f$ from $x = a$ to $x = b$ is:

$$\frac{f(b) - f(a)}{b - a}$$

This is the slope of the line connecting the two points $(a, f(a))$ and $(b, f(b))$ on the graph. It measures the net change in output divided by the net change in input.

An example. The number of bacteria in a culture (in thousands) after $t$ hours is $N(t) = 50 + 10t - t^2$ for $0 \leq t \leq 12$. The average rate of change from $t = 0$ to $t = 5$:

$$\frac{N(5) - N(0)}{5 - 0} = \frac{(50 + 50 - 25) - 50}{5} = \frac{25}{5} = 5 \text{ thousand bacteria per hour}$$

The culture is growing at an average rate of 5,000 bacteria per hour over the first five hours.

Now completing the square: $N(t) = -(t-5)^2 + 75$. The maximum occurs at $t = 5$, where $N = 75$ thousand. After that, the population decreases — the culture is overcrowded, resources are depleted, the model says the count falls.

The average rate of change from $t = 5$ to $t = 10$:

$$\frac{N(10) - N(5)}{10 - 5} = \frac{(50 + 100 - 100) - 75}{5} = \frac{50 - 75}{5} = -5 \text{ thousand per hour}$$

Same magnitude, opposite sign. Symmetric around the peak, as the parabolic model demands.

One warning about averages: a positive average rate of change over an interval does not mean the function increased throughout the interval. The function might have risen sharply, then dipped, with an overall net increase. The average captures the net; it hides what happened in between. This is the cost of algebra. Calculus refines the picture.

<!-- → [IMAGE: graph of N(t) = −(t−5)² + 75 on [0, 12] with two secant lines drawn — one from (0, 50) to (5, 75) with positive slope labeled "+5 thousand/hr", one from (5, 75) to (10, 50) with negative slope labeled "−5 thousand/hr" — student should see that the secant slope is average rate of change and that it changes sign at the peak] -->

---

## Building functions from other functions

Once you have two functions, you can combine them. The combinations are simple; the one that requires attention is the last one.

**Arithmetic combinations.** Given $f(x) = x^2$ and $g(x) = x + 3$:

$$(f + g)(x) = x^2 + x + 3$$
$$(f - g)(x) = x^2 - x - 3$$
$$(fg)(x) = x^2(x + 3) = x^3 + 3x^2$$
$$(f/g)(x) = \frac{x^2}{x+3}, \quad x \neq -3$$

Nothing surprising here. The domain of each combination is the intersection of the domains of $f$ and $g$, with any new constraints (like division by zero) added on.

**Composition.** This is the genuinely new operation. The composition $(f \circ g)(x)$ means: apply $g$ first, then apply $f$ to the result.

$$(f \circ g)(x) = f(g(x)) = f(x + 3) = (x + 3)^2$$

Read right to left: $x$ enters, $g$ adds 3, $f$ squares the result.

The order matters. The composition $(g \circ f)(x)$ is different:

$$(g \circ f)(x) = g(f(x)) = g(x^2) = x^2 + 3$$

Apply $f$ first (squaring), then $g$ (adding 3). You get $x^2 + 3$, not $(x+3)^2$. These are the same only by accident — try another pair of functions and they will be different.

The domain of $(f \circ g)(x)$ has two constraints: $x$ must be in the domain of $g$, and $g(x)$ must be in the domain of $f$. Both must hold simultaneously.

Decomposing a composition — working backwards from the combined function to its pieces — is an important skill. For $h(x) = \sqrt{2x + 1}$, notice the structure: something is being square-rooted. The inner function is $g(x) = 2x + 1$ (it goes in first); the outer function is $f(u) = \sqrt{u}$ (it acts on the result). So $h = f \circ g$. There is often more than one valid decomposition; what matters is finding one that reveals structure.

<!-- → [INFOGRAPHIC: pipeline diagram showing composition — a value x enters a box labeled g, the output g(x) travels along an arrow into a box labeled f, the final output f(g(x)) exits — a second pipeline below shows the reverse order (f first, then g) producing a different result — student should see why order is not interchangeable] -->

### Transforming a graph

Now comes an elegant result: once you know the graph of one function, you can deduce the graphs of many related functions without plotting any new points.

Start with a function $f$ and its graph. Five operations:

**Vertical shift.** $f(x) + c$ lifts the entire graph up by $c$ units (or down if $c < 0$). Every point $(x, y)$ becomes $(x, y + c)$.

**Horizontal shift.** $f(x - c)$ shifts the graph *right* by $c$ units. This confuses students because the shift is in the direction opposite to the sign: $f(x - 3)$ is $f$ shifted *right* by 3, and $f(x + 3)$ is $f$ shifted *left* by 3.

Here is why: $f(x - 3) = f(0)$ when $x = 3$. The output that $f$ used to produce at input 0 is now produced at input 3. The whole graph slid right by 3.

**Reflection across the $x$-axis.** $-f(x)$ flips every output to its negative. Every point $(x, y)$ becomes $(x, -y)$.

**Reflection across the $y$-axis.** $f(-x)$ replaces every input $x$ with $-x$. The graph folds in half along the $y$-axis.

**Vertical stretch and compression.** $cf(x)$ for $c > 1$ stretches the graph vertically — every output is multiplied by $c$. For $0 < c < 1$, it compresses. The graph retains its shape but grows taller or shorter.

These transformations compose. The graph of $g(x) = -2(x - 3)^2 + 5$ is the parabola $y = x^2$ after four operations: shift right by 3, stretch vertically by 2, reflect across the $x$-axis (the negative sign), shift up by 5. Understanding this does not require re-plotting; it requires reading the formula.

<!-- → [IMAGE: sequence of four small graphs showing the parabola y = x² being transformed step by step into g(x) = −2(x−3)² + 5 — each panel labeled with the operation applied — student should be able to read any transformation sequence from a formula by recognizing this pattern] -->

### Even and odd functions

Two symmetries worth knowing:

A function is *even* if $f(-x) = f(x)$ for every $x$ in the domain. The graph is symmetric about the $y$-axis — the left half mirrors the right half. $f(x) = x^2$ is even: $f(-3) = 9 = f(3)$.

A function is *odd* if $f(-x) = -f(x)$. The graph is symmetric about the origin — rotate it 180° and it looks the same. $f(x) = x^3$ is odd: $f(-2) = -8 = -f(2)$.

Most functions are neither. But knowing a function is even or odd halves the work of graphing it.

---

## Inverting a function

Suppose $f$ takes input $x$ to output $y$. The *inverse function* $f^{-1}$ takes input $y$ back to $x$. The machine runs in reverse.

Not every machine can run in reverse. If $f(2) = 4$ and also $f(-2) = 4$, then a reversed machine receiving input 4 does not know whether to output 2 or $-2$. The reversed rule would not be a function.

The requirement for an invertible function: each output must come from exactly one input. This is called *one-to-one*. You test it on a graph with the *horizontal-line test*: every horizontal line must cross the graph at most once.

The parabola $f(x) = x^2$ over all real numbers fails this test — a horizontal line at $y = 4$ crosses at $x = 2$ and at $x = -2$. The function is not one-to-one, and it has no inverse over its full domain. (Restrict the domain to $x \geq 0$, and it passes. On that restricted domain, the inverse is $f^{-1}(x) = \sqrt{x}$.)

The linear function $f(x) = 2x + 3$ passes — every horizontal line crosses a non-horizontal line at most once. It has an inverse. To find it:

1. Write $y = 2x + 3$.
2. Swap $x$ and $y$: $x = 2y + 3$.
3. Solve for $y$: $y = \frac{x - 3}{2}$.

So $f^{-1}(x) = \frac{x - 3}{2}$.

Verify by composition: $f(f^{-1}(x)) = 2 \cdot \frac{x-3}{2} + 3 = (x - 3) + 3 = x$. ✓

The composition $f(f^{-1}(x)) = x$ is the defining property of an inverse. Applying $f$ after $f^{-1}$ (or $f^{-1}$ after $f$) returns you to where you started. This is not magic — it is the definition of reversal.

One notation warning: $f^{-1}(x)$ does *not* mean $\frac{1}{f(x)}$. The superscript $-1$ means inverse function, not reciprocal. The reciprocal is written $[f(x)]^{-1}$ or $\frac{1}{f(x)}$ to distinguish it.

<!-- → [IMAGE: two graphs on the same axes — f(x) = 2x + 3 and its inverse f⁻¹(x) = (x−3)/2 — with the line y = x drawn as a dashed reference — student should see that the two graphs are reflections of each other across y = x, which is the geometric meaning of "swap x and y"] -->

---

## One object, many questions

A delivery van's distance from its depot, in miles, after $t$ hours of driving is:

$$d(t) = 60t - 5t^2, \quad 0 \leq t \leq 12$$

At $t = 12$, $d(12) = 720 - 720 = 0$ — the van is back at the depot. This is one function, and it answers several different questions depending on which lens you use.

**The function question.** Is $d$ a function of $t$? Yes — each time produces exactly one distance. Domain: $[0, 12]$. Range: completing the square gives $d(t) = -5(t - 6)^2 + 180$, so the maximum distance is 180 miles. Range: $[0, 180]$.

**The behavior question.** When is the van moving away from the depot, and when is it returning? $d$ is increasing on $[0, 6)$ (outbound) and decreasing on $(6, 12]$ (returning). The van is farthest from the depot at $t = 6$ hours.

Average speed in the first three hours: $\frac{d(3) - d(0)}{3} = \frac{135}{3} = 45$ mph. Average speed from $t = 3$ to $t = 6$: $\frac{d(6) - d(3)}{3} = \frac{180 - 135}{3} = 15$ mph. The van is decelerating as it approaches the turnaround.

**The transformation question.** Suppose the van departs an hour late. The new distance function is $d_{\text{new}}(t) = d(t - 1)$ — the graph of $d$ shifted one unit to the right. The van still travels 180 miles from the depot; it just reaches the maximum at $t = 7$ instead of $t = 6$. The shape of the trip is unchanged; only its timing shifts.

Three concepts, one function, completely different questions. That is what the function framework does: it takes a relationship and makes it available to analysis from multiple angles.

<!-- → [IMAGE: graph of d(t) = 60t − 5t² on [0, 12] — downward parabola with vertex labeled (6, 180), two secant lines drawn from (0, 0) to (3, 135) and from (3, 135) to (6, 180) with slopes 45 and 15 labeled, and a second dashed curve showing d(t−1) shifted one unit right — student should see all three lenses (domain/range, average rate of change, transformation) operating on the same graph] -->

---

## The design decision the mathematicians made

Why define functions so restrictively — requiring each input to produce exactly one output? It excludes perfectly reasonable geometric objects. A circle is a fine shape, but it is not a function.

The answer is that the definition is what makes the operations well-defined.

If you compose two functions, you get a function. The proof uses the one-output rule at each step. If you invert a one-to-one function, you get a function. The operations of calculus — derivatives, integrals — are defined on functions, and they work precisely because the one-output rule holds throughout.

The circle is excluded because it cannot be operated on in these ways without first breaking it into pieces (the upper semicircle is a function; the lower semicircle is a function; the whole circle is not). The restriction is the cost. The operations you gain are the benefit.

This is the kind of trade-off that appears everywhere in mathematics: you accept a constraint, and in exchange you get a rich set of tools. Reject the constraint, and you have to give back the tools. The function definition is the most important such trade-off in college algebra, because every chapter after this one is about what you can do with those tools.

---

## What you can do now

You can determine whether a relation is a function — from a set of ordered pairs, from a formula, from a graph. You can find the domain and range. You can identify intervals where a function increases or decreases, locate its maxima and minima, and compute its average rate of change over any interval.

You can compose two functions and decompose a composite back into pieces. You can transform the graph of a function by shifting, reflecting, stretching, and compressing, and you can read those transformations from the formula without re-plotting. You can find the inverse of a one-to-one function and verify it by composition.

The single idea underneath all of this: **a function is a single-valued rule, and almost every operation of algebra is defined so as to preserve that single-valuedness.** The concept is not decorative. It is structural. Every chapter after this one builds on it.

---

## LLM Exercises

**Exercise 3-L1.** Ask an AI to explain the vertical-line test to you in a completely different way than your textbook. Then evaluate the explanation: does it correctly capture *why* the test works (the connection to the one-output rule), or does it describe the test without explaining the underlying idea? Write one paragraph identifying what the explanation got right and, if anything, what it missed or oversimplified.

**Exercise 3-L2.** Give an AI this prompt: "A function's average rate of change over [1, 5] is positive. Does that mean the function is increasing on [1, 5]? Explain." Evaluate the response carefully. If the AI says yes, identify the specific error. If it says no, check whether the counterexample it provides is valid. Write a short paragraph assessing the quality of the reasoning.

**Exercise 3-L3.** Ask an AI to find the inverse of $f(x) = \frac{2x + 3}{x - 1}$. Have it show every step. Then verify the answer yourself by checking that $f(f^{-1}(x)) = x$. If the AI made an error, identify where and why. If it was correct, identify which step was most likely to go wrong and explain what a student would have to understand to catch that error.

**Exercise 3-L4.** Describe to an AI a function that is odd but not one-to-one, and ask whether its inverse exists. Then ask the same about a function that is one-to-one but neither even nor odd. Evaluate whether the AI correctly applies the one-to-one requirement (not the even/odd symmetry) as the criterion for invertibility. Write a paragraph summarizing what the AI got right and where it conflated the two ideas, if it did.

**Exercise 3-L5.** Ask an AI to give you a real-world situation that is *not* a function, explain why it is not, and then show how you could modify the situation so it becomes a function. Evaluate the response: does the modification genuinely restore the one-output-per-input property, or does it just restate the original situation with different words?

---

## AI Wayback Machine

**Leonhard Euler** introduced the modern function notation *f(x)* in 1734 — and built much of the theory of functions in the 1740s. His notation is so successful that we rarely notice it.

**Run this:**

```
Who was Leonhard Euler, and how does his work on functions connect to what we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Leonhard Euler"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to list five other pieces of standard mathematical notation we owe to Euler.
- Ask it about Euler's prolific output despite becoming blind in his later years.

What changes? What gets better? What gets worse?
