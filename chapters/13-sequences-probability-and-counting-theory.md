# Chapter 13 — Sequences, Probability, and Counting Theory
*Surprising but Certain: What Mathematics Produces When It Works Correctly.*

Here is a question that sounds easy: what is $0.\overline{36}$?

Not as a decimal — you know that. As a fraction. The decimal $0.363636\ldots$ repeats forever, which means you cannot just read off a numerator and denominator. It seems to require infinitely many steps. And yet the answer is $\frac{4}{11}$, and you can prove it in three lines using a tool you will learn in this chapter.

That is not the only surprising thing in these pages. The probability that two strangers in a room of 23 people share a birthday turns out to be over 50% — a result that most people refuse to believe until they work it out. The number of ways to arrange a 10-item menu into a 5-course dinner is 252, but the number of ways to assign them to a *specific order of courses* is 30,240. Counting and probability produce numbers that routinely surprise human intuition, and the discipline of actually working them out is one of the most valuable habits this course can leave you with.

This chapter is about the mathematics of discrete things — things you count rather than measure, add up rather than integrate, list rather than graph. Sequences, series, the algebra of binomial powers, counting arguments, and probability are all, at root, about the same question: *given a structured collection of possibilities, what can we say about them?*

---

## Sequences: The Rules Behind the List

A sequence is an ordered list of numbers. What makes it mathematical is that the terms follow a rule — the list is not arbitrary. Two families of sequences appear everywhere.

In an *arithmetic* sequence, each term is the previous plus a fixed constant $d$, the *common difference*. The simplest example: $5, 8, 11, 14, 17, \ldots$ with $d = 3$. The sequence grows by 3 at every step. The $n$th term is

$$a_n = a_1 + (n-1)d$$

This is just repeated addition: starting from $a_1$, add $d$ exactly $n-1$ times to reach $a_n$.

In a *geometric* sequence, each term is the previous times a fixed constant $r$, the *common ratio*. The bank account: $1000, 1050, 1102.50, 1157.63, \ldots$ with $r = 1.05$. The $n$th term is

$$a_n = a_1 \cdot r^{n-1}$$

Repeated multiplication instead of repeated addition. The two sequences — arithmetic and geometric — are the simplest possible structures you can impose on a list. Any more complicated sequence is either a combination of these or a departure from the pattern entirely.

The distinction matters because the long-run behavior of each is completely different. An arithmetic sequence grows without bound if $d > 0$, shrinks without bound if $d < 0$, and stays constant if $d = 0$. The growth is *linear* — proportional to the number of steps taken. A geometric sequence with $r > 1$ grows *exponentially* — each step multiplies by $r$, so the terms accelerate. A geometric sequence with $0 < r < 1$ shrinks toward zero, each term a fixed fraction of the last. The bank account with $r = 1.05$ keeps growing, faster and faster in absolute terms, because each year's interest is computed on a larger base. The key word here is *compounding* — and compounding is geometric, not arithmetic.

<!-- → [CHART: Two side-by-side line graphs over n = 1 to 20 — left shows arithmetic sequence a_n = 5 + 3(n−1) as a straight line; right shows geometric sequence a_n = 1000 · (1.05)^(n−1) as an accelerating curve; both use the same n-axis scale; student should see at a glance that arithmetic growth is linear and geometric growth accelerates, making the compound-interest claim visually immediate rather than just asserted] -->

---

## Series: Adding Up the Terms

A *series* is the sum of a sequence. It seems like a simple extension — just add the terms — but the formulas that result are both clean and powerful.

**The arithmetic series.** Add the first $n$ terms of an arithmetic sequence. There is a famous shortcut, attributed to the young Gauss, who reportedly computed the sum of all integers from 1 to 100 in seconds: pair the first and last terms ($1 + 100 = 101$), the second and second-to-last ($2 + 99 = 101$), and so on. There are 50 such pairs. So the sum is $50 \times 101 = 5050$.

The same argument gives the general formula. The first term is $a_1$, the last is $a_n$, and there are $n$ terms. Pair first with last, second with second-to-last; each pair sums to $a_1 + a_n$, and there are $n/2$ pairs:

$$S_n = \frac{n(a_1 + a_n)}{2}$$

The sum of $n$ terms is $n$ times their average. Arithmetic sequences have a constant average over any symmetric interval, which is why this works.

**The geometric series.** For the geometric sequence with first term $a_1$ and common ratio $r \neq 1$, the sum of $n$ terms is

