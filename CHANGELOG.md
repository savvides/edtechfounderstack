# Changelog

## 2.1.1 (2026-06-13)

### Cross-tool agent support via AGENTS.md

Point any agentic AI tool at the repo and it now gets the same directive Claude Code already had: answer from the cited `data/` files, not stale training data. [AGENTS.md](AGENTS.md) is the single source of truth, and each tool reads it through the file it already looks for, so there's one file to maintain and no content drift.

- **New canonical `AGENTS.md`** — the cross-tool instructions file. Codex and Cursor read it at the repo root natively.
- **Thin pointers for the rest** — `CLAUDE.md` and `GEMINI.md` import `AGENTS.md`; `.github/copilot-instructions.md` points GitHub Copilot to it. No agent is left answering from stale training data.
- **Fixed the README version badge** — was stuck at 2.0.0; now tracks the release, and CI fails if the badge and `VERSION` ever disagree again.
- **Doc accuracy** — the research-table format in `AGENTS.md`, `CONTRIBUTING.md`, and `ARCHITECTURE.md` now matches the real tables (a leading `#` column), so a contributor who follows the docs passes CI.

## 2.1.0 (2026-05-30)

### Demand-validation toolkit + knowledge from sibling repos

Folds content from three sibling repos — Cracking Higher Ed (SXSW EDU 2026), the JTBD Switch toolkit, and ASU+GSV 2026 Summit Intelligence — into the knowledge base, centered on demand validation. Sources are CC BY 4.0 (Cracking Higher Ed, summit) and MIT (JTBD), attributed in-file; summit and JTBD material is labeled practitioner signal, not peer-reviewed.

- **New `data/demand-validation.md`** — the 5-question demand diagnostic with scoring and the validation depth probes.
- **New `data/jtbd-interviews.md`** — the JTBD "Switch" interview method (four forces, job stories, backward-timeline guide), reframed for edtech.
- **New `data/defensibility-moats.md`** — the exposure spectrum, four moats, and the AI-substitution durability test.
- **New `data/ai-risk-and-trust.md`** — AI's effect on learners and trust, with design responses founders can adopt.
- **New `data/buyer-demand-signals.md`** — the durable jobs institutional buyers switch for, and how to read real demand.
- **Fixed `data/higher-ed-jobs-atlas.md`** — completed from 11 to the full 15 jobs (the phase counts already implied 15).
- Augmented `procurement-guide.md` and `pilot-benchmarks.md` with summit-sourced buyer and pilot realities; added case-study and job-statement issue templates; updated README, ARCHITECTURE.md, and CLAUDE.md.

## 2.0.0 (2026-05-29)

### Repositioned as a knowledge base

EdTech Founder Stack is now a curated, AI-friendly knowledge base for edtech founders — markdown you point your AI tools at or read directly — rather than a set of interactive skills. The knowledge in `data/` is the product.

- **New `data/operator-lessons.md`** — 71 field lessons on validation, product, GTM, sales, pricing, pilots, fundraising, and team, distilled and attributed from the free public archive of Lenny's Podcast and Lenny's Newsletter and mapped to selling into schools, universities, and L&D. Paraphrased under the source's personal/non-commercial terms.
- **Removed the interactive skills** — the `skills/` directory and the `setup` script are gone; the `data/` knowledge base is the whole product. CI now validates the data and research files only.
- **Docs rewritten** — README, ARCHITECTURE.md, CONTRIBUTING.md, and CLAUDE.md now describe the knowledge base and how to use it with Claude Code, Cursor, and ChatGPT.
- **Version badge** — bumped to 2.0.0.

## 1.4.0 (2026-04-25)

### Public launch readiness

- **New `/edtechfounderstack` welcome skill** — first-run orientation that asks one question and routes founders to the right starting skill. Lives in `skills/welcome/` (frontmatter `name: edtechfounderstack`). Setup script now hands new users off to it directly.
- **Count-agnostic documentation** — removed hard-coded skill, paper, and job counts from README, ARCHITECTURE.md, CLAUDE.md, CONTRIBUTING.md, ETHOS.md, and TODOS.md so docs don't drift as the corpus grows. CHANGELOG.md keeps historical counts where they were accurate at the time of release.
- **README polish** — dropped the brittle `skills-N` and `papers-N` badges. New tagline: "Executable expertise for edtech founders — grounded in peer-reviewed learning science and ScaleU's higher ed jobs framework."
- **LICENSE typo fix** — copyright now reads "ASU ScaleU" (was "ASU ScaleUp").
- **Hygiene** — `.claude/settings.local.json` added to `.gitignore` so contributors don't accidentally commit their local Claude Code settings.

## 1.3.0 (2026-04-01)

### AI-native framework integration

Every skill is now AI-native aware. When a founder's product involves AI, skills detect whether the AI is load-bearing (AI-native) or decorative (bolted-on) and adapt guidance accordingly.

