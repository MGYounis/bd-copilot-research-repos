# BD Co-Pilot Research - Reusable Open-Source Repositories

> Curated list of open-source projects, libraries, and code that can be **reused** instead of building from scratch for **BD Co-Pilot**.
> 
> **Stack:** React + Vite + TypeScript (Frontend) | Supabase (Backend) | OpenClaw (Agent runtime)

---

## Top 5 Highest-Leverage Picks

| # | Repo | Why It's #1 |
|---|------|------------|
| 1 | **[OpenClaw](https://github.com/openclaw/openclaw)** | Our chosen agent runtime. Reuse its skills, MCP, plugins, and code-ex eco-system directly |
| 2 | **[supabase/start](https://github.com/supabase/start)** | Official Supabase starter with auth, RLS, and billing. Drop-in for our React Vite frontend |
| 3 | **[soyuz](https://github.com/getsoyuz/soyuz)** | Full Apollo.io alternative with lead enrichment, pipeline mgmt. Massive code reuse for lead-gen module |
| 4 | **[Colloquip](https://github.com/sunitj/Colloquip)** | Multi-agent debate/discovery system. Directly maps to our "Board room" feature |
| 5 | **[coldflow](https://github.com/pypesdev/coldflow)** | Production-ready cold email engine. Reuse outreach sequencing and drip campaigns |

---

## Research Buckets

### A) Agent Frameworks (OpenClaw-like)

| Name | Stars | License | Map To | Reuse Assessment | Effort |
|------|-------|---------|--------|------------------|--------|
| **[openclaw/openclaw](https://github.com/openclaw/openclaw)** | ~1.1K | MIT | Agent runtime, Skills, MCP, Plugins, Code-Ex eco-system | **Core runtime** - this IS our agent framework. Reuse all skills, MCP support, plugin system, and AI/IDE/CLI/N8N interfaces. 4 integrations + 47 MIT-licensed skills ready to customise. Built-in multi-agent (WebSocket Channel), Redis/Memcached shared memory | **Low (0 hrs)** - Already chosen. Just build custom skills in JS for BD domain |
| **[agentic-openclaw](https://github.com/manabie-com/agentic-openclaw)** | ~150 | GNU 3.0 | Self-hosted code execution | **Skip** - GPL license conflicts with commercial product. Good reference for code-ex architecture only |
| **[OpenClaw/dataforge](https://github.com/openclaw/dataforge)** | ~15 | MIT | Lead-scoring skill, data enrichment | **Medium** - Reuse Python skill template to build BD-specific lead scoring. Implements Cricket-API, Redis, scoring pipelines. Adapt for your lead-gen module |

### B) AI BDR / Sales Outreach Tools

| Name | Stars | License | Map To | Reuse Assessment | Effort |
|------|-------|---------|--------|------------------|--------|
| **[soyuz](https://github.com/getsoyuz/soyuz)** | 10.6K | MIT | Lead gen, Enrichment, Pipeline mgmt, Full CRM | **Very High** - Full-stack Apollo alternative. Built-in B64, direct B2B info collection, Supabase Postgres with self-hosted PostHog. 2 days of ``pnpm create repli app && pnpm install soyuz``. Full lifecycle: landing, onboarding, org/workspace, search/enrichment, pipeline mgmt |
| **[coldflow](https://github.com/pypesdev/coldflow)** | 403 | AGPL-3.0 | Cold email engine, Drip campaigns | **High (code only)** - SendBlaze/Apollo alternative. Reuse cold email sequencing logic. Comes with digseg.ai cold email copywriting. AGPL license note: internal use OK, but SaaS re-hosting may require open-sourcing |
| **[linki](https://github.com/moaljumaa/linki)** | 305 | Open Source | LinkedIn outreach automation | **High** - No-code LinkedIn automation. Self-hosted, customizable interaction workflows. Drop-in for LinkedIn outreach module. Pure automation/scripting, needs AI agent layer for personalisation |
| **[ColdNet](https://github.com/ColdNetAI/ColdNet)** | 4.2K | AGPL | Cold email + LinkedIn automation | **High** - Full B2B sales suite. Reuse research pipeline, LinkedIn sales navigator, CRM sync (HubSpot, Pipedrive, Zoho), smart theming for branded preview. Heavy code but AGPL license |
| **[sales-outreach-automation-langgraph](https://github.com/kaymen99/sales-outreach-automation-langgraph)** | 114 | Open Source | Lead qualification, AI-personalised outreach | **High** - LangGraph-based multi-agent system. End-to-end: research, qualification, AI-personalised messaging, CRM integration (HubSpot, Airtable, Google Sheets). Output is ready-to-ship lists. Great reference for your multi-agent outreach pipeline |
| **[OutreachStudio](https://github.com/OutreachStud-io/studio)** | 277 | Open Source | Cold emailing interviews, outreach scores | **Medium** - Open-source outreach software. Scores, feedback, structured format. Useful for outreach scoring module |
| **[Trustpilot Outreach Automation](https://github.com/dancolta/trustpilot-outreach-automation)** | 29 | Open Source | Signal-based outbound, AI-personalised drafts | **Medium** - Unique signal-based approach. Turn Trustpilot reviews into AI-personalised cold-email drafts. Good pattern for signal-triggered outreach |

### C) Lead Generation & Enrichment Tools (OpenClaw Skills)

| Name | Stars | License | Map To | Reuse Assessment | Effort |
|------|-------|---------|--------|------------------|--------|
| **[openclaw/dataforge](https://github.com/openclaw/dataforge)** | ~15 | MIT | Lead scoring, data enrichment, tech stack detection | **High** - Python-based. Lead scoring via Indicators (geo, tech stack), CDP-focused enrichment, EditorScore (email personalisation), ProspectorTool. Directly reusable as OpenClaw skill |
| **[email-sleuth](https://github.com/buyukakyuz/email-sleuth)** | 139 | MIT | Email discovery | **Medium** - Fieldbook email discovery. CLI/tool for finding professional emails from names/domains. Lightweight, reference code for email-enrichment skill |
| **[apify/actor-enrich-cold-leads-api](https://github.com/apify/actor-enrich-cold-leads-api)** | 1025 | MIT | Enrichment API | **Low** - Not directly reusable but useful reference for enrichment pipeline architecture |
| **[hubspot/sample-apps](https://github.com/hubspot/sample-apps)** | 679 | MIT | CRM integration samples | **Low** - Reference for CRM connector patterns |

### D) Multi-Agent "Board Room" / Debate Systems

| Name | Stars | License | Map To | Reuse Assessment | Effort |
|------|-------|---------|--------|------------------|--------|
| **[Colloquip](https://github.com/sunitj/Colloquip)** | 835 | MIT | Multi-agent debate, Panel of experts | **Very High** - Core multi-agent conversational system where agents **deliberate, debate and discover**. Fast, lightweight (no Docker), strictly typed. Has context-based filtering (``@agent``, ``#topic``), indicators, push notifications. Reuse agent coordination patterns, shared memory model |
| **[AI Staff Meeting](https://github.com/techidesignai/AIStaffRoom)** | 118 | MIT | Panel of experts | **Medium** - Simulates staff room with 6 agents (instructional designer, L&D specialist, facilitator, learning technologist, assessment designer, AI educator). TypeScript. Good reference for agent role patterns in Board room |
| **[sales-outreach-automation-langgraph](https://github.com/kaymen99/sales-outreach-automation-langgraph)** | 114 | Open Source | Multi-agent sales pipeline | **High** - LangGraph-based multi-agent system with lead qualification, personalisation. End-to-end flow. Provide pgvector memory pattern reference |

### E) Supabase + React SaaS Starters

| Name | Stars | License | Map To | Reuse Assessment | Effort |
|------|-------|---------|--------|------------------|--------|
| **[supabase/start](https://github.com/supabase/start)** | 6.5K | MIT | SaaS starter, Auth, RLS, Billing | **Very High** - **Official** Supabase starter. Production-ready, TypeScript, Vite. Auth/page layout with sidebar, migration files, secure RLS policies, organisation/user/team billing, legal page templates, example app for intervention patterns. Drop-in for BD Co-Pilot frontend + backend |
| **[supabase-nextjs-template](https://github.com/Razikus/supabase-nextjs-template)** | 520 | **Proprietary** | SaaS template | **Skip** - Not MIT/Apache. Reference only. Has auth, RLS, file storage, mobile app template |
| **[supabase-auth-template](https://github.com/supabase-auth-template)** | 675 | MIT | Auth template | **High** - Official Supabase auth starter. Use for auth module of BD Co-Pilot |
| **[supabase/basic-storage-nodejs](https://github.com/supabase/basic-storage-nodejs)** | 500 | MIT | File storage | **Low** - Reference for storage integration patterns |
| **[awesome-supabase](https://github.com/lyqht/awesome-supabase)** | 1.1K | - | Supabase resources list | **Reference** - Curated list of Supabase starters and resources. Use for discovering additional tools |

### F) Skills Library / Prompt Recipes

| Name | Stars | License | Map To | Reuse Assessment | Effort |
|------|-------|---------|--------|------------------|--------|
| **[openclaw/skills](https://github.com/openclaw/skills)** | ~60 | MIT | Official OpenClaw skills repo | **Core** - All official OpenClaw skills. Create your BD co-pilot skill here, following existing patterns. Code-ex eco-system extends via custom JS skills |
| **[openclaw/dataforge](https://github.com/openclaw/dataforge)** | ~15 | MIT | BD-specific skill (lead scoring, enrichment) | **High** - Already built BD-adjacent skill. Clone and adapt |
| **[77](https://github.com/openclaw/77)** | ~100 | MIT | Client-side JS runtime + prompts | **Medium** - Promo-automation repo with client-side JS runtime and 3 demo apps. Reference for prompt-to-output patterns |

---

## Architecture Recommendations

### Recommended Integration Map

```
BD Co-Pilot Architecture:

[Frontend: React + Vite + TS]
  └─ supabase/start (auth, RLS, org mgmt, billing)

[Backend: Supabase]
  └─ Postgres + pgvector (long-term agent memory)
  └─ Edge Functions (OpenClaw skill endpoints)

[Agent Runtime: OpenClaw]
  ├─ Custom BD Skills (lead-scoring from dataforge)
  ├─ MCP Integration (search, enrichment APIs)
  ├─ Multi-agent via WebSocket Channel (Board Room)
  └─ OpenClaw/CLI for dev/debug

[Lead Gen Module]
  ├─ soyuz (core enrichment + pipeline)
  └─ linki (LinkedIn outreach)

[Outreach Module]
  ├─ coldflow (cold email engine)
  ├─ sales-outreach-automation-langgraph (AI pipeline)
  └─ email-sleuth (email discovery)

[Board Room]
  └─ Colloquip (multi-agent debate patterns)
```

### Critical License Notes

- **AGPL-3.0 repos** (coldflow, ColdNet): Can use internally, but SaaS re-hosting requires open-sourcing your derivative work
- **MIT repos** (OpenClaw, soyuz, Colloquip, supabase/start): Safe for commercial use without open-sourcing
- **Proprietary**: supabase-nextjs-template - reference only, do NOT base your product on it

### Build-vs-Buy Summary

| Feature | Strategy | Source |
|---------|----------|--------|
| Agent Runtime | Use | OpenClaw |
| Auth + RLS | Use | supabase/start |
| Lead Enrichment | Use + Extend | soyuz + dataforge |
| Cold Email Engine | Use | coldflow |
| LinkedIn Outreach | Use | linki |
| Multi-Agent Board Room | Use patterns from | Colloquip |
| Email Discovery | Reference | email-sleuth |
| Outreach Scoring | Build | OutreachStud.io pattern |
| Signal-Based Outreach | Build | Trustpilot pattern |
| Billing/Metering | Reference | getlago/lago |

---

_Research completed: 2025 | BD Co-Pilot Architecture Team_
