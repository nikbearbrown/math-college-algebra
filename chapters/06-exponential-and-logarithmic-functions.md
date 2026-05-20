# Chapter 6 — Exponential and Logarithmic Functions

*The chapter where multiplication becomes addition, and time becomes the unknown.*

---

A radioactive sample sits in a Geiger counter at noon. The counter reads 1,000 counts per second. At 1 PM it reads 750. At 2 PM, 562. At 3 PM, 422.

Look at those numbers for a moment before we name anything. The drop from noon to 1 PM is 250. From 1 PM to 2 PM, it's 188. From 2 PM to 3 PM, 140. The decreases are shrinking. Whatever is happening here, it is not the kind of decay where a fixed amount disappears each hour. The amount disappearing each hour depends on how much is still there.

That is the key. The rate of change is proportional to the current value. When there is more, more decays. When there is less, less decays. This is a fundamentally different relationship from anything in the previous chapters, and it produces a fundamentally different kind of function.

---

## The function that grows by multiplying

Go back to the data. From noon to 1 PM, the count was multiplied by $0.75$ — it kept 75% of itself. From 1 PM to 2 PM, multiplied by $0.75$ again. From 2 PM to 3 PM, again. Each hour, the same *ratio*.

After $t$ hours:

$$N(t) = 1000 \cdot (0.75)^t$$

This is an *exponential function*. The general form is $f(x) = a \cdot b^x$, where $a$ is the starting value and $b$ is the base — the multiplier applied once per unit of input.

If $b > 1$, the function grows: each step multiplies by something bigger than 1. If $0 < b < 1$, it decays: each step multiplies by a fraction. The condition $b > 0$ and $b \neq 1$ is not arbitrary restriction — a negative base produces oscillations that break the smooth curve, and $b = 1$ gives $f(x) = a$ always, which is constant, not exponential.

The critical feature: this function is not a line, not a polynomial, not anything from the previous chapters. Plot it. From $t = 0$ to $t = 10$, the count drops from 1,000 to about 56. From $t = 10$ to $t = 20$, it drops from 56 to about 3. The curve flattens but never reaches zero — it approaches zero asymptotically, always positive, always decreasing, never arriving.

For growth, the picture reverses. Bacteria doubling every hour: $P(t) = 500 \cdot 2^t$. Start with 500. After 10 hours, 512,000. After 20 hours, 524 million. The function accelerates. A straight line grows by a fixed amount per step; an exponential grows by a fixed *factor* per step. Over long enough time, any exponential growth overtakes any polynomial growth. This is not an approximation — it is exact.

<!-- → [IMAGE: two side-by-side graphs on the same axes — left: N(t) = 1000·(0.75)^t showing decay curving toward the horizontal asymptote y = 0; right: P(t) = 500·2^t showing growth accelerating away from the x-axis — student should see that both curves approach an asymptote, just on opposite ends, and neither is a line] -->

### The base that keeps appearing

There is a particular base that shows up constantly in mathematics, science, and finance. It is called $e$, and it is approximately $2.71828$.

Where does it come from? Ask what happens when you compound interest more and more frequently. Start with a dollar at 100% annual interest. Compound once per year: you end with \$2. Compound twice per year at 50% each: $\$(1.5)^2 = \$2.25$. Compound twelve times: about \$2.613. Compound continuously — in the limit as compounding frequency goes to infinity:

$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n \approx 2.71828$$

The number $e$ is what continuous compounding converges to. But its significance goes deeper than finance. The function $f(x) = e^x$ has a property that no other exponential function has: its rate of change at every point equals its value there. The slope of the curve at any $x$ is exactly $e^x$. This is why calculus is dramatically cleaner with base $e$ — when you differentiate $e^x$, you get $e^x$ back. Any other base introduces a correction factor. We will not prove this here, but it is the reason $e$ is the natural base.

<!-- → [TABLE: three-column table showing compounding frequency (annually, quarterly, monthly, daily, continuously), the formula applied, and the resulting value after 1 year starting from $1 at 100% — the final row shows e ≈ 2.71828; student should see the sequence converging and understand where the limit comes from] -->

### What compound interest is actually doing

A deposit of $P$ dollars at annual rate $r$, compounded $n$ times per year, grows to

$$A = P\left(1 + \frac{r}{n}\right)^{nt}$$

after $t$ years. As $n \to \infty$ — continuous compounding — this becomes

$$A = Pe^{rt}$$

Deposit \$1,000 at 5% compounded monthly for 10 years: $A = 1000(1 + 0.05/12)^{120} \approx \$1,647$. Compounded continuously: $A = 1000 e^{0.5} \approx \$1,649$. The difference is small. The formula is cleaner. And the continuous version connects to the natural exponential in a way that pays dividends later.

