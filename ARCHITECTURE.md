# Architecture

How EdTech Founder Stack is put together.

## What it is

A knowledge base for edtech founders, stored as plain markdown. No app, no API, no backend, no dependencies — just files that an AI tool (Claude Code, Cursor, ChatGPT) or a person reads. Edit a file and the next read is current. Every claim traces to a source you can check.

## The knowledge

All of it lives in `data/`, in three kinds of files.

### Reference data — `data/*.md`

Structured domain knowledge, grounded in real sources rather than model training data:

- **Regulatory** — FERPA, COPPA, and state privacy law (K-12); accreditation and accessibility (higher ed)
- **Market** — competitive landscape by segment, buyer personas, buyer demand signals, funding landscape by stage, procurement, pilot benchmarks
- **Frameworks** — ESSA evidence tiers, AI-native vs. bolted-on, defensibility moats, the higher-ed jobs atlas, founder traps, and the demand-validation toolkit (the 5-question diagnostic plus the JTBD Switch interview method)

Each regulatory and market file carries a "last updated" date. Update cadence is roughly quarterly; regulatory data when laws change; the competitive landscape goes stale fastest.

### Research corpus — `data/research/`

Hundreds of peer-reviewed papers across the major learning-science topics, each stored in a numbered markdown table: `#`, Title, Takeaway, Type, Year, Citations, DOI. The index lives in `data/research/README.md`. This is the evidence base — claims about what works in learning cite specific papers with author, year, finding, and DOI.

### Operator playbooks — `data/operator-lessons.md`

Dozens of field lessons from operators and investors, distilled and attributed from the public archive of Lenny's Podcast and Lenny's Newsletter, then mapped to selling into schools, universities, and L&D. These are practitioner experience, not peer-reviewed evidence — the research corpus is the evidence layer, and the file says so. The same practitioner-not-peer-reviewed labeling applies to the summit-sourced files (`data/buyer-demand-signals.md`, `data/ai-risk-and-trust.md`), which each carry their source and an evidence-tier note.

## How it's consumed

Point an AI tool at the repo or a single file and ask; it reads the relevant knowledge and answers in context. Or read the markdown directly. Because the knowledge is files you can diff and audit, it stays current and checkable in a way baked-in model knowledge isn't.

## Agent instructions

The repo ships a small instructions file for each major agent. [`AGENTS.md`](AGENTS.md) is the canonical one, read at the repo root by Codex and Cursor; `CLAUDE.md` and `GEMINI.md` import it, and `.github/copilot-instructions.md` points GitHub Copilot to it. They all tell the agent the same thing: read the relevant `data/` file and cite the source rather than lean on training data. `AGENTS.md` is the single source; edit it, not the pointers.

## Cross-platform

Anything that can read markdown works: Claude Code, Cursor, ChatGPT, Claude, or a plain text editor. There's nothing to install beyond cloning the repo.
