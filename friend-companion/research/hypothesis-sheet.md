---
project: friend-companion
date: 2026-04-15
author: Sjoerd
status: complete
phase: discovery
template: hypothesis-sheet
---

# Hypothesis Sheet

> Hypotheses are falsifiable statements about our beliefs. They exist to be tested, not confirmed.

---

## Problem Context

The designer experiences friendship drift despite caring about his friends. The most acute case: a close friend whose friendship was held together by a recurring weekend cycling + family ritual. A health condition (SUNCT) ended the cycling; medication-related memory issues, parenting load, and fatigue compounded the drift; aversion to chat apps (WhatsApp, Instagram) removed the usual keep-in-touch fallback. The painful moment is not "I didn't message" — it is "I didn't know [friend] was on holiday in France." The failure is _awareness_ and _relationship texture_, not _communication volume_.

The product hypothesis: a **personal relationship-memory** tool — voice/text capture with LLM categorization, mobile-first with native reminders, private from the friends themselves, optimizing for **reassurance** rather than productivity.

**Key context (from Intake):**
- New product, greenfield, solo designer, single-user app
- Designer initiative only (no external feedback/data) → high self-delusion risk
- No primary user testing planned at this stage → we lean hard on secondary research

---

## Hypothesis H1 — Ritual-Loss Hypothesis

**ID:** H1
**Status:** `untested`
**Last updated:** 2026-04-15
**Persona linkage:** The owner (sole persona)

**We believe** adults 30–55 who had a close friendship anchored in a recurring shared activity
**struggle with** acute friendship drift once that activity stops
**in the context of** life changes (health, relocation, parenting, career).

**True if:**
- Secondary sources (Reddit, published studies on adult friendship decline) show ≥3 accounts of friendships fading specifically after a ritual/activity ended
- The designer can name ≥2 additional friendships of his own where the same pattern holds
- Adjacent competitors (Dex, Clay) discuss "last activity" separately from "last contact" in their UX or marketing

**False if:**
- Secondary accounts frame drift as generic busyness with no ritual-loss trigger
- The designer can't reproduce the pattern in other friendships — this one is idiosyncratic
- Competitor research shows the category treats friendships as undifferentiated "contacts"

**Cheapest test:** Reddit sweep (r/askmenover30, r/adulting, r/friendship, r/AskMenOver25), Substack essays on adult friendship decline, review of the Surgeon General's 2023 loneliness report.

**Stop criteria:** If <2 secondary sources name ritual-loss explicitly, pivot framing to a broader "life-transition drift" model. The product survives; the positioning changes.

**Evidence collected:**
| Date | Source | Finding | Confirms/Disconfirms | Confidence |
|------|--------|---------|----------------------|------------|
| 2026-04-15 | Designer interview (Step 1) | Cycling + kids ritual ended due to SUNCT → friendship faded | Confirms (n=1, designer) | Low (self-selected) |

---

## Hypothesis H2 — Relational-Memory Hypothesis ⭐

**ID:** H2
**Status:** `untested` (directional support already collected)
**Last updated:** 2026-04-15
**Persona linkage:** The owner

