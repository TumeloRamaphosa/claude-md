# Agentic Lab PRD — StudEx Dark Factory
**Product Requirements Document · v3 (2026-07-16)**

> **Brand:** StudEx D#VOP$ — Cyberpunk bull identity, dark theme, magenta/cyan/green neon
> **Status:** 🔨 Building (compressed from 8-week → today-forward)
> **Owner:** Tumelo Ramaphosa · The Agent Lord
> **Builder:** Robusca (Adam Sma$her) + The 9 Chiefs

---

## 1) Product Vision

**Auto Agent Lab** = a SaaS platform that autonomously builds applications for private-sector clients using the **BMAD methodology** (Breakthrough Method for Agile AI-Driven Development), powered by **OpenClaw** as the task/revenue engine.

**One-liner:** *Clients describe what they want (voice note + form) → AI builds it in 13–24 hours with 5–10 iterations → humans approve at every gate.*

**Brand:** StudEx D#VOP$ — cyberpunk bull, dark theme, magenta/cyan/green neon.

---

## 2) Problem

Building custom software is expensive (R 50 k–R 500 k+), slow (weeks–months), requires constant back-and-forth with devs. Most AI-generated code is "vibe coded" — works superficially, fails in production. **No platform combines autonomous AI agents + enterprise-quality gates to deliver production-ready software in 13–24 hours at a fraction of traditional cost.**

---

## 3) Target Users

- **SMEs** — custom web apps, automations, AI agents
- **Startups** — MVPs in 24 h
- **Enterprises** — internal tools, workflow automation
- **Agencies** — white-label build capacity

---

## 4) Core Features (Prioritized — TODAY-FORWARD)

### P0 — MVP (deliver this week)

| Feature | Tool | Cost |
|---|---|---|
| **DATA DIVE** (Step 1) — paste URL → 3-page AI audit | Claude Sonnet + Firecrawl | ~$0.05/audit |
| Client intake (Google Form + voice note) | Google Forms + Whisper | free |
| Auto-PDF PRD generation | @react-pdf/renderer | free |
| BMAD pipeline (PM → Architect → Scrum → Dev → QA) | Claude Sonnet (Opus for arch) | per-token |
| 5 human approval gates | Discord reactions | free |
| Code gen in VS Code | **Continue.dev + Aider + Cline → Ollama** | free |
| Auto code review | **Qodana + SonarQube + Semgrep** | free |
| Preview deploys | Vercel | free tier |
| Kanban dashboard | Next.js + DnD kit | free |
| PayFast payment | PayFast | 3.5 % |
| Discord notifications | Discord webhook | free |

### P1 — Should Have (Week 2)
- Live build visualization (see-claude style)
- 3D template gallery (React Three Fiber)
- Data Dive → Supabase → auto-PRD feed
- Cost estimation engine
- Client site/Instagram analyzer
- 3D before/after website preview
- Financial dashboard (revenue, cost, margin)

### P2 — Nice to Have (Month 2)
- 3D cyberpunk bull landing page (Remotion + Spline)
- White-label option
- Client portal (login + tracking)
- AI chat for requirement clarification
- Template marketplace

---

## 5) Client Journey (Full Agentic Experience)

### Landing Page (before login)
- AI-assisted explainer + BMAD 3D walkthrough
- **Live work status banner:** "12 builds in progress · 47 delivered this month"
- How the platform learns from every project
- **StudEx Specialist Agents** in 3D (army assembled)
- Link to "Meet the Army"
- **NO mention of GitHub** — these are StudEx Specialist Agents

### Step 1 — Data Dive
- Paste URL → 3-page free preview
- Paid tiers:
  - **R 2 500** Full Medium Report
  - **R 5 000** Full Deep Dive
  - **R 2 500/mo** Deep Dive subscription
- 3D pictures + video explain
- Results stored in Supabase, fed into PRD

### Step 2 — AI Consultation Agent
- Real-time voice + chat agent:
  - **Fish Audio TTS** (sub-300 ms, voice cloning, 30+ langs)
  - **Pika Skills** (video meeting avatar)
- **Diagnosis Agent** knows all platform capabilities
- **Sales Agent** helps complete PRD
- RAG-powered — gets smarter every interaction
- Knows: custom dev, StudExClaw, Anthropic SDK, Google Agent Toolkit, n8n

