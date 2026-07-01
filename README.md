# TrendAI Endpoint Security — Hands-on Training

A dashboard-driven training for **customers and partners** using Trend Vision One – Endpoint Security with AI (Trend Companion).

This is a **show-me** course. Every topic tells you **where to click** and **how to do it live** in the console.

> Menu names follow the current Trend Vision One console. If your tenant differs, use the global **Search** in the top bar to jump to any app by name. Path notation: `App ▸ Menu ▸ Sub-menu`.

---

## Contents

**Get Started**
- [1. Sign In](#1-sign-in)
- [2. Console Navigation](#2-console-navigation)
- [3. Dashboard](#3-dashboard)
- [4. Operations Dashboard](#4-operations-dashboard)

**Manage Endpoints**
- [5. Endpoint Inventory](#5-endpoint-inventory)
- [6. Agent Deployment](#6-agent-deployment)
- [7. Endpoint Groups & Tags](#7-endpoint-groups--tags)
- [8. Endpoint Security Policies](#8-endpoint-security-policies)
- [9. Protection Modules](#9-protection-modules)
- [10. Agent Settings & Updates](#10-agent-settings--updates)

**Detect & Respond**
- [11. Workbench (Alerts)](#11-workbench-alerts)
- [12. Root Cause Analysis](#12-root-cause-analysis)
- [13. Observed Attack Techniques](#13-observed-attack-techniques)
- [14. Response Actions](#14-response-actions)
- [15. Response Management](#15-response-management)

**Hunt & Intelligence**
- [16. Search (Threat Hunting)](#16-search-threat-hunting)
- [17. Custom Detections & Watchlists](#17-custom-detections--watchlists)
- [18. Threat Intelligence](#18-threat-intelligence)
- [19. Suspicious Objects & Exceptions](#19-suspicious-objects--exceptions)
- [20. Sandbox Analysis](#20-sandbox-analysis)

**Manage Risk**
- [21. Cyber Risk Exposure Management](#21-cyber-risk-exposure-management)
- [22. Vulnerabilities](#22-vulnerabilities)
- [23. Security Configuration](#23-security-configuration)

**AI**
- [24. Trend Companion](#24-trend-companion)

**Report & Administer**
- [25. Reports](#25-reports)
- [26. Notifications](#26-notifications)
- [27. Audit Logs](#27-audit-logs)
- [28. User Accounts & Roles](#28-user-accounts--roles)
- [29. Service Gateway & Connectors](#29-service-gateway--connectors)

[Quick Navigation Cheat Sheet](#quick-navigation-cheat-sheet)

---

## Learning Outcomes

By the end of this session, you will be able to:

- Navigate the console and read the dashboards.
- Manage endpoints: inventory, deployment, groups, policies, and protection modules.
- Investigate detections in the Workbench and read a Root Cause Analysis.
- Take and track response actions.
- Hunt for threats with Search and apply threat intelligence.
- Review and reduce risk with Cyber Risk Exposure Management.
- Use Trend Companion (AI) to speed up investigation and response.
- Generate reports and administer users, notifications, and connectors.

---

## Prerequisites

- A **Trend Vision One** account with Endpoint Security enabled (trial/sandbox is fine).
- A role that can view Endpoint Security, Workbench, and Search.
- At least **one managed endpoint** (a test VM) for the live demo.
- A supported browser and internet access.

---

# Get Started

## 1. Sign In

Access the console and understand what you are looking at.

**Path:** `https://signin.v1.trendmicro.com`

- Sign in with your account (SSO or username/password).
- Confirm your **region/data center** is correct (shown after login).
- Note the **top bar**: global Search, Companion (sparkle icon), notifications, help, and account menu.

[Back to top](#contents)

## 2. Console Navigation

Learn to move around quickly.

**Path:** Left navigation menu (collapsible)

- Apps are grouped in the **left menu**; click the ☰ icon to expand/collapse.
- Use the top **Search** box to jump straight to any app (e.g., type `Endpoint Inventory`).
- **Pin** frequently used apps for one-click access.
- Breadcrumbs at the top of each page show where you are.

[Back to top](#contents)

## 3. Dashboard

Read your security posture at a glance.

**Path:** `Dashboard`

- Review the default widgets: detections over time, endpoint status, top risks.
- Change the **date range** (top-right) to adjust the reporting window.
- Click **⋯ ▸ Edit** on a widget to configure it; use **Add Widget** to build a custom view.
- Create additional **tabs** for different audiences (e.g., SOC vs. management).
- Click any metric to **drill down** into the underlying records.

[Back to top](#contents)

## 4. Operations Dashboard

See day-to-day security operations health.

**Path:** `Operations Dashboard`

- Review detection and response **workload** (open vs. resolved alerts).
- Track **mean time** metrics and analyst activity trends.
- Identify backlogs and coverage gaps to prioritize work.

[Back to top](#contents)

---

# Manage Endpoints

## 5. Endpoint Inventory

The single place to view and act on every endpoint.

**Path:** `Endpoint Security ▸ Endpoint Inventory`

- Review columns: **name, OS, agent status, last connected, policy, risk**.
- Use **filters** and the search bar to find hosts (by OS, status, tag, group).
- Click an endpoint to open its **detail panel**: installed components, versions, activity, and assigned policy.
- Select one or more endpoints to run **actions** (move group, assign policy, run response tasks, uninstall).
- Export the list with **Export**.

[Back to top](#contents)

## 6. Agent Deployment

Install protection on a new endpoint.

**Path:** `Endpoint Security ▸ Endpoint Inventory ▸ Agent Installer`

1. Click **Agent Installer** (top-right of the inventory).
2. Choose the OS: **Windows / macOS / Linux**.
3. Download the installer package **or** copy the deployment script/command.
4. Deploy via your preferred method: manual, GPO, SCCM/Intune, script, or golden image.
5. Run it on the target machine.
6. Return to **Endpoint Inventory** and confirm the host shows **Managed / Online**.

**Tip:** For large rollouts, use the deployment script with your existing software-distribution tooling.

[Back to top](#contents)

## 7. Endpoint Groups & Tags

Organize endpoints so policies and searches target the right machines.

**Path:** `Endpoint Security ▸ Endpoint Inventory` (grouping/tag actions)

- Create **groups** (e.g., Servers, Workstations, Executives) to structure policy assignment.
- Apply **tags** for flexible filtering (e.g., `finance`, `pilot`, `kiosk`).
- Move endpoints between groups; policies can follow group membership.
- Use groups/tags as filters in **Search** and **Reports**.

[Back to top](#contents)

## 8. Endpoint Security Policies

Define what protection applies to which endpoints.

**Path:** `Endpoint Security ▸ Endpoint Security Policies`

1. Click **Add / Create Policy**.
2. Name it (e.g., `Workstation-Standard`) and set the **target** group/endpoints.
3. Configure the protection modules (see next section).
4. **Save** to deploy the policy to targeted endpoints.
5. Review **policy priority/inheritance** when multiple policies could apply.

**Verify:** Open an endpoint in **Endpoint Inventory** and confirm the assigned policy and that modules show **Enabled**.

[Back to top](#contents)

## 9. Protection Modules

The individual protections you enable inside a policy.

**Path:** `Endpoint Security ▸ Endpoint Security Policies ▸ (open a policy)`

- **Anti-Malware / Predictive Machine Learning** — signature + AI file detection.
- **Behavior Monitoring / Anti-Ransomware** — blocks malicious behavior and encryption attempts.
- **Web Reputation** — blocks access to malicious URLs.
- **Firewall** — host-based network rules.
- **Device Control** — restrict USB and peripheral use.
- **Application Control** — allow/deny application execution.
- **Vulnerability Protection (Virtual Patching)** — shields unpatched vulnerabilities.
- **Data Loss Prevention (DLP)** — controls sensitive data movement.

**Tip:** Start in a monitoring/log-only mode where available, review results, then enforce.

[Back to top](#contents)

## 10. Agent Settings & Updates

Keep agents healthy and current.

**Path:** `Endpoint Security ▸ Endpoint Security Policies` (agent/update settings) and `Endpoint Inventory` (per-agent)

- Configure **update source and schedule** for components and patterns.
- Set **self-protection** and uninstall protection options.
- Check **agent version** and component status per endpoint.
- Trigger **Update Now** or component rollback where supported.

[Back to top](#contents)

---

# Detect & Respond

## 11. Workbench (Alerts)

The primary place to triage and investigate detections.

**Path:** `XDR Threat Investigation ▸ Workbench`

- Review the **alert list** sorted by severity/risk score.
- Open an alert to see the **summary/highlights**, impacted assets, and mapped **MITRE ATT&CK** techniques.
- Set alert **status** (new, in progress, closed) and **assign** it to an analyst.
- Filter by severity, status, detection model, or asset.

**Optional demo:** Trigger a safe detection with an **EICAR** test file on the test VM.

[Back to top](#contents)

## 12. Root Cause Analysis

Understand exactly what happened, step by step.

**Path:** `XDR Threat Investigation ▸ Workbench ▸ (open alert) ▸ Execution Profile / Root Cause Analysis`

- Read the **process chain** graph from initial access to impact.
- Inspect each node: process, command line, file, registry, and network activity.
- Identify the **root cause** and the **blast radius** (affected users/hosts).
- Pivot from any entity (hash, IP, host) into **Search** for related activity.

[Back to top](#contents)

## 13. Observed Attack Techniques

See lower-level suspicious behaviors that may not yet be full alerts.

**Path:** `XDR Threat Investigation ▸ Observed Attack Techniques`

- Review individual techniques observed across endpoints.
- Filter by **risk level** and MITRE tactic/technique.
- Use these signals to hunt early or tune detections.

[Back to top](#contents)

## 14. Response Actions

Contain and remediate a threat directly from the console.

**Path:** `XDR Threat Investigation ▸ Workbench ▸ (open alert) ▸ Response`

- **Isolate Endpoint** — cut network access while keeping it manageable.
- **Terminate Process** — stop a malicious process.
- **Collect File** — retrieve a sample for analysis.
- **Delete / Quarantine** — remove a malicious file.
- **Add to Block List** — block a hash/URL/IP across the environment.
- **Remote Shell** (if enabled) — run investigation commands on the host.
- **Restore / Un-isolate** — return the endpoint to normal after remediation.

[Back to top](#contents)

## 15. Response Management

Queue, track, and audit every response task.

**Path:** `Workflow and Automation ▸ Response Management`

- View task **status** (pending, running, succeeded, failed) and who initiated it.
- Re-run or cancel tasks; review command output for **Remote Shell**.
- Manage **Custom Scripts** for repeatable response actions.
- Explore **Security Playbooks** to automate responses based on conditions.

[Back to top](#contents)

---

# Hunt & Intelligence

## 16. Search (Threat Hunting)

Proactively look for suspicious activity across all endpoints.

**Path:** `XDR Threat Investigation ▸ Search`

1. Select a **data source** (e.g., Endpoint Activity Data).
2. Build a query with field filters, for example:
   - Encoded PowerShell: `processCmd:*EncodedCommand*`
   - LOLBins: `processName:(mshta.exe OR wscript.exe OR rundll32.exe)`
3. Adjust the **time range** and run the search.
4. Click a result to pivot into detail, or **Save** the query for reuse.

**Tip:** From Workbench, right-click an entity and choose **Search** to pivot instantly.

[Back to top](#contents)

## 17. Custom Detections & Watchlists

Turn a good hunt into an ongoing detection.

**Path:** `XDR Threat Investigation ▸ Search ▸ Save as` and detection/watchlist management

- Save a query as a **Watchlist / Custom Filter** for repeated use.
- Create **custom detection models/rules** to alert automatically on a pattern.
- Review and tune saved queries to reduce noise.

[Back to top](#contents)

## 18. Threat Intelligence

Apply external and Trend intelligence to your environment.

**Path:** `Threat Intelligence ▸ Intelligence Reports`

- Read **Intelligence Reports** relevant to your industry/region.
- Run **Sweeping** to retroactively search your environment for report IOCs.
- Import indicators (**IOC / STIX**) to hunt or block.

[Back to top](#contents)

## 19. Suspicious Objects & Exceptions

Manage what to block and what to allow.

**Path:** `Threat Intelligence ▸ Suspicious Object Management`

- Add hashes, URLs, IPs, or domains to the **Suspicious Object List** (block).
- Maintain an **exception/allow list** to prevent false positives.
- Set expiration and scope for entries.

[Back to top](#contents)

## 20. Sandbox Analysis

Detonate suspicious files/URLs safely.

**Path:** `Threat Intelligence ▸ Sandbox Analysis`

- Submit a file or URL for **sandbox detonation**.
- Review the behavior report and verdict.
- Promote confirmed indicators to the **Suspicious Object List**.

[Back to top](#contents)

---

# Manage Risk

## 21. Cyber Risk Exposure Management

Measure and reduce your organization's risk.

**Path:** `Cyber Risk Exposure Management` (Risk Overview / Attack Surface)

- Review the **Risk Index / Risk Score** and its contributing factors.
- Explore **attack surface**: accounts, devices, applications, and internet-facing assets.
- Drill into high-risk items and follow recommended mitigations.
- Track the score over time to show improvement.

[Back to top](#contents)

## 22. Vulnerabilities

Find and prioritize what to patch.

**Path:** `Cyber Risk Exposure Management ▸ Vulnerabilities` (and endpoint detail)

- Review detected **CVEs** across endpoints, ranked by exploitability/impact.
- Identify assets exposed to critical vulnerabilities.
- Pair with **Vulnerability Protection** (virtual patching) as a compensating control.

[Back to top](#contents)

## 23. Security Configuration

Fix weak settings that increase risk.

**Path:** `Cyber Risk Exposure Management ▸ Security Configuration`

- Review misconfigurations and posture gaps on endpoints.
- Follow remediation guidance for each finding.
- Re-check the score after remediation.

[Back to top](#contents)

---

# AI

## 24. Trend Companion

Use AI to explain, summarize, and accelerate response.

**Path:** **Companion** — the sparkle icon in the top bar, or the Companion panel inside a Workbench alert.

- **Summarize this alert** — plain-language explanation of what happened.
- **Explain this script/command** — decode obfuscated PowerShell or command lines.
- **Recommend next steps** — suggested response actions for the current alert.
- **Ask in natural language** — e.g., "Which endpoints did this threat touch?"

**Good practice:** Validate AI output against the raw evidence (RCA, Search), and be mindful of what data you enter into prompts.

[Back to top](#contents)

---

# Report & Administer

## 25. Reports

Communicate results to stakeholders.

**Path:** `Reports`

1. Click **Add / Generate Report** or start from a template.
2. Select content (detections, endpoint status, risk) and the **time range**.
3. Generate, then **download** or **schedule** recurring delivery.

[Back to top](#contents)

## 26. Notifications

Get alerted when it matters.

**Path:** `Administration ▸ Notifications` (or account ▸ Notifications)

- Configure **alert notifications** by severity or event type.
- Set delivery channels (email, webhook, integrations).
- Tune thresholds to avoid alert fatigue.

[Back to top](#contents)

## 27. Audit Logs

Know who did what in the console.

**Path:** `Administration ▸ Audit Logs`

- Review **admin and analyst actions** (logins, policy changes, response tasks).
- Filter by user, action type, and time range.
- Export for compliance evidence.

[Back to top](#contents)

## 28. User Accounts & Roles

Control access with least privilege.

**Path:** `Administration ▸ User Accounts` and `Administration ▸ Roles`

- Create **user accounts** and assign **roles**.
- Use **role-based access control (RBAC)** to scope permissions.
- For partners/MSPs, review **multi-tenant** access where applicable.

[Back to top](#contents)

## 29. Service Gateway & Connectors

Connect the platform to your environment.

**Path:** `Service Gateway Management` and `Point Product Connectors`

- Deploy/monitor a **Service Gateway** for on-prem connectivity and caching.
- Configure **product connectors** to bring in additional telemetry.
- Check connector **health/status**.

[Back to top](#contents)

---

## Quick Navigation Cheat Sheet

| Task | Path |
|------|------|
| Overall posture | `Dashboard` |
| Operations health | `Operations Dashboard` |
| View / act on endpoints | `Endpoint Security ▸ Endpoint Inventory` |
| Deploy an agent | `Endpoint Security ▸ Endpoint Inventory ▸ Agent Installer` |
| Configure protection | `Endpoint Security ▸ Endpoint Security Policies` |
| Investigate alerts | `XDR Threat Investigation ▸ Workbench` |
| Root cause analysis | `Workbench ▸ (alert) ▸ Execution Profile` |
| Observed techniques | `XDR Threat Investigation ▸ Observed Attack Techniques` |
| Contain a threat | `Workbench ▸ (alert) ▸ Response` |
| Track response tasks | `Workflow and Automation ▸ Response Management` |
| Hunt for threats | `XDR Threat Investigation ▸ Search` |
| Intelligence & sweeping | `Threat Intelligence ▸ Intelligence Reports` |
| Block / allow objects | `Threat Intelligence ▸ Suspicious Object Management` |
| Detonate a sample | `Threat Intelligence ▸ Sandbox Analysis` |
| Measure risk | `Cyber Risk Exposure Management` |
| Ask the AI | `Companion (sparkle icon)` |
| Build a report | `Reports` |
| Manage users | `Administration ▸ User Accounts / Roles` |
| Audit activity | `Administration ▸ Audit Logs` |

---

## References

- Trend Vision One Online Help / Documentation
- MITRE ATT&CK — https://attack.mitre.org

---

_Maintained for Trend Micro customer & partner enablement._
