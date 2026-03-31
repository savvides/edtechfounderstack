# Changelog

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
