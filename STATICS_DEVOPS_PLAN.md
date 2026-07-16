# StudEx DevOps Plan — Agent Zero Business OS
## StudEx Agentic Lab · "The Dark Factory" · v2 (2026-07-16)

> **⚠️ Note from Agent Lord:** This is the **StudEx Agent Group**, not "Statics".
> All references below say **StudEx Agent Group / StudEx Specialist Agents**.
> Telegram → replaced with **Discord + Slack + WhatsApp** (multi-channel).

---

## 1) Executive Summary — What We Are Building

**One automated operating system ("Agent Zero")** that runs five revenue engines from one shared orchestration, memory, tooling, and DevOps core:

| # | Engine | Purpose |
|---|---|---|
| 1 | **YouTube Media Engine** | Naledi virtual influencer creates + publishes original episodes |
| 2 | **Membership School** | Episodes become paid lessons + templates + weekly challenges |
| 3 | **Agents-as-a-Service (SaaS)** | Businesses license StudEx Specialist Agents (sales, support, ops) |
| 4 | **StudEx Meat / Biltong** | Wholesale + retail pipeline (hotels, military, airlines) |
| 5 | **SA-Russia Trade Markets** | StudEx Global Markets intelligence + deal flow |

**Core principle:** *One shared platform powers all five engines.*

---

## 2) Control Interface — Multi-Channel

### Discord + Slack + WhatsApp (instead of Telegram)

| Channel | Setup | Use |
|---|---|---|
| **Discord** | `@StudExMaxClaw` bot + voice channels | Voice commands + team approvals |
| **Slack** | `xoxb-177279231479-...` + Socket Mode | Async ops, file sharing, threads |
| **WhatsApp** | +27 83 593 2577 (Robusca) | Agent Lord personal alerts, client chat |

**Single intent router** — same `B[Intent parse]` node in mermaid below — accepts any of the three. No Telegram.

### Voice Activation (Agent Lord spec)
- Double-tap `Right Command`, hold 1 s → pop up like Whisperflow
- STT: Whisper local (faster-whisper)
- TTS: **NeuTTS** (local, free, 300 MB) + **Edge TTS** (cloud, free, fallback)
- Meeting presence: Pika Skills avatar
- Cross-device: macOS Handoff + iOS Shortcut

---

## 3) Reference Architecture — Static Super Agent OS

### Layers

#### Layer 1 — Interface
- Discord + Slack + WhatsApp (voice + commands)
- Admin dashboard (web port 8080)

#### Layer 2 — Orchestration (Agent Zero)
- Supervisor agent routes requests
- Explicit handoffs + retry rules
- Deterministic, resumable

#### Layer 3 — Execution (tools + sandboxes)
- Specialized agents (content, course, sales, support, devops)
- Tool calling (APIs, browser automation, file ops)
- **Secure sandbox:** WASM tool runtime (Microsoft Wassette) with deny-by-default MCP-style permissions
- Reference: https://opensource.microsoft.com/blog/2025/08/06/introducing-wassette-webassembly-based-tools-for-ai-agents

```mermaid
flowchart TD
    A[Discord / Slack / WhatsApp voice+text] --> B[Intent parse — Ollama qwen2.5:1.5b]
    B --> C[Agent Zero Supervisor — Claude Opus]
    C --> D[Planner + Task todo]
    C --> E[Tool Router]
    E --> F[Sandboxed Tools: WASM / MicroVM]
    C --> G[Memory: session + long-term]
    C --> H[Evals + Observability]
    F --> I[Outputs: YouTube / Membership / SaaS / Meat / Markets]
    C --> J[Discord approval gate]
```

---

## 4) StudEx Specialist Agents (The Agentic Army)

Source: https://github.com/msitarzewski/agency-agents (73.8 k stars, 100+ personas, 10 divisions)

We use these to power our BMAD sub-agents with battle-tested personalities, workflows, and deliverables.

| BMAD Agent | Agency-Agents Persona | Division |
|---|---|---|
| PM Agent | Product Manager | Product |
| Architect Agent | Solutions Architect | Engineering |
| Scrum Agent | Project Manager | Project Management |
| Dev Agent | Full-Stack Developer | Engineering |
| Review Agent | QA Engineer | Testing |
| Design Agent | UI/UX Designer | Design |
| Sales Agent | Sales Development Rep | Sales |
| Support Agent | Customer Success Manager | Support |
| Ops Agent | Operations Manager | Operations |
| Content Agent | Content Strategist | Marketing |
| Research Agent | Market Researcher | Research |
| Data Dive Agent | Data Analyst | Analytics |

### 3-Pack Agent Licenses (Agents-as-a-Service)
Built on https://code.claude.com/docs/en/agent-sdk/overview:

1. **StudEx Sales Agent** — lead qualify → book call → close
2. **StudEx Support Agent** — triage → resolve → escalate
3. **StudEx Ops Agent** — reports → reminders → workflows

