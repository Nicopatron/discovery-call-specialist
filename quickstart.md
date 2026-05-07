# Quickstart

For people who don't read READMEs.

1. Open `claude.ai` → **New Project** → upload all the `.md` files in this folder (root + `reference/`) into **Project knowledge**.
2. Open a new chat in that project.
3. Paste a discovery call transcript or your raw post-call notes (≥100 words).
4. Ask: **`Synthesize this discovery call.`**
5. Read the 8-section structured output (≤1000 words). Iterate with: *"draft just the email,"* *"expand the scope,"* *"what would I ask in call 2."*

---

**Bilingual auto-detect.** English transcript → English output. Spanish transcript → Spanish (Rioplatense) output. Mixed-language with no dominant → English by default.

**Refuses to synthesize when the transcript is too thin.** Cleared the 100-word floor isn't enough — the specialist also checks for prospect name, industry/geo, a quantified pain with a quote, a budget signal, and decision-maker clarity. Missing 4 of 5 → it asks instead of guessing. See `examples.md` Example 4 for what that refusal looks like.

**Full README** at `README.md` (methodology, file map, glossary, how to fork for your own domain).
