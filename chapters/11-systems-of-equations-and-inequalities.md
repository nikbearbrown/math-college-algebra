# Chapter 11 — Systems of Equations and Inequalities


## TL;DR

- What happens when one equation isn't enough.
- The chapter moves through Two constraints, one Saturday morning, Part 1 — Linear systems: the geometry of intersection, Substitution, Elimination, and related ideas.
- Read it for the main argument, the vocabulary it introduces, and the practical judgment it asks you to develop.

*What happens when one equation isn't enough.*

---

## Two constraints, one Saturday morning

A market vendor sells bread and bagels. Bread goes for $\$4$ a loaf, bagels for $\$1$ each. At the end of the day she counts her sales: 100 items sold, $\$220$ collected. How many of each did she sell?

One equation isn't enough. If all you knew was the total count — $L + B = 100$ — the answer could be anything from 100 loaves and 0 bagels to 0 loaves and 100 bagels. If all you knew was the total revenue — $4L + B = 220$ — same problem. But together, the two equations pin down a unique answer.

This is a *system of equations*. Two constraints, two unknowns, one solution. The constraint is that both equations must be satisfied simultaneously — not one or the other, but both at once.

Systems appear wherever multiple conditions must hold at the same time. Two substances mixed to hit a target concentration. Two routes that must arrive at the same intersection. Two species competing for the same resource pool. The problem, in every case, is the same: combine the equations in some clever way until each unknown stands alone. The chapter is an exploration of how to do that cleverly — and what it means when you can't.

---

## Part 1 — Linear systems: the geometry of intersection

Two linear equations in two unknowns each describe a line in the plane. A solution to the system is a point that lies on *both* lines simultaneously. Geometrically, that's the intersection.

Three things can happen.

The lines cross at exactly one point. One solution. The system is *consistent and independent* — the equations give genuinely different information, and together they narrow the answer to a single point.

The lines are parallel and never meet. No solution. The system is *inconsistent* — the equations make contradictory demands. No pair $(x, y)$ can satisfy both.

The lines coincide — they are the same line. Infinitely many solutions. The system is *dependent* — one equation is a scalar multiple of the other. They're not two constraints; they're the same constraint written twice.

Knowing which case you're in before you start solving saves a lot of computation. If the slopes of the two lines are equal but the intercepts differ, you already know there's no solution. If the equations are proportional, you already know there are infinitely many.

![Three side-by-side coordinate plane sketches ](images/11-systems-of-equations-and-inequalities-fig-01.png)
*Figure 11.1 — Three side-by-side coordinate plane sketches *

### Substitution

The bread/bagel system:

$$\begin{cases} L + B = 100 \\ 4L + B = 220 \end{cases}$$

The first equation gives $B = 100 - L$ directly. Substitute into the second:

$$4L + (100 - L) = 220 \implies 3L = 120 \implies L = 40$$

Then $B = 100 - 40 = 60$. She sold 40 loaves and 60 bagels.

Substitution works best when one variable already has coefficient 1 in some equation — the isolation is free, and you avoid fractions. The technique is just what it says: solve for one variable in terms of the other, then replace.

### Elimination

The same system, different approach. Subtract the first equation from the second:

$$(4L + B) - (L + B) = 220 - 100 \implies 3L = 120 \implies L = 40$$

The $B$ terms vanished. Elimination works by engineering a cancellation — multiply one equation by a constant chosen to make the coefficients of one variable equal and opposite, then add. The variable disappears, leaving one equation in one unknown.

The two methods are algebraically equivalent. Which you use is a matter of convenience. Substitution is often faster for a $2 \times 2$ system; elimination scales better to larger systems, which is why it underlies the matrix methods in Part 3.

![Coordinate plane showing both lines $L + B](images/11-systems-of-equations-and-inequalities-fig-02.png)
*Figure 11.2 — Coordinate plane showing both lines $L + B*

### Three unknowns

With three equations and three unknowns, the geometry changes: each equation is a plane in three-dimensional space. A solution is a point where all three planes meet.

![3D diagram showing the three possible outcomes for](images/11-systems-of-equations-and-inequalities-fig-03.png)
*Figure 11.3 — 3D diagram showing the three possible outcomes for*

The technique extends naturally. Pick a pair of equations and eliminate one variable. Pick a different pair and eliminate the same variable. Now you have two equations in two unknowns — a system you already know how to solve. Back-substitute to get the third.

**Example.** Solve:

$$\begin{cases} x + y + z = 6 \\ 2x + y + 3z = 14 \\ x + 2y + z = 9 \end{cases}$$

