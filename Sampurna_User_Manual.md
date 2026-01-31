<style>
:root{
  --primary:#ec4899;
  --secondary:#8b5cf6;
  --dark:#0f172a;
  --card:#111827;
  --text:#e5e7eb;
  --muted:#9ca3af;
  --good:#22c55e;
  --warn:#f59e0b;
  --bad:#ef4444;
  --stroke:rgba(255,255,255,0.12);
}
body{ background:linear-gradient(180deg,#020617,#0f172a); }
.hero{
  background:radial-gradient(circle at top,var(--secondary),var(--dark) 45%);
  padding:44px 40px;
  border-radius:24px;
  color:white;
  text-align:center;
  border:1px solid rgba(255,255,255,0.10);
  box-shadow:0 24px 60px rgba(0,0,0,0.45);
}
.hero h1{
  margin:10px 0 6px;
  font-size:44px;
  background:linear-gradient(90deg,var(--primary),var(--secondary));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}
.hero p{ margin:0; color:rgba(255,255,255,0.82); }
.card{
  background:linear-gradient(180deg,rgba(255,255,255,0.08),rgba(255,255,255,0.02));
  backdrop-filter:blur(14px);
  border-radius:20px;
  padding:28px 30px;
  margin:26px 0;
  border:1px solid rgba(255,255,255,0.10);
  box-shadow:0 20px 40px rgba(0,0,0,0.35);
}
.badge{
  display:inline-block;
  padding:7px 14px;
  border-radius:999px;
  background:linear-gradient(90deg,var(--primary),var(--secondary));
  color:white;
  font-weight:700;
  font-size:12px;
  letter-spacing:0.3px;
}
.kpi{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:14px;
  margin-top:14px;
}
.kpi .box{
  background:rgba(2,6,23,0.65);
  border:1px solid rgba(255,255,255,0.10);
  border-radius:16px;
  padding:14px 14px;
}
.kpi .box b{ display:block; margin-bottom:4px; }
.flow{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:14px;
}
.flow div{
  background:rgba(2,6,23,0.65);
  border-radius:16px;
  padding:16px 16px;
  border:1px solid rgba(255,255,255,0.10);
}
.callout{
  border:1px solid var(--stroke);
  background:rgba(2,6,23,0.55);
  padding:12px 14px;
  border-radius:14px;
  margin:12px 0 0;
  color:rgba(255,255,255,0.88);
}
.callout.good{ border-color: rgba(34,197,94,0.35); background: rgba(34,197,94,0.10); }
.callout.warn{ border-color: rgba(245,158,11,0.35); background: rgba(245,158,11,0.10); }
.callout.bad{ border-color: rgba(239,68,68,0.35); background: rgba(239,68,68,0.10); }
hr{ border:none; height:1px; background:rgba(255,255,255,0.10); margin:22px 0; }
code{ background:rgba(2,6,23,0.6); padding:2px 6px; border-radius:8px; }
.footer{
  text-align:center;
  color:rgba(255,255,255,0.65);
  margin:44px 0 10px;
  font-size:13px;
}
</style>

<div class="hero">
  <span class="badge">USER MANUAL</span>
  <h1>Sampurna HR Portal</h1>
  <p>Forms 1–4 • Dashboard • HR Operations</p>
  <div class="kpi">
    <div class="box"><b>Version</b>1.3</div>
    <div class="box"><b>Last Updated</b>31 Jan 2026</div>
    <div class="box"><b>Audience</b>Candidate • HR • Interviewers • Admin</div>
  </div>
</div>

---

<div class="card">

## How to use this manual

This is the **official operating guide** for the Sampurna HR Portal.

- Follow the journey strictly: **Form‑1 → Form‑2 → Form‑3 → Form‑4 → Dashboard**
- One **mobile number = one candidate lifecycle**
- Do not skip stages or override rules (unless you are **HR Admin**)
- For best view: open via your docs viewer (theme.html). VS Code preview will look simpler.

> **Golden Rule:** If it’s not written here, it’s not an approved process.

<div class="callout good"><b>Pro tip</b><br/>If something looks wrong, don’t guess—check the <b>Dashboard stage</b> first.</div>

</div>

---

<div class="card">

## User roles

| Role | Responsibility |
|---|---|
| 👤 **Candidate** | Submit Form‑1 application + upload documents |
| 🧾 **HR Screening** | Verify Form‑1, complete Form‑2 outcome |
| 🎯 **Interviewer** | Conduct interview, score in Form‑3 |
| ✅ **HR Ops** | Onboarding day formalities in Form‑4 |
| 📊 **HR Admin** | Dashboard oversight, exports, master data, corrections |

<div class="callout warn"><b>Rule</b><br/>Only HR Admin should change master data (Designation/Position/Question sets). Everyone else uses the dropdowns.</div>

</div>

---

<div class="card">

## End‑to‑end workflow

```mermaid
flowchart TB
  A["Candidate<br/>(Form‑1)<br/>Application + Docs"] --> B["Candidate Screening<br/>(Form‑2)<br/>Eligibility + Verification"]
  B --> C["Interview<br/>(Form‑3)<br/>Score + Remarks"]
  C --> D["Onboarding<br/>(Form‑4)<br/>Joining Day Details"]
  D --> E["HR Dashboard<br/>Tracking + Export + Ops"]
```

<div class="flow" style="margin-top:14px">
  <div>📱 <b>Form‑1</b><br/>Collect candidate info + resume</div>
  <div>🧾 <b>Form‑2</b><br/>Screening outcome (Eligible/Hold/Reject)</div>
  <div>🎯 <b>Form‑3</b><br/>Marks + recommendation</div>
  <div>✅ <b>Form‑4</b><br/>Joining day + final verification</div>
  <div>📊 <b>Dashboard</b><br/>Pipeline, filters, exports</div>
</div>

</div>

---

<div class="card">

## Form‑1 — Job Application (Candidate Entry)

### Purpose
Form‑1 creates the candidate record, generates an **Application ID**, and captures **documents** (Resume mandatory).

<div class="callout warn"><b>Entry gate</b><br/>If Form‑1 is incomplete, Form‑2/3/4 must not start.</div>

### Form‑1 flow
```mermaid
flowchart TD
  A["Start Form‑1"] --> B["Step‑1: Mobile Verification"]
  B --> C{"Eligible?"}
  C -- "No" --> D["Wait message<br/>Remaining days shown"]
  C -- "Yes" --> E["Step‑2: Basic Details"]
  E --> F["Step‑3: Extra Details + Documents"]
  F --> G["Submit"]
  G --> H["Success<br/>Application ID + FORM1_SUBMITTED"]
```

<hr/>

### Step‑1: Mobile verification
**Candidate does**
1. Enter a **10-digit mobile number**
2. Click **Verify**

**System checks**
- Must be numeric and exactly 10 digits
- Cooldown: **30 days** between applications (same mobile)

**Outcomes**
- **Eligible** → proceed
- **Wait** → remaining days displayed
- **Invalid** → fix number

<div class="callout bad"><b>Don’t do this</b><br/>Using a different mobile number to bypass the rule breaks tracking and audit.</div>

<hr/>

### Step‑2: Basic details (what candidate fills)

**A) Personal**
- First name (required)
- Middle name (optional)
- Last name (optional)
- Gender (required)
- Email (required)

**B) Reference**
- Reference Flag: Yes/No  
- If Yes → Referral Name (required)

