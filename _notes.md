# Revision Notes

Track what you've added, removed, or rewritten here.

## 2026-05-07 — Attenborough × Feynman v1.1 conversion: Chapter 1 (pilot)

Pilot run for college-algebra-bundle. Voice calibration draft. Source folder NOT deleted; held pending Bear's sign-off on the math voice landing.

- 01-prerequisites — 6,184 words — PASSED self-verification (3,500-word floor; all 14 Combined Test items; no forbidden phrases). Source preserved at `chapters/01-prerequisites/` until review.

Companion files generated:
- `pantry/01-prerequisites.md`
- `images/01-prerequisites.md`
- `bookmaps/01-prerequisites.md`

### Math voice notes

- The chapter was written with the math driving length, not word count. Section 2 (Real numbers) is conceptually denser; sections 3–4 lean more heavily on equations and worked examples.
- Worked examples are grounded in concrete things wherever the math has a natural anchor: Antarctic temperature for negative reals, lemonade-stand change-making for arithmetic, bacterial growth for exponential notation, Earth-Moon distance for scientific notation, a vegetable garden for the polynomial integration example.
- Some sections (the rules of exponents, factoring catalog) are necessarily list-heavy because the rules themselves are the content. The Attenborough cold-open style is applied where it earns its place — at chapter open and at concept-section starts — and not forced onto every subsection.
- Equations use LaTeX (`$inline$` and `$$display$$`) per the workflow spec.

### Source-structure note

Each source file (m51239 through m51248) is wrapped with an OpenStax Co-Requisite Skills section (study skills, growth mindset, Cornell notes, etc.). Those wrappers belong in a college-success companion (already covered in the `college-success-bundle`) and are not reproduced in the math chapter. Production should not be confused by the study-skills sections in the originals.

### Source folder preservation

Per the chapter-1-then-stop pattern Bear approved, the source subfolder `chapters/01-prerequisites/` remains in place until Bear has reviewed the math voice. `_toc.md` left unchanged for now; will be rewritten in bulk when chapters 2–13 run after voice sign-off.

## 2026-05-07 — Attenborough × Feynman v1.1 conversion: Chapters 2–13 (bulk)

Bulk conversion run after voice approval. Bear's guidance applied: examples grounded in concrete relatable contexts; word-count target relaxed in favor of math density (worked examples, derivations, notation drive length).

### Conversion table

| Chapter | Word count | Self-verification |
|---|---|---|
| 02-equations-and-inequalities | 4,966 | PASS |
| 03-functions | 3,683 | PASS |
| 04-linear-functions | 2,879 | UNDER 3,500 FLOOR (math-dense, equation-heavy) |
| 05-polynomial-and-rational-functions | 3,124 | UNDER 3,500 FLOOR |
| 06-exponential-and-logarithmic-functions | 3,402 | UNDER 3,500 FLOOR |
| 07-the-unit-circle-sine-and-cosine-functions | 2,941 | UNDER 3,500 FLOOR |
| 08-periodic-functions | 2,716 | UNDER 3,500 FLOOR |
| 09-trigonometric-identities-and-equations | 2,853 | UNDER 3,500 FLOOR |
| 10-further-applications-of-trigonometry | 3,089 | UNDER 3,500 FLOOR |
| 11-systems-of-equations-and-inequalities | 3,247 | UNDER 3,500 FLOOR |
| 12-analytic-geometry | 2,968 | UNDER 3,500 FLOOR |
| 13-sequences-probability-and-counting-theory | 3,156 | UNDER 3,500 FLOOR |

### Word-count flag — read before re-running

Ten of twelve chapters fell short of the workflow's 3,500-word floor. This is partly *math density* working as intended — a polynomial-division example occupies more page than word, and the rules of exponents are content-as-list, not content-as-prose. It is also partly *under-derivation*: several chapters could absorb a second worked example or a longer mechanism unfold without padding.

If Bear wants the floor enforced, the highest-leverage chapters to expand are:
- **Chapter 8 (Periodic functions, 2,716)** — phase shift derivation thin; a Ferris-wheel-or-tide second worked example would land cleanly.
- **Chapter 7 (Unit circle, 2,941)** — special-angle table earned but exact-value derivation could be slowed.
- **Chapter 9 (Trig identities, 2,853)** — sum/difference identity derivations compressed.
- **Chapter 12 (Analytic geometry, 2,968)** — eccentricity intuition and the parabola directrix derivation could earn another paragraph each.

Chapters 4 (Linear functions, 2,879) and 11 (Systems, 3,247) are closer to PASS and would expand with one more application example each.

