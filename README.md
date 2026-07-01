# TrendAI Endpoint Security Training — Zero to Hero

> คอร์สเทรนนิ่งสำหรับ **ลูกค้า (Customers)** และ **พาร์ทเนอร์ (Partners)** ที่ใช้งาน Trend Vision One – Endpoint Security ร่วมกับความสามารถด้าน AI (Trend Companion / Trend Cybertron)
>
> ออกแบบให้เรียนได้ตั้งแต่ผู้ที่ไม่เคยใช้งานมาก่อน (Zero) จนถึงระดับผู้เชี่ยวชาญที่ดูแลระบบและตอบสนองภัยคุกคามได้เอง (Hero)

---

## 📌 ภาพรวมคอร์ส (Course Overview)

| หัวข้อ | รายละเอียด |
|--------|-----------|
| **ชื่อคอร์ส** | TrendAI Endpoint Security — Zero to Hero |
| **กลุ่มเป้าหมาย** | IT Admin, Security Analyst (SOC), Partner SE/Sales Engineer, MSP/MSSP Operator |
| **ระยะเวลารวม** | ~5 วัน (40 ชั่วโมง) หรือแบ่งเรียนแบบ modular ได้ |
| **รูปแบบ** | บรรยาย + Demo + Hands-on Lab + Workshop จำลองสถานการณ์ |
| **ภาษา** | ไทย (ศัพท์เทคนิคเป็นอังกฤษ) |
| **สิ่งที่ได้รับ** | Certificate of Completion + Lab Guide + Cheat Sheet |

### ผลลัพธ์การเรียนรู้ (Learning Outcomes)
เมื่อจบคอร์สผู้เรียนจะสามารถ:
1. เข้าใจสถาปัตยกรรมของ Trend Vision One และ Endpoint Security
2. ติดตั้ง (Deploy) และตั้งค่า Agent บน Windows / macOS / Linux / Server
3. สร้างและปรับ Policy ให้เหมาะกับองค์กร
4. ใช้ความสามารถ EDR/XDR ในการล่าภัยคุกคาม (Threat Hunting) และสืบสวน (Investigation)
5. ใช้ AI (Trend Companion) ช่วยวิเคราะห์และเร่งการตอบสนอง (Response)
6. ทำ Incident Response และ Automation (Workflow / Playbook)
7. อ่านรายงาน วัดผล และปรับแต่งเพื่อลด False Positive

---

## 🗺️ เส้นทางการเรียนรู้ (Learning Path)

```
LEVEL 0            LEVEL 1           LEVEL 2            LEVEL 3           LEVEL 4
Foundation   →    Deploy &     →    Detection &   →   Threat Hunt  →   Hero:
(Zero)            Configure         Response (EDR)     & AI Ops         Automation & Architect
```

| Level | ชื่อ | เหมาะกับใคร | Modules |
|-------|------|-------------|---------|
| **0** | Foundation | ทุกคน | M1–M2 |
| **1** | Deploy & Configure | IT Admin | M3–M5 |
| **2** | Detection & Response | Analyst มือใหม่ | M6–M8 |
| **3** | Threat Hunting & AI Ops | SOC Analyst | M9–M11 |
| **4** | Hero — Automation & Architect | Senior / Partner SE | M12–M14 |

---

## 📚 เนื้อหาแบบละเอียด (Curriculum)

### 🟢 LEVEL 0 — Foundation (Zero)

#### Module 1: Cybersecurity & Endpoint Threat Landscape 101
- ภัยคุกคามยุคใหม่: Ransomware, Fileless, Living-off-the-Land (LOLBins), Supply Chain
- MITRE ATT&CK Framework เบื้องต้น (Tactics → Techniques)
- Cyber Kill Chain และทำไม Endpoint ถึงเป็นด่านสำคัญ
- คำศัพท์พื้นฐาน: EPP vs EDR vs XDR vs MDR
- **Lab 0.1:** สำรวจ MITRE ATT&CK Navigator

#### Module 2: รู้จัก Trend Vision One & Endpoint Security
- แพลตฟอร์ม Trend Vision One คืออะไร (Unified Cybersecurity Platform)
- ตำแหน่งของ Endpoint Security ในแพลตฟอร์ม
- ภาพรวมความสามารถ AI: **Trend Companion** (GenAI assistant) และ **Trend Cybertron** (security AI model)
- Licensing, Credits และ Editions (Essentials / Advanced / Enterprise)
- ทัวร์หน้า Console: Dashboard, Workbench, Threat Intelligence, Endpoint Inventory
- **Lab 0.2:** เข้าใช้งาน Console และตั้งค่า user/role เบื้องต้น

---

### 🔵 LEVEL 1 — Deploy & Configure