**C) Language**
- Preferred language (Hindi/English/Bengali)
- Read / Write / Speak flags

**D) Job mapping**
- Designation (dropdown)
- Position (dropdown; depends on designation)

**E) Experience**
- Experience: Yes/No
- If Yes → Years + Months (system calculates total months)

**F) Address**
- Full address
- Pincode (auto fills State + District)

**G) Skills**
- Select skills from master list
- Add custom skills only if missing

**Validation rules**
- Email format must be valid
- If Reference = Yes → Referral name required
- Position cannot be blank
- Pincode must exist in master to auto-fill State/District

<div class="callout good"><b>Best practice</b><br/>Missing designation/position? Raise to HR Admin. Don’t “manage” it by free-typing.</div>

<hr/>

### Step‑3: Extra details + documents

**Computer skills**
- Excel skill: Yes/No → Level (Basic/Intermediate/Advanced)
- MS Office skill: Yes/No
- Basic computer skill: Yes/No
- Computer certificate available: Yes/No

**Operations/Field role rules (strict)**
If designation contains Field/Collection/Recovery/Operations:
- Candidate must have **Bike** OR be **Willing to buy**
- If Bike = Yes → Vehicle number required
- If Loan = Yes → Loan type + closure timeline required

<div class="callout warn"><b>Operations rule</b><br/>No bike + not willing to buy → cannot proceed for operational roles.</div>

**Documents**
| Document | Required | Notes |
|---|---:|---|
| Resume | ✅ Yes | readable + relevant |
| Certificates | Optional | max 5 files |
| Max size | — | 3 MB per file |

<div class="callout bad"><b>Upload failed?</b><br/>If file > 3MB: compress PDF or upload a smaller scan (JPG/PNG).</div>

<hr/>

### Form‑1 submission success
On submit:
- **Application ID** generated
- Stage set to **FORM1_SUBMITTED**
- Candidate sees confirmation + Application ID

</div>

---

<div class="card">

## Form‑2 — Candidate Screening (Additional Details)

### Purpose
HR validates candidate eligibility and decides whether the candidate moves to interview.

<div class="callout good"><b>Entry condition</b><br/>Start Form‑2 only after Form‑1 is submitted and documents are available.</div>

