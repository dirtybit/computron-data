# Haskell Learning Resources

A guide for someone returning to Haskell after a long break, with a focus on finally understanding monads this time around.

## Refreshing the basics

### Programming in Haskell (2nd ed.) — Graham Hutton

The best fit for a returning learner. ~300 pages, well-paced, and builds up to monads carefully across the whole book rather than dropping them on you in one chapter. Chapters 1–8 refresh the fundamentals (types, recursion, higher-order functions, type classes). Chapters 9–12 cover functors, applicatives, monads, and monadic parsers — by the time you reach the monad chapter, you’ve already used monad-shaped things without the name, so the abstraction lands as “oh, *that* pattern.”

### Get Programming with Haskell — Will Kurt

More hands-on and modern in tone, built around small lessons with exercises. Good if you want to feel productive quickly. Slightly less rigorous than Hutton — better as a complement than a replacement.

### Haskell Programming from First Principles — Allen & Moronuki

The thorough option. ~1200 pages, exhaustive, lots of exercises. Probably overkill as a primary text but excellent to keep nearby as a reference when something confuses you.

## Understanding monads

The trap to avoid: don’t try to understand monads in the abstract first. Work bottom-up — really understand `Maybe` as a monad, then `List`, then `IO`, then `State`. Only after you’ve used four or five concrete monads does the general pattern click. People who try to start from the abstract definition tend to bounce off for years.

### Functors, Applicatives, and Monads in Pictures — Aditya Bhargava

Free illustrated blog post (`adit.io`), about 15 minutes. The best gentle on-ramp. Read this *first*, before any book chapter.

### You Could Have Invented Monads — Dan Piponi

Short essay that derives monads from a problem you’d naturally encounter. The title is accurate — it makes them feel inevitable rather than mystical.

### Learn You a Haskell for Great Good — Miran Lipovača

Free online at `learnyouahaskell.com`. Stylistically dated but its chapters on `Maybe`, `IO`, and `State` monads are still some of the friendliest explanations available.

### Hutton chapters 9–12

The rigorous version. Lands well after the intuition pieces above. The monadic parser chapter is the payoff — where monads stop feeling like an abstraction and start feeling like a power tool.

## Modern Haskell landscape

Things that have evolved or become standard in the last 15 years.

### What I Wish I Knew When Learning Haskell — Stephen Diehl

Free online. A dense survey of the modern ecosystem. Perfect for someone who already grasps the basics and wants a tour of current libraries, language extensions, and idioms.

### Serokell blog & FP Complete tutorials

Good for specific topics — applicatives, the `Foldable`/`Traversable` hierarchy, the `text`/`bytestring` ecosystem, GHC2021, and other things that became standard since you last looked.

## Tooling

The editor and build experience is night-and-day better than it used to be.

- **GHCup** (`ghcup.haskell.org`) — installs and manages GHC, Cabal, Stack, and HLS. The standard entry point now.
- **Cabal** — the default build tool. Stack still works fine, but Cabal has caught up.
- **Haskell Language Server (HLS)** — set this up in your editor (VS Code, Neovim, and Emacs all have good support). Type info on hover, jump to definition, refactoring hints.

## Suggested plan (3–4 weeks of evenings)

1. **Hutton chapters 1–8**, doing the exercises. Refreshes everything and gets your hands moving in modern Haskell.
1. **Bhargava’s “in Pictures” post + Piponi’s “You Could Have Invented Monads.”** Build the intuition before the formalism.
1. **Hutton chapters 9–12** (functors → applicatives → monads → monadic parsers).
1. **Build something small using monads on purpose** — a parser for a tiny expression language is the classic exercise, and it’s a natural bridge into DSL work.

## A note on monads

Monads are genuinely simpler than their reputation suggests. The mystique exists mostly because early tutorials were written by people who learned them through category theory and taught them that way. The pattern itself — “a type that wraps values plus a way to chain operations on them” — is something you’ve already used in other languages without noticing (promises in JS, optionals in Swift, `Result` in Rust). Haskell just makes the pattern first-class and gives it a name.

If a tutorial starts with burritos or spacesuits, close it.