#### Module 3: Architecture & Deployment Planning
- สถาปัตยกรรม: Cloud Console, Agent, Connector, Service Gateway
- ข้อกำหนดระบบ (System Requirements) และ Network/Firewall/Proxy
- รูปแบบการ Deploy: Direct, via Service Gateway, Air-gapped
- การวางแผน Rollout สำหรับองค์กรขนาดต่างๆ
- **Lab 1.1:** วางแผน deployment diagram

#### Module 4: Agent Installation & Onboarding
- ติดตั้ง Agent บน **Windows, macOS, Linux**
- Deployment methods: Manual, GPO, SCCM/Intune, Script, Image/Golden Master
- การ Migrate จาก Apex One / ผลิตภัณฑ์เดิม
- ตรวจสอบสถานะ Agent (Health, Connectivity, Version)
- **Lab 1.2:** ติดตั้ง Agent และยืนยันการเชื่อมต่อกับ Console

#### Module 5: Policy & Protection Configuration
- โครงสร้าง Policy และการจัดกลุ่ม Endpoint (Groups / Tags)
- ตั้งค่า Protection Modules:
  - Anti-Malware / Predictive Machine Learning
  - Behavior Monitoring / Anti-Ransomware
  - Web Reputation, Firewall, Device Control
  - Application Control, Vulnerability Protection (Virtual Patching)
  - Data Loss Prevention (DLP) เบื้องต้น
- Policy inheritance และ best practice การตั้งค่า
- **Lab 1.3:** สร้าง Policy สำหรับ workstation และ server พร้อมทดสอบ

---

### 🟡 LEVEL 2 — Detection & Response (EDR)

#### Module 6: เข้าใจ Detection & Telemetry
- Endpoint Sensor / Activity Monitoring ทำงานอย่างไร
- Detection types: Malware, Behavior, IOC, IOA
- Telemetry & Data Retention
- **Lab 2.1:** จำลองภัย (EICAR / test scripts) และดู detection

#### Module 7: Workbench & Alert Investigation
- ทำความเข้าใจ **Workbench Alerts** และ Risk Scoring
- อ่าน **Execution Profile / Root Cause Analysis (RCA)** chain
- Correlation ข้าม Endpoint / Email / Network (XDR)
- การจัดลำดับความสำคัญ (Triage) ของ Alert
- **Lab 2.2:** สืบสวน alert หนึ่งเคสตั้งแต่ต้นจนจบ

#### Module 8: Response Actions
- Response บน Endpoint: Isolate, Terminate Process, Collect File, Remote Shell
- Custom Scripts และ Response ระดับ Agent
- Add to Block/Allow List, Suspicious Object Management
- **Lab 2.3:** Isolate เครื่องที่ติดภัยและเก็บหลักฐาน

---

### 🟠 LEVEL 3 — Threat Hunting & AI Ops

#### Module 9: Threat Hunting with Search
- ภาษา Search / Query (Search App) และ operators
- สร้าง Custom Detection / Watchlist
- Hunting ตามสมมติฐาน (Hypothesis-driven) และตาม MITRE ATT&CK
- **Lab 3.1:** เขียน query ล่าพฤติกรรมน่าสงสัย เช่น LOLBins

#### Module 10: Threat Intelligence
- Threat Intelligence feeds และ Sweeping
- Suspicious Object List, IOC/STIX import
- Intelligence Reports และการนำไป apply กับ environment
- **Lab 3.2:** ทำ retro-sweep ด้วย IOC ที่ได้รับ

#### Module 11: AI-Powered Operations (Trend Companion / Cybertron) ⭐
- ใช้ **Trend Companion** สรุป Alert, อธิบาย script, และแนะนำ next step
- Natural-language query และ AI-assisted investigation
- AI-guided Root Cause และ recommended response
- แนวปฏิบัติที่ปลอดภัยเมื่อใช้ GenAI (data handling, ตรวจสอบผลลัพธ์)
- **Lab 3.3:** ใช้ Trend Companion วิเคราะห์เคสจริงและเปรียบเทียบกับการทำเอง

---

### 🔴 LEVEL 4 — Hero: Automation & Architect

#### Module 12: Automation, Playbooks & Integration
- Security Playbooks / Workflow Automation
- Automated Response (เงื่อนไข → action)
- Integration: SIEM, SOAR, ticketing (ServiceNow ฯลฯ), API & Webhook
- ภาพรวมการใช้ **API / Automation Center**
- **Lab 4.1:** สร้าง playbook auto-isolate เมื่อพบ risk สูง