### HR screening checklist

**A) Identity & data quality**
- Mobile number matches record
- Name + Email present
- Address + Pincode valid

**B) Job mapping**
- Designation/Position align with requirement
- Operations roles: bike/loan validations checked

**C) Document verification**
- Resume exists and readable
- Certificates checked if provided

### Form‑2 outcome
| Outcome | Use when |
|---|---|
| **Eligible** ✅ | all checks pass |
| **Hold** ⏸️ | missing docs / needs clarification |
| **Rejected** ❌ | not suitable / fails mandatory rules |

<div class="callout warn"><b>Rule</b><br/>Never mark Eligible if resume is missing/unreadable.</div>

### What happens next
- **Eligible** → schedule interview → Form‑3
- **Hold** → follow up → re-check
- **Rejected** → process ends (kept for audit)

</div>

---

<div class="card">

## Form‑3 — HR Interview (Evaluation & Scoring)

### Purpose
Interview panel evaluates candidate using question sets and records scores + recommendation.

### Form‑3 flow
```mermaid
flowchart TD
  A["Open Candidate"] --> B["Select Question Set\n(Set No)"]
  B --> C["Ask Questions + Score"]
  C --> D["Add Remarks"]
  D --> E["Final Recommendation"]
  E --> F["Submit Evaluation"]
```

### Interviewer instructions

**Before interview**
- Confirm Form‑2 outcome = **Eligible**
- Pick correct Question Set for role

**During interview**
- Ask questions in order (recommended)
- Score per question
- Add remarks (strengths, risks, follow-ups)

**Final recommendation**
- **Selected**
- **Hold**
- **Rejected**

<div class="callout good"><b>Best practice</b><br/>If scoring varies across interviewers, HR Admin should standardize scoring guidance and question sets.</div>

</div>

---

<div class="card">

## Form‑4 — Onboarding Day

### Purpose
Complete joining day details and final document verification for selected candidates.

<div class="callout warn"><b>Rule</b><br/>Do not complete Form‑4 unless Form‑3 recommendation is “Selected”.</div>

### Form‑4 steps
1. Confirm selection result and role mapping
2. Verify final documents (ID proofs, education, address, etc.)
3. Capture joining details:
   - Joining date
   - Department / reporting manager
   - Bank/payout details (as applicable)
4. Mark onboarding completed

### Outcome
- Candidate stage becomes **ONBOARDED**
- Candidate appears in onboarding/completed dashboard filters

</div>

---

<div class="card">

## HR Dashboard — Tracking, Filters, Exports

### Purpose
Central view of pipeline + reporting + operational oversight.

### What the dashboard provides
- Pipeline view by stage
- Search: Mobile / Name / Application ID
- Filters: date range, designation, stage, interview outcome
- Export to Excel
- Admin corrections (role-based)

### Stages tracked
- **FORM1_SUBMITTED**
- **FORM2_COMPLETED**
- **INTERVIEW_COMPLETED**
- **ONBOARDED**

<div class="callout good"><b>Best practice</b><br/>Stage should change through form submissions. Manual edits only for Admin correction.</div>

<hr/>

### Dashboard quick operations

**A) Find a candidate fast**
- Search by **Mobile number** (recommended)
- Or by **Application ID**
- Verify stage + last update

**B) Move candidate to interview**
- Form‑2 outcome must be **Eligible**
- Schedule interview (if module exists)
- Interviewer completes Form‑3

**C) Export report**
1. Apply filters
2. Click Export
3. Save with naming standard: `HR_Pipeline_YYYY-MM-DD.xlsx`

</div>

---

<div class="card">

## Troubleshooting — Fast fixes

**1) Candidate shows “Wait / Not eligible”**
- Reason: 30-day cooldown  
- Fix: explain policy; don’t override

**2) Designation/Position missing in dropdown**
- Reason: master data missing/duplicate  
- Fix: HR Admin updates master data

**3) Pincode not found**
- Reason: pincode master missing  
- Fix: Admin updates pincode master

**4) Upload failed**
- Reason: file > 3MB or corrupted  
- Fix: compress/scan smaller; retry

**5) Dashboard stage wrong**
- Reason: partial form submit or manual edits  
- Fix: Admin correction + verify form completion

<div class="callout bad"><b>Do not do this</b><br/>Never edit DB records directly (mobile/designation/stage) without Admin approval. Audit trail matters.</div>

</div>

---

<div class="card">

## Support & escalation

| Issue | First contact | Escalation |
|---|---|---|
| Portal not loading | IT Support | Sampurna IT Lead |
| Wrong stage/status | HR Admin | Sampurna IT Team |
| Master data missing | HR Admin | HR Head + IT |
| Export/report issue | HR Admin | IT Support |

</div>

<div class="footer">
Built with Trust & Care • Sampurna HR Platform
</div>
