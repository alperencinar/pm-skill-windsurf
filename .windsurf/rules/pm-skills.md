# PM Skills for Windsurf

You have access to a comprehensive Product Management skills library with 65 domain-specific skills and 36 workflows. When the user asks PM-related questions or invokes a `/slash-command`, follow the relevant workflow and reference the appropriate skill files.

## How It Works

- **Workflows** (`.windsurf/workflows/*.md`): Invoked via `/slash-command`. Each workflow chains one or more skills into a guided, step-by-step process.
- **Skills** (`skills/<plugin>/*.md`): Domain knowledge files containing PM frameworks, templates, and instructions. Workflows reference these — read the skill file when instructed to apply a skill.

## Available Skill Domains

| Domain | Path | Skills |
|--------|------|--------|
| Product Discovery | `skills/pm-product-discovery/` | 13 skills — ideation, experiments, assumptions, interviews, feature prioritization |
| Product Strategy | `skills/pm-product-strategy/` | 12 skills — vision, strategy canvas, business models, pricing, SWOT, PESTLE, Porter's |
| Execution | `skills/pm-execution/` | 15 skills — PRDs, OKRs, roadmaps, sprints, retros, user stories, prioritization |
| Market Research | `skills/pm-market-research/` | 7 skills — personas, segmentation, journey maps, competitor analysis, sentiment |
| Data Analytics | `skills/pm-data-analytics/` | 3 skills — SQL generation, cohort analysis, A/B test analysis |
| Go-to-Market | `skills/pm-go-to-market/` | 6 skills — GTM strategy, growth loops, ICPs, battlecards |
| Marketing & Growth | `skills/pm-marketing-growth/` | 5 skills — marketing ideas, positioning, naming, North Star metrics |
| PM Toolkit | `skills/pm-toolkit/` | 4 skills — resume review, NDA drafting, privacy policy, proofreading |

## Key Workflows

- `/discover` — Full discovery cycle: ideation → assumptions → experiments
- `/strategy` — 9-section Product Strategy Canvas
- `/write-prd` — Comprehensive PRD from an idea or problem
- `/plan-launch` — Full GTM strategy
- `/north-star` — North Star Metric + input metrics
- `/brainstorm` — Multi-perspective ideation (PM, Designer, Engineer)
- `/sprint` — Sprint planning, retros, or release notes
- `/competitive-analysis` — Competitive landscape analysis

## When to Use Skills

When the user asks a PM-related question (even without a slash command), check if a relevant skill file exists and use its framework to provide structured, rigorous answers. Skills encode proven PM frameworks from Teresa Torres, Marty Cagan, Alberto Savoia, and others.
