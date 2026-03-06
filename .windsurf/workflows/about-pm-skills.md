---
description: Learn what PM Skills for Windsurf is, how it works, and how to use all 36 workflows and 65 skills
---

# /about-pm-skills -- What Is This Skill & How to Use It

Explain the PM Skills for Windsurf system — what it is, what's included, and how to use it effectively.

## What Is PM Skills for Windsurf?

PM Skills for Windsurf is an **AI-powered product management operating system** that gives Cascade (Windsurf's AI assistant) structured PM domain knowledge. It contains **65 skills** and **36 workflows** across 8 PM domains, encoding proven frameworks from leading PM thinkers.

**Source**: Adapted from [github.com/phuryn/pm-skills](https://github.com/phuryn/pm-skills) (originally built for Claude Code/Cowork) by Paweł Huryn of [The Product Compass](https://www.productcompass.pm).

## How It Works

### Skills
Skills are markdown files in `skills/<domain>/` that contain PM frameworks, templates, and step-by-step instructions. They give Cascade deep domain knowledge on specific PM topics. You don't invoke skills directly — workflows reference them automatically.

**65 skills** across 8 domains:
- **Product Discovery** (13): ideation, experiments, assumption testing, interviews, feature prioritization
- **Product Strategy** (12): vision, strategy canvas, business models, pricing, SWOT, PESTLE, Porter's
- **Execution** (15): PRDs, OKRs, roadmaps, sprints, retros, user stories, prioritization frameworks
- **Market Research** (7): personas, segmentation, journey maps, competitor analysis, sentiment
- **Data Analytics** (3): SQL generation, cohort analysis, A/B test analysis
- **Go-to-Market** (6): GTM strategy, growth loops, ICPs, battlecards
- **Marketing & Growth** (5): marketing ideas, positioning, naming, North Star metrics
- **PM Toolkit** (4): resume review, NDA drafting, privacy policy, proofreading

### Workflows
Workflows are invoked via `/slash-command` in Cascade. Each workflow chains one or more skills into a guided, end-to-end process. They live in `.windsurf/workflows/`.

## Quick Start — Top Workflows

| Need | Command | What It Does |
|------|---------|-------------|
| New idea? | `/discover` | Full discovery cycle: ideation → assumptions → experiments |
| Strategic clarity? | `/strategy` | 9-section Product Strategy Canvas |
| Writing a spec? | `/write-prd` | Comprehensive PRD from an idea or problem |
| Planning a launch? | `/plan-launch` | Full GTM strategy: beachhead → ICP → channels → timeline |
| Defining metrics? | `/north-star` | North Star Metric + input metrics |
| Brainstorming? | `/brainstorm` | Multi-perspective ideation (PM, Designer, Engineer) |
| Sprint work? | `/sprint` | Sprint planning, retros, or release notes |
| Competitor intel? | `/competitive-analysis` | Competitive landscape analysis |
| Feature requests? | `/triage-requests` | Categorize and prioritize a batch of requests |
| Business model? | `/business-model` | Lean Canvas, BMC, Startup Canvas, or Value Prop |
| New project? | `/start-project` | Full knowledge base: strategy, PRD, personas, GTM, tech specs, and more |


### Project Kickoff
- `/start-project` — Analyze a project idea and generate a full knowledge base (15 docs) in `NewProjectDetails/`

### Product Discovery
- `/discover` — Full discovery cycle
- `/brainstorm` — Multi-perspective ideation (`ideas|experiments` × `existing|new`)
- `/triage-requests` — Analyze and prioritize feature requests
- `/interview` — Prepare interview script or summarize transcript (`prep|summarize`)
- `/setup-metrics` — Design a product metrics dashboard

### Product Strategy
- `/strategy` — 9-section Product Strategy Canvas
- `/business-model` — Business model exploration (`lean|full|startup|value-prop|all`)
- `/value-proposition` — 6-part JTBD value proposition
- `/market-scan` — SWOT + PESTLE + Porter's + Ansoff in one scan
- `/pricing` — Pricing strategy with competitive analysis

### Execution
- `/write-prd` — Product Requirements Document
- `/plan-okrs` — Team-level OKRs
- `/transform-roadmap` — Convert feature roadmap to outcome-focused
- `/sprint` — Sprint lifecycle (`plan|retro|release-notes`)
- `/pre-mortem` — Risk analysis (Tigers/Paper Tigers/Elephants)
- `/meeting-notes` — Meeting transcript → structured notes
- `/stakeholder-map` — Power × Interest grid + communication plan
- `/write-stories` — Backlog items (`user|job|wwa` format)
- `/test-scenarios` — Test scenarios from user stories
- `/generate-data` — Realistic dummy datasets

### Market Research
- `/research-users` — Personas, segmentation, journey maps
- `/competitive-analysis` — Competitive landscape analysis
- `/analyze-feedback` — Sentiment analysis from user feedback

### Data Analytics
- `/write-query` — SQL from natural language
- `/analyze-cohorts` — Cohort retention analysis
- `/analyze-test` — A/B test analysis with ship/extend/stop recommendation

### Go-to-Market
- `/plan-launch` — Full GTM strategy
- `/growth-strategy` — Growth loops and GTM motions
- `/battlecard` — Competitive battlecard for sales

### Marketing & Growth
- `/market-product` — Marketing ideas, positioning, naming, value props
- `/north-star` — North Star Metric definition

### PM Toolkit
- `/review-resume` — PM resume review
- `/tailor-resume` — Tailor resume to a job description
- `/draft-nda` — Non-Disclosure Agreement
- `/privacy-policy` — Privacy policy (GDPR/CCPA)
- `/proofread` — Grammar, logic, and flow check

## All 37 Workflows

*(Note: The workflow count increased from 36 to 37 with the addition of `/start-project`.)*

## Tips for Best Results

1. **Be specific**: `/discover AI-powered meeting summarizer for remote teams` works better than `/discover`
2. **Attach context**: Upload PRDs, research docs, CSVs, or strategy decks — workflows will use them
3. **Follow the chain**: Each workflow suggests next steps — follow the prompts to chain workflows together
4. **Use skills directly**: Even without a slash command, ask PM questions naturally — Cascade will draw on the skill files

## Project Structure

```
.windsurf/
  workflows/       ← 36 slash-command workflow files
  rules/           ← Global context for Cascade
skills/
  pm-product-discovery/   ← 13 skills
  pm-product-strategy/    ← 12 skills
  pm-execution/           ← 15 skills
  pm-market-research/     ← 7 skills
  pm-data-analytics/      ← 3 skills
  pm-go-to-market/        ← 6 skills
  pm-marketing-growth/    ← 5 skills
  pm-toolkit/             ← 4 skills
```

## Credits

Based on PM frameworks from Teresa Torres, Marty Cagan, Alberto Savoia, Dan Olsen, Ash Maurya, and others. Originally curated by [Paweł Huryn](https://www.productcompass.pm) as [pm-skills](https://github.com/phuryn/pm-skills).
