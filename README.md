# EdTech Founder Stack

![Version](https://img.shields.io/badge/version-1.3.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Skills](https://img.shields.io/badge/skills-10-orange)
![Research](https://img.shields.io/badge/papers-376-purple)

**10 AI skills. 376 peer-reviewed papers. 15 validated jobs across the student journey.**

Built by [ASU ScaleU](https://scaleu.asu.edu), Arizona State University's edtech accelerator. Presented at [SXSW EDU 2026](https://github.com/savvides/cracking-higher-ed-sxswedu).

EdTech Founder Stack gives you executable expertise, not another list of links. Run a skill in your terminal and get opinionated, research-backed guidance at the exact moment you're making decisions. Every recommendation is grounded in ScaleU's experience running pilots at one of the largest universities in the US.

## The founder journey

Skills map to the stages every edtech founder goes through. Start anywhere. Each skill recommends what to run next.

```
Discovery              Product                Evidence
/edtech-landscape      /product-review        /evidence-check
/idea-validation       /accessibility-check   /pilot-design

Sales                  Fundraising
/go-to-market          /pitch-review
/sales-strategy        /fundraising-guide
```

## Install

### Claude Code

```bash
git clone https://github.com/savvides/edtechfounderstack.git ~/.claude/skills/edtechfounderstack
cd ~/.claude/skills/edtechfounderstack && ./setup
```

That's it. All 10 skills are available as slash commands.

### Codex CLI

Clone the repo anywhere. Reference individual SKILL.md files as system prompts:

```bash
codex exec "$(cat path/to/edtechfounderstack/skills/pilot-design/SKILL.md)" -s read-only
```

### Gemini CLI

Clone the repo. Add skill paths to your Gemini configuration or reference SKILL.md files directly.

### Cursor

Clone the repo. Copy the contents of any SKILL.md into Cursor's custom instructions for that workspace.

Interactive features (branching questions based on your answers) work best in Claude Code. Other tools can execute the skills as prompts but the interactive flow may vary.

## Skills

### Discovery & Validation

**`/edtech-landscape`** — Map your market segment, buyer persona, regulatory landscape, and competitive context. This is the entry point. Run it first.

**`/idea-validation`** — Pressure-test your edtech idea against market reality. Uses ScaleU's 5-question diagnostic for higher ed founders. Verdict: GO, PIVOT, DIG DEEPER, or STOP.

### Product

**`/product-review`** — Review your product across 5 dimensions: learning design, user experience, buyer requirements, differentiation, and evidence readiness. Scores each 1-10 with specific recommendations.

**`/accessibility-check`** — Check against WCAG 2.1 AA, Section 508, and Universal Design for Learning. Prioritized checklist, VPAT guidance, and action plan.

### Evidence & Research

**`/evidence-check`** — Classify your evidence on ESSA tiers (1-4). Most founders overestimate their tier. Get an honest assessment, gap analysis, and concrete plan to move up one tier.

**`/pilot-design`** — Design an effective institutional pilot: week-by-week timeline, success metrics, MOU template, IRB guidance, and pilot-to-contract conversion benchmarks.

### Sales & Go-to-Market

**`/go-to-market`** — Build an edtech GTM strategy. Beachhead selection, pricing guidance aligned to procurement thresholds, sales calendar, and first-90-day action plan.

**`/sales-strategy`** — Tactical sales playbook for your specific buyer. Outreach templates, demo scripts, procurement navigation, objection handling, and deal acceleration.

### Fundraising & Growth

**`/pitch-review`** — Review your pitch through an edtech investor lens. Scores 6 dimensions, flags common mistakes, recommends investor targets by stage, and provides a revised pitch outline.

**`/fundraising-guide`** — Who funds edtech at your stage, what evidence they require, and a fundraising playbook with week-by-week execution plan.

## What powers the skills

### Reference data (11 files)

Skills read from `data/` for factual claims, not from the AI's training data. This means guidance is grounded in real regulations, real market data, and real procurement processes.

Covers: K-12 regulatory (FERPA, COPPA), higher ed landscape (accreditation, LMS integration), corporate L&D, ESSA evidence tiers, procurement guides, pilot benchmarks, buyer personas, funding landscape, competitive landscape, higher ed jobs atlas, and founder traps.

### Research corpus (376 papers)

19 topics across learning science in `data/research/`. When a skill recommends an approach, it cites specific studies with author, year, finding, and DOI. Topics include active learning, adaptive learning, spaced repetition, cognitive load theory, formative assessment, multimedia principles, and more.

### Higher ed framework (SXSW EDU 2026)

15 validated jobs across 6 student journey phases. 4 structural patterns founders miss. The noise vs. signal filter. From "Cracking Higher Ed: Why Startups Miss the Mark," presented at SXSW EDU 2026.

## About ASU ScaleU

[ScaleU](https://scaleu.asu.edu) is ASU's edtech validation program. We take 1% equity in early-stage startups in exchange for controlled access and a paid pilot at Arizona State University, generating the evidence founders need to fundraise and sell at enterprise scale.

If designing and running an institutional pilot is your next step, that's literally what we do. [Learn more](https://scaleu.asu.edu) or [apply directly](https://scaleu.asu.edu/apply).

## Philosophy

See [ETHOS.md](ETHOS.md) for what we believe about building edtech products that work. Seven principles, starting with "validate demand, not interest."

## Architecture

See [ARCHITECTURE.md](ARCHITECTURE.md) for how skills, data files, and the research corpus fit together.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to improve existing skills or add new ones. We especially welcome:

- International regulatory data (GDPR, country-specific education regulations)
- New buyer personas and procurement guides for non-US markets
- Additional research papers with peer-reviewed evidence
- Corrections to market data or competitive landscape

## License

MIT. Use these skills however you want.
