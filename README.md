# ⚡ ZAP: Zach's Agile Protocol

ZAP is a lightweight, agile-adjacent framework designed by Zachary Bornheimer to streamline ticket intake, triage, development, QA, and deployment across fast-paced, lean teams. It emphasizes clarity, flexibility, and traceable action, enabling teams to move quickly while enforcing rigor and quality.

---

## ✏️ Ticket Types

All tickets fall into one of the following categories:

- **Bug**: The system is not working as intended
- **Enhancement**: Feature request, UI/UX update, or other change (system was working correctly)
- **Research**: Discovery work or problem definition
- **Documentation**: Technical/process documentation
- **Other**: Anything else (include the context in the ticket)

---

## 🔴 Priority Levels

| Priority | Description                                       | Response Guidance      |
| -------- | ------------------------------------------------- | ---------------------- |
| **P1**   | System is broken, blocking users, no workaround   | Immediate attention    |
| **P2**   | Major issue or business impact, workaround exists | Resolve in next sprint |
| **P3**   | Medium UX bug or improvement                      | Plan via roadmap       |
| **P4**   | Cosmetic/low impact issue                         | Fix when possible      |
| **P5**   | Trivial or won't fix for now                      | Document + archive     |

---

## 🛠️ ZAP Workflow

### 1. **Ticket Intake + Logging**

- Intake handled manually or via tooling (e.g., internal app)
- Ticket must contain: title, type, priority, expected vs actual behavior, and affected component(s)
- Time estimate added by dev
- Sent to QA for **initial review**
- QA Status changed: `Unreviewed` → `Ready for Initial Ticket Review`

### 2. **QA Review**

- QA Status changed: `Ready for Initial Ticket Review` → `Initial Ticket Review In Progress`
- QA validates:
  - Is the ticket understandable?
  - Are reproduction steps clear?
  - Are test cases proposed?
- Result:
  - `Ready for Development`
  - `Not Ready for Development` (further clarification needed, awaiting UI/UX mockups, customer research needed, etc.)
  - `Unclear Requirements`

### 3. **Development**

- Dev self-assigns tickets that are `More Development Needed` based on priority and estimated time
- Dev self-assigns tickets that are `Ready for Development` based on priority and estimated time
- QA Status set to: `Development In Progress`
- Dev confirms failing tests or builds toward proposed tests
- Once complete, status set to `Ready for Final Review`

### 4. **Final Review / QA**

- QA confirms fix is implemented and test cases pass
- QA ensures automated testing is in place to prevent regression
- Status: `Final Review In Progress` → `Approved`
- If cases do not pass: Status: `Final Review In Progress` → `More Development Needed`

### 5. **Staging + Retrospective**

- Status: `Ready for Deployment`
- Once deployed, mark for **retrospective root cause**

---

## ⚖️ Retrospective Labels

For reporting, it's helpful to get a grasp of why we had this ticket to begin with.

Indicate in the ticket why work needed to be done.

- Incomplete Requirements
- Incorrect Assumptions
- Missing Automated Test(s)
- Incorrect / Incomplete Automated Test(s)
- Unverified Source Material
- Outdated Source Material

---

## 🔢 ZAP Ticket Lifecycle Summary

```text
Unreviewed → Initial Ticket Review → Ready for Development
→ Development In Progress → Ready for Final Review
→ Final Review in Progress → Ready for Deployment
```

---

## ⏳ Dev Time Commitment Guidance

- Each dev targets a total number of **planned hours per sprint** (e.g., 40h/2 weeks)
- Tickets are pulled based on priority and estimated time
- Tickets needing clarification are returned to intake

---

## 💡 Philosophy

ZAP assumes:

- Clarity and traceability matter more than perfection
- Developers should own their time and output
- QA is essential but streamlined
- Process should help, not hinder

ZAP is a system designed for scale, autonomy, and impact—with built-in optics for leadership and simplicity for engineering.

---

## 📄 Ownership

This document was created by Zachary Bornheimer.\
© 2025 ZAB Ai, LLC. All rights reserved.\
Use, reproduction, or distribution without explicit permission is prohibited.
