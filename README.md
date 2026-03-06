[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/LICENSE)

# PM Skills for Windsurf: The AI Operating System for Better Product Decisions

> 65 PM skills and 36 chained workflows across 8 domains. Powered by Windsurf Cascade. From discovery to strategy, execution, launch, and growth.

## Start Here

New idea? → `/discover`  
Need strategic clarity? → `/strategy`  
Writing a PRD? → `/write-prd`  
Planning a launch? → `/plan-launch`  
Defining metrics? → `/north-star`

## Why PM Skills?

Generic AI gives you text. PM Skills gives you structure.

Each skill encodes a proven PM framework — discovery, assumption mapping, prioritization, strategy — and walks you through it step by step. You get the rigor of Teresa Torres, Marty Cagan, and Alberto Savoia built into your daily workflow, not sitting on a bookshelf.

The result: better product decisions, not just faster documents.

## How It Works (Skills & Workflows)

**Skills** are the building blocks. Each skill gives Cascade domain knowledge, analytical frameworks, or guided instructions for a specific PM task. Skills live in `skills/<domain>/` as standalone markdown files. Some skills serve multiple workflows.

**Workflows** are user-triggered via `/slash-command`. They chain one or more skills into an end-to-end process. For example, `/discover` chains four skills together: brainstorm-ideas → identify-assumptions → prioritize-assumptions → brainstorm-experiments.

Workflows are designed to flow into each other, matching the PM lifecycle. After any workflow completes, it suggests relevant next workflows — just follow the prompts.

## Installation

This repo is already structured for Windsurf. Clone it into your project:

```bash
git clone https://github.com/phuryn/pm-skills.git
```

The key directories:
- **`.windsurf/workflows/`** — 36 slash-command workflows (invoked via `/command-name` in Cascade)
- **`.windsurf/rules/`** — Global context that tells Cascade about the PM skills system
- **`skills/`** — 65 domain-knowledge skill files organized by PM domain

Cascade will automatically detect the workflows and make them available as `/slash-commands`.

---

## Available Domains

### 1. pm-product-discovery

Continuous product discovery: ideation, experiments, assumption testing, feature prioritization, Opportunity Solution Trees, and customer interviews.

**Skills (13):**

- `brainstorm-ideas-existing` — Multi-perspective ideation for existing products (PM, Designer, Engineer)
- `brainstorm-ideas-new` — Ideation for new products in initial discovery
- `brainstorm-experiments-existing` — Design experiments to test assumptions for existing products
- `brainstorm-experiments-new` — Design lean startup pretotypes for new products (Alberto Savoia)
- `identify-assumptions-existing` — Identify risky assumptions across Value, Usability, Viability, and Feasibility
- `identify-assumptions-new` — Identify risky assumptions across 8 risk categories including Go-to-Market, Strategy, and Team
- `prioritize-assumptions` — Prioritize assumptions using an Impact × Risk matrix with experiment suggestions
- `prioritize-features` — Prioritize a feature backlog based on impact, effort, risk, and strategic alignment
- `analyze-feature-requests` — Analyze and categorize customer feature requests by theme and strategic fit
- `opportunity-solution-tree` — Build an Opportunity Solution Tree (Teresa Torres) — outcome → opportunities → solutions → experiments
- `interview-script` — Create a structured customer interview script with JTBD probing questions
- `summarize-interview` — Summarize an interview transcript into JTBD, satisfaction signals, and action items
- `metrics-dashboard` — Design a product metrics dashboard with North Star, input metrics, and alert thresholds

**Workflows (5):**

- `/discover` — Full discovery cycle: ideation → assumption mapping → prioritization → experiment design
- `/brainstorm` — Multi-perspective ideation (`ideas|experiments` × `existing|new`)
- `/triage-requests` — Analyze and prioritize a batch of feature requests
- `/interview` — Prepare an interview script or summarize a transcript (`prep|summarize`)
- `/setup-metrics` — Design a product metrics dashboard

