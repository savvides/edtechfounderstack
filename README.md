# EdTech Founder Stack

AI-powered skills for edtech founders. Built by [ASU ScaleU](https://scaleu.asu.edu), Arizona State University's edtech accelerator.

Instead of another list of links, this repo gives you **executable expertise**. Run a skill in your terminal and get opinionated, edtech-specific guidance at the exact moment you're making decisions.

## What's inside

### Skills by founder stage

**Discovery & Validation**
- `/edtech-landscape` — Map your market segment, buyer persona, regulatory landscape, and competitive context
- `/idea-validation` — Validate your edtech idea against market reality and buyer needs

**Product**
- `/product-review` — Review your product through the lens of educational outcomes and buyer requirements
- `/accessibility-check` — WCAG, Section 508, and Universal Design for Learning (UDL) compliance

**Evidence & Research**
- `/evidence-check` — Classify your evidence on ESSA tiers (1-4), get a gap analysis, and plan your next study
- `/pilot-design` — Design an effective institutional pilot: timeline, success metrics, MOU template, IRB considerations

**Sales & Go-to-Market**
- `/go-to-market` — Edtech GTM strategy by segment, channel selection, and procurement cycle guidance
- `/sales-strategy` — Selling to schools, districts, and universities: buyer personas, procurement, pricing

**Fundraising & Growth**
- `/pitch-review` — Review your pitch through an edtech investor lens with evidence positioning
- `/fundraising-guide` — Edtech-specific fundraising: who funds what stage, what evidence they require

### Reference data

The `data/` directory contains editable knowledge files that skills draw from:

- Regulatory guides (FERPA, COPPA, state privacy laws, accreditation)
- Buyer personas (district CTO, university provost, department chair)
- Procurement guides (how purchasing actually works at districts and universities)
- Evidence frameworks (ESSA tiers with examples)
- Market landscape (key companies, funding sources, competitive context)

## Install

### Claude Code (primary)

```bash
claude mcp add edtechfounderstack -- npx -y @anthropic-ai/claude-code-mcp
```

Or clone directly:

```bash
git clone https://github.com/philippossavvides/edtechfounderstack.git
cd edtechfounderstack
```

Then add to your project's `.claude/settings.json` or reference the skills directory.

### Other AI coding tools

The skills use the standard `SKILL.md` format. They work as system prompts in Codex CLI, Gemini CLI, and Cursor, though interactive features (branching questions) work best in Claude Code.

## Usage

Once installed, run any skill as a slash command:

```
/edtech-landscape
/pilot-design
/evidence-check
```

Each skill asks you structured questions about your product, market, and stage, then gives you tailored guidance based on your answers.

## About ASU ScaleU

ASU ScaleU is Arizona State University's edtech accelerator. We take 1% equity in early-stage startups in exchange for controlled access and a paid pilot at ASU, helping founders gather evidence for fundraising and acquire new customers.

If designing and running an institutional pilot is your next step, that's literally what we do. [Learn more](https://scaleu.asu.edu) or [apply directly](https://scaleu.asu.edu/apply).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to improve existing skills or add new ones. We welcome PRs, especially for:

- International regulatory data (GDPR, country-specific education regulations)
- New buyer personas and procurement guides
- Corrections to market data or competitive landscape

## License

MIT. Use these skills however you want.
