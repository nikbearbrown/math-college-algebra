# Chapter 4 — Linear Functions

## TL;DR

- A Fixed Part, a Rate Part, and Everything Else Follows.
- The chapter moves through The Anatomy of a Line, Three Ways to Write the Same Line, What Slope Really Means, From Words to Equations, and related ideas.
- Read it for the main argument, the vocabulary it introduces, and the practical judgment it asks you to develop.

*A Fixed Part, a Rate Part, and Everything Else Follows.*

In January, a homeowner in Vermont opens a heating bill. It reads: $\$45$ base service charge, plus $\$1.20$ per gallon of oil delivered. She ordered 80 gallons. The bill is $45 + 1.20 \times 80 = \$141$.

That's it. That's the whole chapter.

Everything we are about to do — slope, intercept, point-slope form, parallel lines, lines of best fit, linear models from words — is a consequence of what just happened in that billing formula. The $\$45$ is fixed regardless of how much oil she buys. The $\$1.20$ changes the bill at a constant rate per gallon. Put those two things together — a fixed part and a rate part — and you have a linear function.

The reason linear functions deserve an entire chapter is not that they are complicated. It is that they are *everywhere*, and the world rewards people who can read them fluently. Cell-phone plans. Taxi fares. Wages. Depreciation. Drug dosages. Temperature conversion. Every relationship of the form *fixed amount plus constant rate times variable* is a linear function, and the techniques for working with one are the techniques for working with all of them.

---

## The Anatomy of a Line

A linear function has the form

$$f(x) = mx + b$$

Two numbers. That is the whole specification. Every other property of the line — its slope, its intercepts, its direction, its position in the plane — follows from $m$ and $b$.

The number $b$ is the *$y$-intercept*: the value of $f$ when $x = 0$. In the heating bill, $b = 45$: the bill when no oil is delivered. It is where the line crosses the vertical axis.

The number $m$ is the *slope*: the rate at which $f$ changes per unit of $x$. In the heating bill, $m = 1.20$: every additional gallon adds exactly $\$1.20$ to the bill. The key word is *exactly* — the rate never changes. That constancy is what makes the function linear. If the rate changed — if the first 50 gallons cost $\$1.20$ each and the next 50 cost $\$0.90$ each — the function would not be linear.

Given any two points $(x_1, y_1)$ and $(x_2, y_2)$ on a line, the slope is

$$m = \frac{y_2 - y_1}{x_2 - x_1} = \frac{\Delta y}{\Delta x}$$

![Coordinate plane showing a single line with two](images/04-linear-functions-fig-01.png)
*Figure 4.1 — Coordinate plane showing a single line with two*

*Rise over run.* The vertical change divided by the horizontal change. This ratio is the same no matter which two points on the line you choose — that constancy is precisely what makes the line straight.

A positive slope means the function is increasing: as $x$ grows, $y$ grows. A negative slope means it is decreasing. A slope of zero means it is constant — a horizontal line $y = b$. A *vertical* line has undefined slope: the denominator $\Delta x$ is zero. A vertical line is not a function; it fails the vertical line test.

---

## Three Ways to Write the Same Line

Any line can be expressed in several forms. Each form reveals the same object from a different angle; the skill is knowing which form to reach for.

**Slope-intercept form**: $y = mx + b$. Reach for this when you know the slope and where the line crosses the $y$-axis. It reads directly: slope is the coefficient of $x$, intercept is the constant.

**Point-slope form**: $y - y_1 = m(x - x_1)$. Reach for this when you know the slope and *one point* on the line, and that point is not necessarily the $y$-intercept. You don't need to find $b$ first; you can work directly with what you have.

**Standard form**: $Ax + By = C$, where $A$, $B$, $C$ are integers and $A \geq 0$. Reach for this when you need to find both intercepts quickly (set $x = 0$ for the $y$-intercept; set $y = 0$ for the $x$-intercept) or when working with systems of equations.

All three forms describe the same line. Converting between them is a matter of distributing and solving for $y$, or multiplying through to clear fractions.

Here is a worked conversion. Find the equation of the line through $(2, 5)$ with slope $3$.

Start with point-slope, since we have a point and a slope:
$$y - 5 = 3(x - 2)$$