**Examples:**

- `What are the riskiest assumptions for our AI writing assistant idea?`
- `/discover AI-powered meeting summarizer for remote teams`
- `/brainstorm experiments existing — We need to reduce churn in our onboarding flow`

### 2. pm-product-strategy

Product strategy, vision, business models, pricing, and macro environment analysis. Covers the full strategic toolkit from vision crafting through competitive landscape scanning.

**Skills (12):**

- `product-strategy` — Comprehensive 9-section Product Strategy Canvas (vision → defensibility)
- `startup-canvas` — Startup Canvas combining Product Strategy (9 sections) + Business Model — an alternative to BMC and Lean Canvas for new products
- `product-vision` — Craft an inspiring, achievable, and emotional product vision
- `value-proposition` — 6-part JTBD value proposition (Who, Why, What before, How, What after, Alternatives)
- `lean-canvas` — Lean Canvas business model for startups and new products
- `business-model` — Business Model Canvas with all 9 building blocks
- `monetization-strategy` — Brainstorm 3–5 monetization strategies with validation experiments
- `pricing-strategy` — Pricing models, competitive analysis, willingness-to-pay, and price elasticity
- `swot-analysis` — SWOT analysis with actionable recommendations
- `pestle-analysis` — Macro environment: Political, Economic, Social, Technological, Legal, Environmental
- `porters-five-forces` — Competitive forces analysis (rivalry, suppliers, buyers, substitutes, new entrants)
- `ansoff-matrix` — Growth strategy mapping across markets and products

**Workflows (5):**

- `/strategy` — Create a complete 9-section Product Strategy Canvas
- `/business-model` — Explore business models (`lean|full|startup|value-prop|all`)
- `/value-proposition` — Design a value proposition using the 6-part JTBD template
- `/market-scan` — Macro environment analysis combining SWOT + PESTLE + Porter's + Ansoff
- `/pricing` — Design a pricing strategy with competitive analysis and experiments

**Examples:**

- `/strategy B2B project management tool for agencies`
- `/business-model startup — AI writing tool for non-native English speakers`
- `Run a Porter's Five Forces analysis for the project management SaaS market`

### 3. pm-execution

Day-to-day product management: PRDs, OKRs, roadmaps, sprints, retrospectives, release notes, pre-mortems, stakeholder management, user stories, and prioritization frameworks.

**Skills (15):**

- `create-prd` — Comprehensive 8-section PRD template
- `brainstorm-okrs` — Team-level OKRs aligned with company objectives
- `outcome-roadmap` — Transform a feature list into an outcome-focused roadmap
- `sprint-plan` — Sprint planning with capacity estimation, story selection, and risk identification
- `retro` — Structured sprint retrospective facilitation
- `release-notes` — User-facing release notes from tickets, PRDs, or changelogs
- `pre-mortem` — Risk analysis with Tigers/Paper Tigers/Elephants classification
- `stakeholder-map` — Power × Interest grid with tailored communication plan
- `summarize-meeting` — Meeting transcript → decisions + action items
- `user-stories` — User stories following the 3 C's and INVEST criteria
- `job-stories` — Job stories: When [situation], I want to [motivation], so I can [outcome]
- `wwas` — Product backlog items in Why-What-Acceptance format
- `test-scenarios` — Test scenarios: happy paths, edge cases, error handling
- `dummy-dataset` — Realistic dummy datasets as CSV, JSON, SQL, or Python
- `prioritization-frameworks` — Reference guide to 9 prioritization frameworks (Opportunity Score, ICE, RICE, MoSCoW, Kano, etc.)

**Workflows (10):**