#### Module 13: Attack Surface & Risk Management
- **Attack Surface Risk Management (ASRM):** Risk Index, Exposure, Compliance
- Vulnerability & Configuration risk บน endpoint
- CVE prioritization และ Virtual Patching strategy
- Reporting สำหรับผู้บริหาร (Executive Dashboard)
- **Lab 4.2:** ลด Risk Score ขององค์กรจำลอง

#### Module 14: Operations, Tuning & Best Practices
- การลด False Positive และ tuning policy/detection
- Health check, Agent troubleshooting, Log collection
- Multi-tenant / MSP management (สำหรับพาร์ทเนอร์)
- Operational runbook และ IR readiness
- **Capstone Workshop:** จำลอง Ransomware Incident เต็มรูปแบบ — Detect → Investigate (AI) → Respond → Report

---

## 🧪 Capstone: End-to-End Incident Simulation

ผู้เรียนจะได้รับสถานการณ์จำลองการโจมตี และต้องทำครบวงจร:
1. **Detect** – รับ alert จาก Workbench
2. **Investigate** – วิเคราะห์ RCA + ใช้ Trend Companion ช่วยสรุป
3. **Hunt** – หา endpoint อื่นที่ได้รับผลกระทบ
4. **Respond** – Isolate / Terminate / Remediate
5. **Automate** – สร้าง playbook ป้องกันซ้ำ
6. **Report** – สรุปเหตุการณ์ให้ผู้บริหาร

---

## 🎓 เกณฑ์การประเมินและใบรับรอง (Assessment & Certification)

| รายการ | สัดส่วน |
|--------|---------|
| Hands-on Labs | 40% |
| Capstone Workshop | 40% |
| Knowledge Check (Quiz ท้าย Module) | 20% |

- ผ่านเกณฑ์ ≥ 70% รับ **Certificate of Completion**
- แนะนำต่อยอดสู่ Trend Micro Certified Professional (official certification)

---

## ✅ สิ่งที่ต้องเตรียม (Prerequisites)

**ผู้เรียน:**
- ความรู้พื้นฐานด้าน IT / Networking (TCP/IP, DNS, AD)
- เข้าใจแนวคิด security เบื้องต้น (สำหรับ Level 2 ขึ้นไป)

**สภาพแวดล้อม Lab:**
- บัญชี Trend Vision One (trial/sandbox tenant)
- เครื่องทดสอบ Windows/Linux (VM) อย่างน้อย 2 เครื่อง
- สิทธิ์ admin สำหรับติดตั้ง Agent
- Browser ที่รองรับ + การเชื่อมต่ออินเทอร์เน็ต

---

## 🗂️ โครงสร้าง Repository (แนะนำ)

```
trendai-training-endpoint-security/
├── README.md                  # ภาพรวมคอร์ส (ไฟล์นี้)
├── modules/                   # เนื้อหาแต่ละ module
│   ├── 00-foundation/
│   ├── 01-deploy/
│   ├── 02-detection-response/
│   ├── 03-threat-hunting-ai/
│   └── 04-hero-automation/
├── labs/                      # Lab guides แบบ step-by-step
├── slides/                    # สไลด์ประกอบการบรรยาย
├── cheatsheets/               # Quick reference / query cheat sheet
└── assessments/               # Quiz และ capstone scenarios
```

---

## ⏱️ ตารางเรียนแนะนำ (5-Day Schedule)

| วัน | Level | Modules | โฟกัส |
|-----|-------|---------|-------|
| Day 1 | 0 | M1–M2 | พื้นฐาน + รู้จักแพลตฟอร์ม |
| Day 2 | 1 | M3–M5 | Deploy + Policy |
| Day 3 | 2 | M6–M8 | EDR Detection & Response |
| Day 4 | 3 | M9–M11 | Threat Hunting + AI |
| Day 5 | 4 | M12–M14 + Capstone | Automation + Workshop |

> สามารถแยกจัดเป็นคอร์สย่อย: **Admin Track (Day 1–2)** และ **Analyst Track (Day 3–5)** ได้

---

## 📖 แหล่งอ้างอิงเพิ่มเติม (References)

- Trend Vision One Online Help / Documentation
- Trend Micro Automation Center (API docs)
- MITRE ATT&CK — https://attack.mitre.org
- Trend Micro Education & Certification

---

## 🤝 การนำไปใช้

คอร์สนี้เป็น **template** ปรับแต่งได้ตามกลุ่มผู้เรียน:
- **ลูกค้า (Customer):** เน้น Level 0–3 (ใช้งานประจำวัน)
- **พาร์ทเนอร์ (Partner SE):** เพิ่ม Level 4 + Multi-tenant + Sales enablement

> หากต้องการเพิ่มเนื้อหาเชิงลึกในแต่ละ module (สไลด์ / lab guide ละเอียด) แจ้งได้เลยครับ

---

_Maintained for Trend Micro customer & partner enablement._
