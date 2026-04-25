# TODOs

## P3: AI-native framework consistency check

**What:** Add a CI step that validates all SKILL.md files reference `data/ai-native-framework.md` consistently. Grep for framework criteria references and flag drift when the data file evolves.

**Why:** The AI-native framework is integrated across all skills with duplicated detection logic (each skill asks its own AI posture question). When the framework criteria evolve (and they will, this space moves fast), updating the data file is easy but verifying all skills still align requires manual review.

**Effort:** S (human: ~2 hours / CC: ~15 min)

**Depends on:** v1.3.0 shipped (AI-native framework integration)
