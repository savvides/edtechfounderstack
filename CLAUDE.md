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

## Research corpus

`data/research/` contains 376 peer-reviewed papers across 19 learning science topics (spaced repetition, cognitive load, formative assessment, adaptive learning, etc.). See `data/research/README.md` for the index. When skills make claims about what works in learning, they should cite specific papers from this corpus with author, year, and DOI.
