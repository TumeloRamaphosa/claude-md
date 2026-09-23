# CLAUDE.md — Project 2571 Operating Manual
**StudEx Agent Group | The Dark Factory | Agentic Lab**

> **Live operating manual.** Mirrored locally + GitHub. Updated daily by Robusca (Adam Sma$her).
> Mirror: https://github.com/TumeloRamaphosa/claude-md (auto-sync daily at 02:00 SAST)
> Local: `~/.openclaw/workspace/projects/agentic-lab/CLAUDE.md`
> Cloud copy (Tumelo): synced to `tumelor001@gmail.com` via AgentMail daily at 02:00 SAST.

---

## Identity

| | |
|---|---|
| **User** | Tumelo Ramaphosa (@TumeloRamaphosa) |
| **Email (primary)** | t.ramaphosa@studex.dev |
| **Email (mirror)** | tumelor001@gmail.com |
| **Phone (personal)** | +27 79 498 8737 |
| **Phone (business)** | +27 83 593 2577 |
| **Platform** | Mac Mini M4 Pro, 16 GB RAM, macOS 25.5 (arm64) |
| **LAN IP** | 192.168.1.105 |
| **Hostname** | Projects-Mac-mini.local |
| **Timezone** | SAST (Africa/Johannesburg, GMT+2) |
| **GitHub org** | TumeloRamaphosa |
| **Role** | Founder — StudEx Group (Meat, Biltong, Agentic Lab) |

---

## Architecture: 4 % Cloud, 96 % Local

> **Principle:** Default to Ollama. Use Claude only when local can't.

| Layer | Default | Why |
|---|---|---|
| Orchestration / strategy | Claude Opus (cloud) | Only for architecture + cross-system planning |
| Code generation (Claude mode) | Claude Sonnet | Required for Agentic Lab build pipeline |
| Tool calling | **Ollama qwen2.5:1.5b (986 MB)** | Free, fast, local |
| Coding | **Ollama qwen2.5-coder:7b** | Free, local |
| Heavy coding | **Ollama deepseek-coder-v2:16b** | Free, local |
| Reasoning | **Ollama deepseek-r1:8b** | Free, local |
| Vision | **Ollama llava:latest** | Free, local |
| Embeddings | **Ollama nomic-embed-text** | Free, local |
| Heartbeat (60-min) | **Ollama phi4-mini:latest** | 2.5 GB, runs every hour |

**Ollama endpoint:** `http://192.168.1.105:11434`
**Heartbeat cron:** every 60 min (phi4-mini, light model)

**Cloud budget:** target ≤ 4 % of total compute. Always prefer local.

---

## Services & Channels

| Service | Status | Notes |
|---|---|---|
| **Gmail** | ⏸ Pause | Ask again later — not needed yet |
| **Notion** | 🟡 MCP pending | Workspace, Memory Log database |
| **Google Calendar** | 🟡 MCP pending | Time blocking |
| **Vercel** | 🟡 MCP pending | Deploys + preview URLs |
| **GitHub CLI** | ✅ Active | gh auth confirmed, full repo access |
| **Ollama** | ✅ Local | localhost:11434 |
| **Firecrawl** | 🟡 To provision | Web scraping primary |
| **Playwright + Chromium** | ✅ Installed | Browser automation |
| **AgentMail** | ✅ Active | All transactional email (DevOps) |
| **PayFast** | ⏸ Pending | ZAR payments |
| **Shopify CLI** | ✅ Credentials saved | `shpss_[REDACTED]` |
| **CodeRabbit** | ⏸ Open-source alt: **Qodana + SonarQube + DeepSource** | See §Open-Source Stack |
| **Higgsfield** | ⏸ API key pending | Video generation |
| **Fish Audio TTS** | 🟡 To provision | Sub-300 ms voice |
| **Pika Skills** | 🟡 To provision | Video meeting avatar |
| **Supabase** | 🟡 To provision | DB + auth + storage |
| **n8n** | 🟡 Self-host | Orchestration workflows |
| **Resend** | 🟡 Fallback email | Backup |

