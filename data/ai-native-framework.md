# AI-Native vs Bolted-On Framework

How to tell whether an edtech product is genuinely AI-native or whether AI was bolted on after the fact. This distinction shapes pricing, sales, fundraising, competitive positioning, and product architecture.

## The Framework

### 4 AI-Native Criteria

A product is AI-native when:

1. **Token/compute spend scales with usage.** Users can spend $100 or $1,000 via tokens as they use the product. The product's cost of goods sold (COGS) scales with the value delivered, not with the number of seats.

2. **Gets substantially better every 6 months as base models improve.** When GPT-5 or Claude 5 ships, the product automatically improves without engineering effort. The product rides the model improvement curve, it doesn't just wrap a static API call.

3. **Core workflow is impossible without AI, not just enhanced by it.** Remove all the AI and the product stops working. The AI isn't a feature... it's the engine.

4. **Creates behavior change when users try it.** Users don't just use the product, they change how they work. They stop doing things the old way because the AI-powered way is fundamentally different, not just faster.

### 5 Bolted-On Indicators

A product has bolted-on AI when:

1. **The main AI feature is a button with sparkle icons.** The AI is a discrete feature you click, not the underlying engine.

2. **There's a chat pane where you ask LLM questions.** A chatbot sidebar that answers questions about the product. The product existed before the chat pane and works fine without it.

3. **No memory or personalization beyond one chat.** Every interaction starts from scratch. The AI doesn't learn from the user's history, preferences, or behavior patterns.

4. **Users try it once and go back to using the app the "normal" way.** The AI feature gets novelty clicks but doesn't change the core workflow. Usage drops after the first week.

5. **AI is optional, not essential to the product working.** You can turn off every AI feature and the product still does its job. The AI is decorative.

### The Removal Test

The simplest way to classify: **remove all the AI from the product. Does it still work?**

- If yes: the AI is bolted on. The product is a traditional edtech tool with AI features added.
- If the product breaks or becomes useless: the AI is native. The product was built around AI from the ground up.

This isn't a judgment call. Both can be valid business models. But they have fundamentally different implications for pricing, fundraising, sales, and competitive positioning.

## AI-Native Architecture Patterns

These patterns apply to any AI-native edtech product, regardless of sector or buyer.

### Memory and personalization across sessions

AI-native products remember. An AI tutoring engine that adapts to a student's learning patterns over weeks is native. A chatbot that starts fresh every conversation is bolted on. The memory creates compounding value: the more you use it, the better it gets for you specifically.

### Model-agnostic design

AI-native products work across model providers. They improve with GPT, Claude, Gemini, or open-source models. The product's value isn't locked to one API. When a better model ships, the product gets better automatically. This is the "improves every 6 months" signal.

### Usage-based economics

The product's COGS scales with value delivered. Heavy users cost more to serve but also get more value. This naturally leads to usage-based or outcome-based pricing. Per-seat pricing creates a mismatch: one teacher using AI tutoring for 30 students consumes 10x the compute of a teacher who logs in once a month, but pays the same.

### Feedback loops

User behavior improves the system. Student responses train better recommendations. Teacher corrections improve content generation. Usage data identifies which AI outputs are helpful and which aren't. The product has a data flywheel, not just an API call.

## The Karpathy Hierarchy

*This section applies if you're building tools for developers or AI workflows. If you're building an AI tutoring app, LMS, or student-facing product, skip to "AI-Native Pricing Models" below.*

Andrej Karpathy articulated the hierarchy for connecting tools to AI coding agents: CLI at the top, API in the middle, MCP at the bottom.

**CLI (best):** Zero context cost until the moment you call it. The AI calls a command-line tool directly from the user's machine. No handshake, no persistent connection, no context window overhead.

**API (middle):** Lightweight and stateless. Each call is independent. The overhead is one request/response cycle. Works well for discrete operations.

**MCP (worst for context):** Eats context the moment it connects. Every MCP you load sits in your context window doing nothing until you call it. Five MCPs connected can lose 15-20% of your usable context before a single message is typed.

**The sub-agent pattern:** Dispatch work to sub-agents to preserve main session context. Carl Vellotti demonstrated this: a web research task with 10 tool calls and 30,000 tokens through a sub-agent moved the main session from 16% to 16.5% context used. Without the sub-agent, that same task would have filled to 25%. The difference between a session that lasts 30 messages and one that compacts after 5.

If you're building AI developer tools for education (coding platforms, AI-assisted curriculum for CS, teacher tooling for programming classes), this hierarchy directly affects your product architecture and user experience.

## AI-Native Pricing Models

### Usage-based

Per token, per API call, per computation. The user pays proportional to value consumed. Best for: products where heavy usage directly correlates with heavy value (AI tutoring, content generation, automated grading at scale).

### Outcome-based

Pay per successful tutoring session, per assessment completed, per learning outcome achieved. Best for: products that can measure specific outcomes and tie pricing to results.

### Hybrid

Base subscription for access + usage tier for AI features. Best for: products transitioning from traditional to AI-native, or selling to institutions that need predictable line items.

### Per-seat is structurally challenged for AI-native

AI-native products have variable COGS. A power user consuming 10x the compute pays the same as a casual user under per-seat pricing. At scale, this creates margin compression on your best customers.

**But: institutional procurement reality matters.** K-12 districts and universities often require per-seat or site-license pricing because their procurement systems can't process usage-based invoices. The budget line item needs to be predictable.

**Tactical advice:** Match your pricing to what the buyer can actually purchase.
- **Direct-to-consumer and enterprise:** Usage-based or outcome-based pricing. Your structural advantage.
- **Institutional procurement (districts, universities, state systems):** Per-seat or site-license pricing, but structure your margins to account for usage-based COGS. Build in usage tiers or fair-use policies to prevent margin compression from power users.
- **Both channels:** Hybrid pricing. Base subscription + usage tier. The subscription gives procurement a line item, the usage tier captures AI-native value.

The structural pressure on per-seat SaaS is real (massive valuation corrections in early 2026 hit per-seat AI-bolted companies hardest). But the tactical reality is: sell in the format your buyer can buy. Optimize internally for usage-based economics.

## Bolted-On Is Not Always Wrong

Some products should be bolted-on. Adding AI features to a working edtech product can be the right call when:

- The core product already solves a real problem without AI
- The AI features genuinely enhance specific workflows (not just sparkle icons)
- The buyer doesn't care about AI architecture, they care about outcomes
- The market isn't ready for a pure AI-native approach in that segment

The framework is diagnostic, not prescriptive. It helps founders understand what they've built and the implications for their strategy. Bolted-on products compete on features and distribution. AI-native products compete on improving output quality over time. Both can win. The mistake is not knowing which game you're playing.

---

Last updated: 2026-04-01