- `/write-prd` — Create a PRD from a feature idea or problem statement
- `/plan-okrs` — Brainstorm team-level OKRs
- `/transform-roadmap` — Convert a feature-based roadmap into outcome-focused
- `/sprint` — Sprint lifecycle (`plan|retro|release`)
- `/pre-mortem` — Pre-mortem risk analysis on a PRD or launch plan
- `/meeting-notes` — Summarize a meeting transcript into structured notes
- `/stakeholder-map` — Map stakeholders and create a communication plan
- `/write-stories` — Break features into backlog items (`user|job|wwa`)
- `/test-scenarios` — Generate test scenarios from user stories
- `/generate-data` — Create realistic dummy datasets

**Examples:**

- `/write-prd Smart notification system that reduces alert fatigue`
- `/sprint retro — Here are the notes from our last sprint`
- `Which prioritization framework should I use for a 50-item backlog?`

### 4. pm-market-research

User research and competitive analysis: personas, segmentation, journey maps, market sizing, competitor analysis, and feedback analysis.

**Skills (7):**

- `user-personas` — Create refined user personas from research data
- `market-segments` — Identify 3–5 customer segments with demographics, JTBD, and product fit
- `user-segmentation` — Segment users from feedback data based on behavior, JTBD, and needs
- `customer-journey-map` — End-to-end journey map with stages, touchpoints, emotions, and pain points
- `market-sizing` — TAM, SAM, SOM with top-down and bottom-up approaches
- `competitor-analysis` — Competitor strengths, weaknesses, and differentiation opportunities
- `sentiment-analysis` — Sentiment analysis and theme extraction from user feedback

**Workflows (3):**

- `/research-users` — Build personas, segment users, and map the customer journey
- `/competitive-analysis` — Analyze the competitive landscape
- `/analyze-feedback` — Sentiment analysis and segment insights from user feedback

**Examples:**

- `/research-users We have interview data from 12 users of our fitness app`
- `/competitive-analysis Figma competitors in the design tool space`
- `Estimate TAM/SAM/SOM for an AI code review tool in the US market`

### 5. pm-data-analytics

Data analytics for PMs: SQL query generation, cohort analysis, and A/B test analysis.

**Skills (3):**

- `sql-queries` — Generate SQL from natural language (BigQuery, PostgreSQL, MySQL)
- `cohort-analysis` — Retention curves, feature adoption, and engagement trends by cohort
- `ab-test-analysis` — Statistical significance, sample size validation, and ship/extend/stop recommendations

**Workflows (3):**

- `/write-query` — Generate SQL queries from natural language
- `/analyze-cohorts` — Cohort analysis on user engagement data
- `/analyze-test` — Analyze A/B test results

**Examples:**

- `/write-query Show me monthly active users by country for Q4 2025 (BigQuery)`
- `/analyze-test Here are the results from our checkout flow A/B test [attach CSV]`
- `How large a sample do I need for 95% confidence with a 2% MDE?`

### 6. pm-go-to-market

Go-to-market strategy: beachhead segments, ideal customer profiles, messaging, growth loops, GTM motions, and competitive battlecards.

**Skills (6):**

- `gtm-strategy` — Full GTM strategy: channels, messaging, success metrics, and launch plan
- `beachhead-segment` — Identify the first beachhead market segment
- `ideal-customer-profile` — ICP with demographics, behaviors, JTBD, and needs
- `growth-loops` — Design sustainable growth loops (flywheels)
- `gtm-motions` — Evaluate GTM motions and tools (product-led, sales-led, etc.)
- `competitive-battlecard` — Sales-ready battlecard with objection handling and win strategies

**Workflows (3):**

- `/plan-launch` — Full GTM strategy from beachhead to launch plan
- `/growth-strategy` — Design growth loops and evaluate GTM motions
- `/battlecard` — Create a competitive battlecard

**Examples:**

- `/plan-launch AI code review tool targeting mid-size engineering teams`
- `/battlecard Our CRM vs Salesforce for the SMB market`
- `Design a growth loop for a B2B SaaS with a freemium tier`

### 7. pm-marketing-growth

Product marketing and growth: marketing ideas, positioning, value proposition statements, product naming, and North Star metrics.