Distribute:
$$y - 5 = 3x - 6$$

Solve for $y$ to get slope-intercept:
$$y = 3x - 1$$

Rearrange to get standard form:
$$3x - y = 1$$

One line. Three names. The algebra is just moving terms around.

| Form Name | General Template | When to Reach For It | Example (the y=3x−1 line in each) |
| --- | --- | --- | --- |
| slope-intercept, point-slope, standard | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | Use the chapter example as the concrete test case. |
| student should be able to scan this and immediately know which form fits the information they have been given | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | Use the chapter example as the concrete test case. |

---

## What Slope Really Means

Slope is not just a number to calculate. It is a *unit rate* — it carries units from the problem, and those units are the interpretation.

In the heating bill: slope is $1.20$ dollars per gallon. In the savings account: slope is $50$ dollars per week. In the depreciation model: slope is $-3{,}500$ dollars per year. In the temperature conversion $F = \frac{9}{5}C + 32$: slope is $\frac{9}{5}$ degrees Fahrenheit per degree Celsius.

The sign of the slope is not incidental. A positive slope means the output increases with the input; a negative slope means it decreases. Depreciation has negative slope. Cooling has negative slope. The stock market, on any given day, has a slope that could be either. The sign is part of the physical interpretation.

The magnitude of the slope measures sensitivity: how much the output changes per unit of input. A slope of $1.20$ means the bill is moderately sensitive to gallons purchased. A slope of $0.001$ means the output barely responds to the input — nearly flat. A slope of $1{,}000$ means the output explodes with small changes in input — nearly vertical.

This is why two linear functions can be parallel: they have the same sensitivity — the same rate of change — but different starting points. And this is why two linear functions are perpendicular: their slopes are *negative reciprocals*,

$$m_1 \cdot m_2 = -1$$

The perpendicular condition comes from geometry. If you rotate a line of slope $m$ by exactly $90°$, the new slope is $-\frac{1}{m}$. So the line $y = 3x - 1$ is parallel to $y = 3x + 7$ (same slope, different intercept) and perpendicular to $y = -\frac{1}{3}x + 4$ (slopes multiply to $3 \cdot (-\frac{1}{3}) = -1$).

![Coordinate plane showing three lines: y=3x−1 (solid), y=3x+7](images/04-linear-functions-fig-02.png)
*Figure 4.2 — Coordinate plane showing three lines: y=3x−1 (solid), y=3x+7*

---

## From Words to Equations

The world does not arrive pre-algebraized. Heating bills come as descriptions. So does almost every real-world linear relationship. The work is translation.

The translation has a structure, and it is always the same:

First, identify the *variable* — what you don't know, what changes, what the problem is asking about. Give it a name and a unit.

Second, find the *rate of change*. It is almost always signaled by a phrase: "per hour," "per gallon," "per mile," "each additional." This rate is the slope.

Third, find the *starting value* — what the output is when the input is zero. This is the intercept.

Fourth, write the function: $f(x) = mx + b$.

Fifth, use the function to answer the specific question — either evaluate it at a given input, or solve for the input that produces a given output.

Let me run this recipe three times, on problems that look different on the surface but have identical structure underneath.

**Savings.** Anya has $\$200$ saved and adds $\$50$ each week. How many weeks until she has $\$1{,}000$?

Rate: $\$50$/week. Starting value: $\$200$. Function: $S(w) = 50w + 200$.

Set equal to $1{,}000$: $50w + 200 = 1000$, so $50w = 800$, so $w = 16$ weeks.

**Truck depreciation.** A delivery truck costs $\$45{,}000$ new and loses $\$3{,}500$ of value per year. When is it worth $\$10{,}000$?

Rate: $-\$3{,}500$/year (negative — the value decreases). Starting value: $\$45{,}000$. Function: $V(t) = -3500t + 45000$.

Set equal to $10{,}000$: $-3500t + 45000 = 10000$, so $-3500t = -35000$, so $t = 10$ years.

**Phone plans.** Plan A charges $\$30$/month plus $\$0.10$ per text. Plan B charges $\$20$/month plus $\$0.20$ per text. At how many texts are they the same price?