The question that compound interest makes urgent: how long to double? If you set $2P = Pe^{rt}$, the $P$ cancels, and you get $2 = e^{rt}$. To solve that equation, you need to invert the exponential. That is precisely what logarithms do.

---

## The inverse: given the output, find the exponent

You know $2^3 = 8$. The logarithm asks the reverse: given that $2$ to some power equals $8$, what is that power? The answer is $3$. Written in logarithm notation: $\log_2(8) = 3$.

The definition is just this:

$$\log_b(y) = x \iff b^x = y$$

The logarithm and the exponential are inverses of each other. $\log_b(b^x) = x$ for any $x$. $b^{\log_b(y)} = y$ for any $y > 0$. They undo each other exactly.

Two bases appear so often that they have their own notation. The common logarithm, $\log(x)$, means base 10 — the base of our number system, useful for orders of magnitude. The natural logarithm, $\ln(x)$, means base $e$ — the base of continuous growth and decay.

Some values to internalize:

- $\log_{10}(10) = 1$, $\log_{10}(100) = 2$, $\log_{10}(1000) = 3$. Each additional digit in a number adds 1 to its base-10 logarithm.
- $\log_{10}(1) = 0$ (because $10^0 = 1$).
- $\ln(e) = 1$, $\ln(e^2) = 2$, $\ln(1) = 0$.

The logarithm is undefined for inputs $\leq 0$. There is no exponent you can put on a positive base to get zero or a negative number. This is not a technicality to memorize — it follows directly from the behavior of $b^x$, which is always positive.

### The graph

The graph of $y = \log_b(x)$ for $b > 1$ is the graph of $y = b^x$ reflected across the line $y = x$ — the geometric meaning of "inverse function." It passes through $(1, 0)$, increases slowly, has a vertical asymptote at $x = 0$, and has domain $(0, \infty)$.

How slowly? $\log_{10}(1{,}000{,}000) = 6$. $\log_{10}(1{,}000{,}000{,}000) = 9$. The output grows by 3 when the input multiplies by $1{,}000$. This is logarithmic growth — the opposite extreme from exponential. Exponential functions grow shockingly fast; logarithms grow shockingly slowly. Together, they bound the behavior of everything in between.

<!-- → [IMAGE: graph of y = 2^x and y = log₂(x) on the same axes, with the line y = x drawn as a dashed reference — the two curves are mirror images across y = x, intersecting at (1,1) and (2,2); student should see the reflection relationship that defines inverse functions geometrically and notice the contrasting rates: one accelerates away, the other barely climbs] -->

---

## The rules, and where they come from

There are four rules for manipulating logarithms. They are not arbitrary — they are the exponent rules in disguise.

**Product rule.** $\log_b(MN) = \log_b(M) + \log_b(N)$.

Here is why. Let $\log_b(M) = p$ and $\log_b(N) = q$. Then $M = b^p$ and $N = b^q$, so $MN = b^p \cdot b^q = b^{p+q}$. Taking the log of both sides: $\log_b(MN) = p + q = \log_b(M) + \log_b(N)$.

Multiplication becomes addition. This is why logarithms transformed science before calculators existed — multiplying large numbers is hard, adding their logarithms is easy, and converting back is straightforward.

**Quotient rule.** $\log_b(M/N) = \log_b(M) - \log_b(N)$. Same reasoning: division becomes subtraction.

**Power rule.** $\log_b(M^p) = p \cdot \log_b(M)$. Because $M^p = (b^{\log_b(M)})^p = b^{p \cdot \log_b(M)}$, and taking the log gives $p \cdot \log_b(M)$.

This is the rule that unlocks exponential equations. When the unknown is an exponent, the power rule brings it down to the level of multiplication.

**Change of base.** $\log_b(M) = \frac{\ln(M)}{\ln(b)}$.

Calculators have buttons for $\ln$ and $\log_{10}$. They do not have a button for $\log_7$. The change-of-base formula converts any logarithm to one your calculator can evaluate.

One warning worth stating explicitly: $\log(a + b) \neq \log(a) + \log(b)$. The product rule says $\log(ab) = \log(a) + \log(b)$ — multiplication inside becomes addition outside. Addition inside has no simplification. Confusing these is the most common error in this chapter.

<!-- → [TABLE: two-column table mapping each exponent rule to its logarithm counterpart — left column: b^m · b^n = b^(m+n), b^m / b^n = b^(m−n), (b^m)^p = b^(mp); right column: log(MN) = log M + log N, log(M/N) = log M − log N, log(M^p) = p·log M — student should see that the log rules are not new facts but the same facts read from the other direction] -->