### Step 3 — PRD Completion
- Google Form + voice note + doc upload
- 35 % deposit (PayFast) before build starts
- **AgentMail** handles all email

### Step 4 — Live Build Visualization
- "Pane of glass" terminal view (**xterm.js**)
- Agents visible like see-claude
- Per agent: status + current task + files + test results
- Supabase Realtime → WebSocket → dashboard

### Step 5 — Delivery
- GitHub repo (created for client) OR zip
- AgentMail: PRD + updates + final
- Fish TTS + Pika for voice/video follow-up

### Services Offered
1. Custom application development
2. StudExClaw (OpenClaw) automation
3. Custom AI agents (Anthropic SDK / Google Agent Toolkit)
4. n8n workflow automation
5. studex.computer AI integrations
6. General app dev + automation

---

## 6) Build Pipeline (VS Code on Mac Mini)

```
Open VS Code (Mac Mini M4 Pro)
    ↓
Continue.dev + Aider + Cline → Ollama local models (qwen2.5-coder:7b / deepseek-coder-v2:16b)
    ↓
Git push → PR to GitHub (TumeloRamaphosa org)
    ↓
Qodana + SonarQube + Semgrep → auto-review
    ↓
If issues → agent fixes → re-push → re-review
    ↓
Clean PR → Discord approval gate (human)
    ↓
Merge → Vercel auto-deploys preview
```

**Claude Auto mode** runs PM + Architect phases.
**Code-gen mode** = Ollama local (cost = 0).
**Build execution = 13 hours** (compressed from 24–48 h).

---

## 7) BMAD Enterprise Workflow

| Phase | Duration | Agent | Deliverable | Quality Gate |
|---|---|---|---|---|
| Intake | 0–1 h | — | Voice note + form | Team approves |
| Planning | 1–2 h | **PM Agent (Claude)** | 2-page PRD (PDF) | PRD validated |
| Solutioning | 2–3 h | **Architect + Scrum (Claude)** | Arch doc + sprint plan | Arch validated |
| Implementation | 3–13 h | **Dev Agent (Ralph Loop, Ollama)** | 5–10 iterations | Qodana clean |
| QA | 13–20 h | **Review Agent (Ollama + Sonar)** | Final validation | Acceptance criteria met |
| Delivery | **13–24 h** | — | Production URL + docs | Client receives live app |

### Quality Standards
- Test coverage ≥ 80 %
- Lighthouse ≥ 90
- SAST: 0 critical/high
- TypeScript strict (no `any`)
- WCAG 2.1 AA
- Full docs (JSDoc + README + API)

---

## 8) Harness Architecture (Production Engineering)

Key patterns from Claude Code's production architecture:

- **Async generator event stream** — all agent events → one yield-based stream to dashboard
- **Prompt cache boundary** — static instructions cached globally, per-project PRD injected dynamically
- **Approval denial feedback** — "Request Changes" fed back as context
- **Memory prefetch** — project context prefetched while agent generates
- **Asymmetric persistence** — client actions sync, agent output async
- **Four-layer compaction** — proactive, reactive, snip, context collapse

**Principle:** *The model is interchangeable. The harness is where production quality lives.*

---

## 9) Tech Stack (Free-OSS First)

| Layer | Technology |
|---|---|
| Frontend | Next.js 16 + React Three Fiber + GSAP + Tailwind 4 |
| Backend | Supabase (PostgreSQL + RLS + Realtime + Auth + Storage) |
| Deployment | Vercel (preview + production) |
| Orchestration | n8n (self-hosted) |
| Code Gen | **Continue.dev + Aider + Cline → Ollama local** (NOT paid CLIs) |
| Code Review | **Qodana + SonarQube Community + Semgrep + DeepSource** (NOT CodeRabbit) |
| Methodology | BMAD + Ralph Loop + GSD (bmalph) |
| Platform Brain | **OpenClaw v2026.6.10** (local, swarmable) |
| Payments | PayFast (ZAR, 3.5 %) |
| Notifications | **Discord + Slack + WhatsApp** (NOT Telegram) |
| Voice | **Whisper (STT) + NeuTTS (local TTS) + Edge TTS (cloud TTS)** + Fish Audio |
| PRD PDF | @react-pdf/renderer |
| 3D | React Three Fiber + Spline + Remotion |
| VPS | Hetzner Cloud CPX31 (EUR 15/mo) |
| LLM local | Ollama (8 models, ~30 GB installed) |
| LLM cloud | Claude Max + API (Haiku/Sonnet/Opus) |

