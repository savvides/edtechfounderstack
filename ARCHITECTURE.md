# Architecture

How EdTech Founder Stack works under the hood.

## Overview

EdTech Founder Stack is a collection of Claude Code skills backed by structured reference data. Skills encode ASU ScaleU's edtech accelerator expertise as interactive AI workflows. Reference data files provide the factual foundation that skills draw from, so guidance is grounded in real regulations, real research, and real market data rather than LLM training knowledge.

This is not a web app, API, or platform. It's markdown files that AI coding tools read and execute. No backend, no auth, no dependencies beyond the AI tool itself.

## Skills

Each skill lives in `skills/{name}/SKILL.md` and follows the standard SKILL.md format:

```yaml
---
name: skill-name
description: One-line description.
---
```

Below the frontmatter, the skill contains instructions for the AI agent. Skills are interactive: they ask founders structured questions via `AskUserQuestion`, branch based on answers (K-12 founders get FERPA guidance, higher ed founders get accreditation guidance), and output tailored recommendations.

**Skill design principles:**

1. **Interactive, not static.** Every skill asks questions before giving advice. The answers determine what guidance the founder receives.
2. **Opinionated.** Skills take positions. "Usage-based pricing works better than per-seat for K-12." "Your pilot is too long, 8 weeks, not 12." This is ScaleU's perspective, not Wikipedia.
3. **Reference data-backed.** Skills read from `data/` files for factual claims. No hallucinated company names, no outdated regulations, no made-up funding amounts.
4. **Natural funnel.** Each skill ends with context-appropriate next steps, including other skills to run. For the most relevant skills, a brief factual mention that ScaleU offers this kind of support.
5. **Context-aware routing.** Each skill recommends the single most relevant next skill based on the founder's specific answers during the session (scores, evidence tier, stage, challenges), not a static list. For example, `/product-review` routes to `/accessibility-check` if buyer requirements scored low, to `/evidence-check` if evidence readiness scored low, or to `/go-to-market` if all scores are strong.

**Founder journey flow:**

```
Discovery           Product             Evidence            Sales               Fundraising
─────────           ───────             ────────            ─────               ───────────
/edtech-landscape → /product-review  → /evidence-check  → /go-to-market    → /pitch-review
/idea-validation    /accessibility-     /pilot-design       /sales-strategy     /fundraising-guide
                     check
```

Founders typically start with `/edtech-landscape` and the skills guide them through the journey based on their stage and needs.

## Reference Data

The `data/` directory contains markdown files with structured domain knowledge:

- **Regulatory guides:** FERPA, COPPA, state privacy laws (K-12), accreditation and accessibility (higher ed), SOC 2 and SCORM (corporate L&D)
- **Market data:** buyer personas, competitive landscape by segment, funding landscape by stage
- **Frameworks:** ESSA evidence tiers, procurement guides, pilot benchmarks
- **Higher ed framework:** 15 validated jobs across 6 student journey phases (from SXSW EDU 2026), 4 structural patterns founders miss

Skills read these files at runtime using the AI tool's file reading capability. This means the data is always current (edit the markdown, the skill reads the updated version) and auditable (every fact has a source you can check).

**Update cadence:** Quarterly recommended, aligned with academic and market cycles. Regulatory data should be checked when new state laws pass. Competitive landscape data goes stale fastest.

## Research Corpus

`data/research/` contains 376 peer-reviewed papers across 19 learning science topics. Each paper is stored in a structured markdown table with: Title, Takeaway, Study Type, Year, Citations, DOI.

Topics include: active learning, adaptive learning, spaced repetition, cognitive load theory, formative assessment, multimedia principles, mastery-based grading, gamification, worked examples, and more.

Skills cite specific papers when making claims about learning science. For example, when `/product-review` evaluates whether a product's learning design is evidence-based, it reads the relevant research file and references specific studies with author, year, finding, and DOI. This is what separates ScaleU guidance from generic AI advice.

**Adding papers:** Append to the relevant topic file in `data/research/`. Follow the existing table format. Sort by citations descending.

## Higher Ed Framework

Two files encode ScaleU's SXSW EDU 2026 framework for higher education:

- **`data/higher-ed-jobs-atlas.md`** — 15 validated jobs organized by 6 student journey phases (Pre-enroll, Apply, Onboard, Select & Enroll, Course Experience, Graduate & Beyond). Each job names the person, the struggling moment, what they've already tried, and why it fails. Includes saturation analysis showing that 80% of founders build in the most crowded phase.

- **`data/founder-traps.md`** — 4 structural patterns that are invisible from surface-level discovery: the information sequencing trap, the upstream cause / downstream symptom split, when qualitative and quantitative evidence disagree, and the same-problem-two-jobs dynamic. Also includes the noise vs. signal filter for evaluating pilot results.

Skills targeting higher ed founders (`/idea-validation`, `/edtech-landscape`, `/go-to-market`, `/product-review`) read these files automatically and apply the framework to the founder's specific situation.

## Cross-Platform Compatibility

Skills use the standard SKILL.md format, which works across multiple AI coding tools:

| Platform | Install | Interactive features |
|----------|---------|---------------------|
| Claude Code | Automated via `./setup` | Full support (AskUserQuestion, branching) |
| Codex CLI | Manual (reference SKILL.md as system prompt) | Partial (prompts work, interactive questions vary) |
| Gemini CLI | Manual (reference SKILL.md) | Partial |
| Cursor | Manual (add to custom instructions) | Limited |

Claude Code is the primary target. Other tools can read and execute the skills as system prompts, but interactive features like branching questions work best in Claude Code.