**We believe** cognitively-loaded adults who care about inner-ring friendships
**struggle with** existing contact/CRM tools because those tools feel transactional and businessy — they want a product that models _the relationship itself_ (user's voice per friend, shared history, ongoing context), not a cadence tracker
**in the context of** having personal (not professional) friendships they are trying not to let drift.

**True if:**
- App Store / Reddit reviews of Dex, Clay, Monica, UpHabit cluster around phrases like "feels transactional", "too businessy", "generic", "feels fake", "LinkedIn-y", "cold"
- Reddit threads in r/productivity or r/askmenover30 describe friendship-CRMs as "not for real friends"
- Target users, when shown a traditional CRM, spontaneously describe wanting the tool to "know them" or "know our history"

**False if:**
- Competitor reviews show satisfaction with last-contact + notes model
- Users find CRM features sufficient and don't describe a "feels fake" quality
- Designer reverses his read on Dex after a genuine trial (two weeks of use)

**Cheapest test:** App Store + Reddit + Trustpilot + G2 review scraping for Dex, Clay, Monica, UpHabit, Nat, Hippo. Keyword hunt: `transactional|businessy|generic|fake|LinkedIn|cold|forced|template`.

**Stop criteria:** If competitor reviews don't show the "feels fake" pattern AND the designer retracts his Dex reaction after real use, the reframe is wrong — build a thinner layer on top of a conventional contact model instead.

**Evidence collected:**
| Date | Source | Finding | Confirms/Disconfirms | Confidence |
|------|--------|---------|----------------------|------------|
| 2026-04-15 | Designer reaction to Dex | "Too focused on LinkedIn stuff and business. I really need something more personal that knows me, my friends, how I'd speak to them and what our history is." | Confirms (directional) | Medium (designer, but unprompted and specific) |

---

## Hypothesis H3 — Reassurance-Not-Productivity Hypothesis

**ID:** H3
**Status:** `untested`
**Last updated:** 2026-04-15
**Persona linkage:** The owner

**We believe** a friendship tool that feels like _peace of mind_ retains users longer than one that feels like _productivity_ (streaks, scores, "you're behind on Anna")
**in the context of** adults who experience shame / guilt about friendship drift already, and who don't want to be reminded of their inadequacy by the very tool trying to help.

**True if:**
- 1–2 star reviews of Dex / Clay / Monica cluster around words like "guilt", "pressure", "made me feel worse", "anxiety", "nagging"
- App teardowns show the tools that survive in this category avoid streak/score patterns
- The designer reacts negatively to productivity-style UI when shown mock variants (informal)

**False if:**
- Negative reviews of competitors cluster elsewhere (bugs, pricing, not around guilt)
- Productivity-style competitors retain users well
- The designer finds productivity patterns motivating rather than stressful

**Cheapest test:** Tag negative reviews of the 4-5 competitors already scheduled for H2's scrape; add this keyword cluster to the same pass. Zero marginal effort.

**Stop criteria:** If productivity-style framing outperforms on retention in competitor analytics OR if no "guilt" pattern appears in reviews, follow conventional consumer-CRM emotional design.

**Evidence collected:**
| Date | Source | Finding | Confirms/Disconfirms | Confidence |
|------|--------|---------|----------------------|------------|
| 2026-04-15 | Designer interview (Step 1) | Target feeling on app open: "reassurance because everything is okay" | Confirms (n=1, designer) | Low (self-selected) |

---

## Hypothesis H4 — Capture-Effort Hypothesis

**ID:** H4
**Status:** `untested` — open technical risk
**Last updated:** 2026-04-15
**Persona linkage:** The owner

**We believe** voice + text + LLM-extracted capture is adoptable IF AND ONLY IF the end-to-end cycle ("thought I want to save" → "saved") stays under 30 seconds in micro-moments (breaks, post-hangout, in bed, on the toilet).

**True if:**
- A Wizard-of-Oz prototype gets the designer capturing ≥3 times per week for 2 consecutive weeks without prompting
- Cycle time stays under 30 seconds for >70% of captures
- Voice-noting feels natural in the designer's actual contexts (not awkward in public / around family)

**False if:**
- Capture cycle exceeds 30 seconds
- LLM misclassification forces manual cleanup that kills the time budget
- Voice capture feels awkward in real contexts — especially the micro-moments named

**Cheapest test:** Telegram bot or iOS Shortcut that accepts voice notes → human-in-the-loop categorization → returns formatted entry. Run with the designer (only) for 2 weeks. _(Deferred — no primary testing planned.)_

**Stop criteria:** If this hypothesis can't be validated without testing, carry it as an **open risk** into the Step 5 prototype brief. Do not commit to voice-first architecture until this is resolved.

**Known secondary risk:** WhatsApp as a data source (mentioned during Step 1) is a Meta walled-garden problem. Workarounds exist (Android backup parsing, chat export) but are brittle. Treat as a v2+ feature, not a v1 requirement. If H4 only works with WhatsApp-mining, the whole ingestion model is fragile.

**Evidence collected:**
| Date | Source | Finding | Confirms/Disconfirms | Confidence |
|------|--------|---------|----------------------|------------|
| | | | | |

---

## Hypothesis H5 — Beyond-Designer Hypothesis (mandatory disconfirming)

**ID:** H5
**Status:** `untested`
**Last updated:** 2026-04-15
**Persona linkage:** The owner — and the open question of whether "the owner" generalizes to a market

**We believe** the pain the designer feels — caring about friendships but losing them to cognitive load, chat-aversion, ritual-loss, and drift — is shared across enough _different_ life contexts (parents, health-affected, caregivers, post-relocation singles) to constitute a real market, not an n=1 frustration.

**True if:**
- Secondary sources show this pain pattern in ≥3 distinct life-context types (not just parents, not just health-affected)
- At least one well-known public figure, journalist, or researcher has named the same problem in the last 18 months
- Reddit threads on adult friendship show engagement (upvotes, comment counts) consistent with a painful problem, not a fringe one
- The adult friendship decline literature (Surgeon General loneliness report 2023, BYU longitudinal studies, Stephanie Cacioppo's work) supports that the decline is cross-demographic

**False if:**
- The pain pattern only shows up in profiles demographically close to the designer (35–55, parents, health issue)
- Secondary sources show most adults are content with their friendship trajectories
- Existing habits (calendars, group chats, regular standing plans) already solve this for most people

**Cheapest test:** Targeted secondary-research sweep:
- Surgeon General's 2023 loneliness advisory
- Reddit threads in r/friendship, r/adulting, r/askmenover30, r/Mommit, r/caregivers, r/ChronicIllness
- Substack essays on adult friendship (Anne Helen Petersen's _Culture Study_, Mandy Brown, Dan Cohen)
- Academic: Rawlins' work on adult friendship, Dunbar's number, BYU loneliness studies
- Journalism: Atlantic, NYT, The Cut in the last 18 months

**Stop criteria:** If the pain only appears in designer-like profiles, reframe the project as "a personal tool for me" and drop product ambitions. Do not build for a market that doesn't exist.

**Evidence collected:**
| Date | Source | Finding | Confirms/Disconfirms | Confidence |
|------|--------|---------|----------------------|------------|
| | | | | |

---

## Prioritization

| Hypothesis | Persona | Risk if Wrong | Ease of Testing | Priority | Test Order |
|------------|---------|---------------|-----------------|----------|------------|
| H5 — Beyond-designer | The owner | **High** — if wrong, product is n=1 and should stop | **Easy** (secondary only) | **P1** | 1 |
| H2 — Relational-memory | The owner | **High** — if wrong, we're building Dex-lite with no edge | **Easy** (review scraping) | **P1** | 2 |
| H1 — Ritual-loss | The owner | **Medium** — wrong → positioning shifts, product survives | **Easy** (secondary sources) | **P2** | 3 |
| H3 — Reassurance-not-productivity | The owner | **Medium** — wrong → emotional framing flips, design iterates | **Easy** (piggybacks on H2 scrape) | **P2** | 4 |
| H4 — Capture-effort | The owner | **High** — wrong → ingestion architecture collapses | **Hard** (requires testing we aren't doing) | **P3 — carry as open risk** | Deferred to Step 5 |

**Prioritization rationale:**

H5 first because if the designer is the only person who feels this pain, everything else is moot. It is cheap to test via secondary research and it directly addresses the designer-initiative self-delusion risk we flagged at Intake.

H2 second because it is the core positioning bet. If "relational memory, not CRM" doesn't hold up against competitor reviews, we are quietly building Dex-lite. The designer already gave directional support (reacting to Dex as "too LinkedIn / businessy"), which is encouraging but n=1.

H1 and H3 are P2 because they inform positioning and emotional design but wouldn't stop the project if they proved wrong — they would reshape it.

H4 is P3 because it can't be validated honestly without testing, which is off the table for now. The sensible move is to carry it as an **open, named risk** into the Step 5 prototype brief rather than pretending we have signal we don't.

---

## Summary Tracker

| ID | One-line Summary | Persona | Status | Key Evidence | Updated |
|----|------------------|---------|--------|--------------|---------|
| H1 | Ritual-loss is what kills adult friendships | Owner | untested | Designer interview (n=1) | 2026-04-15 |
| H2 | Users want relational memory, not a CRM | Owner | untested (directional) | Designer reaction to Dex | 2026-04-15 |
| H3 | Reassurance > productivity for friendship tools | Owner | untested | Designer interview (n=1) | 2026-04-15 |
| H4 | Voice + LLM capture viable only if <30s cycle | Owner | untested — open risk | None | 2026-04-15 |
| H5 | Designer's pain generalizes across life contexts | Owner | untested | None | 2026-04-15 |

---

## Known Blind Spots Carried Into Step 2

1. **Friend privacy** — app is secret from the friends themselves. Design constraint, not hypothesis.
2. **WhatsApp-mining viability** — technical risk, not framing hypothesis. Flagged in H4.
3. **Subscription dynamics** — are friendships a recurring-revenue problem, or a transitional one? Defer to Step 5 business model.
4. **Designer-initiative self-delusion** — H5 is the primary defense. Keep it on the front of every step.
