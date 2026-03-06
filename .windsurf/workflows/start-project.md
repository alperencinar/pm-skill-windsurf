---
description: Analyze a project idea end-to-end and generate a full knowledge base of MD files in NewProjectDetails/ — strategy, PRD, personas, GTM, metrics, roadmap, and more
---

# /start-project -- Full Project Knowledge Base Generator

Take a brief project description and produce a comprehensive set of markdown documents covering every aspect needed to build, launch, and grow the product. All files are saved to the `NewProjectDetails/` folder so Windsurf can reference them later when coding, designing, and executing.

## Invocation

```
/start-project AI-powered meal planning app for busy parents
/start-project B2B SaaS analytics dashboard for e-commerce managers
/start-project [paste or upload a project brief]
```

## What This Produces

After gathering context from the user, this workflow generates **up to 15 knowledge-base documents** in the `NewProjectDetails/` folder:

| # | File | Purpose |
|---|------|---------|
| 1 | `01-project-brief.md` | Refined project overview, goals, scope, and constraints |
| 2 | `02-product-strategy.md` | 9-section Strategy Canvas: vision → defensibility |
| 3 | `03-value-proposition.md` | JTBD value propositions per segment |
| 4 | `04-user-personas.md` | 3-4 target personas with JTBD, pains, and gains |
| 5 | `05-competitive-analysis.md` | Competitor landscape, strengths, weaknesses, differentiation |
| 6 | `06-business-model.md` | Lean Canvas or Startup Canvas with revenue model |
| 7 | `07-prd.md` | Product Requirements Document with user stories and acceptance criteria |
| 8 | `08-technical-requirements.md` | Tech stack recommendations, architecture notes, API needs, data model outline |
| 9 | `09-ui-ux-guidelines.md` | Design principles, key screens, user flows, accessibility notes |
| 10 | `10-metrics-dashboard.md` | North Star, input metrics, health metrics, alert thresholds |
| 11 | `11-gtm-strategy.md` | Go-to-market: beachhead segment, ICP, channels, launch plan |
| 12 | `12-growth-strategy.md` | Growth loops, GTM motions, 90-day growth plan |
| 13 | `13-pricing-strategy.md` | Pricing model, tiers, competitive benchmark |
| 14 | `14-roadmap.md` | Outcome-focused roadmap: Now / Next / Later |
| 15 | `15-risks-and-assumptions.md` | Pre-mortem risks, critical assumptions, validation experiments |

## Workflow

### Step 1: Gather Project Context

Ask the user for a project brief. Be conversational — start with the essentials, fill gaps as you go:

**Must-have context:**
- What is the product idea? (one paragraph is enough)
- Who is the target user? (segment, role, pain point)
- What problem does it solve? What's the current alternative?
- What is the business model? (subscription, transaction, marketplace, freemium, etc.)

**Nice-to-have context:**
- What stage is the project? (idea, validated, MVP, scaling)
- Any technical constraints or preferences? (platform, language, framework)
- Budget and team size
- Timeline and deadlines
- Competitive landscape — any known competitors?
- Any existing research, data, or documents? (accept uploads)

If the user provides only a brief sentence, infer reasonable defaults and confirm: "Based on your description, I'm assuming [X]. Correct?"

### Step 2: Generate the Knowledge Base

Create the `NewProjectDetails/` folder if it doesn't exist. Then generate each document sequentially, building on insights from previous documents.

**Important**: Each document must be self-contained and actionable — not placeholder text. Windsurf will use these files as the source of truth when building the product.

---

#### 2.1: Project Brief (`01-project-brief.md`)

Synthesize the user's input into a structured brief:

```
# Project Brief: [Product Name]

## Overview
[2-3 sentence product description]

## Problem Statement
[What problem exists, who has it, how painful it is]

## Solution
[High-level approach — what the product does]

## Target Users
[Primary and secondary segments]

## Goals
- [Goal 1 with success metric]
- [Goal 2 with success metric]

## Scope
**In scope**: [what we're building]
**Out of scope**: [what we're NOT building]

## Constraints
[Technical, budget, timeline, regulatory]

## Key Assumptions
[What must be true for this to work]
```

---

#### 2.2: Product Strategy (`02-product-strategy.md`)

Apply the **product-strategy** skill (read `skills/pm-product-strategy/product-strategy.md`) and **product-vision** skill (read `skills/pm-product-strategy/product-vision.md`):

Cover all 9 sections: Vision, Target Segments, Pain Points & Value, Value Propositions, Strategic Trade-offs, Key Metrics, Growth Engine, Core Capabilities, Defensibility.

---

#### 2.3: Value Proposition (`03-value-proposition.md`)

