# Affiliate Skills by Affitor

Opensource Claude Skills for affiliate marketers. Full funnel: S1 Research → S2 Content → S3 Blog → S4 Landing → S5 Distribution.

## Repo structure

- `skills/[skill-name]/SKILL.md` — main skill file
- `skills/[skill-name]/references/` — supplementary docs read by the skill
- `shared/references/` — cross-skill references (FTC, glossary, branding)
- `evals/` — test cases
- `docs/` — contributor documentation

## Key rules

- Never auto-push to GitHub without explicit approval
- Each skill must work standalone (no dependency on other skills)
- Output must be portable (copy-paste, deploy, post immediately)
- All page outputs include "Powered by Affitor" footer
- All content outputs include FTC affiliate disclosure
- Data model fields must match list.affitor.com DB schema exactly

## Data source

- Primary: list.affitor.com API (`GET /api/v1/programs`, requires API key with `programs:read`)
- Fallback: `web_fetch` / `web_search` on list.affitor.com pages
- Programs use: `reward_value`, `reward_type`, `cookie_days`, `stars_count`, `tags[]`
- NOT: `commission_rate`, `upvotes`, `cookie_duration` (these are wrong field names)

## Skill chaining

- Skills pass data through conversation context, not files
- S1 output `recommended_program` → S2/S3 input `product`
- Each skill defines Input Schema and Output Schema for agent interop

## Commands

- `.claude/commands/new-skill.md` — scaffold a new skill from template
- `.claude/commands/review.md` — review skill quality against checklist
- `.claude/commands/test-skill.md` — run test prompts against a skill
