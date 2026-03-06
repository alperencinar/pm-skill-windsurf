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

After gathering context from the user, this workflow generates **up to 21 knowledge-base documents** in the `NewProjectDetails/` folder:

| # | File | Purpose |
|---|------|--------|
| 1 | `01-project-brief.md` | Refined project overview, goals, scope, and constraints |
| 2 | `02-product-strategy.md` | 9-section Strategy Canvas: vision → defensibility |
| 3 | `03-value-proposition.md` | JTBD value propositions per segment |
| 4 | `04-user-personas.md` | 3-4 target personas with JTBD, pains, and gains |
| 5 | `05-competitive-analysis.md` | Competitor landscape, strengths, weaknesses, differentiation |
| 6 | `06-business-model.md` | Lean Canvas or Startup Canvas with revenue model |
| 7 | `07-prd.md` | Product Requirements Document with user stories and acceptance criteria |
| 8 | `08-technical-requirements.md` | Tech stack, architecture, env config, dependencies, deployment checklist |
| 9 | `09-ui-ux-guidelines.md` | Design principles, screens, flows, component inventory, design tokens |
| 10 | `10-metrics-dashboard.md` | North Star, input metrics, health metrics, alert thresholds |
| 11 | `11-gtm-strategy.md` | Go-to-market: beachhead segment, ICP, channels, launch plan |
| 12 | `12-growth-strategy.md` | Growth loops, GTM motions, 90-day growth plan |
| 13 | `13-pricing-strategy.md` | Pricing model, tiers, competitive benchmark |
| 14 | `14-roadmap.md` | Outcome-focused roadmap: Now / Next / Later |
| 15 | `15-risks-and-assumptions.md` | Pre-mortem risks, critical assumptions, validation experiments |
| 16 | `16-db-schema.md` | Database tables, fields, types, relations, indexes, seed data |
| 17 | `17-api-specification.md` | Full endpoint spec: routes, methods, payloads, auth, errors |
| 18 | `18-project-structure.md` | Folder layout, module boundaries, env vars, dependency list |
| 19 | `19-test-plan.md` | QA strategy, test scenarios, testing tools, CI integration |
| 20 | `20-content-marketing-plan.md` | Content calendar, SEO keywords, social media, email sequences |
| 21 | `21-legal-compliance.md` | Privacy policy, ToS, GDPR/CCPA checklist, data handling |

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
| Layer | Technology | Version | Why |
|-------|-----------|---------|-----|
| Frontend | [framework] | [version] | [rationale] |
| Backend | [framework] | [version] | [rationale] |
| Database | [type] | [version] | [rationale] |
| Hosting | [platform] | — | [rationale] |
| Auth | [service] | — | [rationale] |
| Styling | [library] | [version] | [rationale] |
| State Mgmt | [library] | [version] | [rationale] |

## Architecture Overview
[High-level architecture description — monolith vs microservices, API design approach]
[Include architecture diagram in text/ASCII if helpful]

## Data Model Summary
[Key entities and their relationships — detailed schema is in 16-db-schema.md]

## API Summary
[Core API patterns and conventions — full spec is in 17-api-specification.md]

## Third-Party Integrations
| Service | Purpose | SDK/API | Cost Model |
|---------|---------|---------|------------|

## Security Requirements
- Authentication method and flow
- Authorization / role-based access
- Data encryption (at rest, in transit)
- OWASP top 10 considerations

## Performance Requirements
| Metric | Target | Measurement |
|--------|--------|-------------|
| Page load time | [target] | [tool] |
| API response time | [target] | [tool] |
| Concurrent users | [target] | [approach] |

## Environment Configuration
| Variable | Purpose | Example Value | Required |
|----------|---------|---------------|----------|
[List all env vars the project will need]

## Dependencies
[Package.json / requirements.txt — list key dependencies with versions]

## DevOps & Deployment
- CI/CD pipeline setup
- Environments: dev, staging, production
- Monitoring and alerting tools
- Backup and disaster recovery