Subtract equation 1 from equation 2: $x + 2z = 8$. Subtract equation 1 from equation 3: $y = 3$.

Now substitute $y = 3$ back into equation 1: $x + 3 + z = 6$, so $x + z = 3$. Combine with $x + 2z = 8$: subtract to get $z = 5$, then $x = -2$.

Check in all three equations: $-2 + 3 + 5 = 6$ ✓; $-4 + 3 + 15 = 14$ ✓; $-2 + 6 + 5 = 9$ ✓.

The same three outcomes are possible: a unique solution (three planes meet at a point), no solution (planes don't share a common point), or infinitely many solutions (the planes share a line or coincide). In elimination, inconsistency shows up as a contradiction — $0 = 5$ — and dependence shows up as a tautology — $0 = 0$. When either appears, you know which case you're in.

---

## Part 2 — Nonlinear systems: more intersections, harder algebra

A linear equation is a line. A nonlinear equation is a curve — a parabola, a circle, a hyperbola. A system of nonlinear equations asks where two curves intersect.

The same techniques apply: substitution and elimination still work. The difference is that nonlinear systems can have more than one solution, and the algebra to find them involves solving a polynomial rather than a linear equation.

**Example.** Where does the line $y = 2x$ intersect the parabola $y = x^2 - 3$?

Set the two expressions for $y$ equal:

$$2x = x^2 - 3 \implies x^2 - 2x - 3 = 0 \implies (x - 3)(x + 1) = 0$$

Two solutions: $x = 3$ (giving $y = 6$) and $x = -1$ (giving $y = -2$). The line crosses the parabola at $(3, 6)$ and $(-1, -2)$.

Geometrically: a line can intersect a parabola in 0, 1, or 2 points. We found 2. A circle and a parabola can intersect in up to 4 points. The number of solutions is bounded by the degrees of the equations — a consequence of Bézout's theorem, which says that two curves of degrees $m$ and $n$ intersect in at most $mn$ points (counting complex and repeated intersections).

![Coordinate plane showing the parabola $y = x^2](images/11-systems-of-equations-and-inequalities-fig-04.png)
*Figure 11.4 — Coordinate plane showing the parabola $y = x^2*

### Systems of inequalities

A linear inequality like $2x + y \leq 6$ doesn't describe a point or a line — it describes a half-plane. The solution to the inequality is every point on one side of the line $2x + y = 6$ (including the line itself, because the inequality is $\leq$ rather than $<$).

A system of inequalities asks: which points satisfy *all* the inequalities at once? The answer is the intersection of the half-planes — a *feasible region*, typically a polygon when the inequalities are linear.

To graph a system of inequalities: graph each boundary line, determine which side satisfies each inequality (test a convenient point), and shade the intersection. The feasible region is where all the shading overlaps.

This is not just a graphing exercise. The feasible region is the geometry of constrained optimization — the set of all feasible solutions in a linear programming problem. Every vertex of the feasible region is a candidate for the optimum.

**Example.** Graph the system:

$$\begin{cases} x + y \leq 8 \\ 2x + y \leq 12 \\ x \geq 0 \\ y \geq 0 \end{cases}$$

The boundary lines are $x + y = 8$, $2x + y = 12$, and the coordinate axes. The feasible region is the quadrilateral with vertices at $(0, 0)$, $(6, 0)$, $(4, 4)$, and $(0, 8)$. (Find the intersection of the first two boundaries: $x + y = 8$ and $2x + y = 12$ give $x = 4$, $y = 4$.)

If you wanted to maximize profit $P = 3x + 2y$ subject to these constraints, you'd evaluate $P$ at each vertex: $P(0,0) = 0$, $P(6,0) = 18$, $P(4,4) = 20$, $P(0,8) = 16$. Maximum is at $(4, 4)$.

The geometry made that optimization tractable. Without the feasible region, you'd have infinitely many candidates. With it, you have four.

![Coordinate plane showing the feasible region for the](images/11-systems-of-equations-and-inequalities-fig-05.png)
*Figure 11.5 — Coordinate plane showing the feasible region for the*

---

## Part 3 — Matrices: systematic elimination at scale

Substitution and elimination work well for two or three equations. What about ten? Or a hundred? The bookkeeping becomes prohibitive — unless you systematize it.

A *matrix* is a rectangular array of numbers. The coefficient matrix of a linear system organizes the equations so that elimination can be applied mechanically, one step at a time.

For the bread/bagel system:

$$\begin{cases} L + B = 100 \\ 4L + B = 220 \end{cases} \quad \longrightarrow \quad \left[\begin{array}{rr|r} 1 & 1 & 100 \\ 4 & 1 & 220 \end{array}\right]$$

The *augmented matrix* appends the constants to the right of a vertical bar. Each row represents one equation; each column (before the bar) represents one variable.

### Row operations and Gaussian elimination

Three operations on rows preserve the solution set:

1. Swap two rows.
2. Multiply a row by a nonzero constant.
3. Add a multiple of one row to another.

These are exactly the moves you make when doing elimination by hand — just organized. *Gaussian elimination* applies these operations systematically to reduce the matrix to *row-echelon form*: zeros below the main diagonal, with a leading nonzero entry (called a *pivot*) in each row.

**Example.** Reduce the bread/bagel augmented matrix.

$$\left[\begin{array}{rr|r} 1 & 1 & 100 \\ 4 & 1 & 220 \end{array}\right]$$

Row 2 $\leftarrow$ Row 2 $- 4 \cdot$ Row 1:

$$\left[\begin{array}{rr|r} 1 & 1 & 100 \\ 0 & -3 & -180 \end{array}\right]$$

Row 2 $\leftarrow$ Row 2 $\div (-3)$:

$$\left[\begin{array}{rr|r} 1 & 1 & 100 \\ 0 & 1 & 60 \end{array}\right]$$

Row 1 $\leftarrow$ Row 1 $-$ Row 2:

$$\left[\begin{array}{rr|r} 1 & 0 & 40 \\ 0 & 1 & 60 \end{array}\right]$$

This is *reduced row-echelon form* — identity matrix on the left, solution on the right. Read off: $L = 40$, $B = 60$.

The matrix method is the same elimination we did before, but the notation strips away the variable names and focuses purely on the numbers. For large systems, this is what makes computation tractable (and eventually, programmable).

![Comparison showing the same bread/bagel elimination done two](images/11-systems-of-equations-and-inequalities-fig-06.png)
*Figure 11.6 — Comparison showing the same bread/bagel elimination done two*

### Matrix arithmetic

Matrices can be added, scaled, and multiplied. Addition and scalar multiplication work entry-by-entry. Matrix multiplication is more subtle: the $(i, j)$ entry of $AB$ is the dot product of row $i$ of $A$ with column $j$ of $B$.

A key consequence: matrix multiplication is *not* commutative. $AB$ and $BA$ may both be defined but give different results — or one may not be defined while the other is.

The identity matrix $I$ (ones on the diagonal, zeros elsewhere) plays the role of 1: $AI = IA = A$ for any appropriately sized $A$.

### The inverse and what it means for solving systems

If $A$ is a square matrix and there exists a matrix $A^{-1}$ such that $AA^{-1} = A^{-1}A = I$, then $A$ is *invertible* and $A^{-1}$ is its *inverse*.

Why does this matter for systems? The system $A\mathbf{x} = \mathbf{b}$ can be solved by multiplying both sides by $A^{-1}$:

$$A^{-1}(A\mathbf{x}) = A^{-1}\mathbf{b} \implies \mathbf{x} = A^{-1}\mathbf{b}$$

This is exact — no approximation. When $A^{-1}$ exists, the system has a unique solution.

For a $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$:

$$A^{-1} = \frac{1}{ad - bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$$

The quantity $ad - bc$ is the *determinant* of $A$, written $\det(A)$. If $\det(A) = 0$, the inverse doesn't exist — the system is either inconsistent or dependent. The determinant is the algebraic signal of which case you're in.

### Determinants and Cramer's Rule

For a $2 \times 2$ matrix, $\det(A) = ad - bc$. For a $3 \times 3$, expand along the first row:

$$\det\begin{pmatrix} a_1 & b_1 & c_1 \\ a_2 & b_2 & c_2 \\ a_3 & b_3 & c_3 \end{pmatrix} = a_1(b_2 c_3 - c_2 b_3) - b_1(a_2 c_3 - c_2 a_3) + c_1(a_2 b_3 - b_2 a_3)$$

*Cramer's Rule* gives a formula for each unknown directly in terms of determinants. For $A\mathbf{x} = \mathbf{b}$ with $\det(A) \neq 0$:

$$x_i = \frac{\det(A_i)}{\det(A)}$$

where $A_i$ is the matrix $A$ with its $i$th column replaced by $\mathbf{b}$.

![Diagram illustrating Cramer's Rule for the $2\times 2$](images/11-systems-of-equations-and-inequalities-fig-07.png)
*Figure 11.7 — Diagram illustrating Cramer's Rule for the $2\times 2$*

**Example.** Solve the bread/bagel system using Cramer's Rule.

The coefficient matrix is $A = \begin{pmatrix} 1 & 1 \\ 4 & 1 \end{pmatrix}$, constants $\mathbf{b} = \begin{pmatrix} 100 \\ 220 \end{pmatrix}$.

$\det(A) = 1 \cdot 1 - 1 \cdot 4 = -3$.

For $L$: replace the first column with $\mathbf{b}$: $A_L = \begin{pmatrix} 100 & 1 \\ 220 & 1 \end{pmatrix}$, $\det(A_L) = 100 - 220 = -120$.

$L = \frac{-120}{-3} = 40$.

For $B$: replace the second column: $A_B = \begin{pmatrix} 1 & 100 \\ 4 & 220 \end{pmatrix}$, $\det(A_B) = 220 - 400 = -180$.

$B = \frac{-180}{-3} = 60$.

Cramer's Rule is elegant and gives each variable its own determinant formula. It's not the most computationally efficient method for large systems — Gaussian elimination beats it — but it is useful when you need a formula for one variable in terms of the parameters of the system, and it connects the solvability of the system ($\det(A) \neq 0$) to a single numerical check.

---

## Putting it together: the factory problem

A small factory makes three products $A$, $B$, $C$. Each requires different amounts of three resources: labor, machine time, and materials. Here are the requirements per unit and the available totals:

| Resource | Per $A$ | Per $B$ | Per $C$ | Available |
|---|---|---|---|---|
| Labor (hr) | 1 | 2 | 1 | 100 |
| Machine (hr) | 2 | 1 | 3 | 130 |
| Materials (lb) | 3 | 4 | 2 | 200 |

The question: find production quantities $a$, $b$, $c$ that use resources exactly. This is a system of three equations in three unknowns:

$$\begin{cases} a + 2b + c = 100 \\ 2a + b + 3c = 130 \\ 3a + 4b + 2c = 200 \end{cases}$$

Write the augmented matrix and row-reduce.

$$\left[\begin{array}{rrr|r} 1 & 2 & 1 & 100 \\ 2 & 1 & 3 & 130 \\ 3 & 4 & 2 & 200 \end{array}\right]$$

R2 $\leftarrow$ R2 $- 2 \cdot$ R1: gives row $(0, -3, 1 \mid -70)$.

R3 $\leftarrow$ R3 $- 3 \cdot$ R1: gives row $(0, -2, -1 \mid -100)$.

$$\left[\begin{array}{rrr|r} 1 & 2 & 1 & 100 \\ 0 & -3 & 1 & -70 \\ 0 & -2 & -1 & -100 \end{array}\right]$$

R3 $\leftarrow$ R3 $- \frac{2}{3} \cdot$ R2: gives row $(0, 0, -5/3 \mid -160/3)$.

From the third row: $-\frac{5}{3}c = -\frac{160}{3}$, so $c = 32$.

Back-substitute into row 2: $-3b + 32 = -70$, so $b = 34$.

Back-substitute into row 1: $a + 68 + 32 = 100$, so $a = 0$.

The solution is $a = 0$, $b = 34$, $c = 32$. The factory should produce 34 units of $B$ and 32 of $C$, and none of $A$. The fact that $a = 0$ isn't a failure of the method — it's a genuine finding. Given the resource constraints, product $A$ is squeezed out entirely. A real factory manager would want to know this.

| Item | Meaning |
| --- | --- |
| the three augmented matrices shown sequentially | initial matrix, after eliminating the first column, after eliminating the second column |
| the final matrix and back-substitution steps shown below | A concrete checkpoint for applying the chapter concept. |
| the solution $a=0$, $b=34$, $c=32$ circled | A concrete checkpoint for applying the chapter concept. |
| student should be able to follow each row operation and verify the arithmetic before attempting their own $3\times 3$ reduction | A concrete checkpoint for applying the chapter concept. |

The row reduction did what elimination always does: combined equations to cancel variables one at a time, until each unknown was isolated. The matrix notation made the bookkeeping manageable. The result is the same as if you'd done substitution with three equations — but faster to track and easier to debug when something goes wrong.

---

## The organizing idea

Every method in this chapter — substitution, elimination, row reduction, Cramer's Rule, matrix inversion — is a different implementation of one idea: **add a multiple of one equation to another to cancel a variable, and repeat until each unknown stands alone.**

Substitution does it by explicit replacement. Elimination does it by adding rows. Gaussian elimination does it systematically in matrix notation, keeping track of which operations were applied and in what order. Cramer's Rule does it by encoding the result of elimination in determinant formulas.

The choice of method is a question of scale and convenience. For a $2 \times 2$ system by hand, substitution is fastest. For a $3 \times 3$ with messy coefficients, elimination or row reduction is safer. For a $100 \times 100$ system on a computer, Gaussian elimination is the standard. For a $2 \times 2$ where you need a formula for one variable in terms of the others, Cramer's Rule gives it directly.

What none of these methods can do is solve a system that has no solution, or produce a unique solution from a system with infinitely many. The algebra faithfully reflects the geometry: parallel lines never intersect; coincident lines intersect everywhere. When the determinant is zero, or when elimination produces a row of zeros or a contradiction, the method is not failing — it's telling you the truth about the system.
## LLM Exercises

These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.

**LLM Exercise 11.1 — Why three lines have 0, 1, or infinite intersections — never 2.** Tell an LLM: "Three distinct lines in the plane can have 0, 1, or infinitely many common intersection points. Why never exactly 2?" Force a clean geometric argument: two lines either are parallel (0), intersect at one point (1), or coincide (infinitely many). Adding a third line adds to those counts only by 0 or by reducing them. Two distinct lines can intersect in only one point — so any common intersection has at most 1 point unless all three coincide. The lesson: solution counts in linear systems are not arbitrary; they reflect geometry.

**LLM Exercise 11.2 — Nonlinear systems break the count.** Ask an LLM: "How many solutions can a system of two equations have if one is a circle and the other is a line?" The answer: 0, 1, or 2, depending on whether the line misses, is tangent to, or crosses the circle. Then ask: "What if I have a circle and a parabola?" The maximum is 4. Force the LLM to articulate Bézout's intuition — the maximum number of intersections between two algebraic curves is bounded by the product of their degrees. Then probe: "When is the actual count *less* than that maximum?" The answer involves tangency, common factors, or the curves missing each other.

**LLM Exercise 11.3 — What the determinant tells you.** Ask an LLM: "For the 2×2 system $ax + by = e$, $cx + dy = f$, the determinant is $ad - bc$. What does it tell me, geometrically?" The expected answer: the determinant measures whether the two coefficient vectors $(a, b)$ and $(c, d)$ are linearly independent — i.e., whether the two lines have different slopes. Determinant zero means parallel (0 or infinite solutions); nonzero means a unique intersection. Then ask: "What does the magnitude of the determinant tell me?" The answer: it's the area of the parallelogram spanned by the coefficient vectors — and that area scales with how "robust" the unique solution is to numerical perturbation.

**LLM Exercise 11.4 — The feasible region.** Tell an LLM: "I have three inequalities defining a feasible region in the plane. What does the feasible region look like, geometrically?" The answer: the intersection of three half-planes — a polygon (possibly unbounded). Then ask: "If I want to maximize a linear function $z = px + qy$ over this region, where will the maximum occur?" Force the explanation: at a *vertex* of the feasible region (or along an edge if the gradient is parallel to the edge). Then probe: "What if the feasible region is unbounded?" The maximum may not exist.

**LLM Exercise 11.5 — Why Gaussian elimination always works.** Ask an LLM: "Gaussian elimination always reduces a system to a form where I can read off the solution. Why is this guaranteed to work for *any* system?" Push for the explanation that the three row operations (swap, scale, add multiple) preserve the solution set, so the reduced system has the same solutions as the original — and the reduced form makes them explicit. Then ask: "What does Gaussian elimination produce when the system has *no* solution?" The answer: a row equivalent to $0 = c$ for some nonzero $c$ — the contradiction. "What about when the system has *infinitely many* solutions?" A row of all zeros, signaling a free variable.

---

##  AI Wayback Machine
**Carl Friedrich Gauss** developed the method of elimination for solving systems of linear equations — now called Gaussian elimination — in 1809. His method is the basis of every modern computational linear-algebra routine.

**Run this:**

```
Who was Carl Friedrich Gauss, and how does Gaussian elimination connect to the systems of equations we covered in this chapter? Keep it to three paragraphs. End with the single most surprising thing about his career or ideas.
```

→ Search **"Carl Friedrich Gauss"** on Wikipedia.

**Now make the prompt better.** Try one of these:

- Ask it to walk through Gaussian elimination on a 3×3 system.
- Ask it about Gauss's habit of not publishing results — and what the field lost because of it.

What changes? What gets better? What gets worse?
