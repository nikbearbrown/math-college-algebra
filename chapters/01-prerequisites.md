# Chapter 1 — Prerequisites

## TL;DR

- Every Number You Will Ever Need Is Already in the Cold.
- The chapter moves through The Kinds of Numbers (And Why the Distinctions Matter), The Rules for Moving Numbers Around, Exponents: Shorthand for Repeated Multiplication, Scientific Notation, and related ideas.
- Read it for the main argument, the vocabulary it introduces, and the practical judgment it asks you to develop.

*Every Number You Will Ever Need Is Already in the Cold.*

On July 21, 1983, a satellite passed over Vostok Station on the East Antarctic Plateau — 11,000 feet above sea level, deep in the continent's interior — and recorded the surface temperature: $-89.2°\text{C}$. The coldest temperature ever measured on Earth.

Look at that number for a moment. It is *negative*. It has a *decimal point*. It is finite — not zero, not infinity, not "very cold." Just $-89.2$. And sitting inside that compact notation, if you know where to look, is almost everything you need to know before the rest of this book makes sense: what kind of number that is, what rules allow you to move it around without changing its meaning, how exponents let you write the mass of the electron in the same line as the mass of the Sun, and how the algebraic machinery of polynomials and rational expressions turns one number like $-89.2$ into a *function* — something that can describe temperatures everywhere, not just at one place on one day.

That is the program of this chapter.

---

## The Kinds of Numbers (And Why the Distinctions Matter)

Most students, when they first hear about "types of numbers," suspect they are being asked to memorize a taxonomy for no reason. They are right to be suspicious — memorizing a taxonomy without understanding why it exists is exactly the wrong way to spend your time. So let me tell you why the distinctions matter.

Consider the question: does the equation $x + 3 = 0$ have a solution? If you are only allowed to use *counting numbers* — the natural numbers $1, 2, 3, \ldots$ — the answer is no. There is no natural number $x$ such that $x + 3 = 0$. The equation is unsolvable.

If you extend your permission to include negative numbers — the *integers*, $\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots$ — then suddenly $x = -3$ works. A new question becomes answerable because you expanded the universe of allowed numbers.

This is the real story of the real number hierarchy: each extension was forced by a question that the previous set couldn't answer. Natural numbers can't handle debts or temperatures below zero, so we invent integers. Integers can't handle the ratio of 2 feet split among 3 people, so we invent rational numbers — any number expressible as a ratio of two integers, $\frac{m}{n}$ with $n \neq 0$. (The word *rational* comes from the Latin *ratio*, meaning *proportion*. It has nothing to do with "logical.") And rational numbers, it turns out, can't handle the diagonal of a unit square.

That last one is worth stopping on. If you draw a square with sides of length 1, the diagonal — by the Pythagorean theorem — has length $\sqrt{2}$. Is $\sqrt{2}$ rational? Can you write it as $\frac{m}{n}$ for some integers $m$ and $n$? The answer is no, and the proof is one of the oldest arguments in mathematics: assume $\sqrt{2} = \frac{m}{n}$ in lowest terms, square both sides to get $2n^2 = m^2$, conclude that $m$ must be even, write $m = 2k$, substitute to get $2n^2 = 4k^2$, conclude that $n$ must also be even — but then the fraction wasn't in lowest terms. Contradiction. The assumption was false. $\sqrt{2}$ is *irrational* — nonterminating and nonrepeating in decimal form.

The real numbers, $\mathbb{R}$, are the rationals and irrationals together. Every point on a number line corresponds to exactly one real number, and every real number corresponds to exactly one point. The hierarchy nests like this:

$$\mathbb{N} \subset \mathbb{W} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$$

![Nested-rectangle diagram of the real number hierarchy ](images/01-prerequisites-fig-01.png)
*Figure 1.1 — Nested-rectangle diagram of the real number hierarchy *

where $\mathbb{N}$ is the natural numbers, $\mathbb{W}$ adds zero (the *whole* numbers), $\mathbb{Z}$ adds negatives (the *integers* — from the German *Zahlen*, meaning *numbers*), $\mathbb{Q}$ adds ratios, and $\mathbb{R}$ adds the irrationals.

The Antarctic temperature $-89.2$ is an integer sign, a rational decimal, and a real number. All three descriptions are simultaneously true.

---

## The Rules for Moving Numbers Around

Here is a question that looks trivial until you think about it: why does $3 + 5$ equal $5 + 3$?

