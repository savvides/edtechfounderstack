# EdTech Founder Stack

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

**An open, AI-friendly knowledge base for edtech founders — built by [ASU ScaleU](https://scaleu.asu.edu).**

Building an edtech product means making calls that schools, universities, and L&D buyers will judge you on. Is there real demand or just polite interest? What evidence does a district actually require before it buys? How does higher-ed procurement really work, and how long does it take? Is your AI load-bearing or decorative? Most founders answer these by Googling for weeks, or by guessing.

This repo puts the answers in one place: a curated body of knowledge you point your AI tools at — Claude Code, Cursor, ChatGPT — or just read. It's grounded in peer-reviewed learning science, real regulatory and market data, and lessons from operators who've actually done it. Not generic model training data that's a year stale.

Built by ASU ScaleU, Arizona State University's edtech validation program. The higher-ed framework comes from "Cracking Higher Ed," presented at SXSW EDU 2026.

## Who it's for

You're building in edtech and the stakes are high. You need straight answers about demand, evidence, procurement, accessibility, pricing, and fundraising that account for how education actually buys — not startup advice written for consumer apps. This is the knowledge ScaleU gives its portfolio companies, written down and kept current.

## What's inside

Everything lives in `data/` as plain markdown, in four layers.

### Learning science research — `data/research/`

Hundreds of peer-reviewed papers across the major learning-science topics: spaced repetition, cognitive load, formative assessment, adaptive learning, worked examples, the learning-styles myth, and more. Each paper carries its takeaway, study type, year, citation count, and DOI. When you tell a buyer or investor that something works, cite the paper, not a vibe. Index: [`data/research/README.md`](data/research/README.md).

### Market & regulatory reference — `data/`

- Competitive landscape by segment (K-12, higher ed, corporate L&D)
- K-12 privacy and compliance: FERPA, COPPA, state laws
- Higher-ed landscape, procurement, and accessibility
- Funding landscape by stage — who funds edtech and what they require
- Buyer personas, pilot benchmarks, and the ESSA evidence tiers (1–4)

### ScaleU frameworks

- **AI-native vs. bolted-on** — is your AI load-bearing or decorative ([`data/ai-native-framework.md`](data/ai-native-framework.md))
- **Higher-ed jobs atlas** — validated jobs across the student journey, with saturation analysis showing where everyone's already crowded ([`data/higher-ed-jobs-atlas.md`](data/higher-ed-jobs-atlas.md))
- **Founder traps** — the structural patterns founders miss ([`data/founder-traps.md`](data/founder-traps.md))
- **The ethos** — seven principles, starting with "validate demand, not interest" ([`ETHOS.md`](ETHOS.md))

### Operator playbooks — `data/operator-lessons.md`

Dozens of field lessons on validation, product, go-to-market, sales, pricing, pilots, fundraising, and team — distilled from operators and investors on Lenny's Podcast and Lenny's Newsletter, and mapped to selling into schools, universities, and L&D. Practitioner experience, attributed and paraphrased; the research corpus is the evidence layer.

## How to use it

Point your AI tool at the repo — or at the one file that fits your decision — and ask. The markdown is written to be read by a model or a person.

```bash
git clone https://github.com/savvides/edtechfounderstack.git
```

- **Claude Code / Cursor:** open the repo and ask; the agent reads the relevant `data/` files.
- **ChatGPT / Claude:** paste the file that fits your question, or upload the repo.
- **Reading it yourself:** start with [`ETHOS.md`](ETHOS.md) for the worldview, [`data/operator-lessons.md`](data/operator-lessons.md) for the playbooks, or [`data/research/README.md`](data/research/README.md) for the evidence base.

Because it's markdown you can audit, every claim traces to something you can check — a named regulation, a paper with a DOI, a named operator.

## About ASU ScaleU

[ScaleU](https://scaleu.asu.edu) is ASU's edtech validation program. We take 1% equity in early-stage startups in exchange for controlled access and a paid pilot at Arizona State University — the kind of evidence you need to fundraise and sell at enterprise scale. If running an institutional pilot is your next step, that's what we do. [Learn more](https://scaleu.asu.edu) or [apply](https://scaleu.asu.edu/apply).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to help, and [ARCHITECTURE.md](ARCHITECTURE.md) for how the knowledge base is laid out. We're always after better regulatory data, new buyer personas, and more peer-reviewed research. For research, follow the table format in `data/research/` and sort by citation count.

## License

The repository's original content is **MIT** — use it however you want.

**Exception:** [`data/operator-lessons.md`](data/operator-lessons.md) is **not** covered by MIT. Those lessons are paraphrased from the free public archive of Lenny's Podcast and Lenny's Newsletter under its personal/non-commercial terms, so treat that one file as personal, non-commercial use only, not for commercial reuse. See the note at the bottom of the file.