---

## 10) Cost Structure

| Item | Monthly Cost |
|---|---|
| Hetzner VPS | ~R 300 |
| Supabase Pro | ~R 450 |
| Vercel Pro | ~R 350 |
| Claude API (per project) | ~R 50–R 500 |
| Qodana + SonarQube | **free** |
| Resend | ~R 0–R 50 |
| PayFast | 3.5 % per txn |
| Fish Audio TTS | ~R 100–R 680 |
| **Total platform** | **~R 1 600/mo + API** |

---

## 11) Revenue Model (Africa-Competitive Pricing)

| Service | Price (ZAR) |
|---|---|
| Data Dive — Free Preview | free with paid build |
| Data Dive — Medium Report | R 2 500 once |
| Data Dive — Full Deep Dive | R 5 000 once |
| Data Dive — Monthly Subscription | R 2 500/mo |
| Starter Build | R 5 000–R 15 000 |
| Standard Build | R 15 000–R 50 000 |
| Enterprise Build | R 50 000–R 150 000+ |
| Monthly Maintenance | R 2 500/mo |
| Custom Agent Development | R 10 000–R 50 000 |
| n8n Workflow Automation | R 5 000–R 25 000 |
| StudExClaw Automation | R 15 000–R 75 000 |

**Sub-agent spawned** — research Africa vs USA vs China vs ROW pricing comparison.

---

## 12) Success Metrics

- First client build delivered in **13 hours** (not 24–48)
- 80 %+ test coverage
- 0 critical security vulnerabilities
- Client satisfaction ≥ 4.5/5
- Platform cost < 20 % of revenue
- **100+ client projects/month by month 3**

---

## 13) Credential Isolation

| Service | Isolation |
|---|---|
| GitHub | bot account, own tokens |
| Supabase | dedicated org, scoped creds |
| Vercel | dedicated account |
| PayFast | merchant account |
| Qodana/Sonar | OSS, self-hosted |
| AgentMail | scoped to tumelor001@gmail.com |

---

## 14) Communication Stack

| Tool | Role |
|---|---|
| **AgentMail** | All email — PRD delivery, progress updates, final |
| **Fish Audio TTS** | Sub-300 ms voice, voice cloning |
| **Pika Skills** | Video meeting presence |
| **Discord** | Team notifications + approval gates |
| **Slack** | Async ops + threads |
| **WhatsApp** | Client chat + Agent Lord alerts |
| **Resend** | Transactional email backup |

---

## 15) RAG Learning System

- **Vector DB:** Qdrant (self-hosted Docker) OR Supabase pgvector
- **Indexed:** PRDs, architecture, code patterns, reviews, error resolutions, client prefs
- **Embeddings:** Ollama nomic-embed-text (free) — NOT OpenAI
- **Retrieval:** top 5–10 chunks injected per task
- **Diagnosis + PRD agents** know all other agents' capabilities
- **Platform continuously improves** accuracy + speed

---

## 16) Infrastructure

| Component | Choice | Monthly Cost |
|---|---|---|
| Hardware | **Mac Mini M4 Pro 16 GB** | ~R 280 elec + R 28 k once |
| AI Models | Claude Max + API + Ollama local | ~R 2 700–4 500 |
| Orchestration | n8n (self-hosted) | free |
| Sandboxes | Docker (primary) + E2B (untrusted) | ~R 360–900 |
| RAG | Qdrant Docker | free |
| Voice | Fish Audio + NeuTTS + Edge TTS | ~R 100–680 |
| Email | AgentMail | free tier |
| Remote | Tailscale + Cloudflare Tunnel | free |
| **Total** | | **~R 3 500–5 800/mo** |

### Cost Optimization
- **Haiku** for scaffolding, **Sonnet** for dev, **Opus** for architecture only
- **Ollama** for everything repetitive
- **Docker** sandboxes free; **E2B** only for untrusted

---

