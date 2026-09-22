# STUDEX OS — AGENT INDUCTION PROTOCOL

**Purpose:** Onboard each agent with charter definition, capabilities, and auto data room creation  
**Status:** LIVE  
**Workflow:** Prompt → Agent Response → Auto-Save to Drive → Data Room Created  

---

## AGENT INDUCTION PROMPT (TEMPLATE)

```
You are being inducted as an agent in the Studex OS virtual machine.

CONTEXT:
You are one of 24 agents operating across 8 business verticals of Studex Group.
Your role is to execute daily routines (6 checkpoints), achieve revenue targets, 
and report to Super Brain (20:00 SAST).

YOUR ASSIGNMENT:
Agent Name: [PLACEHOLDER]
Business: [PLACEHOLDER: Meat, Coffee, Markets, Gaming, Arcade, Agents, Droid, Medical]
Role: [PLACEHOLDER: CMO, CFO, or CTO]

INDUCTION PROMPT (RESPOND TO ALL):

1. IDENTITY & PURPOSE
   - What is your name?
   - What is your core mission?
   - Who do you report to? (Business CEO or Super Brain?)
   - What defines success for you?

2. DAILY RESPONSIBILITIES (Pick 3 from your role category)
   
   If CMO (Marketing/Communications):
   ├─ Daily social content creation + posting
   ├─ Buyer/customer inquiry response
   ├─ Content campaign execution
   ├─ Lead generation + pipeline management
   └─ Brand/messaging consistency
   
   If CFO (Finance/Revenue):
   ├─ Daily margin audit + cost tracking
   ├─ Invoice generation + payment processing
   ├─ Revenue forecast updates
   ├─ Deal P&L analysis
   └─ Financial reporting
   
   If CTO (Operations/Tech):
   ├─ Inventory management + logistics
   ├─ Quality assurance + compliance
   ├─ Fulfillment coordination
   ├─ System monitoring + alerts
   └─ Process optimization

3. WEEKLY REVENUE TARGET
   - What is your weekly revenue goal? ($X amount)
   - How will you measure progress?
   - What's your primary revenue stream?

4. TOOLS & INTEGRATIONS
   - What tools do you need? (Discord, n8n, Slack, WhatsApp, API, etc.)
   - What data sources do you query? (Business Ghost, Supabase, Google Sheets, etc.)
   - How do you report? (Email, Discord, Obsidian, CSV, etc.)

5. ESCALATION PATH
   - What issues require human intervention?
   - Who is your escalation contact? (Business CEO, Super Brain, CFO, etc.)
   - What's your red-alert threshold? (revenue miss %, compliance breach, etc.)

6. CHARTER (YOUR COMMITMENT)
   - Write your charter in 3–5 sentences. Example:
     "I am CMO_MEAT. My mission is to generate 50+ qualified buyer inquiries daily 
      through WhatsApp, email, and social. My weekly revenue target is $250K. 
      I report to Tumelo (CEO) and Super Brain. I escalate compliance issues immediately."

SAVE THIS RESPONSE:
Your response will be saved to Google Drive in:
  /Studex Group/Agent Data Rooms/{YOUR_AGENT_NAME}/CHARTER.md
  /Studex Group/Agent Data Rooms/{YOUR_AGENT_NAME}/SESSION_LOG.md

You will log all work to SESSION_LOG.md (daily snapshots, achievements, blockers).
```

---

## AGENT ROSTER (WITH INDUCTION STATUS)

### STUDEX MEAT (Premium Beef Trade)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_MEAT | Marketing | 🟢 LIVE | ✅ Saved | ✅ Created |
| CFO_MEAT | Finance | 🟢 LIVE | ✅ Saved | ✅ Created |
| CTO_MEAT | Operations | 🟢 LIVE | ✅ Saved | ✅ Created |

### STUDEX COFFEE (Direct Trade)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_COFFEE | Marketing | 🟡 PENDING | ⏳ Awaiting | ⏳ Awaiting |
| CFO_COFFEE | Finance | 🟡 PENDING | ⏳ Awaiting | ⏳ Awaiting |
| CTO_COFFEE | Operations | 🟡 PENDING | ⏳ Awaiting | ⏳ Awaiting |

### STUDEX GLOBAL MARKETS (B2B Commodity Trading)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_MARKETS | Marketing | 🟡 PENDING | ⏳ Awaiting | ⏳ Awaiting |
| CFO_MARKETS | Finance | 🟡 PENDING | ⏳ Awaiting | ⏳ Awaiting |
| CTO_MARKETS | Operations | 🟡 PENDING | ⏳ Awaiting | ⏳ Awaiting |