- New `data/ai-native-framework.md` reference file: 4 AI-native criteria, 5 bolted-on indicators, the removal test, Karpathy hierarchy (for developer-tool founders), architecture patterns, and AI-native pricing models
- `/product-review` adds a 6th scoring dimension (AI Architecture) for products with AI components
- `/idea-validation` evaluates AI Architecture Fit as a validation signal
- `/go-to-market` provides AI-native pricing strategy (usage-based economics, institutional procurement guidance)
- `/pitch-review` coaches the "improves with models" investor narrative and adapts investor targeting
- `/sales-strategy` adds AI-native objection handling ("what if the AI is wrong?") and demo flow guidance
- `/fundraising-guide` targets AI-focused VCs for AI-native products and traditional edtech VCs for bolted-on
- `/edtech-landscape` maps AI-native vs bolted-on competitors in competitive analysis
- `/evidence-check` adds behavior change as an evidence dimension for AI-native products
- `/accessibility-check` flags AI-specific concerns (bias, transparency, explainability, override capability)
- `/pilot-design` adds AI-specific pilot metrics (accuracy, hallucination rate, trust calibration, behavior change)

The framework is diagnostic, not prescriptive. Bolted-on AI can be a valid strategy. The skills help founders understand the implications for their pricing, sales, fundraising, and competitive positioning.

## 1.2.0 (2026-03-31)

### Tier-1 repo infrastructure

- GitHub issue templates for bug reports, feature requests, and research submissions
- Pull request template with contribution checklist
- CI workflow validating skill frontmatter, routing, data footers, and research format
- CODE_OF_CONDUCT.md and SECURITY.md for community governance
- CODEOWNERS routing PRs to ScaleU team
- README badges (version, license, skills, papers)
- Setup script --help flag
- .editorconfig for consistent formatting

## 1.1.0 (2026-03-31)

### Smart skill navigation

Skills now recommend the single most relevant next step based on your specific answers during the session, not a static list. `/product-review` sees your evidence score is low and sends you to `/evidence-check`. `/idea-validation` gives you a GO verdict and routes you to `/product-review`. Every skill is context-aware.

### Framework packaging (modeled after gstack)

- **One-line install:** `./setup` creates symlinks for all 10 skills in Claude Code
- **ETHOS.md:** 7 principles encoding ScaleU's philosophy on what makes edtech products succeed
- **ARCHITECTURE.md:** How skills, data files, research corpus, and higher ed framework fit together
- **Multi-platform install:** Instructions for Claude Code, Codex CLI, Gemini CLI, and Cursor
- **Versioning:** VERSION file and CHANGELOG for release management

### Higher ed framework (SXSW EDU 2026)

- 15 validated jobs across 6 student journey phases in `data/higher-ed-jobs-atlas.md`
- 4 structural patterns founders miss in `data/founder-traps.md`
- Skills for higher ed founders now use ScaleU's 5-question diagnostic and noise vs. signal filter

### Research corpus

- 376 peer-reviewed papers across 19 learning science topics in `data/research/`
- Skills cite specific studies with author, year, finding, and DOI

## 1.0.0 (2026-03-31)

Initial release.

### Skills (10)

- `/edtech-landscape` — Market diagnostic: sector, buyer, regulatory, competitive context
- `/idea-validation` — Pressure-test your edtech idea against market reality
- `/product-review` — Review product through educational outcomes and buyer requirements lens
- `/accessibility-check` — WCAG, Section 508, and Universal Design for Learning compliance
- `/evidence-check` — Classify evidence on ESSA tiers, gap analysis, study design guidance
- `/pilot-design` — Design effective institutional pilots with MOU templates and IRB guidance
- `/go-to-market` — Edtech GTM strategy by segment, channel, and procurement cycle
- `/sales-strategy` — Selling to schools, districts, and universities
- `/pitch-review` — Review pitch through edtech investor lens with evidence positioning
- `/fundraising-guide` — Edtech-specific fundraising: who funds what, what evidence they require

### Reference Data (11 files)

- K-12 regulatory (FERPA, COPPA, state privacy laws)
- Higher ed landscape (accreditation, accessibility, LMS integration)
- Corporate L&D market
- ESSA evidence tiers (Tier 1-4)
- Procurement guide (districts, universities, state systems)
- Pilot benchmarks (anonymized success data)
- Buyer personas (district CTO, provost, department chair, faculty, etc.)
- Funding landscape (VCs, grants, accelerators by stage)
- Competitive landscape (key companies by segment)
- Higher ed jobs atlas (15 validated jobs across 6 student journey phases)
- Founder traps (4 structural patterns founders miss)

### Research Corpus (376 papers)

19 topics across learning science: active learning, adaptive learning, spaced repetition, cognitive load theory, formative assessment, multimedia principles, mastery-based grading, and more. Each paper includes title, takeaway, study type, year, citations, and DOI.
