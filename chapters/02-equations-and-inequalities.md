# Chapter 2 — Equations and Inequalities

*What it means to find the number that makes a sentence true.*

---

## The tollbooth problem

Here is something that happens every day on the New Jersey Turnpike. A driver pulls up to the booth, the display reads $\$8.50$, they hand over a ten-dollar bill, and $\$1.50$ slides back. Nobody solves an equation consciously. But that's exactly what happened. There was a number nobody knew yet — the change — and a relationship that pinned it down: *the change plus the toll equals the bill*. In symbols:

$$x + 8.50 = 10$$

<!-- → [IMAGE: photograph or line illustration of a toll booth display showing $8.50 and a hand extending a $10 bill — anchors the abstract equation to the physical situation the reader just read about] -->

The answer is $x = 1.50$. Done.

I want to spend this chapter on that move — taking a relationship you can describe in words, writing it in symbols, and finding the number (or numbers, or range of numbers) that make it true. That's all solving an equation is. The drama you may have heard about — completing the square, the quadratic formula, interval notation — is just the same idea applied to relationships that are harder to describe than a toll booth.

Three families of equations. Three families of techniques. One organizing question throughout: *what value of the unknown makes this sentence true?*

---

## Part 1 — Linear equations: one unknown, one power

A *linear equation* has the form $ax + b = c$, where the unknown appears once, to the first power, multiplied by something, and set equal to something. The unknown might be change owed, or miles driven, or years since 1990. The form is the same.

Solving means undoing. If $3x + 7 = 22$, then something was done to $x$ — it was multiplied by 3, then 7 was added. Undo those operations in reverse:

$$\begin{aligned}
3x + 7 &= 22 \\
3x &= 15 && \text{subtract 7 from both sides} \\
x &= 5 && \text{divide both sides by 3}
\end{aligned}$$

The legitimacy of each step is one idea: *equality is preserved when you do the same thing to both sides*. Not "almost preserved." Not "preserved if you're careful." Preserved, exactly, every time, as long as you do the same operation to both sides.

<!-- → [INFOGRAPHIC: two-column "balance scale" diagram showing $3x + 7 = 22$ as a balanced scale, then each operation (subtract 7, divide by 3) applied to both pans simultaneously — the scale stays balanced at each step; student should see why doing the same thing to both sides is the only valid move] -->

Check: $3(5) + 7 = 22$. Yes. Checking is not optional ceremony — it's the only way to know you didn't make an arithmetic slip somewhere in the middle.

### The variable on both sides

When the unknown appears on both sides, move the variable terms to one side first, then proceed.

$$\begin{aligned}
4x - 3 &= 7x + 9 \\
-12 &= 3x && \text{subtract } 4x \text{ and } 9 \text{ from both sides} \\
x &= -4
\end{aligned}$$

Nothing here is new. The structure is the same: undo operations, isolate $x$.

### Rational equations

Sometimes the unknown is in a denominator:

$$\frac{x}{2} + \frac{x-1}{3} = 4$$

The fractions look like a complication. They aren't — they're an invitation to multiply. Multiply every term by the least common denominator, which here is 6, and the fractions disappear:

$$3x + 2(x - 1) = 24 \implies 5x = 26 \implies x = \frac{26}{5}$$

One warning worth memorizing: when the denominator contains the unknown, multiplying by it can introduce *extraneous solutions* — values of $x$ that satisfy the transformed equation but make a denominator zero in the original. After solving any rational equation, substitute back and check. Any candidate that makes a denominator zero is not a solution.

### The word problem is really a translation problem

Here is a car rental contract: $\$30$ flat fee per day, plus $\$0.20$ per mile. Budget: $\$120$ for one day. How far can the driver go?

Let $m$ = miles. The cost is $30 + 0.20m$. Set it equal to the budget:

$$30 + 0.20m = 120 \implies 0.20m = 90 \implies m = 450 \text{ miles}$$

The arithmetic is trivial. The work — reading "thirty dollars flat plus twenty cents a mile" and writing $30 + 0.20m$ — is where most mistakes happen. Translation is the skill. Once you have the equation, the mechanics are just undoing operations.

### What linear models can and can't do

A linear equation captures relationships where the unknown enters once, to the first power, with no products of itself. Most real relationships are linear *over small ranges* and nonlinear over larger ones. The dollar-per-mile rate on a rental car is constant; real fuel costs aren't. Linear equations are first approximations — they're the simplest thing that might work, and often they do. When they don't, the next section introduces what's needed.