## Deployment Checklist
- [ ] Environment variables configured
- [ ] Database migrated
- [ ] SSL certificates provisioned
- [ ] CDN configured
- [ ] Monitoring dashboards set up
- [ ] Error tracking enabled
- [ ] Backup schedule verified
```

---

#### 2.9: UI/UX Guidelines (`09-ui-ux-guidelines.md`)

Based on the personas and PRD, generate:

```
# UI/UX Guidelines: [Product Name]

## Design Principles
[3-5 guiding principles for the product's UX]

## Key Screens
| Screen | Purpose | Key Elements | Priority |
|--------|---------|-------------|----------|
[List all primary screens/pages]

## User Flows
[Step-by-step flows for core use cases — onboarding, primary action, settings]
[Include flow diagrams in text/ASCII format]

## Navigation Structure
[Information architecture — how screens connect, sitemap]

## Component Inventory
| Component | Variants | Used On | Notes |
|-----------|----------|---------|-------|
| Button | primary, secondary, ghost, danger | all screens | [specs] |
| Input | text, email, password, search | forms | [specs] |
| Card | content, pricing, feature | dashboard, landing | [specs] |
| Modal | confirmation, form, info | settings, actions | [specs] |
| Navigation | top bar, sidebar, mobile drawer | all screens | [specs] |
| Toast/Alert | success, error, warning, info | all screens | [specs] |
[Add all components needed for the product]

## Design Tokens
| Token | Value | Usage |
|-------|-------|-------|
| `--color-primary` | [hex] | Buttons, links, accents |
| `--color-secondary` | [hex] | Secondary actions |
| `--color-background` | [hex] | Page backgrounds |
| `--color-surface` | [hex] | Cards, modals |
| `--color-text` | [hex] | Body text |
| `--color-error` | [hex] | Error states |
| `--color-success` | [hex] | Success states |
| `--font-heading` | [font family] | H1-H6 |
| `--font-body` | [font family] | Body text, labels |
| `--spacing-xs` | [value] | Tight spacing |
| `--spacing-sm` | [value] | Component padding |
| `--spacing-md` | [value] | Section spacing |
| `--spacing-lg` | [value] | Page sections |
| `--radius-sm` | [value] | Buttons, inputs |
| `--radius-md` | [value] | Cards |
| `--radius-lg` | [value] | Modals |

## Responsive Strategy
| Breakpoint | Width | Layout Changes |
|-----------|-------|----------------|
| Mobile | <640px | [changes] |
| Tablet | 640-1024px | [changes] |
| Desktop | >1024px | [changes] |

## Accessibility
- WCAG 2.1 AA compliance target
- Minimum contrast ratios
- Keyboard navigation requirements
- Screen reader considerations
- Focus management approach

## Brand & Visual Direction
[Color palette, typography scale, iconography style, illustration style, tone of voice]
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

#### 2.16: Database Schema (`16-db-schema.md`)

Based on the PRD and technical requirements, generate a detailed database schema:

```
# Database Schema: [Product Name]

## Overview
[Database type (PostgreSQL, MySQL, MongoDB, etc.) and design philosophy (normalized, denormalized, event-sourced)]

## Entity-Relationship Diagram
[ASCII/text representation of entity relationships]

## Tables / Collections

### users
| Column | Type | Constraints | Description |
|--------|------|------------|-------------|
| id | UUID | PK | Unique identifier |
| email | VARCHAR(255) | UNIQUE, NOT NULL | User email |
| ... | ... | ... | ... |

[Repeat for every table/collection]

## Relationships
| From | To | Type | FK | Cascade |
|------|-----|------|-----|--------|

## Indexes
| Table | Index | Columns | Type | Purpose |
|-------|-------|---------|------|---------|

## Seed Data
[Sample data for development and testing — at least 3-5 rows per table]

## Migration Strategy
[How to handle schema changes over time]
```

---

#### 2.17: API Specification (`17-api-specification.md`)

Based on the PRD and database schema, generate a full API spec:

```
# API Specification: [Product Name]

## Overview
- Base URL: [e.g., /api/v1]
- Authentication: [method — JWT, API key, OAuth2]
- Response format: JSON
- Pagination: [approach]
- Rate limiting: [if applicable]

## Authentication Endpoints

### POST /auth/register
**Description**: Create a new user account
**Request Body**:
| Field | Type | Required | Validation |
|-------|------|----------|------------|

**Response** (201):
[JSON example]

**Errors**:
| Code | Message | When |
|------|---------|------|

[Repeat for every endpoint]

## Resource Endpoints
[Group by resource: /users, /projects, /settings, etc.]
[For each: method, path, description, request, response, errors]

## Webhook Events (if applicable)
| Event | Payload | Trigger |
|-------|---------|--------|

## Error Handling Convention
| HTTP Code | Meaning | Response Shape |
|-----------|---------|---------------|
| 400 | Bad Request | { error, details } |
| 401 | Unauthorized | { error } |
| 403 | Forbidden | { error } |
| 404 | Not Found | { error } |
| 422 | Validation Error | { error, fields } |
| 500 | Server Error | { error } |
```

---

#### 2.18: Project Structure (`18-project-structure.md`)

Based on the tech stack and architecture decisions, generate:

```
# Project Structure: [Product Name]

## Folder Layout
[Full directory tree for the project — use the conventions of the chosen framework]

Example for a Next.js + Node project:
project-root/
├── src/
│   ├── app/              # Pages and layouts
│   ├── components/       # Reusable UI components
│   │   ├── ui/           # Base components (Button, Input, Card)
│   │   └── features/     # Feature-specific components
│   ├── lib/              # Utility functions, helpers
│   ├── hooks/            # Custom React hooks
│   ├── services/         # API client functions
│   ├── types/            # TypeScript type definitions
│   └── styles/           # Global styles, design tokens
├── api/                  # Backend API routes or server
│   ├── routes/
│   ├── middleware/
│   ├── models/
│   └── services/
├── prisma/               # Database schema and migrations
├── public/               # Static assets
├── tests/                # Test files
├── .env.example          # Environment variable template
├── package.json
├── tsconfig.json
└── README.md

## Module Boundaries
[What each top-level folder is responsible for — keep responsibilities clear]

## Naming Conventions
| Type | Convention | Example |
|------|-----------|--------|
| Components | PascalCase | UserProfile.tsx |
| Utilities | camelCase | formatDate.ts |
| API routes | kebab-case | /api/user-settings |
| Database tables | snake_case | user_settings |
| Environment vars | SCREAMING_SNAKE | DATABASE_URL |

## Environment Variables
| Variable | Purpose | Required | Default |
|----------|---------|----------|--------|
[Full list from 08-technical-requirements.md]

## Key Dependencies
| Package | Version | Purpose |
|---------|---------|--------|
[List all key packages with versions]

## Setup Instructions
1. Clone the repository
2. Install dependencies: [command]
3. Copy `.env.example` to `.env` and fill in values
4. Set up the database: [command]
5. Run migrations: [command]
6. Start the dev server: [command]
```

---

#### 2.19: Test Plan (`19-test-plan.md`)

Apply the **test-scenarios** skill (read `skills/pm-execution/test-scenarios.md`):

```
# Test Plan: [Product Name]

## QA Strategy
- **Unit tests**: [scope, tools — e.g., Jest, Vitest]
- **Integration tests**: [scope, tools — e.g., Supertest, Playwright]
- **E2E tests**: [scope, tools — e.g., Playwright, Cypress]
- **Manual testing**: [when and what]

## Test Coverage Targets
| Layer | Target | Priority |
|-------|--------|----------|
| API endpoints | 90% | High |
| Business logic | 85% | High |
| UI components | 70% | Medium |
| E2E flows | Core flows | High |

## Core Test Scenarios

### Feature: [Feature Name from PRD]

#### Happy Path
| # | Step | Action | Expected Result | Priority |
|---|------|--------|----------------|----------|

#### Edge Cases
| # | Scenario | Input | Expected Behavior |
|---|---------|-------|------------------|

#### Error Handling
| # | Scenario | Expected Error | User Feedback |
|---|---------|---------------|---------------|

[Repeat for each P0 and P1 feature from the PRD]

## Test Data Requirements
[What seed data is needed — reference 16-db-schema.md]

## CI Integration
- Tests run on: [every PR, every push to main, nightly]
- Required to pass before merge: [unit, integration]
- E2E runs: [on staging deploys]

## Performance Testing
| Scenario | Tool | Target | Threshold |
|---------|------|--------|----------|
```

---

#### 2.20: Content & Marketing Plan (`20-content-marketing-plan.md`)

Based on the GTM strategy and growth strategy, generate:

```
# Content & Marketing Plan: [Product Name]

## Marketing Goals
| Goal | Metric | Target | Timeline |
|------|--------|--------|----------|

## Target Audience Messaging
[Key messages per persona — reference 04-user-personas.md]

## SEO Strategy
| Keyword Cluster | Target Keywords | Search Volume | Content Type |
|----------------|----------------|---------------|-------------|
[5-10 keyword clusters relevant to the product]

## Content Calendar (First 90 Days)

### Pre-Launch (Weeks 1-4)
| Week | Content | Channel | Goal | Owner |
|------|---------|---------|------|-------|
| 1 | [content piece] | [channel] | [awareness/leads/SEO] | [who] |

### Launch Week
| Day | Content | Channel | Goal |
|-----|---------|---------|------|

### Post-Launch (Weeks 6-12)
| Week | Content | Channel | Goal | Owner |
|------|---------|---------|------|-------|

## Social Media Plan
| Platform | Frequency | Content Mix | Tone |
|---------|-----------|-------------|------|

## Email Sequences

### Welcome Sequence (new signups)
| # | Subject | Content Focus | Send After |
|---|---------|--------------|------------|
| 1 | [subject] | [focus] | Signup |
| 2 | [subject] | [focus] | Day 2 |
| 3 | [subject] | [focus] | Day 5 |

### Onboarding Sequence
[Emails triggered by user behavior]

## Launch Announcements
- Product Hunt: [plan]
- Hacker News: [plan]
- Industry communities: [list and approach]
- Press/media: [outreach plan]

## Paid Channels (if budget allows)
| Channel | Budget | Targeting | Expected CAC |
|---------|--------|----------|-------------|

## Success Metrics
| Metric | Tool | Target |
|--------|------|--------|
| Website traffic | [analytics] | [target] |
| Signups | [tool] | [target] |
| Email open rate | [tool] | [target] |
| Social engagement | [tool] | [target] |
```

---

#### 2.21: Legal & Compliance (`21-legal-compliance.md`)

Apply the **privacy-policy** skill (read `skills/pm-toolkit/privacy-policy.md`) and **draft-nda** skill (read `skills/pm-toolkit/draft-nda.md`) where relevant:

```
# Legal & Compliance: [Product Name]

## Regulatory Requirements
| Regulation | Applies? | Requirements | Status |
|-----------|----------|-------------|--------|
| GDPR | [Yes/No] | [key requirements] | [TODO/Done] |
| CCPA | [Yes/No] | [key requirements] | [TODO/Done] |
| COPPA | [Yes/No] | [key requirements] | [TODO/Done] |
| SOC 2 | [Yes/No] | [key requirements] | [TODO/Done] |
| HIPAA | [Yes/No] | [key requirements] | [TODO/Done] |
| [Industry-specific] | [Yes/No] | [key requirements] | [TODO/Done] |

## Privacy Policy Requirements
- Data collected: [types]
- Data usage: [purposes]
- Data retention: [policy]
- Third-party sharing: [who and why]
- User rights: [access, deletion, portability]
- Cookie policy: [approach]

## Terms of Service Outline
- Acceptable use policy
- Account terms
- Payment terms (if applicable)
- Intellectual property
- Limitation of liability
- Termination
- Dispute resolution

## Data Handling
| Data Type | Storage Location | Encryption | Retention | Access |
|----------|-----------------|-----------|-----------|--------|

## Cookie Consent
- Essential cookies: [list]
- Analytics cookies: [list]
- Marketing cookies: [list]
- Consent mechanism: [banner type]

## Compliance Checklist
- [ ] Privacy policy drafted and published
- [ ] Terms of service drafted and published
- [ ] Cookie consent banner implemented
- [ ] Data subject request process defined
- [ ] Data processing agreements with vendors
- [ ] Data breach notification procedure
- [ ] User data export functionality
- [ ] User data deletion functionality
- [ ] Age verification (if required)
- [ ] Accessibility compliance (WCAG 2.1 AA)

## Legal Review Needed
| Document | Priority | Notes |
|----------|---------|-------|
[Flag items that need real legal counsel review]
```

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
| 08 | [Technical Requirements](08-technical-requirements.md) | Tech stack, architecture, env config |
| 09 | [UI/UX Guidelines](09-ui-ux-guidelines.md) | Design system, components, tokens |
| 10 | [Metrics Dashboard](10-metrics-dashboard.md) | North Star and supporting metrics |
| 11 | [GTM Strategy](11-gtm-strategy.md) | Go-to-market plan |
| 12 | [Growth Strategy](12-growth-strategy.md) | Growth loops and 90-day plan |
| 13 | [Pricing Strategy](13-pricing-strategy.md) | Pricing model and tiers |
| 14 | [Roadmap](14-roadmap.md) | Now / Next / Later outcomes |
| 15 | [Risks & Assumptions](15-risks-and-assumptions.md) | Risk analysis and validation plan |
| 16 | [Database Schema](16-db-schema.md) | Tables, fields, relations, seed data |
| 17 | [API Specification](17-api-specification.md) | Endpoints, payloads, auth, errors |
| 18 | [Project Structure](18-project-structure.md) | Folder layout, setup instructions |
| 19 | [Test Plan](19-test-plan.md) | QA strategy and test scenarios |
| 20 | [Content Marketing Plan](20-content-marketing-plan.md) | Content calendar, SEO, social, email |
| 21 | [Legal & Compliance](21-legal-compliance.md) | Privacy, ToS, regulatory checklist |

## How to Use These Documents

These files are the **single source of truth** for this project.

When **coding and building**:
- `07-prd.md` — Feature requirements and acceptance criteria
- `08-technical-requirements.md` — Tech stack, env config, dependencies
- `16-db-schema.md` — Database tables, fields, and relations
- `17-api-specification.md` — API endpoints and contracts
- `18-project-structure.md` — Folder layout and setup instructions
- `09-ui-ux-guidelines.md` — Components, design tokens, user flows

When **testing**:
- `19-test-plan.md` — Test scenarios and QA strategy
- `16-db-schema.md` — Seed data for test environments

When **making product decisions**:
- `02-product-strategy.md` — Strategic alignment
- `04-user-personas.md` — User needs and JTBD
- `10-metrics-dashboard.md` — What to measure
- `15-risks-and-assumptions.md` — Known risks
- `14-roadmap.md` — Prioritization and phasing

When **preparing for launch and marketing**:
- `11-gtm-strategy.md` — Go-to-market plan
- `12-growth-strategy.md` — Growth mechanisms
- `13-pricing-strategy.md` — Pricing decisions
- `20-content-marketing-plan.md` — Content calendar and channels
- `21-legal-compliance.md` — Privacy, ToS, and regulatory compliance
```

### Step 4: Confirm and Offer Next Steps

Present a summary of all generated files with a brief highlight from each. Then offer:

- "Want me to **start building the product** using these documents as the spec?"
- "Should I **deep-dive into any document** — add more detail or refine a section?"
- "Want me to **create user stories and sprint plan** from the PRD?"
- "Want me to **scaffold the project** — create folders, boilerplate code, and config files based on `18-project-structure.md`?"
- "Should I **set up the database** using `16-db-schema.md`?"
- "Want me to **build the API** from `17-api-specification.md`?"

## Notes

- This is a comprehensive workflow — expect 10-20 minutes for full generation. Let the user know upfront.
- Each document should be **specific to the project**, not generic templates with placeholders. Use real product details.
- The `NewProjectDetails/` folder becomes the project's knowledge base — Windsurf references these files in future conversations.
- If the user provides very little context, make reasonable assumptions, state them clearly, and proceed. The user can refine later.
- For technical requirements, tailor recommendations to the project type (web app, mobile, API, marketplace, etc.).
- If the user already has some documents, skip those sections and focus on gaps.
- Documents should reference each other where relevant (e.g., PRD references personas, GTM references value proposition).