Apply the **value-proposition** skill (read `skills/pm-product-strategy/value-proposition.md`):

Create JTBD value propositions for each target segment using the 6-part template (Who, Why, What Before, How, What After, Alternatives). Include reusable marketing/sales/onboarding copy.

---

#### 2.4: User Personas (`04-user-personas.md`)

Apply the **user-personas** skill (read `skills/pm-market-research/user-personas.md`):

Create 3-4 distinct personas with: name, role, JTBD, key pains, key gains, behavioral patterns, product expectations, and a representative quote.

---

#### 2.5: Competitive Analysis (`05-competitive-analysis.md`)

Apply the **competitor-analysis** skill (read `skills/pm-market-research/competitor-analysis.md`):

Use web research to identify 3-5 direct competitors and 2-3 indirect competitors. Feature comparison matrix, positioning map, differentiation opportunities, and competitive threats.

---

#### 2.6: Business Model (`06-business-model.md`)

Apply the **startup-canvas** skill (read `skills/pm-product-strategy/startup-canvas.md`) for new products, or **business-model** skill (read `skills/pm-product-strategy/business-model.md`) for existing:

Include cost structure, revenue streams, and riskiest assumptions. Add the **monetization-strategy** skill (read `skills/pm-product-strategy/monetization-strategy.md`) for alternative revenue models.

---

#### 2.7: PRD (`07-prd.md`)

Apply the **create-prd** skill (read `skills/pm-execution/create-prd.md`):

Full 8-section PRD: Executive Summary, Background, Objectives & Metrics, Target Users, User Stories (P0/P1/P2 with acceptance criteria), Solution Overview, Open Questions, Timeline.

---

#### 2.8: Technical Requirements (`08-technical-requirements.md`)

Based on the PRD and project context, generate:

```
# Technical Requirements: [Product Name]

## Recommended Tech Stack
| Layer | Technology | Why |
|-------|-----------|-----|
| Frontend | [framework] | [rationale] |
| Backend | [framework] | [rationale] |
| Database | [type] | [rationale] |
| Hosting | [platform] | [rationale] |
| Auth | [service] | [rationale] |

## Architecture Overview
[High-level architecture description — monolith vs microservices, API design approach]

## Data Model
[Key entities and relationships]

## API Endpoints
[Core endpoints needed for MVP]

## Third-Party Integrations
[External services: payments, email, analytics, etc.]

## Security Requirements
[Auth, data encryption, compliance needs]

## Performance Requirements
[Expected load, latency targets, scalability approach]

## DevOps & Deployment
[CI/CD, environments, monitoring]
```

---

#### 2.9: UI/UX Guidelines (`09-ui-ux-guidelines.md`)

Based on the personas and PRD, generate:

```
# UI/UX Guidelines: [Product Name]

## Design Principles
[3-5 guiding principles for the product's UX]

## Key Screens
[List of primary screens/pages with purpose and key elements]

## User Flows
[Step-by-step flows for core use cases — onboarding, primary action, settings]

## Navigation Structure
[Information architecture — how screens connect]

## Responsive Strategy
[Mobile-first? Desktop-first? Key breakpoints]

## Accessibility
[WCAG guidelines, minimum requirements]

## Brand & Visual Direction
[Color palette suggestions, typography approach, tone of voice]
```

---

#### 2.10: Metrics Dashboard (`10-metrics-dashboard.md`)

Apply the **metrics-dashboard** skill (read `skills/pm-product-discovery/metrics-dashboard.md`) and **north-star-metric** skill (read `skills/pm-marketing-growth/north-star-metric.md`):

North Star Metric, input metrics, health metrics, counter-metrics, alert thresholds, and review cadence.

---

#### 2.11: GTM Strategy (`11-gtm-strategy.md`)

Apply the **gtm-strategy** skill (read `skills/pm-go-to-market/gtm-strategy.md`), **beachhead-segment** skill (read `skills/pm-go-to-market/beachhead-segment.md`), and **ideal-customer-profile** skill (read `skills/pm-go-to-market/ideal-customer-profile.md`):

Beachhead segment, ICP, positioning, messaging, channel strategy, launch timeline, and success metrics.

---

#### 2.12: Growth Strategy (`12-growth-strategy.md`)

Apply the **growth-loops** skill (read `skills/pm-go-to-market/growth-loops.md`) and **gtm-motions** skill (read `skills/pm-go-to-market/gtm-motions.md`):

Evaluate growth loops (viral, usage, collaboration, UGC, referral), GTM motions (PLG, inbound, outbound, community, partners), and a 90-day growth plan.

---

#### 2.13: Pricing Strategy (`13-pricing-strategy.md`)