---

## Part 2 — Quadratic equations: when the unknown is squared

A baseball leaves a bat at some angle. You want to know when it hits the ground. The height as a function of time is

$$h(t) = -16t^2 + v_0 t + h_0$$

where $v_0$ is the initial vertical velocity and $h_0$ is the starting height. Setting $h = 0$ asks: *when does the ball hit the ground?* The answer is a quadratic equation. The same form appears in orbit calculations, in the geometry of parabolas, in any situation where the thing you're studying is proportional to the square of something.

A *quadratic equation* in standard form:

$$ax^2 + bx + c = 0, \quad a \neq 0$$

There are four methods for solving it. They are not equally useful in all situations.

<!-- → [TABLE: decision guide for quadratic method selection — columns: method name, when to use it, when NOT to use it, example equation type; rows: factoring, square-root property, completing the square, quadratic formula — student should use this as a quick-reference flowchart before solving any quadratic] -->

### Factoring

If you can write $ax^2 + bx + c$ as a product of two linear factors — say, $(x - r)(x - s)$ — then the *zero-product property* finishes the job: a product is zero if and only if at least one factor is zero.

$$x^2 - 5x + 6 = 0 \implies (x - 2)(x - 3) = 0 \implies x = 2 \text{ or } x = 3$$

Factoring is fast when it works. The catch: most quadratics you encounter outside a textbook don't have integer roots, and trial-and-error factoring is slow or impossible. Use factoring first; when it doesn't yield quickly, move to a more powerful method.

### The square-root property

If the equation is already a perfect square equal to a constant — $(x - h)^2 = k$ — take the square root of both sides. Both $+\sqrt{k}$ and $-\sqrt{k}$ are solutions.

$$(x - 3)^2 = 16 \implies x - 3 = \pm 4 \implies x = 7 \text{ or } x = -1$$

This method is fast but requires the equation to already be in the right shape. When it isn't, completing the square can put it there.

### Completing the square

Take $x^2 + bx$ and add $\left(\frac{b}{2}\right)^2$ to it. Why? Because

$$x^2 + bx + \left(\frac{b}{2}\right)^2 = \left(x + \frac{b}{2}\right)^2$$

You've made a perfect square — deliberately, by adding a specific number. The price is that you must add the same number to the other side to preserve equality.

$$\begin{aligned}
x^2 + 6x - 7 &= 0 \\
x^2 + 6x &= 7 \\
x^2 + 6x + 9 &= 16 && \text{add } (6/2)^2 = 9 \text{ to both sides} \\
(x + 3)^2 &= 16 \\
x + 3 &= \pm 4 \\
x &= 1 \text{ or } x = -7
\end{aligned}$$

Completing the square always works — not just when the roots are integers. It's also the proof behind the quadratic formula: apply the same steps to the general case $ax^2 + bx + c = 0$, and the formula falls out.

### The quadratic formula

For any quadratic $ax^2 + bx + c = 0$:

$$\boxed{x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}}$$

This is completing the square, done once, in symbols, so you don't have to do it again. Memorize it. Not because memorizing things is virtuous, but because you'll use it often enough that having to derive it every time is genuinely slow.

$$2x^2 - 7x + 3 = 0 \quad (a = 2, b = -7, c = 3)$$

$$x = \frac{7 \pm \sqrt{49 - 24}}{4} = \frac{7 \pm 5}{4} \implies x = 3 \text{ or } x = \frac{1}{2}$$

### The discriminant tells you what to expect

The expression under the square root, $b^2 - 4ac$, is called the *discriminant*. Before finishing a computation, compute this first:

- $b^2 - 4ac > 0$: two distinct real solutions
- $b^2 - 4ac = 0$: one repeated solution
- $b^2 - 4ac < 0$: no real solutions — but two complex ones

<!-- → [IMAGE: three side-by-side parabolas (all opening upward) — left parabola crosses x-axis at two points (discriminant > 0), center parabola touches x-axis at exactly one point (discriminant = 0), right parabola floats entirely above x-axis (discriminant < 0); each labeled with its discriminant case; student should see the geometric meaning of each case before reading the complex-numbers section] -->

The third case deserves its own treatment.

### When the discriminant is negative: complex numbers

Apply the formula to $x^2 + 2x + 5 = 0$:

$$x = \frac{-2 \pm \sqrt{4 - 20}}{2} = \frac{-2 \pm \sqrt{-16}}{2}$$

The square root of a negative number. Real numbers don't include this. So mathematicians extended the system.

Define $i = \sqrt{-1}$, so $i^2 = -1$. A *complex number* is any expression $a + bi$ where $a$ and $b$ are real. The arithmetic of complex numbers mirrors polynomial arithmetic, with one substitution rule: wherever $i^2$ appears, replace it with $-1$.

**Addition:** $(a + bi) + (c + di) = (a + c) + (b + d)i$.

**Multiplication:** $(a + bi)(c + di) = ac + adi + bci + bdi^2 = (ac - bd) + (ad + bc)i$.

**Division:** multiply numerator and denominator by the *conjugate* of the denominator — if the denominator is $c + di$, its conjugate is $c - di$. The product of a complex number and its conjugate is always real: $(c + di)(c - di) = c^2 + d^2$.

Returning to the equation: $\sqrt{-16} = 4i$, so

$$x = \frac{-2 \pm 4i}{2} = -1 \pm 2i$$

The two solutions are $-1 + 2i$ and $-1 - 2i$. When a real-coefficient quadratic has complex roots, they always come in *conjugate pairs* — one with $+bi$, one with $-bi$. This is a structural fact, not a coincidence.

A natural question is whether complex numbers are "real" in any meaningful sense. They were called "fictitious" for centuries. Negative numbers were once described the same way. The test isn't whether they correspond to something you can hold in your hand; it's whether the rules of arithmetic are consistent and whether the system is useful. Complex numbers underlie quantum mechanics, signal processing, and alternating-current electrical engineering. They're real enough.

### A note on method choice

The four methods aren't in competition. Factoring is fastest when the roots are rational; use it first as a quick test. The square-root property applies when you already have a perfect square. Completing the square is for when you don't, and it always works. The quadratic formula is what completing the square gives you when you do it symbolically rather than numerically — it's the general-purpose fallback when the other methods stall.

---

## Part 3 — Inequalities: when the answer is a range

So far every equation has asked: *what single value makes this true?* But some questions have ranges as answers. A toll road is free for vehicles under 26,000 pounds; a medication is safe in doses between 200 mg and 800 mg per day; a structural beam must support loads between 1,000 and 5,000 pounds. The answer to these questions is not a number — it's a set of numbers.

An *inequality* is a statement using $<$, $\leq$, $>$, or $\geq$ instead of $=$. Solving means finding the set of values that make the statement true.

### Interval notation

A range of real numbers is most compactly written in *interval notation*. The conventions:

- $(a, b)$: all real numbers strictly between $a$ and $b$ — endpoints excluded
- $[a, b]$: all real numbers between $a$ and $b$ — endpoints included
- $[a, b)$: includes $a$, excludes $b$
- $(a, \infty)$: all real numbers greater than $a$; infinity is always written with an open parenthesis because it's a direction, not a number

So "$x$ is at least $-2$ and strictly less than $5$" writes as $[-2, 5)$.

<!-- → [INFOGRAPHIC: number line showing five interval-notation examples side by side — $(a,b)$ with open circles, $[a,b]$ with closed circles, $[a,b)$ mixed, $(a, \infty)$ with arrow, $(-\infty, \infty)$ full line; each labeled with its notation and plain-English meaning; student should have this as a reference when first reading interval answers] -->

### Solving linear inequalities

The technique is the same as for linear equations — isolate the variable — with one critical difference.

Multiplying or dividing both sides by a *negative number* reverses the inequality.

Why? Consider $2 < 5$. Multiply by $-1$: $-2 > -5$. The original order flipped. On the number line, multiplying by a negative reflects everything through zero, and reflections reverse the order of points.