## 17) StudEx Specialist Agents (100+ from agency-agents)

Source: github.com/msitarzewski/agency-agents (73.8 k stars)

| BMAD Agent | Agency-Agents Persona | Division |
|---|---|---|
| PM Agent | Product Manager | Product |
| Architect Agent | Solutions Architect | Engineering |
| Scrum Agent | Project Manager | Project Mgmt |
| Dev Agent | Full-Stack Developer | Engineering |
| Review Agent | QA Engineer | Testing |
| Design Agent | UI/UX Designer | Design |
| Sales Agent | SDR | Sales |
| Support Agent | CSM | Support |
| Ops Agent | Ops Manager | Ops |
| Content Agent | Content Strategist | Marketing |
| Research Agent | Market Researcher | Research |
| Data Dive Agent | Data Analyst | Analytics |

---

## 18) Google Form (Client PRD Intake)
URL: https://docs.google.com/forms/d/138CVJx6I0nSt7lTOjO10UXtfmJp47Fp7CzbvY0fS4HM/edit

Sections:
1. Client / Company Info (name, email, phone, website, Instagram)
2. Project Request (type, description, problems, target users, features)
3. Technical Prefs (existing codebase, stack, DB, auth)
4. Business Context (budget, urgency, references, notes)
5. Document Uploads (briefs, wireframes, existing docs)

---

## 19) GitHub Repo
Create new repo: **`auto-agent-lab`** under TumeloRamaphosa org.
Each client build → dedicated repo under agent's GitHub account.
Handover: repo access OR zip download.

---

## 20) Out of Scope (V1)
- Mobile native (iOS/Android)
- Multi-language
- Custom domain per client
- Marketplace for third-party templates
- Self-service signup

---

## 21) Daily + Weekly Pipeline (Larry skill + MultiPost + DenchClaw)

### Daily (every day)
- 06:00 Heartbeat (phi4-mini)
- 07:00 Notion sync + plan
- 09:00 StudEx Meat + hotels outreach (DenchClaw)
- 11:00 **Agentic Lab** build pipeline
- 13:00 YouTube production (Naledi avatar, Higgsfield)
- 15:00 SA-Russia research (Static GM)
- 17:00 Code review (Qodana/Sonar)
- 19:00 Social posting (Larry + MultiPost)
- 21:00 Lead pipeline + close
- 22:00 Daily eval + memory flush + GitHub commit

### Weekly
- **Mon:** topic research (10–20) + **2 new product pitches**
- **Tue:** scripts (5 shorts + 1 long-form)
- **Wed:** production (avatar, voice, captions, thumbnails)
- **Thu:** publish + repurpose + community
- **Fri:** SaaS pipeline (leads → demos → onboarding)
- **Sat:** improve agent evals + fix failures
- **Sun:** analytics review + GitHub audit

### Social Account Management (per Agent Lord)
- New Instagram + Facebook for StudEx businesses
- Recommended: **MultiPost** (already configured, API key saved) — manage ALL accounts from one dashboard
- Schedule posts, cross-post, analytics

---

## 22) Compressed Timeline (TODAY-FORWARD, not 8 weeks)

### Day 1 (TODAY 2026-07-16)
- [x] CLAUDE.md written
- [x] Statics DevOps Plan written
- [x] Agentic Lab PRD written
- [x] GitHub repo audit (50+)
- [x] Credentials vault updated (Shopify, AgentMail, KiloClaw)
- [ ] Spawn 4 sub-agents (market research, voice agent, THTR.com, YouTube)
- [ ] Save YouTube workflow videos as skills
- [ ] Save website demo videos as skills (Karpathy-style 1-min demos)

### Day 2–7
- Discord bot live + voice channel listening
- Episode Factory v0 (Naledi TTS → MP4)
- 10 shorts published
- Waitlist live

### Day 8–14
- Membership School MVP outline
- Convert 10 episodes → 10 lessons
- PayFast payment flow

### Day 15–21
- **StudEx Sales Agent** package live
- Tenant model + audit logs

### Day 22–28 — Event month prep
- Event landing page
- Live demo script
- "License an agent" offer

---

*Robusca (Adam Sma$her) — The Iron Engine*
*StudEx Agent Group · The Dark Factory*
*Last updated: 2026-07-16 21:36 SAST*