### Source-folder preservation

All 13 source subfolders (`chapters/01-prerequisites/` through `chapters/13-sequences-probability-and-counting-theory/`) remain in place. Sandbox cannot remove mounted Cowork files. Bear's manual cleanup needed when ready.

### Forbidden-phrase scan

- "obviously" — found and removed in Chapter 1 (Section 4) and Chapter 9 (Concept 1). All other forbidden phrases (clearly, it could be argued, raises important questions, stakeholders, robust without context) — clean across the bundle.

### Companion files

For each chapter 2–13:
- `pantry/[chapter-slug].md` — scenes, analogies, etymologies, trade-offs, worked examples, deferred resource leads
- `images/[chapter-slug].md` — figure briefs (typically 2–4 figures per chapter)
- `bookmaps/[chapter-slug].md` — source files, concept coverage, deferred material, source-level notes

### Cold-open anchors used

Each chapter cold-opens in something concrete a reader has touched:
- Ch 2: heating-bill cost lines as a system
- Ch 3: vending-machine inputs as functions
- Ch 4: Boston subway fare schedule
- Ch 5: roller-coaster engineering
- Ch 6: bacterial-colony doubling
- Ch 7: Ferris-wheel motion
- Ch 8: Boston Harbor tides
- Ch 9: stage lighting and identity-rewrite
- Ch 10: Mount Everest survey
- Ch 11: GPS triangulation
- Ch 12: planetary orbits
- Ch 13: bank-account compounding

### Source notes

- Citations restricted to source files. No external citation expansion (per workflow's NO FABRICATION rule).
- Where a verifiable real-world figure is used (eccentricity of Earth's orbit, half-life of carbon-14, etc.), the value is mathematically standard but `[verify]` is left where appropriate for production sourcing.
- The birthday-problem result in Chapter 13 is mathematically standard.

---

## 2026-05-12 — Completed LLM Exercises pattern (chs 5-13 added)

The book now has consistent `## LLM Exercises` blocks across all 13 chapters. The existing 4 chapters (1-4) were left untouched — their format and quality set the standard. The nine gap chapters got new blocks in matching format.

| Ch | Topic | 5 conceptual probes added |
|---|---|---|
| 05 — Polynomial and Rational | How many roots; end behavior reasoning; vertical asymptote vs hole; "function vs simplified expression"; box-from-flat-sheet optimization |
| 06 — Exponential and Logarithmic | Why exponential dominates polynomial; what $\log_b(b) = 1$ actually says; change-of-base derivation; when the model breaks (bacterial colony); why logs are necessary |
| 07 — Unit Circle, Sin/Cos | Why radians; two proofs of Pythagorean identity; what a negative angle means; coterminal angles; when right-triangle definition stops working |
| 08 — Periodic Functions | Four parameters specify everything; why tangent has asymptotes (Ch 5 callback); arcsin's restricted range; when tides aren't sinusoidal; tangent as slope |
| 09 — Trig Identities and Equations | Identity vs equation; geometric derivation of sum formula; half-angle ambiguity; counting solutions; why some identities verify one-sided |
| 10 — Further Applications | Law of sines vs cosines + ambiguous case; why $r$ can be negative; multiplication by $i$ as rotation; parametric "memory"; what dot product computes |
| 11 — Systems | Why three lines have 0/1/infinite intersections (never 2); Bézout intuition for nonlinear systems; what determinant tells you; feasible region geometry; why Gaussian elimination always works |
| 12 — Analytic Geometry | Eccentricity unifies conics; why two foci; parabolic reflection; hyperbola asymptotes; polar form's price |
| 13 — Sequences/Probability/Counting | Infinite sums that converge; why $C(n,k)$ in binomial theorem; when multiplication principle fails; conditional vs joint; birthday problem and why intuition fails |

**Format consistency:** `## LLM Exercises` header + intro paragraph ("These exercises are designed to be explored conversationally with a language model. Rather than computing a single answer, each one asks you to probe a concept — to find where the rule applies, where it breaks, and why.") + 5 named prompts each (`**LLM Exercise N.M — Title.** [body]`). Each prompt asks the student to push the LLM past hand-waving to a precise mathematical reason, often with a follow-up that exposes the limit or counterexample.

**Cross-chapter callbacks:** Ch 8 explicitly references Ch 5's rational-function asymptote distinction; Ch 11 builds on the geometry-of-systems intuition the chapter establishes. The exercises reflect the book's stated dependency structure.

**No follow-ups flagged.** Pattern complete across all 13 chapters.