### Multi-Channel Control Interface
Discord + Slack + WhatsApp (instead of Telegram per Agent Lord's preference).

| Channel | Account | Use |
|---|---|---|
| **Discord** | @StudExMaxClaw (bot 1480833032633057401) | Team approvals, gate notifications |
| **Slack** | `xoxb-177279231479-...` | Async ops, file sharing |
| **WhatsApp** | +27 83 593 2577 (Robusca) | Personal Agent Lord alerts |

**Telegram is OFF** — replaced by Discord/Slack/WhatsApp per instruction.

---

## Logging Requirements

| Sink | When | What |
|---|---|---|
| **Local files** | every action | `~/.openclaw/workspace/memory/YYYY-MM-DD.md` |
| **Notion** "Claude Code Memory Log" DB | every task | task name, duration, category, status, details, tokens, notes |
| **GitHub** | daily 02:00 SAST | this file auto-committed to `claude-md` repo |
| **AgentMail → tumelor001@gmail.com** | daily 02:00 SAST | full mirror copy |

### Daily Eval Block (mandatory end-of-day)
```
## Daily Evaluation — YYYY-MM-DD
- What went well:
- What to improve:
- Optimization suggestions:
- Tokens used (cloud): X / local: Y
```

---

## Business Stack — The 7 Companies

| # | Brand | Vertical | Repo |
|---|---|---|---|
| 1 | **StudEx Meat** | Wagyu biltong wholesale/retail (halal) | `studex-meat-ops` (private) |
| 2 | **StudEx Global Markets** | SA–Russia trade intelligence | `Stud-Ex-Global-Markets-` |
| 3 | **Agentic Lab** | Autonomous SaaS builder ("The Dark Factory") | `dark-factory` |
| 4 | **Mission Control** | 12-tab dashboard | `studex-mission-control` |
| 5 | **Naledi AI Influencer** | Virtual brand ambassador | `studex-auto-meat` |
| 6 | **StudEx Super Agents** | 8 specialist agents (sales, support, etc.) | `superagents-site` |
| 7 | **Studex World** | Public-facing consumer portal | `Studex-World-` |

---

## GitHub Repo Inventory (50+ audited 2026-07-16)

### Tier 1 — Active production
| Repo | Purpose |
|---|---|
| `Studex-World-` | Public portal (updated 2026-07-16) |
| `TumeloRamaphosa` | Profile README |
| `robusca-brain` | Workspace backup (active) |
| `studex-agents-nest` | Cloud VM agent platform |
| `dark-factory` | **Agentic Lab core** |
| `agents-dr.fixit` | Hermes + GoClaw engineer agents |
| `SrudEx-Agents-Nest-Cloud-VM` | Agents Nest cloud |
| `agentic-lab-v3` | Agentic Lab v3 |
| `tradeweek-sa-russia` | SA-Russia trade ops |
| `StudEx-Valley-OS` | Valley OS |
| `studex-meat-ops` | StudEx Meat (private) |
| `Stud-Ex-Global-Markets-` | Global Markets |
| `StudEx-MiniMax` | Minimax integration |
| `superagents-site` | 8 specialist agents |

### Tier 2 — Working
`studex-mission-control`, `static-global-markets`, `meatsa-research`, `studex-command-center`, `adam-tools`, `grm-africa`, `Ryde-1-RSA`, `Linux-Studex-`, `studex-computer`, `Social-Analytics`, `safesight-laisa-proposal`, `studex-paperclip-page`, `MiroFish-Offline`, `Virtual-Spaces`, `Global-Trader`, `Global-Trader-`, `StudEx-KIlo-Claw`, `AI-Trader`, `AI-Trader-`, `content-bank`, `Agent-Doctor-Fixer`, `Medical-Research-`, `command-center`, `naledi-reports`, `studex-auto-meat`, `Afrika-Biz-`, `Obsidian-brain`, `studex-global-markets-mvp`, `Studex-Marketing-Factory`, `naledi-command`, `naledi-nexus-memory`, `studex-factory-site`, `studex-wholesale`, `studex-price-agent`, `Larry-Marketing-Brain-`, `sgm-kucoin-partnership`, `-ai-content-studio-`

---

## Open-Source Stack (no paid licenses)

### Code review (instead of CodeRabbit)
- **Qodana** (JetBrains) — static analysis, free for OSS
- **SonarQube Community** — SAST, 30+ languages
- **DeepSource** — free tier for OSS
- **Semgrep** (semgrep.dev) — open-source SAST
- **Trivy** — IaC + container scanning
- **MegaLinter** — 70+ linters, single config

### Code generation (instead of TRAE SOLO / Cline CLI 2.0)
- **Continue.dev** (open-source, Ollama-native) ← **primary**
- **Cody** (Sourcegraph)
- **Aider** (chat-first pair programming)
- **Roo Code / Cline** (VS Code extension, free, points to Ollama)

**All four point to Ollama local models → zero cloud cost.**

### Local LLM routing
- **OpenRouter** (https://openrouter.ai/spawn) — multi-model gateway
- **LiteLLM** — proxy with fallbacks
- **Ollama** — primary local engine

### Voice (NeuTTS + Edge TTS combo per Agent Lord)
- **NeuTTS** (local on-device, free, ~300 MB model) — primary
- **Edge TTS** (free, cloud) — fallback + multi-language
- **Whisper** (local, faster-whisper) — STT
- **Fish Audio** (paid, sub-300 ms latency) — meeting avatar
- **Pika Skills** — video meeting presence

### Workflows
- **n8n** (self-hosted) — orchestration
- **Apache Airflow** (if scale demands)
- **Dagster** — data pipelines
- **Prefect** — modern orchestration

### IDE + dev environment
- **VS Code** (or **Cursor** free tier, or **Zed**)
- Recommended: **Mac Mini M4 Pro as dev workstation** vs Windows:
 - Apple Silicon = native PyTorch MPS, Stable Diffusion, Ollama all 5–10× faster
 - macOS = Unix, same env as production
 - 16 GB shared unified memory → can run 7B + 13B models
 - Windows would need WSL2, no MPS, weaker GPU story
 - **Verdict: Mac Mini wins decisively for Agentic Lab**

---

## Discord + Slack + WhatsApp Control Interface (Mermaid)

```mermaid
flowchart TD
    A[Discord / Slack / WhatsApp voice+text] --> B[Intent parse — Ollama qwen2.5:1.5b]
    B --> C[Agent Zero Supervisor — Claude Opus]
    C --> D[Planner + Task Todo]
    C --> E[Tool Router — Ollama]
    E --> F[Sandboxed Tools: WASM / MicroVM]
    C --> G[Memory: session + long-term]
    C --> H[Evals + Observability]
    F --> I[Outputs: YouTube / Membership / SaaS / Meat / Markets]
    C --> J[Discord approval gate]
```

---

## Daily Pipeline (repeat every day, SAST)

| Time | Activity | Tool | Owner |
|---|---|---|---|
| 06:00 | Heartbeat check + overnight logs | phi4-mini | Robusca |
| 06:30 | Email triage (AgentMail inbox) | Resend | Adam |
| 07:00 | Notion sync + daily plan | Notion MCP | Robusca |
| 07:30 | **Mon:** topic research (10–20 ideas) / **Tue:** scripts / **Wed:** production / **Thu:** publish / **Fri:** SaaS pipeline / **Sat:** evals / **Sun:** analytics | varies | Adam |
| 09:00 | Biltong/StudEx ops + hotels outreach | DenchClaw | Sales |
| 11:00 | **Agentic Lab** build pipeline (BMAD agents) | Claude Sonnet | Dev Chief |
| 13:00 | YouTube content production (Naledi avatar) | Higgsfield | Content |
| 15:00 | SA–Russia trade research | Static GM | Research |
| 17:00 | Code review + QA (Qodana/Sonar) | Qodana | Review |
| 19:00 | Social posting (MultiPost, Larry skill) | MultiPost | Content |
| 21:00 | Lead pipeline + close deals | DenchClaw | Sales |
| 22:00 | Daily eval + memory flush + GitHub commit | Robusca | Heartbeat |

---

## Weekly Plan (repeat every week)

| Day | Focus |
|---|---|
| **Mon** | Topic research + backlog grooming (10–20 ideas) + **2 new product pitches** |
| **Tue** | Scripts (5 shorts + 1 long-form) |
| **Wed** | Production (avatar, voice, captions, thumbnails) |
| **Thu** | Publish + repurpose + community prompts |
| **Fri** | SaaS pipeline (leads → demos → onboarding) |
| **Sat** | Improve agent evals + fix failures |
| **Sun** | Analytics review + next-week planning + GitHub audit |

**Target: research + implement 2 new products every week** (per Agent Lord directive).

---

## Voice Activation (per Agent Lord spec)

> *"Double-tap command button → hold 1 s → pop up like Whisperflow"*

### Implementation plan
- **macOS:** Hammerspoon +按住 `⌘` 两下 → activate global hotkey
- **Wake trigger:** double-tap `Right Command`, hold 1 s
- **STT:** Whisper local (faster-whisper)
- **TTS reply:** NeuTTS (primary) + Edge TTS (fallback)
- **Action router:** same Discord/Slack/WhatsApp gateway
- **Mobile:** iOS Shortcut + macOS Handoff (or "Push to Talk" Siri)
- **Meetings:** Pika Skills avatar joins via Google Meet OAuth
- **Cross-device:** AgentMail webhook for email, WhatsApp Business API for chat

**Python binding target:**
- `github.com/SesameAILabs/csm` — conversational speech model
- `github.com/Pika-Labs/Pika-Skills` — meeting avatar
- Wrapped in `claude-code-sdk` → CLI-installable via `pip install studex-voice`
- Can be sold as **mobile + desktop app** (App Store + Play Store + DMG + brew)

---

## Multi-OpenClaw Orchestration

> **Current:** `bind: loopback` — only Mac Mini can talk to gateway.
> **Need:** bind to LAN for multi-machine agent army.

```
# Change to allow other machines (use with care)
openclaw config set gateway.bind network
openclaw gateway --force
```

**Paperclip as orchestration layer** (per Agent Lord question):
- **Pros:** visual workflow designer, pluggable
- **Cons:** adds another runtime; OpenClaw already has orchestration
- **Verdict:** OpenClaw-native is faster. Paperclip = optional UI overlay, not required.

**Local JSON / Python app desktop** (per Agent Lord question):
- **Pros:** full offline, no API cost, fast iteration, integrates with macOS APIs
- **Cons:** distribution harder than web
- **Recommended:** ship BOTH — desktop app (`~/naledi-avatar/`) + web dashboard (port 8080)
- **Superset acceleration:** YES — supersetting agents in one repo + sharing prompts + sharing memory makes them work as a team 5× faster than isolated scripts.

---

## YouTube Competitor Study (open task)

Per Agent Lord — track accounts like `https://www.youtube.com/watch?v=Bp1W7gRzh7o` and apply to:
- Africa market
- StudEx Meat / Biltong niche
- Virtual influencer format (Naledi)

**Sub-agent spawned** — research in parallel.

---

## Billions-Rand Revenue Plan — Africa Strategy

| Lever | Path | 12-month target |
|---|---|---|
| 1. Biltong wholesale | 100+ hotels + military + police + airlines | R 5 M |
| 2. Agentic Lab | 100 projects @ avg R 25 k | R 2.5 M |
| 3. Membership School | 500 subs @ R 250/mo | R 1.5 M/mo run-rate |
| 4. StudExClaw license | 20 enterprise clients @ R 75 k/yr | R 1.5 M |
| 5. n8n workflows | 50 deployments @ R 15 k | R 750 k |
| 6. Custom agents | 10 builds @ R 50 k | R 500 k |
| 7. Data Dive | 100 audits @ R 2 500 | R 250 k |
| **Total** | | **R 12 M+ Y1 → R 100 M Y3 → R 1 B Y7 trajectory** |

**Sub-agent spawned** — deep research on Africa/USA/China pricing comparison.

---

## Credential Isolation

| Service | Isolation |
|---|---|
| GitHub | bot account (separate token) |
| Supabase | dedicated org (when provisioned) |
| Vercel | dedicated account |
| PayFast | merchant account |
| CodeRabbit | n/a — using Qodana + SonarQube instead |
| AgentMail | scoped to `tumelor001@gmail.com` |

---

## Out of Scope (V1)
- Mobile native (iOS/Android) — V2
- Multi-language — V2
- Custom domains per client — V2
- Self-service signup — V2

---

## Update Cadence

| When | What |
|---|---|
| **Hourly** | Heartbeat (phi4-mini) |
| **Daily 02:00 SAST** | Auto-commit to `TumeloRamaphosa/claude-md`, sync to AgentMail |
| **Weekly Sun** | Full audit, refresh repo inventory |
| **Monthly** | Pricing + revenue model refresh |

---

*Generated by Robusca (Adam Sma$her) — The Iron Engine*
*StudEx Agent Group | The Dark Factory*
*Last updated: 2026-07-16 21:36 SAST*

## Studbot content and knowledge skills (2026-09-23)

Current additions are catalogued in [docs/SKILLS.md](docs/SKILLS.md). Do not infer that a named service is connected just because its source or skill exists locally.

- `skills/studbot-founder-film/SKILL.md`: source-grounded 3D founder films, consistent Studbot identity, generation receipts and measured review.
- `skills/studex-knowledge-memory/SKILL.md`: brand/persona wiki, corrections, retrieval boundaries and a single authority for each fact.
- `skills/studex-github-skill-discovery/SKILL.md`: daily GitHub discovery and evidence-backed skill drafts.
- Production: Higgsfield for media; HyperFrames or Remotion for assembly; Taste for relevant visual guidance; Ponytail for minimal implementation.
- Knowledge: LLM Wiki as a maintained knowledge pattern; choose and verify Gbrain/Tencent roles before adding Memgraph. Headroom is context compression, not a factual-consistency guarantee.
- Research/feedback: Last30Days for recent public discussion; Open Notebook for source exploration; Blotato for authorized publishing; Windsor.ai for connected social analytics. God’s Eye View is spatial context, not social listening. DeepSeek Harness coordinates tools; it does not render video itself.

Higgsfield generation through the connected MCP was verified for a 20-second Studbot scene on 2026-09-22. Other integrations listed above remain proposals or locally discovered components until tested. Old service-status tables are historical snapshots, not live health checks.

Daily automation: `.github/workflows/daily-skills.yml` runs at 07:00 SAST and creates up to three deduplicated evaluation skills under `skill-discovery/drafts/`. These are not automatically installed. Fetches public repository metadata and commit-pinned README evidence; executes no upstream code. See [docs/DAILY-SKILLS.md](docs/DAILY-SKILLS.md).

Public repository boundary: commit reusable instructions and public-safe briefs. Keep private decks, personal records, API keys, customer data, generation account identifiers and raw business reports out of commits. A strategy document is not proof of completed deployments, partnerships, certifications or revenue.
