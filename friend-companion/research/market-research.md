---
project: friend-companion
date: 2026-04-26
author: Sjoerd
status: complete
phase: discovery
template: market-research
---

# Market Research

> The friend-companion app sits at the intersection of two trends: the well-documented "friendship recession" and the failure of existing personal CRM tools to address personal (non-professional) relationships. This document maps the evidence.

---

## 1. Market Definition

**What market are we in?**

> Personal relationship management tools for non-professional use — specifically, software that helps individuals maintain and deepen personal friendships by remembering context, nudging follow-ups, and reducing the cognitive load of staying in touch.

**Market category:** Personal CRM / Relationship Management (personal segment)

**Adjacent markets:** Professional networking CRMs (Dex, Clay), journaling apps (Day One), reminder/habit apps (Todoist, Streaks), messaging platforms (WhatsApp, iMessage)

**How we define the boundary:**
> We include tools whose primary job is helping users maintain personal relationships (friends, family, non-work contacts). We exclude professional CRMs (HubSpot, Salesforce), professional networking tools (LinkedIn, Dex in its primary positioning), and general-purpose note/reminder apps unless they are explicitly marketed for relationship management.

---

## 2. Market Size

> Traditional TAM/SAM/SOM analysis is difficult here because the "personal friendship CRM" category barely exists as a market. Instead, we estimate from the demand side: how many people experience the problem, and what's a reasonable willingness-to-pay?

### Demand-Side Sizing

| Metric | Value | Source | Date | Confidence |
|--------|-------|--------|------|------------|
| US adults experiencing "significant loneliness" | ~44 million | Gallup poll cited in Surgeon General advisory | Feb 2023 | High |
| US adults with no close friends | 12% (~31 million) | American Perspectives Survey (AEI/Survey Center on American Life) | May 2021 | High |
| US adults who lost a best friend (1990→2021) | 75% → 59% had a best friend (16pp decline) | American Perspectives Survey | May 2021 | High |
| Adults 30-55 who are parents (our core ICP overlap) | ~60 million in US | US Census estimates | 2023 | Medium |

### Bottom-Up Estimate