One answer is: "because both equal 8, and 8 = 8." True but circular. The deeper answer is that the *commutative property* of addition is a rule we have agreed to adopt, and we adopted it because it reflects something true about the physical world — if I have 3 apples and you give me 5 more, it doesn't matter in what order we count them.

The five properties of real numbers are the complete list of the agreements that underlie all of algebra. They are:

**Commutative property** — order doesn't change the result, for addition and multiplication:
$$a + b = b + a \qquad a \cdot b = b \cdot a$$
Subtraction and division are *not* commutative: $7 - 3 \neq 3 - 7$.

**Associative property** — grouping doesn't change the result, for addition and multiplication:
$$(a + b) + c = a + (b + c) \qquad (a \cdot b) \cdot c = a \cdot (b \cdot c)$$
Subtraction is not associative: $8 - (3 - 1) = 6$ but $(8 - 3) - 1 = 4$.

**Distributive property** — multiplication distributes over addition:
$$a(b + c) = ab + ac$$
This is the only property that connects two different operations. It is the single most-used identity in all of algebra.

**Identity property** — there exist special elements that leave numbers unchanged:
$$a + 0 = a \qquad a \cdot 1 = a$$

**Inverse property** — every number has an "undo":
$$a + (-a) = 0 \qquad a \cdot \frac{1}{a} = 1 \quad (a \neq 0)$$

The reason to name these explicitly is not to pass a quiz on the names. It is this: every legal algebraic move you will make for the next thirteen chapters is an application of one of these five rules. When you "rearrange" terms, you are using the commutative property. When you "factor out" a number, you are using the distributive property in reverse. When you "cancel" a fraction, you are using the inverse property. The names are handles on the moves.

There is also the question of *order* when several operations appear together. The convention is PEMDAS: Parentheses first, then Exponents, then Multiplication and Division (left to right, equal priority), then Addition and Subtraction (left to right, equal priority). This is a social contract, not a mathematical law — but everyone follows the same one, which is the point.

$$24 + 6 \cdot \frac{2}{3} - 4^2 = 24 + 6 \cdot \frac{2}{3} - 16 = 24 + 4 - 16 = 12$$

| Step | Operation Applied | Expression After |
| --- | --- | --- |
| Step-by-step PEMDAS trace for 24 + 6 · (2 | 3) − 4² — | A concrete checkpoint for applying the chapter concept. |

Exponent first, then multiplication, then left-to-right arithmetic. If you got a different answer, go back through and count which rule you applied in which order.

---

## Exponents: Shorthand for Repeated Multiplication

A single bacterium divides in two every twenty minutes. After ten divisions — about three hours — you have $2^{10} = 1024$ bacteria. After twenty, $2^{20} = 1{,}048{,}576$. After thirty, more than a billion. The growth doesn't feel like multiplication because it doesn't happen one step at a time in your head; it happens all at once, as an exponent.

$a^n$ means $a$ multiplied by itself $n$ times. That is all it means. From this single definition, five rules follow by counting the factors:

**Product rule**: $a^m \cdot a^n = a^{m+n}$

Why? $a^m$ is $m$ copies of $a$; $a^n$ is $n$ more. Together: $m + n$ copies.

**Quotient rule**: $\dfrac{a^m}{a^n} = a^{m-n}$ for $a \neq 0$

The denominator cancels $n$ factors from the numerator; $m - n$ remain.

**Power rule**: $(a^m)^n = a^{mn}$

Raising a power to a power multiplies the exponents, because you are making $n$ groups of $m$ factors each.

**Zero exponent**: $a^0 = 1$ for $a \neq 0$

This isn't defined separately; it's *forced* by the quotient rule. $\frac{a^m}{a^m} = 1$ by division; the quotient rule says it also equals $a^{m - m} = a^0$. So $a^0$ must equal $1$.

**Negative exponent**: $a^{-n} = \dfrac{1}{a^n}$ for $a \neq 0$

Same logic: $\frac{a^0}{a^n} = \frac{1}{a^n}$; the quotient rule says $a^{0-n} = a^{-n}$. The negative exponent is the reciprocal, not the negative.

Two more rules, derived from the definition:

$$(ab)^n = a^n b^n \qquad \left(\frac{a}{b}\right)^n = \frac{a^n}{b^n}$$

| Rule Name | Formula | Plain-English Meaning | Common Mistake to Avoid |
| --- | --- | --- | --- |
| product, quotient, power, zero exponent, negative exponent, product-to-a-power, quotient-to-a-power | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |
| student should use this as a single-glance reference before attempting any simplification | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. | A concrete checkpoint for applying the chapter concept. |