<!-- → [IMAGE: number line showing $2$ and $5$ with an arrow indicating "multiply by $-1$" and the resulting positions $-2$ and $-5$, with the inequality sign explicitly flipping direction; the reflection through zero should be visually clear — this is the one rule students consistently forget and a picture cements why it's true] -->

$$5 - 2x \geq 11 \implies -2x \geq 6 \implies x \leq -3$$

The flip on the last step is not optional. Forgetting it is the single most common error in working with inequalities.

In interval notation: $(-\infty, -3]$.

### Compound inequalities

A *compound inequality* combines two. The two cases:

**Intersection ("and"):** both conditions must hold simultaneously. Written as a chain: $a < x < b$, meaning $x > a$ *and* $x < b$.

**Union ("or"):** either condition is sufficient. Written separately: $x < a$ or $x > b$.

To solve a chain inequality, apply the same operations to all three parts simultaneously:

$$-1 \leq 3x + 2 < 8 \implies -3 \leq 3x < 6 \implies -1 \leq x < 2$$

In interval notation: $[-1, 2)$.

### Absolute-value inequalities

The absolute value $|x|$ is the *distance* of $x$ from zero. This geometric reading makes the inequality rules easy to see.

$|x| < 3$ means: all $x$ within distance 3 of zero. That's $-3 < x < 3$.

$|x| > 3$ means: all $x$ farther than distance 3 from zero. That's $x < -3$ or $x > 3$.

<!-- → [IMAGE: number line with zero at center — two diagrams stacked: top shows $|x| < 3$ with a shaded interval between $-3$ and $3$ (the "within distance 3" region); bottom shows $|x| > 3$ with shading on both outer rays beyond $-3$ and $3$ (the "farther than distance 3" regions); student should see why one case is an intersection and the other is a union before reading the formula] -->

In general:

$$|x| < a \iff -a < x < a$$
$$|x| > a \iff x < -a \text{ or } x > a$$

**Example.** Solve $|2x - 1| \leq 5$.

Translate: the distance of $2x - 1$ from zero is at most 5. So:

$$-5 \leq 2x - 1 \leq 5 \implies -4 \leq 2x \leq 6 \implies -2 \leq x \leq 3$$

In interval notation: $[-2, 3]$.

### Other equations that reduce to the same families

Some equations look unfamiliar but collapse into familiar form.

**Radical equations** have the variable inside a radical. Isolate the radical, then raise both sides to the appropriate power. The hazard: raising both sides to an even power can introduce extraneous solutions. Check every candidate.

$$\sqrt{x + 5} = x - 1 \implies x + 5 = (x-1)^2 = x^2 - 2x + 1 \implies x^2 - 3x - 4 = 0 \implies (x-4)(x+1) = 0$$

Candidates: $x = 4$ or $x = -1$. Check $x = 4$: $\sqrt{9} = 3$ and $4 - 1 = 3$. ✓  
Check $x = -1$: $\sqrt{4} = 2$ and $-1 - 1 = -2$. ✗  

Only $x = 4$ is a solution.

**Rational-exponent equations.** $x^{2/3} = 4$ — raise both sides to the $3/2$ power: $x = 4^{3/2} = (4^3)^{1/2} = 64^{1/2} = 8$.

**Absolute-value equations.** $|x - 3| = 5$ — the distance from $x$ to $3$ is exactly $5$, so $x = 8$ or $x = -2$.

---

## Putting it together: a garden, all at once

A homeowner wants a rectangular garden against the back wall of the house. Three sides of fencing, $40$ feet total. The house forms the fourth side. Let $x$ = the length of the sides running perpendicular to the house.

**Setting up the relationship.** The two perpendicular sides use $2x$ feet of fencing. The parallel side gets $40 - 2x$ feet. The area is:

$$A = x(40 - 2x) = 40x - 2x^2$$

**Where is the area maximized?** This is a question about the vertex of a downward-opening parabola. Complete the square:

$$A = -2x^2 + 40x = -2(x^2 - 20x) = -2(x^2 - 20x + 100) + 200 = -2(x - 10)^2 + 200$$

The maximum occurs when $(x - 10)^2 = 0$, i.e., $x = 10$. Maximum area: $200$ square feet. Dimensions: $10$ ft perpendicular, $20$ ft parallel.

**For what range of $x$ does the area exceed 150 square feet?** Now it's an inequality.

$$40x - 2x^2 > 150 \implies -2x^2 + 40x - 150 > 0 \implies x^2 - 20x + 75 < 0$$

Dividing by $-2$ flipped the inequality. Factor the left side:

$$(x - 5)(x - 15) < 0$$

The product is negative when the two factors have opposite signs. That happens when $5 < x < 15$. In interval notation: $(5, 15)$.

So: the homeowner gets more than 150 square feet of garden when the perpendicular dimension is between 5 and 15 feet. The sweet spot — the maximum — is at exactly 10 feet. The same piece of land, the same fence, described three ways: as an algebraic expression, as a quadratic extremum, as an inequality with a range solution. All three descriptions are about the same situation. The different forms exist because we asked different questions.

<!-- → [IMAGE: two-panel figure — left panel: top-down diagram of the rectangular garden with the house as one wall, the two perpendicular sides labeled $x$, and the parallel side labeled $40-2x$; right panel: downward-opening parabola $A = 40x - 2x^2$ with vertex marked at $(10, 200)$, zeros at $x=0$ and $x=20$, horizontal dashed line at $A=150$ intersecting the curve at $x=5$ and $x=15$, and the interval $(5,15)$ shaded on the x-axis — student should see the geometry, the algebra, and the inequality solution all in one picture] -->

That's the honest summary of this chapter. One question: what value makes this sentence true? Three sentence types — linear, quadratic, inequality — each requiring its own set of moves, all driven by the same organizing idea: *undo what was done to the unknown until it stands alone*.

---

## LLM Exercises

The following prompts are designed for extended engagement with a large language model. Use them to deepen your intuition, test the edges of the techniques, and generate your own practice problems. Treat the LLM's responses as starting points for your own reasoning — verify, push back, and request derivations, not just answers.

---

**LLM Exercise 2-A.** Ask the LLM to generate five linear word problems of increasing difficulty: one involving a flat fee and per-unit cost, one involving two people's ages, one involving mixing two solutions to hit a target concentration, one involving a rate-time-distance problem, and one that requires setting up two linear equations (even though you only know Chapter 2 linear tools — ask it to design one that reduces to a single equation). For each problem, write out the translation step explicitly — English sentence to algebraic expression — before solving. Compare your translations to the LLM's.

---

**LLM Exercise 2-B.** Ask the LLM: *"Give me a quadratic equation for which (a) factoring over the integers is fast, (b) factoring over the integers is impossible but the quadratic formula gives rational roots, and (c) the quadratic formula gives irrational roots. For each, show me all four methods and explain which is most efficient and why."* Work through each example yourself before reading the LLM's explanation. Note where your efficiency judgments agree or disagree.

---

**LLM Exercise 2-C.** Ask the LLM to walk you through the derivation of the quadratic formula from scratch — starting with $ax^2 + bx + c = 0$ and arriving at $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$ by completing the square, one step at a time. After it does, reproduce the derivation yourself on paper without looking. Then ask the LLM: *"What does the discriminant tell us geometrically, in terms of where the parabola $y = ax^2 + bx + c$ intersects the $x$-axis?"* Sketch a parabola for each of the three discriminant cases.

---

**LLM Exercise 2-D.** Ask the LLM to generate a quadratic inequality problem — something like *"a ball thrown upward is above 30 feet for what time interval?"* — and walk you through solving it step by step. Then ask it to generate three more, each with a different structure: one where the solution is a union of two intervals, one where it's a single closed interval, and one where the solution is all real numbers (ask it to explain why that can happen). Work each problem yourself before reading the solution.

---

**LLM Exercise 2-E.** Ask the LLM: *"I want to understand extraneous solutions. Generate three radical equations — one where squaring introduces exactly one extraneous solution, one where it introduces two, and one where it introduces none. For each, explain geometrically or algebraically why the extraneous solution appeared."* After reading the explanations, ask a follow-up: *"When I clear denominators in a rational equation, am I at risk of the same phenomenon? Why or why not?"*

---

**LLM Exercise 2-F.** Describe the fencing optimization problem in this chapter to the LLM (homeowner, 40 feet of fencing, garden against the house). Ask it to: (a) solve it by completing the square, (b) solve it by calculus (derivative = 0) if you want a preview of where this goes, (c) explain why the maximum always occurs when the parallel side is twice the perpendicular side. Then vary the problem — 60 feet of fencing, or fencing on all four sides with a budget — and work the variations yourself before asking the LLM to check your setup.

---

## AI Wayback Machine

**Diophantus of Alexandria** wrote *Arithmetica* around 250 CE — the first systematic treatment of equations and unknowns. He invented much of the notation that classical algebra eventually formalized.

**Run this:**

```
Who was Diophantus of Alexandria, and how does his work on equations connect to what we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Diophantus"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to solve one of Diophantus's *Arithmetica* problems in modern notation.
- Ask it about the famous riddle of Diophantus's age (the epitaph problem) — and whether it's plausibly autobiographical.

What changes? What gets better? What gets worse?
