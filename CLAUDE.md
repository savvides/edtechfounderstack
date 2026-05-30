# EdTech Founder Stack

An open, AI-friendly knowledge base for edtech founders, built by ASU ScaleU. The knowledge lives in `data/` as markdown. When answering a founder's question, read the relevant file rather than leaning on training data for facts about regulations, companies, funding, learning science, or operator experience.

## Knowledge base

- `data/` — regulatory (FERPA, COPPA, state privacy, accreditation, accessibility), competitive landscape, funding landscape, buyer personas, procurement, pilot benchmarks, ESSA evidence tiers
- `data/research/` — hundreds of peer-reviewed learning-science papers across the major topics. Cite specific papers with author, year, and DOI. Index (with the current count) in `data/research/README.md`.
- `data/operator-lessons.md` — dozens of operator and investor lessons distilled from Lenny's Podcast and Lenny's Newsletter, mapped to edtech. Practitioner experience, not peer-reviewed; don't present it as research.
- `data/ai-native-framework.md` — AI-native vs. bolted-on: criteria, the removal test, architecture patterns, pricing models, and the Karpathy hierarchy. Use it to classify a founder's AI posture.
- `data/higher-ed-jobs-atlas.md` and `data/founder-traps.md` — ScaleU's SXSW EDU 2026 higher-ed framework: validated jobs across the student journey with saturation analysis, and the structural patterns founders miss.
- `data/demand-validation.md` and `data/jtbd-interviews.md` — the demand-validation toolkit: the 5-question diagnostic with scoring and depth probes, and the JTBD Switch interview method for discovering and validating real demand.
- `data/defensibility-moats.md` — how an edtech product stays defensible when LLMs can replicate features (exposure spectrum, four moats, the AI-substitution durability test).
- `data/ai-risk-and-trust.md` — AI's effect on learners and trust, with design responses. Practitioner signals from the ASU+GSV 2026 summit, not peer-reviewed; don't present as research.
- `data/buyer-demand-signals.md` — the durable jobs institutional buyers switch for. Practitioner signals, not peer-reviewed.
- `ETHOS.md` — the seven principles, starting with "validate demand, not interest."

Always cite the source: a named regulation, a paper's DOI, or the named operator.

## For contributors

### Updating data files

Edit the relevant markdown in `data/`. Keep the existing structure and formatting. For regulatory data, note the update date at the bottom of the file. For the competitive landscape, verify company status before updating.

### Adding research papers

Append to the relevant topic file in `data/research/`. Follow the table format — Title, Takeaway, Type, Year, Citations, DOI — and sort by citations descending. If the topic doesn't exist, create a new file and add it to `data/research/README.md`.