### Scientific Notation

These five rules have a practical consequence that physicists and engineers depend on every day. The mass of an electron is approximately

$$0.0000000000000000000000000000009109 \text{ kg}$$

Try computing with that. Now write it as $9.109 \times 10^{-31}$ kg. The number is the same; the form is tractable. Scientific notation $a \times 10^n$, where $1 \leq |a| < 10$, packages the size of a number into the exponent and leaves the significant figures in $a$. The exponent rules then handle arithmetic directly:

$$(a \times 10^m)(b \times 10^n) = (ab) \times 10^{m+n}$$

The Earth-Sun distance is $1.496 \times 10^{11}$ meters. The speed of light is $2.998 \times 10^8$ m/s. The time light takes to travel from the Sun to Earth:

$$t = \frac{1.496 \times 10^{11}}{2.998 \times 10^8} = \frac{1.496}{2.998} \times 10^{11-8} \approx 0.499 \times 10^3 = 4.99 \times 10^2 \text{ seconds}$$

About 499 seconds. About 8 minutes and 19 seconds. The exponent rules did the order-of-magnitude work; we only had to think about $\frac{1.496}{2.998}$.

![Number line or scale diagram showing representative measurements](images/01-prerequisites-fig-02.png)
*Figure 1.2 — Number line or scale diagram showing representative measurements*

### Radicals Are Exponents

The square root $\sqrt{a}$ is the non-negative number whose square is $a$. The connection to exponents is:

$$\sqrt{a} = a^{1/2} \qquad \sqrt[n]{a} = a^{1/n} \qquad \sqrt[n]{a^m} = a^{m/n}$$

Once you accept this, all five exponent rules apply to radicals. There is no separate set of radical rules to memorize.

The product rule for radicals follows from the product rule for exponents:
$$\sqrt{a \cdot b} = \sqrt{a} \cdot \sqrt{b} \quad (a, b \geq 0)$$

This is what lets you simplify $\sqrt{50}$. Factor 50 into a perfect square times something:
$$\sqrt{50} = \sqrt{25 \cdot 2} = \sqrt{25} \cdot \sqrt{2} = 5\sqrt{2}$$

A note on a common mistake: $\sqrt{x^2} = |x|$, not $x$. If $x = -3$, then $x^2 = 9$ and $\sqrt{9} = 3$. The square root always returns a non-negative value — the absolute value, not the original signed number.

**Rationalizing the denominator** is the convention that a fully simplified expression should not have a radical in a denominator. To rewrite $\frac{2}{\sqrt{3}}$:

$$\frac{2}{\sqrt{3}} = \frac{2}{\sqrt{3}} \cdot \frac{\sqrt{3}}{\sqrt{3}} = \frac{2\sqrt{3}}{3}$$

Multiply top and bottom by the radical you want to eliminate. You haven't changed the value — $\frac{\sqrt{3}}{\sqrt{3}} = 1$ by the identity property — you've only changed the form.

---

## Polynomials: Algebra's Working Language

Consider a rectangular garden. The width is $x$ feet; the length is $x + 3$ feet. The area is $x(x+3)$. Apply the distributive property:

$$x(x + 3) = x^2 + 3x$$

That expression — $x^2 + 3x$ — is a *polynomial*. A polynomial in $x$ is a sum of terms of the form $a_n x^n$, where each coefficient $a_n$ is a real number and each exponent $n$ is a non-negative integer. The largest exponent appearing is the *degree*.

Note what is *not* a polynomial: $\frac{1}{x}$ (the exponent on $x$ is $-1$) and $\sqrt{x} = x^{1/2}$ (the exponent is $\frac{1}{2}$). Polynomials are well-behaved precisely because their exponents are non-negative integers. That restriction is what makes factoring possible.

### Combining Polynomials

**Addition and subtraction** combine like terms — terms with the same variable raised to the same power:
$$(3x^2 + 2x - 5) + (x^2 - 4x + 7) = 4x^2 - 2x + 2$$

For subtraction, distribute the minus sign first:
$$(3x^2 + 2x - 5) - (x^2 - 4x + 7) = 3x^2 + 2x - 5 - x^2 + 4x - 7 = 2x^2 + 6x - 12$$

**Multiplication** applies the distributive property repeatedly. For two binomials, the acronym FOIL — *First, Outer, Inner, Last* — names the four products:
$$(2x + 3)(x - 4) = 2x^2 - 8x + 3x - 12 = 2x^2 - 5x - 12$$

FOIL isn't a new rule; it's just the distributive property applied twice. Three products you will use constantly enough to memorize:

