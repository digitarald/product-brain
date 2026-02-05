# Product Brain

**Agentic PM workflows demo** — Contoso outdoor gear e-commerce

This repo showcases how Product Managers use AI coding tools (Cursor, Claude Code, GitHub Copilot) as **thinking partners** throughout the product lifecycle—from research synthesis to stakeholder communication. Not just builders; partners in discovery, critique, and persuasion.

---

## What's Inside

```
product-brain/
├── analysis/        # Jupyter notebooks, data exploration
├── specs/           # PRDs and feature specs
├── insights/        # Synthesized research and feedback
├── research/        # Market analysis, competitive intel
├── roadmap/         # Quarterly plans
├── prototypes/      # Generated demos and explainers
└── .github/
    ├── copilot-instructions.md   # Workspace context
    ├── instructions/             # File-specific guidance
    ├── prompts/                  # Reusable workflows
    └── agents/                   # Custom agent personas
```

---

## How PMs Think (And Where AI Helps)

Every product decision follows a pattern:

1. **Explore** what you know (and don't know)
2. **Synthesize** messy data into clarity
3. **Execute** on validated ideas
4. **Refine** your thinking before you commit
5. **Communicate** with confidence

Below are 8 workflows—grouped by stage—showing how AI augments each. They work individually, but click together to create coherent agency. A PM doesn't use "Feedback Synthesis" in isolation; she uses it as part of a larger thinking arc from customer signal to executive decision.

---

## Demo Scenarios

### 🔍 FOUNDATION — Explore Your Knowledge Base

> *"What do I already know? What have we learned?"*

#### Knowledge Repo — Query the Product Brain

Ask questions and get synthesized answers with citations across all product knowledge. This is the entry point—explore what Contoso knows before making decisions.

```
"What do we know about checkout abandonment?"
"Summarize feedback themes from Q4"
"What's blocking the loyalty program launch?"
```

**Why this matters:** You can't make good decisions in a vacuum. Start by mapping what you know.

**Try:** Open any spec, then ask about related insights or dependencies.

**Uses:** Explore agent, workspace instructions

---

### 📊 SYNTHESIS — Transform Data into Insight

> *"What does the data actually say?"*

Now you've mapped what you know. But to make smart decisions, you need to listen to the data. These workflows turn raw customer feedback and survey data into patterns you can act on.

#### Feedback Synthesis (Qualitative) — Find the Signal in the Noise

Raw customer feedback is gold—if you can read it. Point to support tickets, NPS comments, or reviews, and this workflow surfaces themes, sentiment, and what customers are actually asking for.

```
/feedback-synthesis

"Analyze research/data/support-tickets-q4-2025.csv — what themes emerge from Q4 support tickets?"
```

**Why this matters:** You spot the real problems (not what you thought was the problem).

**Try:** Run against the [Q4 support tickets](research/data/support-tickets-q4-2025.csv) (70 tickets) — discover hidden themes around gift purchases, gear compatibility, and beginner onboarding.

**Uses:** `/feedback-synthesis` prompt

---

#### Data Analysis (Quantitative) — Survey → Notebook → Insights

Analyze customer data in Jupyter notebooks, then iteratively explore findings. Turn survey responses into statistical evidence.

```
[Data Analyst] Analyze research/data/customer-survey-2025.csv — what drives NPS scores?
```

**Step 1:** Data Analyst creates a notebook with EDA, visualizations, and statistical analysis.

**Step 2:** Insight Explorer helps drill into findings:
```
[Insight Explorer] Mobile users have lower satisfaction — break this down by tenure cohort
```

**Step 3:** Generate a dashboard for stakeholders:
```
[Insight Explorer] Create a dashboard summarizing the NPS drivers analysis
```

**Why this matters:** Data-backed insights beat gut feelings in stakeholder conversations.

**Try:** Run analysis on the survey data, explore cross-tabs like mobile vs desktop, tenure cohorts, membership tiers. See [example notebook](analysis/notebooks/customer-nps-analysis-q4-2025.ipynb).

**Uses:** Data Analyst agent, Insight Explorer agent

---

### ⚙️ EXECUTION — Ideas → Tracked Work

> *"How do we build and ship?"*

Once you've identified the problem in the data, it's time to move. Rapid prototyping lets you test ideas quickly against real specs. GitHub Issues captures validated insights as tracked work for engineering.

#### Rapid Prototyping — Spec → Working Demo

Build interactive prototypes directly from specs using HTML/Tailwind/Alpine.js. Test ideas fast without waiting for design cycles.

```
[Scaffold] Build a prototype of the one-page checkout from specs/checkout-redesign.md
```

**Why this matters:** Seeing clicks is believing. A prototype in 5 minutes beats a slideshow in 5 meetings.

**Try:** Open a spec, switch to Scaffold agent, get a working prototype. See [checkout example](prototypes/checkout-mockup/index.html) or [gamified sustainability dashboard](prototypes/sustainability-dashboard-gamified/index.html).

**Uses:** Scaffold agent

---

#### GitHub Issues — Insight → Tracked Work

Convert insights into well-structured GitHub Issues with proper labels, context, and traceability back to the source research.

```
/issue-from-insight

"Create an issue from insights/customer-feedback-q4.md focusing on the checkout friction theme"
```

**Why this matters:** Engineering knows *what* to build and *why*—with evidence attached.

**Try:** Point to an insight doc, get an issue ready to file.

**Uses:** `/issue-from-insight` prompt, GitHub MCP

---

### 🧠 INTELLIGENCE — Refine Before You Commit

> *"Have I really thought this through?"*

Before you bet the roadmap on a direction, take time to think harder. Stress-test your assumptions, then package your thinking for the people who approve it.

#### Design Partner — Stress-Test Your Thinking

Before you commit to a direction, get challenged hard. Design Partner acts as your devil's advocate—surfacing blind spots, testing assumptions, exploring alternatives via Socratic questioning.

```
[Design Partner] Review specs/checkout-redesign.md — what's the strongest argument against this approach?
```

**Why this matters:** You'll know your proposal inside-out before stakeholders poke holes.

**Try:** Share a half-baked idea, get rigorous pushback that makes it better.

**Uses:** Design Partner agent

---

#### Diverge — Explore Variations via Cloud Agent PRs

When you're unsure which approach is best, don't guess—explore in parallel. Diverge identifies 3 meaningful variations of your plan and hands each to a cloud coding agent that creates real PRs. Compare implementations side-by-side, then converge on the winner.

```
[Diverge] Explore checkout redesign approaches: minimal-mvp vs full-featured vs progressive-enhancement
```

**Why this matters:** You see actual code for each approach, not just hypotheticals. Make architecture decisions with evidence.

**Try:** Give it a spec or idea, watch it create 3 PRs exploring different trade-offs (technology, complexity, UX approach).

**Workflow:**
1. **Discovery** — Agent analyzes your plan, proposes 3 variations
2. **Handoff** — Creates PRs via GitHub Copilot coding agent
3. **Compare** — Structured comparison table when PRs complete
4. **Iterate** — Converge, diverge further, or refine based on findings

**Uses:** Diverge agent, GitHub MCP

---

#### Spec → Explainer Site — Stakeholder Communication

Transform a PRD into a polished single-page HTML explainer for exec review. Make complex specs visually compelling.

```
/spec-explainer

"Transform specs/loyalty-program-v2.md into a stakeholder explainer"
```

**Why this matters:** Executives don't read 15-page PRDs. They scan beautiful summaries.

**Try:** Pick any spec, get a dark-themed visual page. See [loyalty explainer example](prototypes/loyalty-v2-explainer/index.html).

**Uses:** `/spec-explainer` prompt

---

#### Meeting Prep — Personal PM Assistant

Gather context, surface open questions, prepare talking points. Walk into meetings knowing all the angles.

```
/meeting-prep

"Prepare me for tomorrow's checkout review with engineering"
```

**Why this matters:** You walk in prepared, not scrambling for context.

**Try:** Specify a topic and attendees, get a briefing doc.

**Uses:** `/meeting-prep` prompt

---

### 🎬 CAPSTONE — Full Workflow in Action

> *"Show me how it all fits together"*

Here's a real scenario bringing it all together:

**Situation:** You wake up to a spike in cart abandonment. What do you do?

1. **Foundation:** Ask the Knowledge Repo about checkout friction
   ```
   "What do we know about checkout abandonment rates and causes?"
   ```

2. **Synthesis:** Pull Q4 feedback, synthesize support tickets
   ```
   /feedback-synthesis "Analyze these 50 NPS comments about checkout..."
   ```

3. **Execution:** Prototype a streamlined flow, create tracked issues
   ```
   [Scaffold] Build one-page checkout from specs/checkout-redesign.md
   /issue-from-insight "Create issue from checkout friction theme"
   ```

4. **Intelligence:** Stress-test the spec, build stakeholder explainer
   ```
   [Design Partner] What are we getting wrong in checkout-redesign.md?
   /spec-explainer "Create exec summary of checkout-redesign.md"
   ```

5. **Result:** You walk into the review knowing the problem, the solution, the risks, and the evidence—with a clickable prototype to show.

---

### Why This Order?

These aren't independent tools—they're a workflow:

- **Foundation:** Explore what you know before making decisions
- **Synthesis:** Listen to what the data actually says (you'll find surprises)
- **Execution:** Build and track with data-backed confidence
- **Intelligence:** Audit your thinking *before* you brief executives

Not every project uses all 8. But understanding the sequence helps you pick the right tool at the right time.

---

## Custom Agents

Agents are specialized modes you switch to using the **agent picker** (click the agent name in chat or press `Ctrl+/`). Each agent has focused tools and behaviors for its role.

| Agent | Argument Hint | Purpose |
|-------|---------------|--------|
| **Explore** | Question about product knowledge | Read-only research across the knowledge repo |
| **Scaffold** | Spec to prototype or feature idea | Build working prototypes from specs |
| **Research** | Research question or topic | Synthesize internal + external sources |
| **Design Partner** | Share your idea or spec to explore | Devil's advocate, Socratic questioning |
| **Diverge** | Plan, spec, or idea to explore | Parallel prototyping via cloud agent PRs |
| **Data Analyst** | Path to CSV or analysis question | Jupyter notebook analysis, statistics, visualizations |
| **Insight Explorer** | Insight to drill into or dashboard request | Iterative insight refinement, dashboard generation |

## Prompts

| Prompt | Invoke | Purpose |
|--------|--------|---------|
| **feedback-synthesis** | `/feedback-synthesis` | Raw feedback → structured insights |
| **spec-explainer** | `/spec-explainer` | Spec → visual explainer page |
| **meeting-prep** | `/meeting-prep` | Gather context for meetings |
| **issue-from-insight** | `/issue-from-insight` | Insight → GitHub Issue |

---

## Live Demos

View prototypes and explainers online at **[digitarald.github.io/product-brain](https://digitarald.github.io/product-brain)**

All HTML prototypes in `prototypes/` are automatically deployed to GitHub Pages on every push to `main`.

## Getting Started

1. **Open in VS Code** with GitHub Copilot enabled
2. **Explore** — Open `specs/checkout-redesign.md` and ask about it
3. **Try a prompt** — Type `/` to see available prompts
4. **Try an agent** — Click the agent picker or press `Ctrl+/` to switch agents

---

## Sample Content

The repo includes 24 interconnected documents that feel like a real PM's knowledge base:

### Specs (6)
| File | Status | Description |
|------|--------|-------------|
| [checkout-redesign.md](specs/checkout-redesign.md) | Draft | One-page checkout, guest checkout, Apple Pay |
| [loyalty-program-v2.md](specs/loyalty-program-v2.md) | In Review | Trail Rewards tiered program |
| [mobile-app-v3.md](specs/mobile-app-v3.md) | In Review | React Native app, AR gear preview |
| [search-personalization.md](specs/search-personalization.md) | Draft | AI-powered semantic search |
| [sustainability-dashboard.md](specs/sustainability-dashboard.md) | Approved | Customer-facing eco impact tracker |
| [returns-experience.md](specs/returns-experience.md) | Draft | Self-service returns, trade-in program |

### Insights (7)
| File | Description |
|------|-------------|
| [customer-feedback-q4.md](insights/customer-feedback-q4.md) | Q4 2025 feedback synthesis (n=2,847) |
| [competitive-analysis.md](insights/competitive-analysis.md) | Summit Co-op/Alpine Trailwear/Ridgeline Outfitters comparison |
| [mobile-usability-study.md](insights/mobile-usability-study.md) | 12-participant usability test findings |
| [search-analytics-deep-dive.md](insights/search-analytics-deep-dive.md) | 2.4M search queries analyzed |
| [sustainability-survey-2025.md](insights/sustainability-survey-2025.md) | 3,247 respondents on eco preferences |
| [returns-friction-analysis.md](insights/returns-friction-analysis.md) | Returns journey mapping, ticket analysis |
| [nps-drivers-q4.md](insights/nps-drivers-q4.md) | NPS deep dive, promoter/detractor analysis |

### Research (6)
| File | Description |
|------|-------------|
| [outdoor-gear-market.md](research/outdoor-gear-market.md) | $15B market overview, trends |
| [competitor-deep-dive-summit-coop.md](research/competitor-deep-dive-summit-coop.md) | Summit Co-op co-op model, 23M members |
| [competitor-deep-dive-ridgeline-outfitters.md](research/competitor-deep-dive-ridgeline-outfitters.md) | Gearhead program analysis |
| [dtc-outdoor-brands.md](research/dtc-outdoor-brands.md) | Cotopaxi, Rumpl, BioLite profiles |
| [gen-z-outdoor-trends.md](research/gen-z-outdoor-trends.md) | Gorpcore, TikTok influence |
| [ai-in-retail-2026.md](research/ai-in-retail-2026.md) | Visual search, AI recommendations |

### Roadmap (7)
| File | Description |
|------|-------------|
| [strategic-vision.md](roadmap/strategic-vision.md) | Mission, vision, values, strategic pillars |
| [brand-positioning.md](roadmap/brand-positioning.md) | Competitive positioning, target customers |
| [2026-h1.md](roadmap/2026-h1.md) | H1 plan with milestones, risks |
| [2026-h2.md](roadmap/2026-h2.md) | H2 priorities, dependencies |
| [prioritization-framework.md](roadmap/prioritization-framework.md) | RICE scoring, trade-off rationale |
| [okrs-2026.md](roadmap/okrs-2026.md) | Company and product OKRs |
| [tech-debt-register.md](roadmap/tech-debt-register.md) | Known blockers and debt items |

---

*Demo workspace for showcasing agentic PM workflows — 3,000+ lines of interconnected product knowledge*