**Skills (5):**

- `marketing-ideas` — Creative, cost-effective marketing ideas with channels and messaging
- `positioning-ideas` — Product positioning differentiated from competitors
- `value-prop-statements` — Value proposition statements for marketing, sales, and onboarding
- `product-name` — Product name brainstorming aligned to brand values and audience
- `north-star-metric` — North Star Metric + input metrics with business game classification

**Workflows (2):**

- `/market-product` — Brainstorm marketing ideas, positioning, value props, and product names
- `/north-star` — Define your North Star Metric and supporting input metrics

**Examples:**

- `/market-product B2B analytics dashboard for e-commerce managers`
- `/north-star Two-sided marketplace connecting freelancers with clients`
- `Brainstorm 5 positioning angles that differentiate us from Notion`

### 8. pm-toolkit

PM utilities beyond core product work: resume review, legal documents, and proofreading.

**Skills (4):**

- `review-resume` — PM resume review and tailoring against 10 best practices (XYZ+S formula, keywords, structure)
- `draft-nda` — Non-Disclosure Agreement with jurisdiction-appropriate clauses
- `privacy-policy` — Privacy policy covering GDPR/CCPA compliance
- `grammar-check` — Grammar, logic, and flow checking with targeted fixes

**Workflows (5):**

- `/review-resume` — Comprehensive PM resume review
- `/tailor-resume` — Tailor a resume to a specific job description
- `/draft-nda` — Draft an NDA
- `/privacy-policy` — Draft a privacy policy
- `/proofread` — Check grammar, logic, and flow

**Examples:**

- `/review-resume [attach your PM resume]`
- `/tailor-resume [attach resume + paste job description]`
- `/proofread Here's the draft of our Q1 investor update`

---

## About

This project is a Windsurf adaptation of the [PM Skills Marketplace](https://github.com/phuryn/pm-skills) originally built for Claude Code/Cowork.

Selected skills based on the work of:

- Teresa Torres — [*Continuous Discovery Habits*](https://www.amazon.com/Continuous-Discovery-Habits-Discover-Products/dp/1736633309/)
- Marty Cagan — [*INSPIRED*](https://www.amazon.com/INSPIRED-Create-Tech-Products-Customers/dp/1119387507/) and [*TRANSFORMED*](https://www.amazon.com/dp/1119697336/)
- Alberto Savoia — [*The Right It*](https://www.amazon.com/Right-Many-Ideas-Yours-Succeed/dp/0062884654)
- Dan Olsen — [*The Lean Product Playbook*](https://www.amazon.com/dp/1118960874/)
- Roger L. Martin — [*Playing to Win*](https://www.amazon.com/Playing-Win-Expanded-Bonus-Articles/dp/B0F25SDYWV/)
- Ash Maurya — [*Running Lean*](https://www.amazon.com/dp/B004J4XGN6/)
- Strategyzer — [*Business Model Generation*](https://www.amazon.com/dp/0470876417/) and [*Value Proposition Design*](https://www.amazon.com/dp/1118968050/)
- Christina Wodtke — [*Radical Focus*](https://www.amazon.com/Radical-Focus-Achieving-Important-Objectives/dp/0996006052)
- Anthony W. Ulwick — [*Jobs to Be Done*](https://jobs-to-be-done-book.com/)
- Alistair Croll & Benjamin Yoskovitz — [*Lean Analytics*](https://www.amazon.com/Lean-Analytics-Better-Startup-Faster/dp/1449335675/)
- Sean Ellis — [*Hacking Growth*](https://www.amazon.com/Hacking-Growth-Fastest-Growing-Companies-Breakout/dp/045149721X/)
- Maja Voje — [*Go-To-Market Strategist*](https://gtmstrategist.com/)

Curated by Paweł Huryn from [The Product Compass Newsletter](https://www.productcompass.pm).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — see [LICENSE](LICENSE).
