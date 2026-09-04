# Developer Profile — Calibration

_Private calibration notes so the learning plan targets a real gap, not an invented one.
Derived from ~3.5 years of my own commit history. Update as evidence changes._

## Self-assessment (own words)

- Newly promoted senior. Wants depth in architecture, system design, modularisation.
- Weakest: **system design** (client-side app architecture at scale).
- Strong, clean coder. "All-rounder, master of none."
- Thinks in head, then codes. Wants to **externalise** thinking — especially diagrams.
- Goal skills: produce architecture diagrams; run brown-bag sessions.
- Wants portable iOS knowledge, not tied to one employer's codebase.

## Focus order

1. **Modularisation & dependency graphs** (primary) — framed as "SOLID scaled up",
   avoiding long-term tech debt, code that "fits in".
2. **Data flow / architecting a feature from a product brief** (close second) — wants to be
   able to invent something like a Screen-Store-Router pattern, see its flaws, and improve it.

## Evidence from my own past work (patterns, generalised)

- **A core-UI modularisation (2024).** Pushed higher-level components (tiles, cells,
  accordions) *out* of a shared "core" package, keeping only primitives (colours, fonts, one
  input accessory). This is the **Stable Dependencies Principle** by instinct — and the
  instinct was correct. The judgement of *where the line goes* was never written down.
- **A screen-reuse refactor (2022).** Collapsed a near-duplicate parallel journey and reused
  a shared screen; net deletion. Good "don't build the 90%-duplicate" instinct. The seam
  reasoning (why reuse was safe here) was never externalised.
- **A composite-key cache fix.** Modelled identity correctly with a composite `Hashable` key
  so two logically-distinct entries stopped colliding. Sharp micro-level identity modelling.
- **A type-safe event-factory refactor.** The *direction* came from a mentor; I implemented
  it on intuition. The boundary/deprecation of the old API was left unresolved because the
  model wasn't mine to own. I'm good at executing a handed-down design — not yet the person
  whose model it is.

## The through-line (the actual gap)

Instincts and taste about boundaries/reuse are **already strong** — visible consistently
across years. The gap is that the model **lives in my head**: rarely written, rarely
diagrammed, rarely argued from a *named* principle.

Can't yet reliably: teach where the line goes, defend it in review, or generalise it into a
principle others can apply. That is the senior→staff move.

## Implication for the plan

- Don't teach taste — it's there. Teach **externalisation**: model → boundaries → diagram →
  named principle → *then* mechanism.
- Default failure mode: jumping to mechanism (reactive streams, pub/sub, type tricks) before
  nailing the model (ownership, invariants, consistency, boundaries). Every week drills
  top-down discipline against that.
- Retrofit theory onto decisions already made well ("that core-UI split was Stable
  Dependencies — here's the name and the rule"). Powerful because the instinct is proven.

## Logistics

- 1 afternoon/week, ~2h baseline (can stretch to 3). Progressive: study → hands-on.
- 12-week block, then re-evaluate.
- Diagrams: **Mermaid for thinking** (diffable, checked-in), **draw.io for polish**.
- Public repo — keep everything here generic and employer-neutral.