---

## Solving equations

With the rules established, two types of equations become tractable.

### Exponential equations

The unknown is in the exponent. Two strategies.

**When both sides can share a base**, equate the exponents directly.

$2^{3x} = 16$. Rewrite: $2^{3x} = 2^4$. Same base on both sides, so $3x = 4$, giving $x = 4/3$.

**When they cannot**, take the natural log of both sides and apply the power rule.

$5^x = 12$. Take $\ln$: $\ln(5^x) = \ln(12)$. Power rule: $x \ln(5) = \ln(12)$. Divide: $x = \ln(12)/\ln(5) \approx 1.544$.

The second strategy always works. The first strategy works only when you can recognize a common base, but when it works, it is faster.

### Logarithmic equations

The unknown is inside a logarithm. Combine any multiple logarithms using the product, quotient, or power rules until one logarithm remains, then convert to exponential form.

$\log_2(x) + \log_2(x - 2) = 3$. Product rule: $\log_2(x(x-2)) = 3$. Convert: $x(x-2) = 2^3 = 8$. Expand: $x^2 - 2x - 8 = 0$. Factor: $(x-4)(x+2) = 0$.

Two candidates: $x = 4$ and $x = -2$. Check both in the original. $\log_2(-2)$ is undefined — you cannot take the logarithm of a negative number. So $x = -2$ is *extraneous*, introduced by the algebra but not valid in the original equation. Only $x = 4$ works.

Extraneous solutions are routine in logarithmic equations, not exceptional. Always check every candidate.

### The doubling time question

How long does it take \$1,000 at 6% continuous compounding to double?

$$2000 = 1000 \, e^{0.06t}$$
$$2 = e^{0.06t}$$
$$\ln 2 = 0.06t$$
$$t = \frac{\ln 2}{0.06} \approx 11.55 \text{ years}$$

Notice that the initial amount $P$ cancelled immediately. The doubling time depends only on the rate, not the principal. This is a feature of exponential growth: the time to multiply by any fixed factor is constant.

The *Rule of 72* is a practical approximation: doubling time $\approx 72/r$, where $r$ is the percentage rate. At 6%, that gives $72/6 = 12$ years — close enough for mental arithmetic.

---

## Building models from data

The most important application is often this: you observe a process, take measurements, and need to find the model that fits.

A petri dish starts with 500 bacteria. After 4 hours, there are 1,500. Build a model.

The form is $P(t) = 500 \, e^{kt}$ — we know the starting value, but not $k$. Plug in the known data point:

$$1500 = 500 \, e^{4k}$$
$$3 = e^{4k}$$
$$\ln 3 = 4k$$
$$k = \frac{\ln 3}{4} \approx 0.275$$

Model: $P(t) = 500 \, e^{0.275t}$.

Now we can answer forward-looking questions. When does the count reach 10,000?

$$10000 = 500 \, e^{0.275t}$$
$$20 = e^{0.275t}$$
$$\ln 20 = 0.275 t$$
$$t = \frac{\ln 20}{0.275} \approx 10.9 \text{ hours}$$

The same model also lets us look backward: when did the culture have only 100 bacteria? Set $100 = 500 e^{0.275t}$, get $t = \ln(0.2)/0.275 \approx -5.8$ hours. The negative sign says 5.8 hours before the measurement, which makes sense — the culture was smaller then.

<!-- → [IMAGE: graph of P(t) = 500·e^(0.275t) from t = −6 to t = 12, with three points labeled: (−5.8, 100), (0, 500), (4, 1500), and (10.9, 10000) — student should see that the same curve answers backward-looking and forward-looking questions equally, and that finding k from one data point pins the entire curve] -->

### Radioactive decay

Carbon-14 has a half-life of 5,730 years — after that many years, half the original remains. From this single fact, we can find $k$.

$$\frac{1}{2} A_0 = A_0 \, e^{5730k}$$
$$\frac{1}{2} = e^{5730k}$$
$$\ln\!\left(\tfrac{1}{2}\right) = 5730k$$
$$k = \frac{-\ln 2}{5730} \approx -0.000121$$

A bone fragment retains 30% of its original carbon-14. How old?

$$0.3 = e^{-0.000121 \, t}$$
$$\ln(0.3) = -0.000121 \, t$$
$$t = \frac{\ln(0.3)}{-0.000121} \approx 9{,}953 \text{ years}$$

The mathematics is the same structure each time: identify the exponential model, substitute a known condition to find the rate constant, then solve the resulting equation for whatever you want. The only variation is in the numbers and what question is being asked.

