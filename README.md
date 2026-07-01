# TrendAI Endpoint Security — Hands-on Training (3 Hours)

> A **3-hour, dashboard-driven** training for **customers and partners** using Trend Vision One – Endpoint Security with AI (Trend Companion).
>
> This is a **show-me** course: every topic tells you **exactly where to click** in the console and **how to do it live**.

> ℹ️ **Note:** Menu names/paths follow the current Trend Vision One console. If your tenant differs slightly, use the global **Search** (top bar) to jump to any app by name.

---

## ⏱️ Agenda (180 minutes)

Click any topic to jump to it.

| # | Topic | Time | Where in Console |
|---|-------|------|------------------|
| 0 | [Getting Started & Login](#0-getting-started--login) | 10 min | `sign-in` |
| 1 | [Console Tour & Dashboard](#1-console-tour--dashboard) | 15 min | `Dashboard` |
| 2 | [Endpoint Inventory & Agent Deployment](#2-endpoint-inventory--agent-deployment) | 25 min | `Endpoint Security ▸ Endpoint Inventory` |
| 3 | [Endpoint Policies & Protection](#3-endpoint-policies--protection) | 30 min | `Endpoint Security ▸ Endpoint Security Policies` |
| 4 | [Detections & Workbench Investigation](#4-detections--workbench-investigation) | 30 min | `XDR Threat Investigation ▸ Workbench` |
| 5 | [Response Actions](#5-response-actions) | 20 min | `Workbench ▸ Response` / `Response Management` |
| 6 | [Threat Hunting with Search](#6-threat-hunting-with-search) | 20 min | `XDR Threat Investigation ▸ Search` |
| 7 | [AI-Powered Investigation (Trend Companion)](#7-ai-powered-investigation-trend-companion) | 15 min | `Companion (sparkle icon)` |
| 8 | [Reports & Wrap-up](#8-reports--wrap-up) | 15 min | `Reports` |

**Total: ~3 hours** · Format: live demo + follow-along in your own tenant.

---

## 🎯 Learning Outcomes

By the end of this session, you will be able to:
1. Navigate the Trend Vision One console and read the Dashboard.
2. Check endpoint status and deploy an agent from the console.
3. Create and apply an Endpoint Security policy.
4. Investigate a detection in the Workbench (Root Cause Analysis).
5. Take response actions (Isolate, Terminate, Collect File).
6. Run a threat-hunting query in Search.
7. Use Trend Companion (AI) to summarize and speed up investigation.
8. Generate a report.

---

## ✅ Before You Start (Prerequisites)

- A **Trend Vision One** account with Endpoint Security enabled (trial/sandbox is fine).
- Role with permission to view Endpoint Security, Workbench, and Search.
- At least **one managed endpoint** (a test VM) for the live demo.
- A supported browser and internet access.

---

## 0. Getting Started & Login

**Goal:** Sign in and understand the top-level navigation.

**How to access:**
1. Open **https://signin.v1.trendmicro.com** and sign in.
2. Note the **left-hand navigation menu** (all apps live here).
3. Note the **top bar**: global **Search**, **Companion** (sparkle icon), alerts, and account menu.

**Try it:**
- Use the top **Search** box → type `Endpoint Inventory` → press Enter to jump directly to an app. This is the fastest way to reach any screen in this course.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 1. Console Tour & Dashboard

**Goal:** Read your security posture at a glance.

**How to access:** Left menu ▸ **Dashboard**

**Show these on the dashboard:**
- **Risk / Operations widgets** — overall exposure and detections over time.
- **Endpoint status** — online/offline, protected/unprotected counts.
- Click **⋯ (top-right of a widget) ▸ Edit** to add/remove widgets.
- Use the **date range** selector (top-right) to change the reporting window.

**Try it:**
- Click any number on a widget (e.g., a detection count) to **drill down** into the underlying list.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 2. Endpoint Inventory & Agent Deployment

**Goal:** See all endpoints and deploy protection to a new one.

**How to access:** Left menu ▸ **Endpoint Security** ▸ **Endpoint Inventory**

**Show the inventory:**
- Columns: **Endpoint name, OS, Agent status, Last connected, Policy, Risk**.
- Use the **filter/search bar** to find a specific host.
- Click an endpoint name to open its **detail panel** (components, versions, activity).

**Deploy an agent (live):**
1. On **Endpoint Inventory**, click **Agent Installer** (top-right).
2. Choose OS (**Windows / macOS / Linux**) and download the installer **or** copy the deployment script.
3. Run it on the test VM.
4. Return to **Endpoint Inventory** → confirm the endpoint appears as **Managed / Online**.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 3. Endpoint Policies & Protection

**Goal:** Create a policy and turn on the right protection modules.

**How to access:** Left menu ▸ **Endpoint Security** ▸ **Endpoint Security Policies**

**Create a policy (live):**
1. Click **Add** (or **Create Policy**).
2. Name it (e.g., `Workstation-Standard`) and set the **target group/endpoints**.
3. Enable the key protection modules:
   - **Anti-Malware / Predictive Machine Learning**
   - **Behavior Monitoring / Anti-Ransomware**
   - **Web Reputation**
   - **Device Control** and **Firewall** (as needed)
   - **Vulnerability Protection** (virtual patching)
4. Click **Save** → the policy deploys to targeted endpoints.

**Verify:**
- Go back to **Endpoint Inventory** → open the endpoint → confirm the **assigned policy** name and that modules show **Enabled**.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 4. Detections & Workbench Investigation

**Goal:** Investigate an alert end to end.

**How to access:** Left menu ▸ **XDR Threat Investigation** ▸ **Workbench**

**Generate a safe test detection (optional):**
- On the test VM, create an **EICAR** test file, or run a benign flagged test script, to trigger a detection.

**Investigate a Workbench alert:**
1. Open **Workbench** → click an alert to open the **alert detail**.
2. Review the **Highlights / summary** and the **severity / risk score**.
3. Open the **Execution Profile / Root Cause Analysis (RCA)** graph — trace the process chain from the initial action to impact.
4. Check the mapped **MITRE ATT&CK** techniques.
5. Expand **impacted assets/users** to see the blast radius.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 5. Response Actions

**Goal:** Contain and remediate a threat from the console.

**How to access:**
- From an alert: **Workbench ▸ (open alert) ▸ Response** (per-object action menu), or
- Left menu ▸ **Response Management** (to track/queue tasks)

**Common actions to demo:**
- **Isolate Endpoint** — cut off network access while keeping it manageable.
- **Terminate Process** — kill a malicious process.
- **Collect File** — retrieve a sample for analysis.
- **Add to Block List / Suspicious Objects** — block a hash/URL/IP everywhere.
- **Remote Shell** (if enabled) — run investigation commands.

**Track & undo:**
- Open **Response Management** to see task **status** (pending/succeeded/failed).
- Use **Restore/Un-isolate** on the endpoint once the incident is resolved.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 6. Threat Hunting with Search

**Goal:** Proactively look for suspicious activity across endpoints.

**How to access:** Left menu ▸ **XDR Threat Investigation** ▸ **Search**

**Run a hunt (live):**
1. Select the **data source** (e.g., Endpoint Activity Data).
2. Enter a query using field filters, for example:
   - Suspicious PowerShell: `processCmd:*EncodedCommand*`
   - LOLBin usage: `processName:(mshta.exe OR wscript.exe OR rundll32.exe)`
3. Adjust the **time range** and run the search.
4. Click a result row to pivot into details, or **Save** the query as a **Watchlist / Custom Filter** for reuse.

> Tip: You can also start from **Workbench**, right-click an entity (hash, IP, host) and choose **Search** to pivot instantly.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 7. AI-Powered Investigation (Trend Companion)

**Goal:** Use AI to explain, summarize, and accelerate response.

**How to access:** **Companion** — the **sparkle icon** in the top bar, or the **Companion** panel inside a Workbench alert.

**Demo these AI actions:**
- **Summarize this alert** — get a plain-language summary of what happened.
- **Explain this script/command** — decode an obfuscated PowerShell command.
- **Recommend next steps** — get suggested response actions.
- **Ask in natural language** — e.g., "What endpoints did this threat touch?"

**Good practice to mention:**
- Always **validate AI output** against the raw evidence (RCA, Search).
- Be mindful of **what data** you paste into prompts.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 8. Reports & Wrap-up

**Goal:** Communicate results to stakeholders.

**How to access:** Left menu ▸ **Reports**

**Show it:**
1. Click **Add / Generate Report** (or use a template).
2. Select content (detections, endpoint status, risk) and the **time range**.
3. Generate → **download / schedule** the report.

**Wrap-up recap (5 min):**
- Dashboard → Inventory → Policy → Workbench → Response → Search → Companion → Reports.
- **Q&A** and next steps for your environment.

[⬆ Back to Agenda](#-agenda-180-minutes)

---

## 🧭 Quick Navigation Cheat Sheet

| Task | Path |
|------|------|
| See overall posture | `Dashboard` |
| Find/deploy endpoints | `Endpoint Security ▸ Endpoint Inventory` |
| Configure protection | `Endpoint Security ▸ Endpoint Security Policies` |
| Investigate alerts | `XDR Threat Investigation ▸ Workbench` |
| Contain a threat | `Workbench ▸ Response` / `Response Management` |
| Hunt for threats | `XDR Threat Investigation ▸ Search` |
| Ask the AI | `Companion (sparkle icon)` |
| Build a report | `Reports` |

---

## 📖 References
- Trend Vision One Online Help / Documentation
- MITRE ATT&CK — https://attack.mitre.org

---

_Maintained for Trend Micro customer & partner enablement._