$$(a + b)^2 = a^2 + 2ab + b^2$$
$$(a - b)^2 = a^2 - 2ab + b^2$$
$$(a + b)(a - b) = a^2 - b^2$$

Verify the first: $(a + b)^2 = (a + b)(a + b)$. Apply FOIL: $a^2 + ab + ab + b^2 = a^2 + 2ab + b^2$. The middle term $2ab$ is the thing students most often forget. The expression $(a + b)^2 = a^2 + y^2$ is one of the most common errors in algebra. It is wrong every time.

### Factoring: Running Multiplication in Reverse

Factoring converts a sum into a product. This matters because products are what let you find zeros, simplify fractions, and solve equations. Sums don't factor as naturally. So when you meet a polynomial and need to understand its structure, you factor it.

**Greatest common factor (GCF).** Pull out what every term shares:
$$6x^3 + 9x^2 - 3x = 3x(2x^2 + 3x - 1)$$

**Trinomials with leading coefficient 1.** For $x^2 + bx + c$, find two numbers that multiply to $c$ and add to $b$:
$$x^2 + 5x + 6 = (x + 2)(x + 3)$$
since $2 \cdot 3 = 6$ and $2 + 3 = 5$.

**Trinomials with leading coefficient $\neq 1$.** The method called *factoring by grouping* is the most reliable. For $2x^2 + 7x + 3$: find two numbers that multiply to $2 \cdot 3 = 6$ and add to $7$. They are $1$ and $6$. Split the middle term and group:
$$2x^2 + 7x + 3 = 2x^2 + x + 6x + 3 = x(2x + 1) + 3(2x + 1) = (2x + 1)(x + 3)$$

**Difference of squares:**
$$a^2 - b^2 = (a + b)(a - b)$$
So $x^2 - 9 = (x + 3)(x - 3)$, and $4x^2 - 25 = (2x + 5)(2x - 5)$.

**Perfect square trinomials:**
$$a^2 + 2ab + b^2 = (a + b)^2 \qquad a^2 - 2ab + b^2 = (a - b)^2$$

**Sum and difference of cubes:**
$$a^3 + b^3 = (a + b)(a^2 - ab + b^2)$$
$$a^3 - b^3 = (a - b)(a^2 + ab + b^2)$$

So $x^3 - 8 = (x - 2)(x^2 + 2x + 4)$. These two identities are worth memorizing — they appear in calculus more often than you'd expect.

| Pattern to Recognize | Technique | Example In | Example Out |
| --- | --- | --- | --- |
| , identify which row matches the polynomial in front of them, and apply the corresponding technique without guessing | A concrete checkpoint for applying the chapter concept. | Use the chapter example as the concrete test case. | Use the chapter example as the concrete test case. |

### Rational Expressions: Fractions Built from Polynomials

A rational expression is a polynomial divided by a polynomial:

$$\frac{x^2 - 9}{x + 3}, \qquad \frac{x^2 + 5x + 6}{x + 2}, \qquad \frac{x + 1}{x^2 - 4}$$

Each looks complicated until you factor. The first:
$$\frac{x^2 - 9}{x + 3} = \frac{(x + 3)(x - 3)}{x + 3} = x - 3 \quad (x \neq -3)$$

The cancellation is just division: a factor that appears in both numerator and denominator divides out. But — and this is important enough to say twice — the restriction $x \neq -3$ comes from the *original* denominator. The simplified form $x - 3$ has no such restriction visually, but the original expression is undefined at $x = -3$. The simplified form is valid for all $x$ except $x = -3$. The restriction travels with the expression even after simplification.

Operations on rational expressions follow the same rules as ordinary fractions.

*Multiply* — multiply tops, multiply bottoms, cancel common factors:
$$\frac{x + 2}{x - 1} \cdot \frac{x - 1}{x + 3} = \frac{(x + 2)(x - 1)}{(x - 1)(x + 3)} = \frac{x + 2}{x + 3} \quad (x \neq 1, -3)$$

*Divide* — multiply by the reciprocal:
$$\frac{a}{b} \div \frac{c}{d} = \frac{a}{b} \cdot \frac{d}{c}$$

*Add or subtract* — find a common denominator first:
$$\frac{1}{x} + \frac{1}{x + 1} = \frac{x + 1}{x(x + 1)} + \frac{x}{x(x + 1)} = \frac{2x + 1}{x(x + 1)}$$

One worked example in full: simplify $\dfrac{x^2 + 5x + 6}{x^2 - 9}$.