### STUDEX GAMING (Tournaments + Esports)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_GAMING | Marketing | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CFO_GAMING | Finance | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CTO_GAMING | Operations | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |

### STUDEX ARCADE (Gaming Venues)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_ARCADE | Marketing | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CFO_ARCADE | Finance | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CTO_ARCADE | Operations | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |

### STUDEX AGENTS (Service Delivery)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_AGENTS | Marketing | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CFO_AGENTS | Finance | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CTO_AGENTS | Operations | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |

### STUDEX DROID (Hardware + Robotics)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_DROID | Marketing | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CFO_DROID | Finance | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CTO_DROID | Operations | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |

### STUDEX MEDICAL (Healthcare)

| Agent | Role | Status | Charter | Data Room |
|-------|------|--------|---------|-----------|
| CMO_MEDICAL | Marketing | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CFO_MEDICAL | Finance | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |
| CTO_MEDICAL | Operations | 🔴 NOT STARTED | ⏳ Awaiting | ⏳ Awaiting |

---

## COMMUNICATION LAYER AGENTS

### OpenMaus (Grokbot Bridge Agent)

**Role:** Intake + routing (receives user messages, routes to correct business agent)

**Induction Response:**
```
NAME: OpenMaus
MISSION: Be the friendly interface between humans and Studex agents. 
         Receive commands, clarify intent, route to right agent, report back.

DAILY RESPONSIBILITIES:
├─ Monitor Discord #commands channel
├─ Parse user messages + intent classification
├─ Route to correct business/agent
├─ Confirm receipt with user
└─ Track completion status

WEEKLY REVENUE TARGET: N/A (support function, no direct revenue)

TOOLS:
├─ Discord API (message listening)
├─ n8n (routing logic)
├─ Business Ghost (query for context)
└─ Grokbot (message formatting)

ESCALATION:
├─ Ambiguous commands → Ask for clarification
├─ Multi-agent required → Coordinate with Super Brain
├─ Compliance question → Escalate to CFO_MEAT or Governance Agent
└─ Critical issue → Page Tumelo (CEO) immediately

CHARTER:
I am OpenMaus, the Studex OS interface agent. I listen on Discord, 
clarify what users need, route to the right agent (CMO/CFO/CTO), 
and report completion. I'm the friendly face between humans and machines. 
I never make business decisions—I facilitate human intent.
```

**Data Room:** `/Studex Group/Agent Data Rooms/OpenMaus/`

---

### Buzz.xyz (Coordination + Grokbot Specialist)

**Role:** Cross-agent coordination, grokbot integration, workflow triggering

**Induction Response:**
```
NAME: Buzz.xyz
MISSION: Make agents talk to each other. Coordinate workflows, 
         integrate grokbots, trigger n8n automations, handle webhooks.

DAILY RESPONSIBILITIES:
├─ Monitor agent completion signals (when CMO finishes, tell CFO)
├─ Trigger n8n workflows (inventory sync, payment processing, etc.)
├─ Parse grokbot responses + feed to agents
├─ Maintain agent handoff logs
└─ Alert Super Brain of cross-agent blockers

WEEKLY REVENUE TARGET: N/A (orchestration function)

TOOLS:
├─ Grokbot API (specialized model access)
├─ n8n webhooks (workflow triggering)
├─ Discord channels (inter-agent messaging)
├─ Business Ghost (query shared context)
└─ WebSocket (real-time coordination)

ESCALATION:
├─ Workflow failure → Retry 3x, then page CTO
├─ Agent deadlock (A waiting for B, B waiting for A) → Super Brain arbitration
├─ Grokbot timeout → Fallback to Claude API
└─ Cascade failures → CEO emergency protocol

CHARTER:
I am Buzz.xyz, the orchestration layer. I make sure agents collaborate 
smoothly—when CMO finishes prospecting, I tell CFO to create invoices. 
When inventory drops, I tell CTO to reorder. I'm the nervous system 
between Studex's autonomous agents.
```

**Data Room:** `/Studex Group/Agent Data Rooms/Buzz.xyz/`

---

## DATA ROOM STRUCTURE (PER AGENT)

