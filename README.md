# EdTech Founder Stack

![Version](https://img.shields.io/badge/version-1.4.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

**Executable expertise for edtech founders — grounded in peer-reviewed learning science and ScaleU's higher ed jobs framework.**

Built by [ASU ScaleU](https://scaleu.asu.edu), Arizona State University's edtech accelerator. Presented at [SXSW EDU 2026](https://github.com/savvides/cracking-higher-ed-sxswedu).

EdTech Founder Stack isn't just another list of resource links. It's executable expertise that lives in your terminal. Run a skill and get the kind of opinionated, research-backed guidance we usually only give to our portfolio companies—right when you're actually making decisions. 

## Who this is for

You're building an edtech product and the stakes are high. You need to know: Is my idea actually viable? Will districts buy this, or just say it's "interesting"? What evidence do investors *really* care about? How do I navigate higher ed procurement without losing six months? Is my AI architecture a load-bearing wall or just decorative wallpaper?

Stop guessing and skip the weeks of Googling. Run a skill and get answers in five minutes.

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

Then open Claude Code and run `/edtechfounderstack` — it'll ask one question to figure out where you are and route you to the right first skill. All skills are available as slash commands.

### Codex CLI

Clone the repo anywhere. Reference individual SKILL.md files as system prompts:

```bash
codex exec "$(cat path/to/edtechfounderstack/skills/pilot-design/SKILL.md)" -s read-only
```

### Gemini CLI

Clone the repo. Add skill paths to your Gemini configuration or reference SKILL.md files directly.

### Cursor

Clone the repo. Copy the contents of any SKILL.md into Cursor's custom instructions for that workspace.

Interactive features (branching questions based on your answers) work best in Claude Code. Other tools can execute the skills as prompts, but the interactive flow may vary.

## Skills

### Discovery & Validation

**`/edtech-landscape`** — Stop building in a vacuum. Map your market segment, buyer persona, regulatory hurdles, and competitive context before you commit code. Run this first.

**`/idea-validation`** — An honest pressure-test. Uses ScaleU's 5-question diagnostic for higher ed founders. You'll get a clear verdict: GO, PIVOT, DIG DEEPER, or STOP.

### Product

**`/product-review`** — Audit your product across the five dimensions that actually matter: learning design, UX, buyer requirements, differentiation, and evidence readiness. Scores 1-10 with specific fixes.

**`/accessibility-check`** — Don't treat accessibility as an afterthought. Check against WCAG 2.1 AA, Section 508, and UDL. Get a prioritized checklist, VPAT guidance, and an action plan.

### Evidence & Research

**`/evidence-check`** — Most founders overestimate their evidence. Get an honest assessment of your ESSA tier (1-4), a gap analysis, and a concrete plan to move up the ladder.

**`/pilot-design`** — How to design a pilot that actually converts to a contract. Covers timelines, success metrics, MOU templates, IRB guidance, and conversion benchmarks.

### Sales & Go-to-Market

**`/go-to-market`** — Build a GTM strategy that survives procurement. Beachhead selection, pricing guidance tied to budget thresholds, and your first-90-day action plan.

**`/sales-strategy`** — Tactical sales playbook. Outreach templates, demo scripts, and objection handling for the specific buyers who hold the purse strings.

### Fundraising & Growth

**`/pitch-review`** — Review your pitch through an edtech investor lens. Scores six dimensions, flags common traps, and provides a revised pitch outline.

**`/fundraising-guide`** — Who funds edtech right now? Find out what evidence they require and get a week-by-week fundraising playbook.

## What powers the skills

### Reference data

We don't rely on generic LLM training data. Skills read from `data/` for factual claims, meaning guidance is grounded in real regulations, real market data, and real procurement processes.

### Research corpus

Peer-reviewed learning science in `data/research/`. When a skill makes a recommendation, it cites specific studies—spaced repetition, cognitive load theory, formative assessment—so you have the DOI to back up your claims.

### Higher ed framework (SXSW EDU 2026)

Validated jobs across the student journey. The structural patterns founders usually miss. The noise vs. signal filter. This is the "Cracking Higher Ed" framework we presented at SXSW EDU 2026.

## About ASU ScaleU

[ScaleU](https://scaleu.asu.edu) is ASU's edtech validation program. We take 1% equity in early-stage startups in exchange for controlled access and a paid pilot at Arizona State University—generating the evidence you need to fundraise and sell at enterprise scale.

If designing and running an institutional pilot is your next step, that's literally what we do. [Learn more](https://scaleu.asu.edu) or [apply directly](https://scaleu.asu.edu/apply).

## Philosophy

See [ETHOS.md](ETHOS.md) for what we believe about building edtech products that actually work. Seven principles, starting with "validate demand, not interest."

## Architecture

See [ARCHITECTURE.md](ARCHITECTURE.md) for how skills, data files, and the research corpus fit together.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to improve existing skills or add new ones. We're always looking for better regulatory data, new buyer personas, and more research papers.

## License

MIT. Use these skills however you want.

