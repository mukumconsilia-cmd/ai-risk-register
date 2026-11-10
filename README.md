# AI Risk Register: T and A Technology LLC

An AI risk register for a consulting firm that builds and uses AI systems. It identifies, scores, assigns and tracks 17 AI risks across six AI systems, and maps each risk to NIST AI RMF, ISO/IEC 42001, the EU AI Act and GDPR.

> **Note:** All risks, owners, systems and figures are fictitious and were created for demonstration. The framework references are real.

## Files

| File | What it is |
| --- | --- |
| `risk-register.csv` | The full register: 17 risks × 23 fields (viewable as a table on GitHub) |
| `T-and-A-AI-Risk-Register.xlsx` | The working spreadsheet with formulas, dropdowns, color coding, a summary dashboard and the scoring key |

## Scenario

T and A Technology LLC is a technology consulting firm. It runs four in-house AI systems and also relies on third-party AI tools:

| AI system | Purpose |
| --- | --- |
| **TA-Assist** | Client-facing generative AI chatbot |
| **RiskLens** | Machine-learning model that scores risk for clients |
| **TalentMatch** | Resume screening for internal hiring |
| **ForecastIQ** | Demand forecasting for clients |
| **DocuSense** | LLM contract summarization (third-party model) |
| **AI coding assistant** | Used by internal developers |

## Methodology

**Risk score = Likelihood × Impact**, each rated 1–5, giving a score from 1 to 25.

| Score | Level | Required response | Review cycle |
| --- | --- | --- | --- |
| 20–25 | Critical | Escalate to the CEO within 24 hours; treat immediately | 30 days |
| 12–19 | High | Treatment plan within 30 days; reported monthly to the AI Governance Committee | 30 days |
| 6–11 | Medium | Treat, or accept with risk owner sign-off | 90 days |
| 1–5 | Low | Accept and monitor | 180 days |

- **Inherent risk** is scored before controls. **Residual risk** is scored after controls.
- **Risk appetite** is a residual score of **8**. A risk above 8 is flagged as outside appetite and needs escalation.
- **Treatment options** are Mitigate, Transfer, Avoid or Accept.
- Each risk has an **owner**, a **key risk indicator (KRI)**, a **target date** and a **next review date**. The next review date is calculated from the residual level.
- Descriptions follow a **Cause → Event → Consequence** structure.

## Register fields

Risk ID · Risk Title · AI System · Category · Risk Owner · Likelihood · Impact · Inherent Score · Inherent Level · Treatment · Controls / Mitigation · Residual Likelihood · Residual Impact · Residual Score · Residual Level · Within Appetite? · Status · Target Date · Last Review · Next Review · Key Risk Indicator · Framework Mapping · Description

## Key findings

1. **Controls reduce exposure substantially.** Before controls, 10 of 17 risks rated High or Critical. After controls, 2 do, and none is Critical.
2. **Two risks remain outside appetite** and are escalated:
   - **AI-004: Staff paste confidential client data into public AI tools** (residual 12, High). Data loss prevention (DLP) rules and the approved-tools rollout are still in progress, so likelihood stays at 3 until adoption is confirmed.
   - **AI-009: Non-compliance with EU AI Act obligations** (residual 12, High). The regulation is still being phased in and the gap assessment is incomplete, so the risk stays High until high-risk systems are classified and documented.
3. **One risk is formally accepted.** AI-017 (lower-quality fallback model during outages) is Low. A premium backup would cost more than the benefit, and the AI Governance Committee signed off on accepting it.
4. **Risk ownership is spread across the leadership team.** The CTO owns 4 risks, the CISO owns 3, and the other five owners have 2 each. No single person carries the program.

### Inherent risk heat map (number of risks before controls)

| Likelihood ↓ / Impact → | 1 | 2 | 3 | 4 | 5 |
| --- | :-: | :-: | :-: | :-: | :-: |
| **5 Almost certain** | | | | | |
| **4 Likely** | | | 2 | 1 | 2 |
| **3 Possible** | | | 3 | 3 | 2 |
| **2 Unlikely** | | 1 | | 2 | 1 |
| **1 Rare** | | | | | |

### Residual risk heat map (number of risks after controls)

| Likelihood ↓ / Impact → | 1 | 2 | 3 | 4 | 5 |
| --- | :-: | :-: | :-: | :-: | :-: |
| **5 Almost certain** | | | | | |
| **4 Likely** | | | | | |
| **3 Possible** | | | | 2 | |
| **2 Unlikely** | | 3 | 5 | 3 | |
| **1 Rare** | | | 1 | 2 | 1 |

## Risks by category

| Category | Risk IDs |
| --- | --- |
| Accuracy & Reliability | AI-001, AI-005 |
| Security | AI-002, AI-007, AI-011, AI-014 |
| Privacy | AI-004, AI-016 |
| Fairness & Bias | AI-003 |
| Transparency & Explainability | AI-008 |
| Regulatory Compliance | AI-009 |
| Legal / IP | AI-010 |
| Governance | AI-013, AI-015 |
| Human Oversight | AI-012 |
| Third-Party / Supply Chain | AI-006 |
| Operational Resilience | AI-017 |

## Frameworks referenced

- **NIST AI Risk Management Framework (AI RMF 1.0)**: the GOVERN, MAP, MEASURE and MANAGE functions
- **ISO/IEC 42001:2023**: AI management system requirements and Annex A controls
- **EU AI Act (Regulation (EU) 2024/1689)**: risk tiers, high-risk obligations, transparency and AI literacy
- **GDPR**: personal data in AI training, prompts and logs
- **NYC Local Law 144**: bias audits for automated employment decision tools
- **OWASP Top 10 for LLM Applications** and **NIST SP 800-218 (SSDF)**: AI security and secure development

## Skills demonstrated

AI risk identification and assessment · risk scoring and appetite setting · control design · mapping to governance frameworks · KRI definition · risk ownership and accountability · governance reporting (heat maps, dashboards)
