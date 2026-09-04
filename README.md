# iOS Architecture Growth — 12-Week Plan

A structured, practical block to move from _strong instincts kept in your head_ to
_explicit, defensible, teachable models_. One afternoon/week (~2h, stretch to 3).

> This is a personal, employer-neutral learning repo. Examples reference generic iOS
> architecture patterns, not any specific codebase.

## The one idea this whole plan drills

You already have good architectural taste (your 2022–2026 commits prove it). What you
don't yet do is **externalise the model before reaching for a mechanism.**

```
   YOUR CURRENT DEFAULT          THE HABIT WE'RE BUILDING
   ───────────────────          ────────────────────────
   problem                       problem
      │                             │
      ▼                             ▼
   mechanism  ◄── you skip ──►   MODEL   (ownership, invariants,
   (AsyncStream,      this        │       consistency, boundaries)
    pub/sub,                      ▼
    phantom types)            DIAGRAM  (make it legible + testable)
      │                           │
      ▼                           ▼
   code                       PRINCIPLE (name it, so you can defend
                                 │       & teach it)
                                 ▼
                              mechanism  ← now a *derived* choice
                                 │
                                 ▼
                               code
```

Every deliverable — a diagram, a written principle, a brown-bag — is a tool for getting
the model out of your head and in front of others. That is the senior→staff shift.

## How each session is shaped (progressive)

- **Weeks 1–4 — Foundations (study-heavy).** Learn the vocabulary, the diagram types,
  and the named principles. Light hands-on to cement each.
- **Weeks 5–8 — Applied (balanced).** Take real problems, model them, diagram them,
  critique existing designs (including your own past MRs). Study shrinks, hands-on grows.
- **Weeks 9–12 — Ownership (hands-on-heavy).** Produce artifacts others consume: a design
  doc from a cold brief, a dependency-graph refactor proposal, and a brown-bag talk.

## Two learning tracks, interleaved

- **Track A — Modularisation & dependency graphs** (primary). "SOLID scaled up."
- **Track B — Data flow & designing a feature from a brief** (invent-your-own-SSR).

Odd sessions lean Track A, even sessions lean Track B, and the later weeks fuse them.

## Deliverables you accumulate (all checked into this repo)

- `diagrams/` — Mermaid diagrams, one folder per week. You watch them improve over time.
- `sessions/week-NN.md` — pre-filled with the session's plan; you fill the "Output" and
  "Reflection" sections. This is your reviewable growth log.
- `reference/` — your own written-up principles (dependency rules, data-flow patterns).
  These become brown-bag source material.

## The 12 weeks

### Foundations
- **Week 1 — Boxes & arrows: the 4 diagrams + Mermaid.** Learn dependency, data-flow,
  sequence, state diagrams. Redraw a system you already know. (Track A bias)
- **Week 2 — Dependency direction & the Stable Dependencies Principle.** Retrofit the
  theory onto a "what belongs in Core" split you've made before. (Track A)
- **Week 3 — Modelling before mechanism: ownership, invariants, consistency.** Redo the
  "3 independent screens, one consistent source of truth" problem — model first. (Track B)
- **Week 4 — Abstraction seams: when to reuse, when to duplicate.** Retrofit onto a
  screen-reuse call you've made. The Rule of Three, premature abstraction. (Track B)

### Applied
- **Week 5 — Module boundaries at scale: acyclic dependencies, layering, leaf packages.**
  Map a real module graph; find a cycle or a wrongly-placed type. (Track A)
- **Week 6 — Unidirectional data flow, deconstructed.** Derive SSR / TCA / MVVM from first
  principles. What problem does each solve? Where do they hurt? (Track B)
- **Week 7 — Critique clinic.** Take an existing architecture (yours or open-source),
  diagram it, list its failure modes and blockers *before* code. (fuse A+B)
- **Week 8 — Designing for change & testability as an architectural property.** How
  boundaries make things mockable/replaceable. (fuse A+B)

### Ownership
- **Week 9 — Cold brief → design doc.** Take a PO-style one-paragraph feature brief.
  Produce model, diagrams, boundary decisions, and named tradeoffs. No code.
- **Week 10 — Dependency-graph refactor proposal.** Pick a real messy area, propose a
  staged (deprecate-then-remove) modularisation with a before/after graph.
- **Week 11 — Brown-bag build.** Turn one `reference/` principle into a 20-min talk with
  draw.io slides. Rehearse the argument, not just the slides.
- **Week 12 — Deliver + retrospect.** Give the brown-bag (or dry-run to me). Review the
  12-week diff of your diagrams. Re-assess the profile. Plan the next block.

## Ground rules

- Model and diagram **before** writing or choosing a mechanism. Every week enforces this.
- Every principle you learn gets **named and written down** in `reference/` — if you can't
  name it, you can't defend it in an MR or teach it.
- Prefer Mermaid while thinking (fast, diffable). Polish in draw.io only for the brown-bag.
- Commit your session output each week. The git history IS the evidence of growth.

## Progress

- [ ] Week 1  - [ ] Week 2  - [ ] Week 3  - [ ] Week 4
- [ ] Week 5  - [ ] Week 6  - [ ] Week 7  - [ ] Week 8
- [ ] Week 9  - [ ] Week 10 - [ ] Week 11 - [ ] Week 12