| Assumption | Value | Reasoning |
|------------|-------|-----------|
| Adults who care enough about friendship drift to try a tool | ~2-5% of the 44M lonely adults | Most will not seek a software solution; mirrors typical adoption for personal productivity tools |
| Addressable "would try" population | ~900K–2.2M in US alone | Conservative; European markets (NL, UK, DE) add ~30-50% |
| Willingness to pay | €10/month (designer's stated price point) | Aligned with Monica ($9/mo) and below Dex ($12/mo) |
| Realistic Year 3 conversion (if product works) | 0.1–0.5% of addressable | Comparable to niche consumer subscription apps |
| Year 3 revenue range | €10K–€130K ARR | This is a personal tool first; commercial viability is secondary |

**Key takeaway:** This is not a venture-scale market. It is a viable personal/indie project. The designer stated no commercial goal — success is personal utility, not revenue.

---

## 3. The Friendship Recession — Evidence Base

### Core Statistics

| Finding | Statistic | Source | Date | Confidence |
|---------|-----------|--------|------|------------|
| Americans with no close friends | Quadrupled from 3% (1990) to 12% (2021) | American Perspectives Survey, Survey Center on American Life | May 2021 | High |
| Americans with 10+ close friends | Dropped from 33% (1990) to ~13% (2021) — nearly threefold decline | American Perspectives Survey | May 2021 | High |
| Americans with a best friend | Dropped from 75% (1990) to 59% (2021) | American Perspectives Survey | May 2021 | High |
| Young adults (15-24) social interaction decline | 70% less in-person social interaction than two decades ago | Surgeon General Advisory | May 2023 | High |
| Americans experiencing significant loneliness | ~44 million adults (18+) | Gallup poll, cited in Surgeon General Advisory | Feb 2023 | High |
| Americans with no close friends (Pew) | 8% | Pew Research Center | Oct 2023 | High |
| Gender gap | Men experienced the steepest decline in close friendships | American Perspectives Survey | May 2021 | High |

### Health Impact

| Finding | Source | Date | Confidence |
|---------|--------|------|------------|
| Loneliness increases risk of premature death by 26% | Surgeon General Advisory (citing Holt-Lunstad meta-analyses) | 2023 | High |
| Social isolation comparable to smoking 15 cigarettes/day | Surgeon General Advisory (citing Holt-Lunstad 2010, 2015) | 2023 | High |
| Loneliness increases heart disease risk by 29% and stroke risk by 32% | Surgeon General Advisory (citing Valtorta et al. 2016) | 2023 | High |
| Social connection is a "significant predictor of longevity and better physical, cognitive, and mental health" | Surgeon General Advisory | 2023 | High |

### What Drives the Decline

| Driver | Evidence | Relevance to Friend-Companion |
|--------|----------|-------------------------------|
| Life transitions (parenting, relocation, career changes) | Friendship decline accelerates during major life transitions; the designer's own experience with SUNCT/parenting matches this pattern | **Direct** — the core use case |
| Loss of shared rituals/activities | When the recurring activity that anchored a friendship stops, the friendship drifts without a replacement mechanism | **Direct** — H1 (ritual-loss hypothesis) |
| Digital communication replacing in-person contact | More screen time, less face time; but digital tools don't maintain relationship depth | **Indirect** — the app must avoid becoming "just another screen" |
| Cognitive overload | Working parents, caregivers, and health-affected adults lack the mental bandwidth to maintain friendship proactively | **Direct** — voice/LLM capture targets this |
| Stigma around expressing friendship needs | Adults (especially men) find it awkward to say "I miss my friends" or to proactively reach out | **Indirect** — reassurance-first design addresses this |

---

## 4. Growth Trends

| Trend | Direction | Evidence | Source |
|-------|-----------|----------|--------|
| Public awareness of loneliness epidemic | Growing | Surgeon General Advisory (May 2023) made national news; ongoing media coverage in Atlantic, NYT, NPR | Multiple, 2023-2026 |
| "Friendship recession" as a cultural concept | Growing | Term coined by Survey Center on American Life; widely adopted by media | AEI, 2021 |
| AI-powered personal tools | Growing | LLM capabilities now enable voice→structured-data pipelines that weren't feasible 2 years ago | Industry trend |
| Personal CRM startup activity | Declining/consolidating | Clay acquired by Automattic; UpHabit pivoted to enterprise; multiple shutdowns documented by Dex | Competitor research |
| Consumer willingness to pay for personal software | Stable/low | Most personal tools struggle with subscription fatigue; free alternatives (Notes, spreadsheets) are "good enough" for many | Indie Hackers thread, App Store trends |

**Tailwinds:**
- Surgeon General Advisory created mainstream awareness and destigmatized the problem
- LLM + speech-to-text technology makes voice-first capture viable for the first time
- Remote/hybrid work means fewer organic friendship touchpoints, increasing need for intentional tools
- Media coverage (Atlantic, NYT, NPR, Substack) keeps the topic in public discourse

**Headwinds:**
- Personal CRM category has a high failure rate — most startups shut down or pivot within 1-2 years
- Subscription fatigue for personal tools (users pay for Netflix, not for friendship apps)
- "Good enough" substitutes (WhatsApp, calendar, memory) have zero switching cost
- The people most affected by friendship drift are the least likely to adopt a new tool (cognitive load paradox)

---

## 5. Technology Trends

| Trend | Relevance to Us | Timeframe | Implication |
|-------|-----------------|-----------|-------------|
| LLM-powered voice-to-structured-data | **Critical** | Now | Core architecture depends on this; Whisper + GPT-4 class models make it feasible |
| On-device AI (Apple Intelligence, Gemini Nano) | High | 1-2 years | Could enable private, on-device processing — addresses privacy concerns without server costs |
| Native iOS/Android speech APIs | High | Now | Reduces dependency on third-party speech-to-text; lowers latency for voice capture |
| WhatsApp Business API / chat export | Medium | Uncertain | WhatsApp mining is a Meta walled-garden problem; Android backup parsing exists but is brittle; treat as v2+ |
| Notification intelligence (iOS Focus modes, Android priority) | Medium | Now | Reminder timing must respect OS-level Do Not Disturb; poorly-timed reminders will be muted or cause uninstalls |

---

## 6. Regulatory & Compliance

| Regulation / Requirement | Relevance | Impact on Product | Timeline |
|--------------------------|-----------|-------------------|----------|
| GDPR (notes about friends are personal data about identifiable individuals) | **High** | Even for single-user app: if data is stored on a server, GDPR applies to the friends' data. Self-hosted or on-device storage simplifies compliance. | Now |
| Apple App Store review guidelines (privacy nutrition labels) | High | Must declare data collection practices; "notes about other people" is a sensitive category | At submission |
| WhatsApp Terms of Service (automated access / scraping) | Medium | Automated WhatsApp data extraction violates ToS; chat export is manual and user-initiated (likely compliant) | v2+ |
| Right to erasure (friend asks to be removed) | Medium | Even without formal consent flow, the ethical design principle says: if a friend asks, their data should be deletable | v1 design constraint |

---

## 7. Customer Segments

| Segment | Est. Size (individuals) | Pain Level (1-5) | Willingness to Pay | Accessibility | Priority |
|---------|------------------------|-------------------|---------------------|---------------|----------|
| Parents 30-45 with friendship drift | ~15-20M (US) | 4 | Low-Medium (€5-10/mo) | Medium — reachable via parenting communities, Reddit | 1st (designer's segment) |
| Health-affected adults (chronic illness, disability) | ~5-10M (US) | 5 | Low (€5-10/mo) | Low — fragmented communities | 2nd (designer's personal experience) |
| Post-relocation adults (moved cities, lost local network) | ~8-12M (US, annually) | 3 | Low-Medium | Medium — reachable via expat/relocation communities | 3rd |
| Remote workers who lost office friendships | ~20-30M (US) | 2 | Low | High — reachable via tech/remote-work communities | Deprioritized (pain is lower) |

**Segment selection rationale:**
> The designer is building for themselves first (parent, health-affected). These segments have the highest pain and the most direct need for a memory-augmentation tool. Remote workers have lower pain because they typically maintain digital contact; their friendships drift slower.

---

## 8. Disconfirming Evidence

> What evidence suggests this product might not work, even if the pain is real?

| Belief | Disconfirming Evidence | Source | Severity |
|--------|------------------------|--------|----------|
| People want a dedicated tool for friendship maintenance | Most people use WhatsApp/iMessage group chats and consider them "good enough." The Indie Hackers thread shows users defaulting to Excel or doing nothing. | Indie Hackers thread, 2023 | **High** |
| The personal CRM market can sustain products | UpHabit pivoted to enterprise (Salesforce integration) after failing to grow on personal use alone. Dex's own blog documents "20+ startups, apps, and failed attempts." Clay was acquired rather than scaling independently. | Competitor research, Dex blog | **High** |
| Voice + LLM capture will lower friction enough for adoption | Zero competitors have shipped voice-first capture — this could mean it's an untapped opportunity, OR that it doesn't work in practice. No evidence either way. | Competitor feature comparison | **Medium** (unknown, not disproven) |
| The friendship recession creates market demand for tools | The Surgeon General Advisory recommends community programs, policy changes, and in-person connection — not apps. "Technology" appears as a cause of isolation, not a solution. | Surgeon General Advisory, 2023 | **Medium** |
| Adults will pay a subscription for a friendship tool | Monica's pricing ($9/mo) and UpHabit's ($30/year) suggest low willingness-to-pay. No personal CRM has achieved meaningful consumer subscription scale. | Pricing data across competitors | **Medium** |

---

## 9. Wedge Hypothesis

**Wedge statement:**
> We will enter the personal relationship management space by building a voice-first, LLM-powered friendship memory tool for cognitively-loaded adults (parents, health-affected, post-relocation) who maintain 15-30 close relationships. We differentiate on: (1) personal friendships as the sole focus, (2) voice + text capture under 30 seconds, (3) reassurance-first emotional design, and (4) per-friend relationship context that feels like memory, not a database.

**Why this wedge:**
- No competitor owns the personal-friendship positioning (see competitor teardown)
- The pain is well-documented and growing (Surgeon General, friendship recession data)
- LLM technology makes voice-first capture feasible for the first time
- The designer IS the user — fastest possible feedback loop for v1

**Risks to this wedge:**
- The personal CRM category has a near-100% failure rate at scale — we may be entering a graveyard
- Voice capture may be awkward in real contexts (H4 open risk, untestable without prototype)
- The designer may be the only person who wants this level of friendship tooling (H5)
- Subscription willingness is unproven and likely low
- "Notes about your friends" may trigger social discomfort when described to others

**Next steps to validate:**
- [x] Step 1: Hypotheses framed (complete)
- [x] Step 2: Competitor + market research (this document)
- [ ] Step 3: Research plan (secondary research sweep for H5, H2, H1, H3)
- [ ] Step 4: Synthesize evidence and update hypothesis statuses
- [ ] Step 5: GO/PIVOT/STOP decision

---

## Sources & References

| # | Source | Type | URL / Citation | Date Accessed | Confidence |
|---|--------|------|----------------|---------------|------------|
| 1 | Surgeon General Advisory: "Our Epidemic of Loneliness and Isolation" | Government advisory | https://www.hhs.gov/surgeongeneral/reports-and-publications/connection/index.html | 2026-04-26 | High |
| 2 | Survey Center on American Life: "The State of American Friendship" | Survey research | https://www.americansurveycenter.org/research/the-state-of-american-friendship-change-challenges-and-loss/ | 2026-04-26 | High |
| 3 | Pew Research Center: Americans with no close friends (8%) | Survey | Referenced via NPR coverage of Surgeon General Advisory | Oct 2023 | High |
| 4 | Gallup: 44 million Americans experiencing significant loneliness | Poll | Referenced via Surgeon General Advisory | Feb 2023 | High |
| 5 | NPR: "America has a loneliness epidemic" | Journalism | https://www.npr.org/2023/05/02/1173418268/loneliness-connection-mental-health-dementia-surgeon-general | 2026-04-26 | High |
| 6 | Harvard GSE: "What is Causing Our Epidemic of Loneliness" | Academic summary | https://www.gse.harvard.edu/ideas/usable-knowledge/24/10/what-causing-our-epidemic-loneliness-and-how-can-we-fix-it | 2026-04-26 | Medium |
| 7 | Harvard Happiness Lab: "The Friendship Recession" | Research brief | https://www.happiness.hks.harvard.edu/february-2025-issue/the-friendship-recession-the-lost-art-of-connecting | 2026-04-26 | Medium |
| 8 | Indie Hackers: "Have you paid for a personal CRM app?" | Forum thread | https://www.indiehackers.com/post/have-you-paid-for-a-personal-crm-app-did-it-work-for-you-cb68ea9a7c | 2026-04-26 | Medium |
| 9 | Dex blog: "Personal CRM in 2020: 20+ startups, apps, and failed attempts" | Industry analysis | https://getdex.com/blog/personal-crm-in-2020-20-startups-apps-and-failed-attempts/ | 2026-04-26 | Medium |
| 10 | Holt-Lunstad et al. (2010, 2015): loneliness mortality meta-analyses | Academic | Cited in Surgeon General Advisory | 2010, 2015 | High |
