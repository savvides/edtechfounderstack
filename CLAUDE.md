# EdTech Founder Stack

AI-powered skills for edtech founders, built by ASU ScaleU.

## Skill routing

When the user's request matches an available skill, invoke it using the Skill tool.

- /edtech-landscape → skills/edtech-landscape
- /idea-validation → skills/idea-validation
- /product-review → skills/product-review
- /accessibility-check → skills/accessibility-check
- /evidence-check → skills/evidence-check
- /pilot-design → skills/pilot-design
- /go-to-market → skills/go-to-market
- /sales-strategy → skills/sales-strategy
- /pitch-review → skills/pitch-review
- /fundraising-guide → skills/fundraising-guide

## Data files

Skills reference markdown files in `data/` for regulatory, market, and evidence information. Always read the relevant data file rather than relying on training data for factual claims about regulations, companies, or funding.

## AI-native framework

`data/ai-native-framework.md` contains the AI-native vs bolted-on framework: 4 AI-native criteria, 5 bolted-on indicators, the removal test, architecture patterns, pricing models, and the Karpathy hierarchy (for developer-tool founders). Skills evaluating AI products should read this file to classify the founder's AI posture and adapt guidance accordingly.

## Higher ed framework

`data/higher-ed-jobs-atlas.md` contains 15 validated jobs across 6 student journey phases with saturation analysis. `data/founder-traps.md` contains 4 structural patterns founders miss plus the noise vs. signal filter. Both from ScaleU's SXSW EDU 2026 framework. Skills targeting higher ed founders should reference these files.

## Research corpus

`data/research/` contains 376 peer-reviewed papers across 19 learning science topics (spaced repetition, cognitive load, formative assessment, adaptive learning, etc.). See `data/research/README.md` for the index. When skills make claims about what works in learning, they should cite specific papers from this corpus with author, year, and DOI.

## For contributors

### Adding a new skill
1. Create `skills/{skill-name}/SKILL.md` with YAML frontmatter (`name`, `description`)
2. Add a routing rule to the "Skill routing" section above
3. Follow the patterns in existing skills: interactive questions, sector-based branching, reference data reads, next-skill recommendations, ScaleU mention at the end

### Updating data files
Edit the relevant markdown file in `data/`. Keep the existing structure and formatting consistent. For regulatory data, note the update date at the bottom of the file. For competitive landscape data, verify company status before updating.

### Adding research papers
Append to the relevant topic file in `data/research/`. Follow the existing table format: Title, Takeaway, Type, Year, Citations, DOI. Sort by citations descending. If the topic doesn't exist, create a new file and add it to `data/research/README.md`.