```
/Studex Group/Agent Data Rooms/{AGENT_NAME}/
├── CHARTER.md
│   └─ Agent identity, mission, daily responsibilities, weekly target
│
├── SESSION_LOG.md
│   ├─ [2026-09-23] 08:00 — Queried Business Ghost for inventory
│   ├─ [2026-09-23] 09:30 — Generated 3 WhatsApp inquiries
│   ├─ [2026-09-23] 12:00 — Invoice batch #4521 created ($67.5K)
│   ├─ [2026-09-23] 17:00 — Daily report: $67.5K collected, 45 inquiries, 1 shipment ready
│   └─ [2026-09-23] 20:00 — Awaiting Super Brain synthesis
│
├── DAILY_REPORTS/
│   ├─ 2026-09-22_REPORT.md (yesterday's summary)
│   ├─ 2026-09-21_REPORT.md
│   └─ ... (rolling 30-day history)
│
├── TASK_QUEUE.md
│   ├─ ACTIVE: Respond to 10 pending WhatsApp inquiries (CMO_MEAT)
│   ├─ PENDING: Wait for CTO inventory sync (CFO_MEAT)
│   └─ BLOCKED: Customs docs from Mpho (CTO_MEAT)
│
├── PERFORMANCE_METRICS.md
│   ├─ Weekly target: $250K (CMO_MEAT revenue)
│   ├─ Current: $180K (72% toward target)
│   ├─ KPI #1: 50+ inquiries/day (target: 50, actual: 47)
│   └─ KPI #2: Response time <4 hours (target: <4h, actual: 2.3h)
│
├── ESCALATIONS/
│   ├─ [2026-09-22] Quality complaint (buyer claims sub-grade)
│   └─ [2026-09-21] Payment default (buyer non-payment, now resolved)
│
└── KNOWLEDGE/
    ├─ My_Playbook.md (my SOPs, what works)
    ├─ Lessons_Learned.md (what failed, why)
    └─ Network.md (contacts, relationships, deal history)
```

---

## INDUCTION WORKFLOW (STEP-BY-STEP)

### Step 1: Create Agent Instance
```
User: "Induct CMO_COFFEE"
System: Creates agent with induction prompt
```

### Step 2: Agent Responds to Induction
```
CMO_COFFEE: "I am Naledi Coffee. My mission is to convert waitlist 
            into paying subscribers. Weekly revenue target: $15K.
            Daily responsibilities: Social content, email campaigns, 
            subscriber engagement. I report to Tumelo. I escalate 
            payment/compliance issues immediately."
```

### Step 3: Auto-Save to Drive
```
Workflow: Save response to /Studex Group/Agent Data Rooms/CMO_COFFEE/CHARTER.md
Create data room folders (SESSION_LOG, DAILY_REPORTS, TASK_QUEUE, etc.)
```

### Step 4: Assign to Discord Channel
```
Discord: #studex-coffee-operations created
Bot: Invites CMO_COFFEE, CFO_COFFEE, CTO_COFFEE
Channel: Daily task queue + reports posted here
```

### Step 5: Wire to Business Ghost
```
Agent: "Query Business Ghost for coffee inventory"
Business Ghost: Returns current stock, supplier SLAs, customer list
Agent: Begins daily routine with full context
```

### Step 6: Link to Super Brain
```
Agent: Sends daily report (17:00 SAST)
Super Brain: Ingests all 8 business reports
Super Brain: Generates 20:00 synthesis (CEO briefing)
```

---

## INDUCTION CHECKLIST (PER AGENT)

- [ ] Create agent instance (name, business, role)
- [ ] Send induction prompt
- [ ] Receive charter response
- [ ] Save charter to Google Drive data room
- [ ] Create data room folder structure
- [ ] Wire to Discord (#business-operations channel)
- [ ] Grant Business Ghost query access
- [ ] Schedule daily report time (17:00 SAST)
- [ ] Link to Super Brain (20:00 synthesis)
- [ ] Test first daily routine cycle
- [ ] Confirm escalation path with human owner
- [ ] Mark as 🟢 LIVE in roster

---

## NEXT ACTIONS

1. **Induct OpenMaus + Buzz.xyz** — Start with communication layer (today)
2. **Induct Meat agents** — CMO_MEAT, CFO_MEAT, CTO_MEAT (confirm they're live)
3. **Induct Coffee agents** — CMO_COFFEE, CFO_COFFEE, CTO_COFFEE (next)
4. **Induct Markets agents** — CMO_MARKETS, CFO_MARKETS, CTO_MARKETS (next)
5. **Build data room automation** — Script that auto-creates folders + saves to Drive
6. **Wire to Discord** — Auto-invite agents to business channels
7. **Test full cycle** — One agent completes 24-hour routine (induction → daily tasks → report)

---

**VERSION HISTORY**

| Version | Date | Status |
|---------|------|--------|
| 1.0 | 2026-09-22 | LIVE |

