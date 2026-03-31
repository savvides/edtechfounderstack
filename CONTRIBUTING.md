# Contributing to EdTech Founder Stack

Thanks for helping make this resource better for edtech founders.

## How skills work

Each skill lives in `skills/{skill-name}/SKILL.md` and follows the standard SKILL.md format:

```markdown
---
name: skill-name
description: One-line description of what this skill does.
---

# Skill Title

Instructions for the AI...
```

Skills read from reference data in `data/` for regulatory, market, and evidence information, and cite studies from `data/research/` (376 peer-reviewed papers) when making claims about learning science. This keeps domain knowledge editable without touching skill logic.

## What we're looking for

### High-value contributions

- **International regulatory data** — GDPR guidance, country-specific education regulations, international accreditation bodies
- **New buyer personas** — we're US-focused right now. Buyer personas for international education markets would be valuable
- **Corrections** — if our market data, competitive landscape, or regulatory information is wrong or outdated, please fix it
- **New skills** — if you've identified a gap in the founder journey that a skill could fill

### Guidelines

1. **Be opinionated.** These skills take positions. "Usage-based pricing works better than per-seat for K-12." If you're adding guidance, have a point of view backed by experience.

2. **Reference data, not hallucination.** Skills should read from `data/` files for factual claims. Don't rely on the AI's training data for company names, funding amounts, or regulatory specifics.

3. **Interactive branching.** Skills ask structured questions and branch based on answers. K-12 founders get different guidance than higher ed founders. Design for this.

4. **Keep it practical.** Every piece of guidance should end with something the founder can do. Not "consider your options" but "here's the procurement timeline for a district of this size."

5. **Context-aware next steps.** Every skill ends by recommending the single most relevant next skill based on what the founder said during the session. Don't use static lists. Route based on scores, evidence tier, stage, and challenges.

## Process

1. Fork the repo
2. Create a branch for your changes
3. Make your edits
4. Open a PR with a description of what you changed and why

The ScaleU team reviews all PRs to maintain quality and consistency.

## Questions?

Open an issue or reach out to the ScaleU team.