Two functions, both linear: $A(T) = 0.10T + 30$ and $B(T) = 0.20T + 20$. Set equal:
$$0.10T + 30 = 0.20T + 20$$
$$10 = 0.10T$$
$$T = 100 \text{ texts}$$

At 100 texts, both plans cost $\$40$. Below 100, Plan B is cheaper. Above 100, Plan A is.

![Line graph with texts on the x-axis (0–300)](images/04-linear-functions-fig-03.png)
*Figure 4.3 — Line graph with texts on the x-axis (0–300)*

Three different stories. One structure. The algebra was identical each time.

The only move that varies is the final step: sometimes you evaluate the function (plug in $x$, get $y$); sometimes you solve the function (know $y$, find $x$). These are inverse operations. One asks "what does the function produce at this input?" The other asks "what input produces this output?" Both are legitimate; the setup is the same.

---

## When the Data Is Messy

The heating bill is a clean linear relationship — exact by contract. Most real data is not. You plot a scatter of points and they cluster *near* a line, with deviations.

A *scatter plot* shows data as dots in the coordinate plane. When the dots cluster near a line, the relationship is approximately linear. The question is: which line?

The standard answer is *linear regression*: find the line that minimizes the sum of squared vertical distances between the data points and the line. This is called the *line of best fit* or *least-squares regression line*. The formulas exist:

$$m = \frac{n \sum x_i y_i - \sum x_i \sum y_i}{n \sum x_i^2 - (\sum x_i)^2}, \qquad b = \frac{\sum y_i - m \sum x_i}{n}$$

In practice, you let a calculator or computer compute this. What you must be able to do is interpret the result.

Consider a hardware store that tracks monthly nail sales (in pounds) against average daily temperature:

| Temperature ($T$, °F) | Sales ($S$, lbs) |
|---|---|
| 30 | 110 |
| 45 | 145 |
| 60 | 175 |
| 75 | 210 |

First question before fitting any line: is this actually linear? Check the differences in $S$ at equally spaced $T$ values. The gap in $T$ is constant at 15 degrees. The differences in $S$ are: $35$, $30$, $35$. Close to constant — not perfectly, but close enough. A linear model is defensible.

The slope between the extreme points is $\frac{210 - 110}{75 - 30} = \frac{100}{45} \approx 2.22$ pounds per degree. Using the first point $(30, 110)$ in point-slope form:

$$S = 2.22(T - 30) + 110 = 2.22T + 43.4$$

![Scatter plot of the four nail-sales data points](images/04-linear-functions-fig-04.png)
*Figure 4.4 — Scatter plot of the four nail-sales data points*

Now interpret it. The slope $2.22$ means: each additional degree of average daily temperature corresponds to about $2.22$ more pounds of nails sold per month. Why would that be? Warmer weather → more construction activity → more nails. The model captures a real phenomenon.

The intercept is $43.4$ pounds, which would be the predicted sales at $T = 0°F$. That is well outside the data range. We should not trust it as a physical prediction — there are no data points near $0°F$ — but mathematically the line has to cross the vertical axis somewhere.

This brings up the most important limitation of linear models.

---

## The Limits of Linearity

A linear model is reliable *within* the range of the data that produced it. Outside that range, it is an *extrapolation*, and extrapolations can fail dramatically.

The nail-sales line predicts $S = 2.22(100) + 43.4 = 265.4$ pounds of sales at $T = 100°F$. Maybe. Or maybe sales plateau in extreme heat because construction slows down. The model has no way of knowing; it was built on data from $30°F$ to $75°F$. Beyond that, it is a guess dressed up as a formula.

The same applies at the other extreme. The model predicts negative sales below about $T = -20°F$. Negative pounds of nails. The formula produces a number; the number is physically nonsensical. The model has been pushed past its domain of applicability.

This is not a flaw in linear modeling; it is a fact about all models. A model is a simplified description of a phenomenon over a specific range of conditions. It captures what it captures. The discipline is to *know the range*, to be honest about what the model can and cannot predict.

There is also the deeper issue of correlation and causation. The nail-sales model shows that temperature and sales are *correlated* — they move together. It does not show that temperature *causes* increased sales. Both could be driven by a common factor: construction season, perhaps, which correlates with both warmth and nail purchases. The line of best fit is a description of the data, not a causal mechanism.