$$S_n = a_1 \cdot \frac{1 - r^n}{1 - r}$$

The derivation is elegant. Write $S = a_1 + a_1 r + a_1 r^2 + \cdots + a_1 r^{n-1}$. Multiply both sides by $r$: $rS = a_1 r + a_1 r^2 + \cdots + a_1 r^n$. Subtract: $S - rS = a_1 - a_1 r^n$. Factor: $S(1 - r) = a_1(1 - r^n)$. Divide: $S = a_1\frac{1-r^n}{1-r}$.

The algebra is three lines. What it reveals is more interesting.

**The infinite geometric series.** What happens if we let $n \to \infty$? The term $r^n$ appears in the numerator. If $|r| < 1$ — if the ratio is between $-1$ and $1$ — then $r^n$ shrinks toward zero as $n$ grows. In the limit:

$$S_\infty = \frac{a_1}{1-r} \qquad (|r| < 1)$$

The sum of infinitely many terms is finite. This is the result that lets us handle repeating decimals.

Consider $0.\overline{36} = 0.36 + 0.0036 + 0.000036 + \cdots$. This is a geometric series with $a_1 = 0.36$ and $r = 0.01$. Since $|0.01| < 1$:

$$S_\infty = \frac{0.36}{1 - 0.01} = \frac{0.36}{0.99} = \frac{36}{99} = \frac{4}{11}$$

The infinite decimal is exactly $\frac{4}{11}$. Not approximately — exactly. The repeating decimal is a geometric series in disguise, and the geometric series formula converts it to a fraction in three steps. This is how we proved, in Chapter 1, that all repeating decimals are rational numbers — not just asserted it, but showed the mechanism.

<!-- → [IMAGE: Number line zoomed in between 0 and 1, showing the partial sums of the geometric series for 0.36̄ converging from the left — S₁ = 0.36, S₂ = 0.3636, S₃ = 0.363636, with arrows showing each partial sum landing closer to the target 4/11 ≈ 0.3636̄; the gap between each partial sum and the limit halved (approximately) each step; student should see convergence not just as an algebraic limit but as a sequence of points visibly closing in on a value] -->

---

## The Binomial Theorem: What Happens When You Expand $(a + b)^n$

You know how to expand $(a + b)^2 = a^2 + 2ab + b^2$. The coefficient of $ab$ is 2 because there are two ways to pick one $a$ and one $b$ from the two factors $(a+b)(a+b)$: take $a$ from the first and $b$ from the second, or $b$ from the first and $a$ from the second.

That combinatorial observation scales. When you expand $(a + b)^n$, you multiply $n$ copies of $(a + b)$ together. Each term in the expansion comes from choosing either $a$ or $b$ from each factor. A term with $a^{n-k}b^k$ arises whenever you chose $b$ from exactly $k$ of the $n$ factors — and the number of ways to choose which $k$ factors give the $b$ is $\binom{n}{k}$, the *binomial coefficient*:

$$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$

Here $n! = n \cdot (n-1) \cdot (n-2) \cdots 2 \cdot 1$ is the *factorial* of $n$. So the full expansion is:

$$(a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k$$

This is the Binomial Theorem. The coefficients $\binom{n}{k}$ form Pascal's triangle, where each entry is the sum of the two above it:

```
Row 0:          1
Row 1:        1   1
Row 2:      1   2   1
Row 3:    1   3   3   1
Row 4:  1   4   6   4   1
```

Row $n$ gives the coefficients for $(a+b)^n$. Pascal's triangle is not just a pattern — each row entry counts something real: the number of ways to select $k$ items from $n$, which is exactly the coefficient that appears in the expansion.

<!-- → [IMAGE: Pascal's triangle through Row 6 with each entry labeled both as C(n,k) and its numeric value; Row 4 highlighted to match the (x+2)⁴ expansion, with each entry annotated to show which term it produces — e.g., C(4,2)=6 labeled with "coefficient of x²·2²=24"; alongside, a small diagram showing the combinatorial interpretation: for C(4,2), four factor-slots with two marked "choose b" in all possible 6 arrangements; student should see that the triangle is a counting device, not just a pattern to memorize] -->

Here is the expansion of $(x + 2)^4$ in full:

$$(x + 2)^4 = \binom{4}{0}x^4 + \binom{4}{1}x^3 \cdot 2 + \binom{4}{2}x^2 \cdot 4 + \binom{4}{3}x \cdot 8 + \binom{4}{4} \cdot 16$$
$$= x^4 + 8x^3 + 24x^2 + 32x + 16$$

Notice where the 24 comes from: $\binom{4}{2} \cdot 2^2 = 6 \cdot 4 = 24$. The binomial coefficient counts the ways, the power of 2 scales the term. Both pieces are necessary.

---

## Counting: The Multiplication Principle and Its Consequences

Before you can find the probability of an event, you need to know how many outcomes are possible. Counting structured collections is a skill — and it is easy to get wrong, in both directions. People regularly undercount (missing cases they didn't realize existed) and overcount (counting the same arrangement twice under different names).

The foundation is the *multiplication principle*: if task A can be done in $m$ ways and task B in $n$ ways, independently, then doing both tasks can be done in $mn$ ways. Four sizes of pizza times six topping choices gives $24$ distinct pizza orders. This sounds obvious, but its consequences extend further than intuition suggests.

**Permutations.** How many ways can 8 horses finish 1st, 2nd, and 3rd in a race? The first-place finisher can be any of 8. Given that, the second-place finisher can be any of the remaining 7. The third-place finisher can be any of the remaining 6. Multiply: $8 \times 7 \times 6 = 336$. This is a *permutation* — an arrangement of $r$ items from $n$, where order matters.

$$P(n, r) = \frac{n!}{(n-r)!}$$

For $P(8, 3)$: $\frac{8!}{5!} = 8 \cdot 7 \cdot 6 = 336$. The denominator $5!$ cancels the factors you don't use.

**Combinations.** How many 5-card hands can be dealt from a 52-card deck? Order doesn't matter — the hand $\{A\heartsuit, K\spadesuit, Q\diamondsuit, J\clubsuit, 10\heartsuit\}$ is the same hand regardless of which card you were dealt first. We want *selections*, not arrangements.

$$C(n, r) = \binom{n}{r} = \frac{n!}{r!(n-r)!}$$

For $C(52, 5)$: $\frac{52!}{5! \cdot 47!} = 2{,}598{,}960$ distinct 5-card hands. The denominator $r!$ divides out all the orderings you don't want to count separately.

The relationship between permutations and combinations is clean: $P(n,r) = C(n,r) \cdot r!$. Every combination (unordered selection) generates $r!$ permutations (ordered arrangements). If you want orderings, multiply by $r!$. If you want just selections, divide.

The practical skill is reading the problem and deciding: does order matter here? Finishing positions in a race: yes. Committee membership: no. Card hands: no. Assignment of prizes to ranked places: yes. The formula is always the same; the judgment about which formula applies requires understanding what you are actually counting.

<!-- → [TABLE: Counting technique decision guide — columns: Situation, Order Matters?, Formula, Example; rows: (race finishing positions) ordered arrangement of r from n → P(n,r) = n!/(n−r)! → P(8,3)=336; (committee selection) unordered selection of r from n → C(n,r) = n!/r!(n−r)! → C(10,5)=252; (pizza order) independent sequential choices → multiplication principle → 4×6=24; (relationship between them) every C(n,r) selection × r! orderings = P(n,r); student should identify which row applies before picking up a formula] -->

---

## Probability: From Counting to Likelihood

The definition of probability, for equally likely outcomes, is simple:

$$P(E) = \frac{\text{number of outcomes in } E}{\text{total number of equally likely outcomes}}$$

Probability is between 0 and 1. An impossible event has probability 0; a certain event has probability 1. Everything else is between.

The machinery of combinations is exactly what you need to compute most interesting probabilities. A random 5-card hand: how likely is it to contain exactly two aces? There are $C(4, 2) = 6$ ways to choose 2 aces from 4, and $C(48, 3) = 17{,}296$ ways to fill the remaining 3 cards from the non-ace cards. Total favorable hands: $6 \times 17{,}296 = 103{,}776$. Probability: $\frac{103{,}776}{2{,}598{,}960} \approx 3.99\%$. The counting principles are the engine; the probability formula is just the final ratio.

A few rules extend the basic definition to combinations of events.

**Complement.** The probability of "not $E$" is $1 - P(E)$. This is useful when $E$ is complicated but its complement is simple. If the probability of rolling at least one 6 in three dice rolls is hard to compute directly, the complement (rolling no 6 in three rolls) is $\left(\frac{5}{6}\right)^3 = \frac{125}{216}$, and the original probability is $1 - \frac{125}{216} = \frac{91}{216}$.

**Union.** The probability of $A$ or $B$ occurring is

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

The subtraction prevents double-counting outcomes where both events occur. If $A$ and $B$ cannot both occur (they are *mutually exclusive*), then $P(A \cap B) = 0$ and the formula reduces to $P(A) + P(B)$.

**Independence.** For events that have no influence on each other, the probability of both occurring is $P(A) \times P(B)$. Roll two dice: the first result has no effect on the second. The probability of two sixes is $\frac{1}{6} \times \frac{1}{6} = \frac{1}{36}$.

These three rules — complement, union, independence — handle most practical probability problems at this level.

---

## The Birthday Problem, and Why Intuition Fails

Here is the birthday problem done honestly.

In a room of 23 people, what is the probability that at least two share a birthday?

The direct computation is messy — you'd have to account for every possible pair, triple, or larger group of people who might share a birthday. The complement is cleaner: what is the probability that *all 23 people have different birthdays*?

Line the 23 people up in some order. The first person has a birthday: 365 choices out of 365. The second person must have a different birthday: 364 choices out of 365. The third: 363 out of 365. Continue:

$$P(\text{all different}) = \frac{365}{365} \cdot \frac{364}{365} \cdot \frac{363}{365} \cdots \frac{343}{365} = \frac{365!/(342!)}{365^{23}}$$

Computing this numerically: $P(\text{all different}) \approx 0.493$.

So $P(\text{at least two share}) = 1 - 0.493 = 0.507$.

With only 23 people, there is already a better-than-even chance that two of them share a birthday. Most people, when asked, guess this threshold is somewhere around 180 people — roughly half of 365. That intuition is wrong by nearly an order of magnitude.

Why is it so low? Because it is not about any specific birthday — it is about whether *any* pair matches among all $\binom{23}{2} = 253$ possible pairs. Each pair is unlikely to match, but 253 tries is a lot of tries. The multiplication of many small probabilities accumulates fast when the number of pairs grows as the square of the number of people. This is the same structural reason that networks become densely connected much faster than their size grows, that diseases spread faster than headcounts suggest, and that mutual acquaintances appear unexpectedly in large groups. Combinatorial growth is counterintuitive at the gut level; the calculation is the only reliable guide.

<!-- → [CHART: Line graph of P(at least one shared birthday) on the y-axis (0 to 1) vs. number of people in the room on the x-axis (1 to 60); the curve rises steeply, crossing 0.5 at n=23 (marked with a vertical dashed line and label "50% threshold: 23 people"), reaching ~0.97 by n=50; a horizontal annotation at n=180 labeled "common intuition" shown dramatically to the right of where the curve has already reached ~1; student should see how fast the probability saturates and how far off the intuitive estimate of "half of 365" actually is] -->

---

## What This Chapter Is Really About

The topics in this chapter — sequences, series, the binomial theorem, counting, probability — are sometimes taught as separate methods, each with its own set of formulas. But there is a single thread running through all of them.

Each topic is about a *structured collection of discrete things*, and the question is always: *how many?* or *how likely?*

A sequence is a structured list. Its formula tells you how many steps to reach a given term. A series is a structured sum. Its formula tells you how much all the terms add up to — finitely or infinitely. The binomial theorem is a structured expansion. Its coefficients count how many ways each term can arise. Permutations and combinations count structured arrangements and selections. Probability turns those counts into likelihoods.

The connection between the binomial theorem and probability is especially close. The binomial coefficient $\binom{n}{k}$ counts the number of ways to choose $k$ items from $n$. It also counts the number of heads-and-tails sequences with exactly $k$ heads in $n$ flips. The expansion $(p + (1-p))^n$ — where $p$ is the probability of heads — gives you the probability of each possible number of heads directly as a term in the expansion. This connection is the origin of the *binomial distribution*, which is the foundation of a large part of statistics.

The patterns found in this chapter have echoes everywhere — in computer science (how many subsets does a set have?), in finance (how does compound interest accumulate?), in genetics (how likely is a particular combination of traits?), in cryptography (how hard is it to guess a password?). Discrete mathematics turns out to underlie much of the computational world in ways that continuous mathematics does not.

This is the last chapter of college algebra. The subject has traveled from the arithmetic of real numbers, through equations and functions, through polynomials and exponentials and logarithms and trigonometry, to the discrete tools of sequences and counting. These are not thirteen unrelated topics. They are a single connected language for describing quantitative structure — the language that the sciences, the social sciences, and engineering all share as their mathematical foundation.

The repeating decimal $0.\overline{36}$ is $\frac{4}{11}$. The room of 23 people has better than even odds of containing a shared birthday. Both results are surprising. Both are certain. That combination — surprising but certain — is what mathematics produces when it works correctly.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 13.1 — Infinite sums that converge.** Tell an LLM: "How can an infinite sum equal a finite number? The intuition is that adding infinitely many positive things should give infinity." Push for the precise condition: a geometric series $\sum_{n=0}^{\infty} ar^n$ converges if and only if $|r| < 1$, and the sum equals $a/(1-r)$. Then ask: "Why does $|r| < 1$ make all the difference?" The LLM should explain: each successive term is *less than* a fixed fraction of the previous, so the sum is bounded. Probe: "What about the harmonic series $1 + 1/2 + 1/3 + 1/4 + \dots$ — that's a sum of decreasing terms but it diverges. Why?" Force the explanation that the terms don't shrink fast enough.

**LLM Exercise 13.2 — Why $C(n,k)$ appears in the binomial theorem.** Ask an LLM: "When you expand $(a + b)^n$, the coefficient of $a^{n-k}b^k$ is $C(n,k)$. Why?" Push for the combinatorial argument, not the algebraic one: each term in the expansion comes from choosing either $a$ or $b$ from each of the $n$ factors. To get a term with $k$ copies of $b$, you need to *choose* which $k$ of the $n$ factors contribute the $b$ — and there are exactly $C(n,k)$ such choices. Then ask: "Why is this the same coefficient that appears in Pascal's triangle?" The answer: Pascal's triangle counts the same combinatorial selections.

**LLM Exercise 13.3 — When the multiplication principle fails.** Tell an LLM: "If I have 5 shirts and 3 pants, the multiplication principle says I can make $5 \times 3 = 15$ outfits. But what if my pants don't go with one specific shirt — do I still get 15?" The answer: no. The multiplication principle requires *independence* — every shirt goes with every pant. Then ask: "Give me three real-world counting situations where the multiplication principle would silently fail because of unstated dependencies." Probe whether the LLM identifies dependencies of the right kind (e.g., a route that requires you to pick up one specific item; a menu where ordering an entrée forces the side; a sports schedule where home/away alternates).

**LLM Exercise 13.4 — Conditional vs. joint probability.** Ask an LLM: "In a deck of 52 cards, what is the probability of drawing a king? What is the probability of drawing a king *given* that you drew a face card?" The first is $4/52 = 1/13$; the second is $4/12 = 1/3$. Then ask: "Why are these so different?" Push for the explanation that conditional probability restricts the sample space to the conditioning event. Then ask: "Construct a real-world example where the conditional probability is *smaller* than the unconditional probability." The answer requires the conditioning event to make the target event less likely.

**LLM Exercise 13.5 — The birthday problem.** Tell an LLM: "In a room of 23 people, what is the probability that two people share a birthday?" The answer is approximately 50%. Then ask: "Why does intuition say this should be much smaller — most people guess that you need 100+ people for a 50% chance." Push for the explanation that intuition tracks the wrong probability — we instinctively imagine *matching one specific birthday*, but the question allows *any* two people to match. With 23 people, there are $C(23, 2) = 253$ pairs. Each pair has a 1/365 chance — and 253 chances accumulates fast. Then ask: "How does the answer change with 50 people? With 100?" The LLM should give approximately 97% and 99.99996% respectively. The lesson: combinatorial growth dominates intuition.

---

## AI Wayback Machine

**Sofia Kovalevskaya** was the first woman to earn a doctorate in mathematics (in 1874) — and her later work on partial differential equations, combinatorics, and elliptic functions reshaped multiple subfields. She spent most of her career at the University of Stockholm because no Russian university would hire her.

**Run this:**

```
Who was Sofia Kovalevskaya, and how does her mathematical work connect to the sequences, probability, and counting theory we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about her career or ideas.
```

→ Search **"Sofya Kovalevskaya"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it about Kovalevskaya's "Cauchy-Kovalevskaya theorem" and what it does for partial differential equations.
- Ask it about her parallel career as a novelist and the autobiographical novel *Nihilist Girl*.

What changes? What gets better? What gets worse?
