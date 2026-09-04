# Week 1 — Boxes & Arrows: the 4 diagrams + Mermaid

**Track bias:** A (modularisation)  ·  **Shape:** study-heavy  ·  **Time:** ~2h (stretch 3)

**Goal of the week:** start externalising. By the end you can produce all four diagram
types in Mermaid and you've redrawn a system you already understand — proving the tool,
not learning new domain.

## Why this is first

Your whole growth edge is that your model lives in your head. You can't fix that until you
have a fast, low-friction way to get it onto a page. Diagrams are that way. This week is
deliberately about a system you already know cold, so the *only* new thing is the
externalising skill.

## Study (~45 min)

1. Read `reference/mermaid-primer.md`. Open https://mermaid.live and paste each of the four
   examples. Change something in each and watch it re-render. Get the feedback loop in your hands.
2. Fix the four questions in your mind — they matter more than syntax:
   - Dependency graph: _should this arrow exist, and does it point at the stabler thing?_
   - Data-flow: _where's the single source of truth; who mutates vs. observes?_
   - Sequence: _what if two of these overlap?_
   - State: _can I represent an illegal state?_

## Hands-on (~60–75 min)

Pick a **feature you already know well** (from work or a side project — doesn't matter, this
is about the skill). Produce all four diagrams of it, in Mermaid, saved under
`diagrams/week-01/`:

1. `dependency.mmd` — the modules/types it depends on, arrows in dependency direction.
2. `data-flow.mmd` — where its state lives, who mutates, who observes.
3. `sequence.mmd` — one key interaction (e.g. load-then-refresh) over time.
4. `state.mmd` — the states its main screen/model can be in.

Constraint that trains the real habit: **draw each diagram before you look at the code.**
Draw it from your mental model first. _Then_ open the code and mark (in the session notes
below) every place your mental model was wrong or vague. Those gaps are the whole point —
they're the bits that were fuzzy in your head and would have stayed fuzzy without the diagram.

## Output (fill in)

- Feature chosen:
- Diagrams committed: [ ] dependency [ ] data-flow [ ] sequence [ ] state
- Where my mental model was wrong/vague vs. the actual code:
  -
  -

## Reflection (fill in)

- Which of the four diagrams was hardest to draw? (That's likely your weakest modelling axis.)
- Did drawing surface a question you'd never have asked before coding?
- One sentence: what did externalising show you that thinking-in-head hadn't?

## Definition of done

- [ ] Four `.mmd` files under `diagrams/week-01/`
- [ ] Output + Reflection filled in
- [ ] Committed (`git add . && git commit`) — this is your week-1 baseline in the history
