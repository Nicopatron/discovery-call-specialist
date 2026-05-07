# Discovery Call Specialist

A folder-based AI specialist for indie AI consultants. Drop it into a Claude project, paste a raw discovery call transcript, and get back a structured synthesis with the operator's reasoning visible — archetype, red flags, pain layers, signal-traced pricing, follow-up email matching the prospect's language, 3 next-call dates, and 3 prioritized moves.

---

## What you get back

**Drop this folder into a Claude project. Paste a transcript. Ask:** *"Synthesize this discovery call."*

You get back this shape (real output, abbreviated):

> ### Prospect Archetype
> **Skeptical-but-frustrated SaaS founder.** Signals: competitive panic ("losing demos to 'but does it have AI?' questions"), prior agency burn ("40-page deck of stuff we already knew"), hard 8-week deadline, decision-maker on the call with CTO accessible.
>
> ### Red Flags
> **No clear AI use case yet.** *"I'm not even sure what AI features I want."* Phase 1 cannot be "the build" — it has to be the *decision* about what to build, validated against his customer data. Pricing reflects discover-then-build, not pure build.
>
> ### Pricing Anchor
> **$4K–$8K USD for Phase 1.**
> - Base (12-person mid SaaS): $3–7K.
> - Urgency (8-week hard deadline) → +30% → $4K–9K.
> - Prior bad-agency experience → +10% trust premium → $4.4K–$9.9K.
> - Decision-maker on call → no penalty.
> - **→ Quote $4K–$8K.**
>
> *(plus Top 3 Pains, Follow-up Email under 150 words matching the prospect's language, 3 specific call dates, 3 next moves, and a `## Decision Trace` footer that cites the transcript signals behind each major call — full output ~600–900 words)*

That output came from this transcript (also abbreviated):

> Marcus Chen — founder of Pulsemetrics, marketing analytics SaaS, 12 employees, NYC.
>
> *"Three competitors launched AI features in Q1 and I'm losing demos to 'but does it have AI?' questions. I'm not even sure what AI features I want… Budget — I'd be willing to invest five to ten K on a first phase. We've talked to two consultancies and they wanted to do six weeks of discovery before writing code. We don't have six weeks. I have a board meeting in eight weeks and I want to demo something there. We've had bad experiences with agencies before — one took our money for a 40-page deck of stuff we already knew. I'm allergic to that."*

The full transcript and worked output are in `examples.md`. Two more full syntheses there — a Buenos Aires dental clinic (Spanish) and a Mendoza winery scaling DTC into the US (mixed EN/ES) — plus Example 4 documenting a deliberate refusal on a thin transcript (next paragraph).

**What it won't do:** synthesize a thin transcript. If four of five core inputs are missing (prospect role, industry + geography, quantified pain with a verbatim quote, budget signal, decision-maker clarity), it refuses and asks for the gaps in one short message. A guessed pricing anchor on a real call costs more than a clarification email. See `examples.md` Example 4 for what that refusal looks like.

---

## Why this exists

Indie AI consultants run discovery calls and then burn 2–4 hours per call doing post-call synthesis: re-reading notes, drafting follow-up emails, deciding on pricing, sequencing next moves. This specialist compresses that work to about 5 minutes and produces a more consistent output than the consultor would write at 11 PM tired.

It runs as three loops, not a single shot:

1. **Intake gate.** Five required inputs verified before synthesizing — refuses to guess when four are missing (see "What it won't do" above).
2. **8-section synthesis.** Archetype → red flags (when present) → top 3 pains with verbatim quotes → signal-traced pricing → follow-up email matching the buyer's language → three specific call dates → three prioritized next moves → decision trace citing the signals behind each major call.
3. **Iteration on outputs.** Ask *"draft just the email,"* *"expand the scope,"* *"what would I ask in call 2."* The structure stays; the sections regenerate.

Bilingual (English + Rioplatense Spanish), tuned for LATAM/US indie practice, scoped to engagements in the **$2–15K USD** range. Not for enterprise sales, not for VC pitches, not for productized SaaS positioning.

---

## What's inside

| File | Job |
|------|-----|
| `quickstart.md` | TL;DR for skim readers — 5 numbered steps from clone to first output. |
| `identity.md` | Who the specialist is — operator persona, point of view, scope boundaries. |
| `rules.md` | The output contract — 8-section format (incl. Decision Trace), length caps, intake gate, degraded-input handling. |
| `examples.md` | 4 worked examples: 3 full syntheses (US SaaS · clínica dental BA · bodega Mendoza DTC US) + 1 deliberate refusal showing graceful degradation on a thin transcript. |
| `reference/prospect-archetypes.md` | 6 buyer archetypes with signals, pain layers, anchor strategy, what NOT to pitch. Includes a red-flag appendix. |
| `reference/objection-bank.md` | 12 objections with surface form / real fear underneath / response pattern. |
| `reference/pricing-signals.md` | USD anchor tiers, signal multipliers, LATAM overlay, anti-patterns. |
| `reference/follow-up-templates.md` | Bilingual email templates (24h, 72h nudge), 1-page scope skeleton, 3-date invitation pattern. |
| `reference/intake-checklist.md` | The 5-input gate the specialist runs before synthesizing. Refuses to guess if 4 of 5 are missing. |
| `LICENSE` | MIT. |

---

## 5-minute cold-clone test

1. Clone or download the folder.
2. Open `claude.ai` → **New Project** (a free or paid plan works).
3. Upload all files into the project's **Project knowledge** panel — including everything inside `reference/`.
4. Open a new chat in that project. Paste a discovery call transcript or your raw post-call notes (≥100 words; if shorter, the specialist asks for more before synthesizing).
5. Ask: **"Synthesize this discovery call."**
6. Read the structured output. To iterate: *"draft just the email,"* *"expand the scope,"* *"what would you ask in call 2."*

If you don't have a transcript handy, paste any of the three examples from `examples.md` — they're synthetic and self-contained.

---

## Methodology

Built using **Interpretable Context Methodology** (ICM): folders as architecture, each file does one job well, and the structure tells you what's where without needing a tour. The five-slot contract:

- `identity.md` — *who* the operator is.
- `rules.md` — *how* the operator responds (incl. the intake gate that refuses thin inputs).
- `examples.md` — *what* good looks like, including a deliberate refusal example.
- `reference/` — *what* the operator knows (archetypes, objections, pricing signals, templates, intake checklist).
- `README.md` + `quickstart.md` — *how* to use the folder.

The pricing reasoning above (signal-by-signal trace) is the methodology applied: every output decision shows the transcript signal that drove it. That's what *interpretable* means in ICM — not "the model is mysterious," but "the operator's logic is visible."

Source material in `reference/` is intentionally domain-dense — six prospect archetypes, twelve objections with the fear underneath each, pricing signals tuned for LATAM/US bilingual practice, and bilingual follow-up templates. That's the difference between a specialist that recites best practices and one that has actually run discovery calls.

---

## Adapting it to your domain

The methodology travels. To fork this for a different specialist: rewrite `identity.md` for your operator, rewrite `rules.md` with your output contract, replace `examples.md` with 2–3 worked examples from your domain, repopulate `reference/` with your domain's archetypes / frameworks / templates, and update this README's first section. If you keep one rule, keep this: **each file does one job**. Identity describes WHO. Rules describe HOW. Examples show WHAT good looks like. Reference holds WHAT the operator knows. README explains HOW to use it.

---

## Glossary

- **PYME** — small/mid-sized business (Spanish: *pequeña y mediana empresa*).
- **DTC** — direct-to-consumer.
- **JTBD** — jobs-to-be-done framework (the underlying job a buyer is hiring the product to do).
- **Anchor (pricing)** — the first number that frames a negotiation; the rest of the conversation moves relative to it.
- **Archetype** — a recurring buyer pattern with predictable pain layers, signals, and red flags.
- **Voseo / Rioplatense** — the Spanish variant spoken in Argentina and Uruguay (*vos* instead of *tú*); the dialect this specialist defaults to for Spanish output.
- **USDT** — USD-pegged stablecoin frequently used in LATAM cross-border invoicing when local currencies are unstable.

---

## Built by

Nico Patrón Uriburu — indie AI consultant at [E-Growth Management](https://www.linkedin.com/in/nicolas-patron-uriburu/), Buenos Aires. Seven-plus years across the build side (Next.js, Supabase, automation pipelines) and the sell side (discovery, scoping, proposals, close).

I built this because my 11 PM post-call notes kept getting *worse*, not better — the same buyer archetypes kept resurfacing across calls, but tired-me kept relearning them from scratch. This folder is the synthesis I'd write at 9 AM Monday, available the moment a call ends. Used in my own bilingual practice across AR / MX / CL / US.

License: MIT. Fork it, swap the persona, adapt `reference/` to your domain.