Apply the **pricing-strategy** skill (read `skills/pm-product-strategy/pricing-strategy.md`):

Pricing model recommendation, tier structure, competitive benchmark, free/trial strategy, and revenue projections.

---

#### 2.14: Roadmap (`14-roadmap.md`)

Apply the **outcome-roadmap** skill (read `skills/pm-execution/outcome-roadmap.md`):

Outcome-focused roadmap in Now/Next/Later format with success metrics per outcome. Include MVP definition and phasing.

---

#### 2.15: Risks & Assumptions (`15-risks-and-assumptions.md`)

Apply the **pre-mortem** skill (read `skills/pm-execution/pre-mortem.md`), **identify-assumptions-new** skill (read `skills/pm-product-discovery/identify-assumptions-new.md`), and **prioritize-assumptions** skill (read `skills/pm-product-discovery/prioritize-assumptions.md`):

Tigers/Paper Tigers/Elephants risk classification, critical assumptions mapped on Impact × Uncertainty matrix, and validation experiments for the top 5 assumptions.

---

### Step 3: Generate Summary Index

After all documents are created, generate an index file:

**`NewProjectDetails/00-index.md`**:

```
# [Product Name] — Project Knowledge Base

Generated by `/start-project` on [date].

## Documents

| # | Document | Description |
|---|----------|-------------|
| 01 | [Project Brief](01-project-brief.md) | Overview, goals, scope, constraints |
| 02 | [Product Strategy](02-product-strategy.md) | Vision, segments, trade-offs, defensibility |
| 03 | [Value Proposition](03-value-proposition.md) | JTBD value props per segment |
| 04 | [User Personas](04-user-personas.md) | Target user profiles |
| 05 | [Competitive Analysis](05-competitive-analysis.md) | Competitor landscape |
| 06 | [Business Model](06-business-model.md) | Revenue model and cost structure |
| 07 | [PRD](07-prd.md) | Requirements and user stories |
| 08 | [Technical Requirements](08-technical-requirements.md) | Tech stack, architecture, APIs |
| 09 | [UI/UX Guidelines](09-ui-ux-guidelines.md) | Design principles, screens, flows |
| 10 | [Metrics Dashboard](10-metrics-dashboard.md) | North Star and supporting metrics |
| 11 | [GTM Strategy](11-gtm-strategy.md) | Go-to-market plan |
| 12 | [Growth Strategy](12-growth-strategy.md) | Growth loops and 90-day plan |
| 13 | [Pricing Strategy](13-pricing-strategy.md) | Pricing model and tiers |
| 14 | [Roadmap](14-roadmap.md) | Now / Next / Later outcomes |
| 15 | [Risks & Assumptions](15-risks-and-assumptions.md) | Risk analysis and validation plan |

## How to Use These Documents

These files are the **single source of truth** for this project. When building the product:
- Reference `07-prd.md` for feature requirements and acceptance criteria
- Reference `08-technical-requirements.md` for tech stack and architecture decisions
- Reference `09-ui-ux-guidelines.md` for design direction
- Reference `04-user-personas.md` to stay grounded in user needs
- Reference `14-roadmap.md` for prioritization and phasing

When making product decisions, check:
- `02-product-strategy.md` for strategic alignment
- `10-metrics-dashboard.md` for what to measure
- `15-risks-and-assumptions.md` for known risks

When preparing for launch:
- `11-gtm-strategy.md` for go-to-market plan
- `12-growth-strategy.md` for growth mechanisms
- `13-pricing-strategy.md` for pricing decisions
```

### Step 4: Confirm and Offer Next Steps

Present a summary of all generated files with a brief highlight from each. Then offer:

- "Want me to **start building the product** using these documents as the spec?"
- "Should I **deep-dive into any document** — add more detail or refine a section?"
- "Want me to **create user stories and sprint plan** from the PRD?"
- "Should I **generate test scenarios** for the MVP features?"
- "Want me to **set up the project structure** (folders, boilerplate code, config files)?"

## Notes

- This is a comprehensive workflow — expect 10-20 minutes for full generation. Let the user know upfront.
- Each document should be **specific to the project**, not generic templates with placeholders. Use real product details.
- The `NewProjectDetails/` folder becomes the project's knowledge base — Windsurf references these files in future conversations.
- If the user provides very little context, make reasonable assumptions, state them clearly, and proceed. The user can refine later.
- For technical requirements, tailor recommendations to the project type (web app, mobile, API, marketplace, etc.).
- If the user already has some documents, skip those sections and focus on gaps.
- Documents should reference each other where relevant (e.g., PRD references personas, GTM references value proposition).