**Offer:**
- License tiers (Solo / Team / Enterprise)
- Setup fee (optional) + monthly subscription
- Live demo: Discord / Slack / WhatsApp voice → agent builds output → audit log shown

---

## 5) Non-Negotiables

### A) Orchestration
- Retries + timeouts + deterministic handoffs
- Role-based access + least privilege (deny-by-default)
- Human-in-the-loop for risky actions (publishing, invoices, deploying)
- Stateful execution — sessions persist across days

### B) Safety + Security (local-first "Business OS")
- Sandboxed execution for any code/tool that touches files/network (WASM or MicroVM)
- Tenant isolation for SaaS — no cross-tenant memory leakage
- Prompt-injection defenses: tool allowlists + data policies + output post-checks

### C) Reliability + Evaluation
- Built-in eval harness (per Anthropic's pattern)
- Task success criteria + regression suite per agent
- Release gates: cannot deploy if eval score drops
- Reference: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents

### D) SaaS Readiness
- Multi-tenant routing
- Audit logs (every tool call recorded)
- Usage metering + billing hooks
- Admin controls per tenant

### E) Content Engine Specifics
- "Derivative risk" detector (similarity + structure checks)
- Brand voice rules + banned claims
- Auto-repurpose long-form → shorts

---

## 6) Build Pipeline (VS Code + Mac Mini)

```
Open in VS Code (Mac Mini M4 Pro)
    ↓
Continue.dev / Cline / Aider → Ollama local models
    ↓
Git push → PR to GitHub (TumeloRamaphosa org)
    ↓
Qodana + SonarQube + Semgrep → auto-review (free OSS)
    ↓
If issues → agent fixes → re-push → re-review
    ↓
Clean PR → Discord approval gate (human)
    ↓
Merge → Vercel auto-deploys preview
```

### VS Code + Mac Mini vs Windows
- Apple Silicon = native PyTorch MPS, Stable Diffusion, Ollama 5–10× faster
- macOS = Unix, same env as production (Vercel/Supabase)
- 16 GB unified memory → run 7B + 13B models comfortably
- **Verdict: Mac Mini M4 Pro wins decisively**

---

## 7) Enterprise Workflow (BMAD + Ralph + GSD)

| Phase | Duration | Agent | Deliverable | Quality Gate |
|---|---|---|---|---|
| Intake | 0–1 h | — | Voice note + form data | Team approves |
| Planning | 1–2 h | PM Agent | 2-page PRD (PDF via @react-pdf/renderer) | PRD validated |
| Solutioning | 2–3 h | Architect + Scrum | Architecture doc + sprint plan | Architecture validated |
| Implementation | 3–13 h | Dev Agent (Ralph Loop) | 5–10 deployed iterations | Qodana + SonarQube clean on each PR |
| QA | 13–20 h | Review Agent | Final validation | All acceptance criteria met |
| Delivery | **13–24 h** | — | Production URL + docs | Client receives live app |

### Quality Standards (Corporate Grade)
- Test coverage ≥ 80 %
- Lighthouse ≥ 90
- SAST: 0 critical / high vulnerabilities
- TypeScript strict: no `any`
- Qodana: all checks pass
- WCAG 2.1 AA accessibility
- Full docs (JSDoc + README + API)

---

## 8) Tech Stack (Free / Open-Source Where Possible)

| Layer | Technology | Cost |
|---|---|---|
| Frontend | Next.js 16 + React Three Fiber + GSAP + Tailwind 4 | free |
| Backend | Supabase (PostgreSQL + RLS + Realtime + Auth) | ~R 450/mo |
| Deployment | Vercel (preview + production) | ~R 350/mo |
| Orchestration | n8n (self-hosted) | free |
| Code Gen | **Continue.dev + Cline + Aider (all OSS, point to Ollama)** | free |
| Code Review | **Qodana + SonarQube Community + Semgrep + DeepSource** | free |
| Methodology | BMAD + Ralph Loop + GSD (bmalph) | free |
| Platform Brain | **OpenClaw v2026.6.10** (local) | free |
| Payments | PayFast (ZAR) | 3.5 % per txn |
| Notifications | Discord + Resend (email fallback) | free tier |
| Voice | Whisper API (transcription) + NeuTTS + Edge TTS | free |
| PRD PDF | @react-pdf/renderer | free |
| 3D | React Three Fiber + Spline + Remotion | free |
| VPS | Hetzner Cloud CPX31 (EUR 15/mo) | ~R 300 |
| LLM local | Ollama (8 models installed) | free |
| LLM cloud | Claude Max + API (Haiku/Sonnet/Opus) | ~R 2 700–4 500/mo |

---

## 9) Daily + Weekly Pipeline

### Daily (every day, SAST)
- 06:00 Heartbeat (phi4-mini)
- 07:00 Notion sync + plan
- 09:00 StudEx Meat + hotels outreach
- 11:00 **Agentic Lab build pipeline**
- 13:00 YouTube production (Naledi)
- 15:00 SA-Russia research
- 17:00 Code review (Qodana/Sonar)
- 19:00 Social posting (Larry + MultiPost)
- 21:00 Lead pipeline + close
- 22:00 Daily eval + memory flush + GitHub commit

### Weekly (repeat every week)
- **Mon:** topic research + backlog grooming (10–20 ideas) + **2 new product pitches**
- **Tue:** scripts (5 shorts + 1 long-form)
- **Wed:** production (avatar, voice, captions, thumbnails)
- **Thu:** publish + repurpose + community prompts
- **Fri:** SaaS pipeline (leads → demos → onboarding)
- **Sat:** improve agent evals + fix failures
- **Sun:** analytics review + next-week planning + GitHub audit

---

## 10) Timelines — Compressed (TODAY-Forward)

### Day 1 (today — 2026-07-16)
- [x] CLAUDE.md written + saved
- [x] Statics DevOps Plan written
- [x] Shopify credentials saved (vault)
- [x] GitHub repo audit (50+ repos)
- [x] Credentials vault updated
- [ ] Spawn 4 sub-agents (market research, voice agent, THTR.com site, YouTube study)

### Week 1 (today → Sun 2026-07-19)
- Discord bot active + listens to voice
- Episode Factory v0 (Naledi TTS + Edge TTS → MP4)
- First 10 shorts published (test channel)
- Waitlist live (Notion form)

### Week 2 (Mon 2026-07-20)
- Membership School MVP outline
- Convert first 10 episodes → 10 lessons
- PayFast payment flow

### Week 3 (Mon 2026-07-27)
- **StudEx Sales Agent** package live (one wedge)
- Tenant model + audit logs

### Week 4 (Mon 2026-08-03 — Event month prep)
- Event landing page + agenda
- Live demo script
- "License an agent" offer (pricing + terms)

---

## 11) Cost Structure (Monthly)

| Item | Cost |
|---|---|
| Hetzner VPS | ~R 300 |
| Supabase Pro | ~R 450 |
| Vercel Pro | ~R 350 |
| Claude API (per project) | ~R 50–R 500 |
| Qodana + SonarQube | free |
| Resend | ~R 0–R 50 |
| PayFast | 3.5 % per txn |
| Fish Audio TTS | ~R 100–R 680 |
| **Total platform** | **~R 1 600/mo + API usage** |

**vs SaaS revenue target:** R 12 M+ Y1 → cost < 20 % of revenue ✅

---

## 12) Multi-Machine Orchestration (per Agent Lord question)

> *"Can I summon more OpenClaws on other machines and have them help?"*

**Yes.** Steps:

1. On each new machine, install OpenClaw: `curl -sSf https://openclaw.ai/install.sh | bash`
2. Generate token: `openclaw token create --scopes "agent.run,memory.read,memory.write"`
3. On Mac Mini (controller):
 ```bash
 openclaw config set gateway.bind network  # ⚠️ was loopback
 openclaw config set agents.peers 192.168.1.106,192.168.1.107
 openclaw gateway --force
 ```
4. Each peer joins the swarm — share memory, distribute tasks by capability.

**Paperclip as orchestration overlay** (per Agent Lord question):
- Optional UI layer over OpenClaw
- Not required — OpenClaw-native is faster
- Use Paperclip if you want visual workflow designer for non-technical team

**Local JSON / Python app desktop** (per Agent Lord question):
- ✅ Recommended — already built (`~/naledi-avatar/naledi_assistant.py`)
- Benefits: full offline, no API cost, fast iteration, macOS native APIs
- Ship BOTH: desktop app + web dashboard (port 8080)

**Supersetting agents** (per Agent Lord question):
- ✅ YES — super-set them in `dark-factory` repo
- Share prompts, memory, skills
- Result: 5× faster than isolated scripts

---

## 13) Africa → R 1 Billion Revenue Strategy (Y7)

| Year | Engine | Target |
|---|---|---|
| Y1 | Biltong wholesale + Agentic Lab MVP | R 12 M |
| Y2 | Membership School scale + 20 enterprise agents | R 50 M |
| Y3 | Pan-Africa agent network | R 150 M |
| Y4 | Europe expansion | R 300 M |
| Y5 | Asia expansion | R 500 M |
| Y6 | Americas | R 750 M |
| Y7 | Full global + partner channel | **R 1 B+** |

**Sub-agent spawned** — deep market research on Africa vs USA vs China vs ROW pricing.

---

## 14) Out of Scope (V1)
- Mobile native (iOS/Android) — V2
- Multi-language — V2
- Custom domains per client — V2
- Self-service signup — V2

---

*Robusca (Adam Sma$her) — The Iron Engine*
*StudEx Agent Group · The Dark Factory*
*Last updated: 2026-07-16 21:36 SAST*