---

## Why Linearity Matters

There is a reason this chapter appears in every algebra textbook and every statistics course and every engineering curriculum. Linear functions are not the most realistic models — almost nothing in nature is perfectly linear. But they are the most tractable.

Two parameters describe the function completely. The graph is a straight line that a student can draw with a ruler. The equation can be solved for any variable in one or two steps. The rate of change is the same everywhere — there is no complicated behavior to track across different regions of the domain.

This tractability is why more sophisticated models are almost always understood by comparison to the linear case. A quadratic function is what you get when the rate of change is itself changing at a constant rate. An exponential function is what you get when the *percentage* rate of change is constant rather than the absolute rate. Every model in the rest of this book is, in some sense, asking: "what's the simplest departure from linearity that captures this phenomenon?"

And in practice, for small enough changes in any variable, almost every smooth function *looks* linear. The tangent line to a curve is a linear approximation to that curve near a point. This is why linear models are useful even for nonlinear phenomena: over a short enough range, the linear approximation is often good enough. The heating bill is linear by contract; most real things are linear only locally. But locally is often where the question lives.

The Vermont homeowner orders oil every few months. The range of gallons she considers — between 50 and 150 — is the range where her bill formula is valid. Within that range, $f(g) = 1.20g + 45$ answers every question she has. She doesn't need to know whether the oil company's underlying cost structure is nonlinear at 10,000 gallons; she's not buying 10,000 gallons. The model she has is sufficient for the decisions she faces.

That is the real lesson of linear functions: *sufficiency within range*. Find the rate, find the starting value, write the function, use it where it applies. Everything else in this chapter is technique in service of that loop.

---

## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the reasoning holds, where it breaks, and why.

**LLM Exercise 4.1 — Slope as rate.** Tell an LLM: "The slope of a line is 3. What does that mean?" Ask it to give you three different real-world scenarios where a slope of 3 would have completely different physical interpretations. Then ask: "Could a slope of 3 ever be bad news?" What does it say?

**LLM Exercise 4.2 — Parallel vs. perpendicular.** Ask an LLM to explain, without using the formula $m_1 \cdot m_2 = -1$, *why* perpendicular lines have slopes that are negative reciprocals. Push it to explain the geometry. If it uses the formula without explaining it, ask again: "But why does rotating a line by 90° produce a negative reciprocal slope?"

**LLM Exercise 4.3 — The limits of a model.** Give an LLM the nail-sales model $S = 2.22T + 43.4$ and ask it to predict sales at $T = -10°F$ and $T = 120°F$. Then ask: "Are these predictions trustworthy?" Ask it to explain what *extrapolation* means and what kinds of things could make the linear trend fail outside the observed range.

**LLM Exercise 4.4 — Correlation vs. causation.** Tell an LLM: "A study finds that ice cream sales and drowning rates are strongly correlated — when ice cream sales go up, drowning rates go up. Does eating ice cream cause drowning?" Ask it to explain the concept of a *confounding variable* and give two other examples of correlations that are not causal. Then ask: "Can a line of best fit ever prove causation?"

**LLM Exercise 4.5 — When is a relationship linear?** Give an LLM this table of $(x, y)$ values: $(0, 1), (1, 2), (2, 4), (3, 8), (4, 16)$. Ask whether the relationship is linear and how it can tell. Then ask it to construct a table that *looks* linear from the first two points but isn't. What does that reveal about the risk of fitting a line to limited data?

---

##  AI Wayback Machine
**René Descartes** introduced the coordinate system bearing his name in *La Géométrie* in 1637 — letting algebra and geometry talk to each other for the first time. Every line graph and linear function lives on his grid.

![René Descartes](../images/rene-descartes-29a.png)

*Puppet Art by [Nik Bear Brown](https://www.nikbearbrown.com/).*

**Run this:**

```
Who was René Descartes, and how does his coordinate system connect to the linear functions we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"René Descartes"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through how Descartes mapped one specific geometric problem onto algebra.
- Ask it about Descartes's parallel role in early modern philosophy — the cogito and beyond.

What changes? What gets better? What gets worse?
