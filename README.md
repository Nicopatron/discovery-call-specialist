# Discovery Call Specialist

A folder-based AI specialist for indie AI consultants. Drop it into a Claude project, paste a discovery call transcript, and get back a structured synthesis ready to act on.

> **Drop this folder into a Claude project. Paste a discovery call transcript (or your raw notes if you didn't record), then ask: "Synthesize this discovery call."** You'll get back: prospect archetype, top 3 pain points with emotional context, red flags surfaced first, USD scope range with signal-based reasoning, follow-up email draft (matching the prospect's language and tone), 3 proposed next-call dates, and 3 prioritized next moves. Built for indie AI consultants running discovery calls weekly. Try it cold: paste any transcript inside `examples.md` and ask the question above.

---

## Why this exists

Indie AI consultants run discovery calls and then waste 2–4 hours per call doing post-call synthesis: re-reading notes, drafting follow-up emails, deciding on pricing, sequencing next moves. This specialist compresses that work to about 5 minutes — and produces a more consistent output than the consultor would write at 11pm tired.

It's bilingual (English + Rioplatense Spanish), tuned for LATAM-and-US indie practice, scoped to engagements in the $2–15K USD range. Not for enterprise sales, not for VC pitches, not for productized SaaS positioning.

---

## What's inside

| File | Job |
|------|-----|
| `identity.md` | Who the specialist is — operator persona, point of view, scope boundaries. |
| `rules.md` | The output contract — strict 7-section format, length caps, degraded-input handling. |
| `examples.md` | 3 worked synthesis examples (US SaaS founder · clínica dental BA · bodega Mendoza DTC US). Calibrates voice. |
| `reference/prospect-archetypes.md` | 6 archetypes with signals, pain layers, anchor strategy, what NOT to pitch. Includes a red-flag appendix. |
| `reference/objection-bank.md` | 12 objections with surface form / real fear / response pattern. |
| `reference/pricing-signals.md` | USD anchor tiers, signal multipliers, LATAM overlay, anti-patterns. |
| `reference/follow-up-templates.md` | Bilingual email templates (24h, 72h nudge), 1-page scope skeleton, 3-date invitation pattern. |
| `LICENSE` | MIT. |

---

## 5-minute cold-clone test

1. Clone this repo (or download the folder).
2. Open Claude — `claude.ai` → "New Project," or any Claude environment that accepts file uploads.
3. Upload all files in this folder, including everything inside `reference/`.
4. Paste a discovery call transcript or your raw post-call notes (minimum ~100 words; if shorter, the specialist will ask you for more).
5. Ask: **"Synthesize this discovery call."**
6. Read the structured output. To iterate: "draft just the email," "expand the scope," "what would you ask in call 2."

If you don't have a transcript handy, paste any of the three examples from `examples.md` — they're synthetic and self-contained.

---

## Methodology

Built using the **Interpretable Context Methodology** (ICM) taught in Clief Notes' Lyceum: folders as architecture, each file does one job well, and the structure tells you what's where without needing a tour. The five-slot contract:

- `identity.md` — *who* the operator is.
- `rules.md` — *how* the operator responds.
- `examples.md` — *what* good looks like, in action.
- `reference/` — *what* the operator knows (loaded on demand).
- `README.md` — *how* to use the folder.

Source material in `reference/` is intentionally domain-dense and non-obvious. That's the difference between a specialist that recites best practices and one that has actually run two hundred of these calls.

---

## Adapting it to your domain

The methodology is what travels. To fork this for a different specialist:

1. Rewrite `identity.md` for your operator persona (background, POV, what they don't cover).
2. Rewrite `rules.md` with your output contract (sections in order, length caps, degraded-input handling).
3. Replace `examples.md` with 2–3 worked examples from your domain.
4. Repopulate `reference/` with your domain's archetypes, objections, frameworks, and templates.
5. Update this README's first paragraph to match the new specialist.

If you keep one structural rule, keep this: **each file does one job**. Identity describes WHO. Rules describe HOW. Examples show WHAT good looks like. Reference holds WHAT the operator knows. README explains HOW to use it. Mixing jobs across files is the fastest way to make a specialist that drifts.

---

## Built by

Nico Patrón Uriburu — indie AI consultant at [E-Growth Management](https://www.linkedin.com/in/nicolas-patron-uriburu/), Buenos Aires. Built for Clief Notes Weekly Comp #3 (May 2026) and used in real practice every week.

License: MIT. Fork it, swap the persona, adapt `reference/` to your domain.
