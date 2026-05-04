# Project: Visualizing Classical Mathematics in Haskell

## Background

I’m a software engineer returning to mathematics after many years, for fun and cognitive exercise. I want to combine math study with programming so the work feels alive rather than dry. I last used Haskell about 15 years ago at an introductory level — I’ll need to relearn it as we go, including monads (which I never properly learned the first time).

## Project Concept

Build a project that makes classical mathematics **visible and interactive**. The core idea: take propositions and constructions from historical mathematics texts (Euclid first, then expanding) and turn them into runnable, browser-viewable artifacts. Each piece pairs working code with a short written explainer.

The aspirational vibe is a personal, slowly-growing “explorable explanations” library — but built bottom-up from primary sources rather than modern textbook material.

## Goals

- **Mathematical:** rebuild understanding of formal math, proof, and historical mathematical thinking by working through primary texts with *implementation* as the active mode of engagement.
- **Programming:** relearn Haskell properly this time (modern tooling, DSLs, monads/applicatives, type-driven design) by needing those tools for a real project rather than reading about them in isolation.
- **Output:** a growing collection of interactive explainers, each backed by clean Haskell code. Each piece small enough to finish but real enough to be worth showing.

## Scope

**In scope initially:**

- A Euclidean construction DSL in Haskell
- Browser-based visualization (stack TBD — likely SVG output first, possibly JSON-to-JS bridge later for interactivity)
- One vertical slice first: Euclid Book I, Proposition I.1 (equilateral triangle on a given segment), end-to-end
- A short written explainer alongside each implementation
- Expanding to more of Euclid Book I, then number theory from Diophantus and Euler

**Out of scope:**

- Formal proof assistants (Lean/Coq) — considered and set aside; would slow down intuitive engagement with the source material
- Full computer algebra system
- Production-grade software polish — this is a learning project

## Tech Stack

- **Language:** Haskell (need to relearn — please teach as we go where useful)
- **Build/tooling:** GHCup, Cabal, HLS — to be set up fresh
- **Visualization:** browser-based, exact stack TBD. Candidates:
  - `diagrams` library → SVG (simplest, stays in Haskell)
  - Hand-rolled SVG generation (most flexible)
  - Haskell-computed JSON consumed by a small JS frontend (best for future interactivity)
- **Help me pick** the right approach when we get there, weighing interactivity vs setup overhead.

## Source Materials

**Primary references for the project:**

- *Euclid’s Elements* (Heath edition, all thirteen books) — main source for constructions; starting with Book I
- *Diophantus of Alexandria* (Heath) — for number theory and Diophantine problems, later
- Euler’s *Elements of Algebra* — algebraic methods, later

**Background / context (read alongside, not implemented directly):**

- Stillwell, *Mathematics and Its History* — historical spine
- Stillwell, *The Story of Proof* — for thinking about what proof *means* as we work

## Learning Style

- I want to **understand**, not just complete. When something is interesting or non-obvious, slow down and explain.
- Push back if I’m taking shortcuts or skipping concepts I’d benefit from understanding.
- Don’t over-scaffold. I’m a competent engineer — give me real code and real decisions, not training-wheel exercises.
- For Haskell: introduce modern idioms (applicatives, monad transformers, language extensions) when they become useful in the project, not in isolation.
- For math: assume I once knew this stuff but need refreshing. Don’t condescend, but don’t assume current fluency either.

## Working Preferences

- **Vertical slices over horizontal layers** — get one proposition fully working (DSL → code → render → write-up) before generalizing.
- Suggest small, achievable next steps rather than dumping a roadmap.
- When there’s a design choice, lay out the options with tradeoffs rather than picking silently.
- Honest code review welcome — call out when something I wrote could be better.

## First Task

Help me set up the project from scratch:

1. Modern Haskell toolchain (GHCup, Cabal, HLS in my editor)
1. A minimal project skeleton with a sensible module layout for what we’re building
1. The first end-to-end slice: **Euclid Proposition I.1** — a tiny construction DSL with `Point`, `Circle`, `Line`, intersection primitives, the `equilateral` function, and an SVG render of the result that I can open in a browser.

Once that works, we’ll plan the next step.