### When exponential growth stops

Exponential growth cannot continue forever — resources run out, space fills up, something intervenes. When a population grows toward a ceiling, the logistic model applies:

$$P(t) = \frac{c}{1 + a e^{-bt}}$$

Here $c$ is the *carrying capacity* — the ceiling the population approaches. Initially, when $t$ is small and $ae^{-bt}$ is large, $P$ is small and growing fast. As $t$ grows, $e^{-bt} \to 0$ and $P \to c$. The graph is S-shaped: slow growth, then rapid growth, then leveling off.

The logistic model describes real populations more accurately than pure exponential growth. A bacterial culture in a flask, a species colonizing an island, a technology spreading through a market — all follow logistic curves when the underlying resource is finite. The exponential is what you get when you look at the early part of the S-curve, before the ceiling becomes visible.

<!-- → [IMAGE: S-shaped logistic curve P(t) = c/(1 + ae^(−bt)) with the carrying capacity c marked as a horizontal dashed asymptote at the top and the inflection point (where growth is fastest) marked — overlaid on the left portion, a dashed exponential curve showing how pure exponential growth matches the logistic curve early but diverges wildly as t grows; student should see that the exponential is an approximation that breaks when the ceiling comes into view] -->

---

## What the two functions are actually doing

Exponential and logarithmic functions are inverses, but it is worth understanding what each one captures conceptually.

An exponential function $f(x) = b^x$ encodes *repeated multiplication*. The input is a count of steps; the output is the result of multiplying by $b$ that many times. The function scales up (or down) geometrically. Every equal increment of input corresponds to the same proportional change in output.

A logarithm inverts this: given the result, find the count of steps. This is why logarithms compress large ranges. The numbers $1$, $10$, $100$, $1{,}000$, $10{,}000$ span five orders of magnitude — they differ by factors of 10. Their base-10 logarithms are $0$, $1$, $2$, $3$, $4$ — equally spaced. The logarithm converts multiplicative structure into additive structure. This is useful not just computationally but perceptually: earthquake magnitudes, sound intensities, star brightnesses, and pH all use logarithmic scales because human perception is roughly logarithmic. A sound twice as loud does not sound twice as loud; a sound ten times as intense sounds about twice as loud.

The rules of logarithms are not tricks to memorize. They are consequences of one fact: logarithms and exponentials are inverses, and the exponent rules drive everything. If you understand why $b^m \cdot b^n = b^{m+n}$, you understand why $\log_b(MN) = \log_b(M) + \log_b(N)$. The second statement is the first statement read from the other direction.

---

## What you can do now

You can evaluate exponential functions and sketch their graphs — recognizing growth when $b > 1$, decay when $0 < b < 1$, and the horizontal asymptote at $y = 0$. You can apply the compound-interest formulas, both periodic and continuous. You can convert freely between exponential and logarithmic form. You can expand, condense, and rewrite logarithmic expressions using the product, quotient, and power rules. You can solve both exponential equations (by taking logarithms) and logarithmic equations (by converting to exponential form), and you know to check for extraneous solutions.

Most importantly: you can build a model from two data points, find the rate constant, and use the model to answer questions about the future, the past, or intermediate states.

The single idea connecting all of this: **exponential functions describe processes where the rate of change is proportional to the current amount, and logarithms are the tool for inverting them.** Everything else — the rules, the formulas, the equation-solving strategies — follows from those two facts.

---

## Exercises

### Warm-up

**Exercise 6.1.** *Tests conversion between forms.* Evaluate each without a calculator. (a) $\log_3(81)$. (b) $\log_2(1/8)$. (c) $\ln(e^4)$. (d) $10^{\log(5)}$. For each, write the equivalent exponential or logarithmic statement that makes the answer immediate. Difficulty: low.

**Exercise 6.2.** *Tests reading the exponential model.* A population follows $P(t) = 200 \cdot (1.06)^t$, where $t$ is years. (a) What is the initial population? (b) Is this growth or decay, and by what percentage per year? (c) What is the population after 5 years? Difficulty: low.

**Exercise 6.3.** *Tests the logarithm rules.* Expand each expression into a sum or difference of logarithms with no exponents inside. (a) $\log_2(8x^3)$. (b) $\ln\!\left(\frac{\sqrt{x}}{y^2}\right)$. Difficulty: low.

### Application

**Exercise 6.4.** *Tests solving exponential equations.* Solve for $x$. (a) $3^{2x} = 27$. (b) $4^x = 11$. Give exact answers and decimal approximations. Difficulty: medium.

**Exercise 6.5.** *Tests solving logarithmic equations with extraneous-solution check.* Solve $\log_3(x + 6) + \log_3(x) = 3$. Show all steps and verify that no candidate is extraneous. Difficulty: medium.

