---
project: friend-companion
date: 2026-04-14
author: Sjoerd
status: in-progress
---

# AGENTS.md

---

## Project Overview

- **Project name:** friend-companion _(working title — final name TBD)_
- **One-line description:** A personal companion app that helps the owner stay better in touch with friends by remembering details about them and nudging well-timed follow-ups, meet-ups, and reminders.
- **Project type:** new product
- **Primary user(s):** The owner (self-use, single-user app). Friends appear in the app as subjects/contacts — they do NOT install or use the app.
- **Key outcome:** TBD — to be defined in Step 5 (Decide) once hypotheses are validated.
- **Project phase:** discovery
- **Related repo(s):** _(none yet — code only starts after Step 5 GO decision)_

---

## Project Classification

_Filled during intake 2026-04-14._

- **User complexity:** single user type
- **Stakeholder landscape:** solo
- **Input triggers:** designer initiative (no external business request, no user feedback, no technical trigger)
- **Existing documentation:** none

**Depth scaling** (derived from classification — per discovery skill):
- Step 1: hypotheses-only framing (greenfield; no current-state analysis)
- Step 3: one research method, one guide
- Step 6: quick self-check only

### Known Personas

| Persona | Role/Description | Primary Flow |
|---------|-----------------|--------------|
| The owner | The sole user of the app — uses it to keep better track of their own friendships. | Capture a note about a friend → get nudged at the right time → message / meet / follow up |

### Known Stakeholders

None. Solo designer / solo product.

_Note: friends are **data subjects** (notes are stored about them) but are not stakeholders or users. Treat their implied interests as an ethics constraint, not as a decision input._

---

## Workflow Philosophy

**Prototype IS the spec. Ship working things, not documents.**

- Prefer a working prototype over a long specification document. If you can show it, don't just describe it.
- Documents exist to support decisions, not to replace demonstrations.
- When a document and a prototype conflict, the prototype is the source of truth.

---

## Research Principles

**Every insight must link to a source. Disconfirming evidence is mandatory.**

- Never state a user need or market fact without linking to evidence (interview quote, data point, published study).
- Actively seek disconfirming evidence for every hypothesis. If you cannot find any, you have not looked hard enough.
- Distinguish "we observed X" (evidence) from "we believe Y" (interpretation) and label each.
- Prefer direct quotes over paraphrased summaries.

**Designer-initiative self-delusion risk is explicit.** This project originated from the owner's personal frustrations only — no external feedback or data. Therefore:

- Step 2 must actively look for competitors who tried this and failed, and for evidence that users DON'T feel the pain acutely.
- Step 3 must include interview questions designed to disconfirm the pain (ask about past behavior, not stated preference).
- At every step, ask: "Are we building a solution only the designer wants?"

---

## Product Direction (captured during Intake — not yet validated)

These are the designer's current inclinations. None are decisions yet — all are tested by the discovery process.

- **Ingestion model:** voice + text input, processed by an LLM for categorization and smart logic (e.g., tagging, reminder timing, suggestion generation).
- **Platform:** mobile-first. A web prototype is acceptable for concept validation, but **true native reminders are a first-class requirement** — so React Native (Expo) or native iOS is the realistic long-term path.
- **Privacy (v1):** the app is private to the owner and runs in a trusted personal environment, so v1 does **not** require end-to-end encryption. Encryption becomes a hard requirement if the scope ever expands beyond single-user.
- **Friends-as-subjects constraint:** even without a formal consent flow, designs must respect that notes describe real people. Avoid features that would be harmful or embarrassing if a friend saw them.

---

## Known Blind Spots (carried forward from Intake)

1. **Friends are data subjects without a voice.** No consent flow, no visibility for the person being described. Carry this as a design constraint into every step.
2. **Ingestion design is wide-open.** Voice+text+LLM is the stated inclination — but whether that actually matches real friction is an open hypothesis. Do not lock it in before Step 4.
3. **Native reminders constrain platform choice.** Reliable OS-level reminders rule out a pure web app. This narrows Step 5's prototype options.
4. **Designer-initiative-only = high self-delusion risk.** Always the loudest blind spot on this project. Call it out at every step boundary.

---

## Code Principles

_Apply when code is introduced (after Step 5 GO decision)._

**Explore → Plan → Code. Run tests. Small commits.**

1. **Explore** — Read relevant code before writing.
2. **Plan** — Outline changes before making them.
3. **Code** — Follow existing conventions.
4. **Test** — Run tests before committing.
5. **Commit** — Small, focused commits.

---

## File Structure Conventions

```
friend-companion/
  AGENTS.md              # This file
  research/              # Discovery artifacts (one per step)
    hypothesis-sheet.md
    competitor-teardown.md
    market-research.md
    research-plan.md
    interview-guide.md
    interview-notes.md
    evidence-log.md
    research-synthesis.md
    user-persona-owner.md
    jtbd-canvas.md
    prototype-brief.md
    stakeholder-brief.md
  docs/
    decisions/
      decision-log.md    # Append-only
```

`CLAUDE.md` (tech-stack config) will be added after Step 5 if the decision is GO.

---

## Behavioral Rules

- **When uncertain, ASK rather than assume.** Better to ask one question than redo work.
- Never delete research files without explicit confirmation.
- When a decision could go multiple ways, present options with trade-offs and recommend one with reasoning — don't pick silently.
- If evidence contradicts the current plan, surface it immediately.
- Proactively flag blind spots as they appear, not only at checkpoints.

---

## Artifacts Reference

| Artifact | Project Path | Created During |
|----------|-------------|----------------|
| Hypothesis Sheet | `research/hypothesis-sheet.md` | Discovery Step 1 |
| Competitor Teardown | `research/competitor-teardown.md` | Discovery Step 2 |
| Market Research | `research/market-research.md` | Discovery Step 2 |
| Research Plan | `research/research-plan.md` | Discovery Step 3 |
| Interview Guide | `research/interview-guide.md` | Discovery Step 3 |
| Interview Notes | `research/interview-notes.md` | Discovery Step 3 (copy per interview) |
| Evidence Log | `research/evidence-log.md` | Discovery Step 4 (append) |
| Research Synthesis | `research/research-synthesis.md` | Discovery Step 4 |
| User Persona | `research/user-persona-owner.md` | Discovery Step 4 |
| JTBD Canvas | `research/jtbd-canvas.md` | Discovery Step 5 |
| Prototype Brief | `research/prototype-brief.md` | Discovery Step 5 (if GO) |
| Stakeholder Brief | `research/stakeholder-brief.md` | Discovery Step 6 |
| Decision Log | `docs/decisions/decision-log.md` | Append at each decision |

Single-persona, solo project — so `system-flow-map.md`, `stakeholder-raci.md`, and `impact-analysis.md` are NOT produced.

---

## Project-Specific Notes

- **This project lives INSIDE the Sociabl tooling repo** as a subfolder (`friend-companion/`), explicitly chosen so the existing GitHub remote provides backup for discovery artifacts. It is not application code — only markdown research. When this moves to implementation (post-Step 5 GO decision), it will be extracted into its own repository.
- **No commercial goal stated.** The owner is building this for themselves. Success is personal utility, not revenue — until/unless the owner decides otherwise.
- **Reminder reliability is the load-bearing feature.** If reminders aren't reliable and well-timed, the app has no job to do. Any technical choice that weakens reminders is a red flag.