Factor the numerator: $x^2 + 5x + 6 = (x + 2)(x + 3)$.

Factor the denominator: $x^2 - 9 = (x + 3)(x - 3)$.

Substitute and cancel the common factor $(x + 3)$:

$$\frac{x^2 + 5x + 6}{x^2 - 9} = \frac{(x + 2)(x + 3)}{(x + 3)(x - 3)} = \frac{x + 2}{x - 3} \quad (x \neq -3, 3)$$

The simplified form is equivalent to the original on its domain. Both restrictions come from the original denominator: $x^2 - 9 = 0$ when $x = 3$ or $x = -3$.

![Graph of y = (x²+5x+6)/(x²−9) and y =](images/01-prerequisites-fig-03.png)
*Figure 1.3 — Graph of y = (x²+5x+6)/(x²−9) and y =*

---

## What This Chapter Is Actually About

Let me tell you the real thing happening in these pages, because the individual techniques — exponents, factoring, rational expressions — can feel disconnected if you don't see the architecture.

College algebra has one central claim: most quantitative relationships in the physical, financial, and engineering world can be expressed as *functions*, and most of those functions are built from polynomials, rational expressions, exponentials, logarithms, and trigonometric functions. The rest of the book is about those function families and what you can do with them. But before you can work with functions, you need to be able to *manipulate* the expressions that define them — simplify them, factor them, recognize when two expressions are the same.

That manipulation is what you have been building in this chapter. The number hierarchy tells you what kind of object you are handling. The five properties of real numbers tell you what moves are legal. The exponent rules extend those moves to expressions with powers. Polynomial arithmetic gives you a language for describing relationships. Factoring and rational expressions give you the tools to simplify that language when it gets complex.

Think of it as learning to read before you read literature. The specific techniques in this chapter are not the point; the fluency they build is the point. Every time you apply the distributive property without thinking about it, every time you recognize a difference-of-squares pattern, every time you track a domain restriction through a simplification — you are building the automaticity that will let you focus on the harder ideas in later chapters.

The Antarctic temperature is $-89.2°\text{C}$. It is a real number, a rational number, an integer multiple of $0.1$. By the end of this course, you will be able to write a *function* that models temperature as a function of location and altitude, simplify that function, find its zeros, graph it, transform it, and analyze its behavior near extremes. All of that depends on what you just learned.

---

## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe the boundary of a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 1.1 — The number hierarchy.** Tell an LLM: "I think all rational numbers are integers. What am I getting wrong?" Ask it to give you three specific counterexamples and explain why each one is rational but not integer. Then ask: "Is there any real number that is *not* rational and *not* irrational?" What does it say?

**LLM Exercise 1.2 — Where PEMDAS gets ambiguous.** Give an LLM the expression $8 \div 2(2 + 2)$ and ask whether the answer is 1 or 16. Ask it to argue *both* sides before giving a verdict. Then ask: "What does this disagreement reveal about the convention?" This is a real source of confusion in mathematics education — the LLM's explanation of the ambiguity will tell you something about how notation works.

**LLM Exercise 1.3 — Exponent rules and their limits.** Ask an LLM: "Which of the five exponent rules applies to $2^3 + 2^3$?" It should tell you: none of them — the product rule requires multiplication, not addition. Then ask it to evaluate $2^3 + 2^3$ two ways: (1) by direct computation, and (2) by rewriting using the distributive property. Both should give $16$. Ask why the distributive property applies here when no exponent rule does.

**LLM Exercise 1.4 — Factoring by design.** Give an LLM a trinomial you have not been able to factor, and ask it to explain which technique applies and why. Then ask: "Is there a polynomial over the integers that cannot be factored by any of the standard techniques?" Ask for a specific example and why it is considered *irreducible* over $\mathbb{Z}$.

**LLM Exercise 1.5 — Domain restrictions.** Ask an LLM to simplify $\frac{x^2 - 4}{x - 2}$ and explain the domain restriction. Then ask: "What is the value of the *original* expression at $x = 2$?" and "What is the value of the *simplified* expression at $x = 2$?" Ask it to explain why those answers differ and what that means geometrically when you graph the two expressions.

---

##  AI Wayback Machine

**Run this:**

```
Who was Brahmagupta, and how does his work with zero and negative numbers connect to the algebraic prerequisites we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Brahmagupta"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Brahmagupta's specific rules for operations with zero — including the one rule (division by zero) he got wrong.
- Ask it about how Brahmagupta's ideas reached medieval Europe through Arabic translations.

What changes? What gets better? What gets worse?