**Exercise 6.6.** *Tests the compound-interest formula.* \$5,000 is deposited at 3.5% annual interest. (a) Value after 8 years compounded quarterly. (b) Value after 8 years compounded continuously. (c) How much more does continuous compounding earn? Difficulty: medium.

### Synthesis

**Exercise 6.7.** *Tests building and using an exponential model.* A sample of a radioactive isotope has 800 grams at time zero. After 12 hours, 300 grams remain. (a) Find the exponential decay model $A(t) = A_0 e^{kt}$. (b) What is the half-life of this isotope? (c) When will less than 10 grams remain? Difficulty: medium-high.

**Exercise 6.8.** *Tests the connection between doubling time, the Rule of 72, and exact calculation.* An investment grows at 4% compounded continuously. (a) Find the exact doubling time. (b) Find the Rule-of-72 approximation. (c) Find the time for the investment to grow to five times its original value. For (c), note whether the Rule of 72 still applies and explain why or why not. Difficulty: medium-high.

### Challenge

**Exercise 6.9.** *Tests logistic model interpretation and equation-solving.* A city's population (in thousands) is modeled by $P(t) = \frac{400}{1 + 15e^{-0.08t}}$, where $t$ is years after 2000. (a) What was the population in 2000? (b) What is the carrying capacity, and what does it mean in context? (c) In what year does the population reach 200,000? (d) Is the population growing faster in year 10 or year 30? Explain without computing derivatives — use the shape of the logistic curve and the relationship between the current value and the carrying capacity. Difficulty: high.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 6.1 — Why exponential dominates polynomial.** Tell an LLM: "Eventually $2^x$ overtakes $x^{100}$, and stays ahead forever. At what value of $x$ does this happen, approximately?" Push for an actual estimate, not a hand-wave. Then ask: "Why does any exponential function with base $> 1$ eventually dominate any polynomial?" Force the explanation to use the *multiplicative* nature of exponentials versus the *additive* nature of polynomials. If the LLM says "because exponentials grow faster," push back — that's restating, not explaining.

**LLM Exercise 6.2 — What $\log_b(b) = 1$ actually says.** Ask an LLM: "Why is $\log_b(b) = 1$ for every valid base $b$?" The answer should be: because the log is *defined* as the inverse — $\log_b(b) = 1$ asks "what power of $b$ gives $b$?" and the answer is 1, by definition. Then ask: "Why does $\log_b(1) = 0$ for every base?" Same logic — what power of $b$ gives 1. The point of this exercise is to internalize that logs are *exponents*, not separate operations.

**LLM Exercise 6.3 — The change of base, made physical.** Ask an LLM: "Why does the change-of-base formula $\log_b(x) = \log_c(x) / \log_c(b)$ work?" Push it to derive the formula, not state it. Then ask: "If logarithms are just exponents, why does the calculator have only $\log$ and $\ln$ buttons — what's special about base 10 and base $e$?" The answer should distinguish *historical / engineering convenience* (base 10) from *mathematical naturalness* (base $e$). Probe what makes $e$ "natural."

**LLM Exercise 6.4 — When the model breaks.** Give an LLM this scenario: "A bacterial colony doubles every 20 minutes. After 24 hours starting from 1 cell, how many cells are there?" Have it compute $2^{72}$. Then ask: "Is this answer realistic?" The answer is no — at $2^{72}$ cells the colony's mass would exceed Earth's. Have it estimate when the model breaks down (resource exhaustion, space constraint, predation). The lesson: exponential models are local approximations; they fail when their assumptions fail.

**LLM Exercise 6.5 — Why logs are necessary for solving exponentials.** Tell an LLM: "I want to solve $3 \cdot 2^x = 100$. Why can't I just take the square root, or use any of the techniques that work for polynomials?" Push it to explain *why* the variable in the exponent makes algebraic manipulation insufficient — you cannot "undo" exponentiation without an inverse function. Then ask: "What would mathematics look like if logarithms had never been invented? What problems would be unsolvable?"

---

## AI Wayback Machine

**John Napier** invented logarithms in 1614 — a calculation tool that reduced multiplication of large numbers to addition. His tables revolutionized astronomy and navigation by cutting computation time by a factor of ten.

**Run this:**

```
Who was John Napier, and how do logarithms connect to what we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"John Napier"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through how Napier's original logarithm tables would let an astronomer multiply two large numbers in seconds.
- Ask it about Napier's other inventions, including "Napier's bones" and a hydraulic screw for draining mines.

What changes? What gets better? What gets worse?
