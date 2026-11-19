# Enterprise ESG data portfolio (operational, supplier and third-party sustainability data, plus the models, lineage and governance around it)

> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS the strategy, version-controlled, board-ready, portable.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** Enterprise ESG data portfolio (operational, supplier and third-party sustainability data, plus the models, lineage and governance around it)
- **AI Value Archetype:** _(add: Automator / Copilot / Oracle / Creator / Orchestrator)_
- **Vulnerability Scores:** _(add: Moat _/5 · Data _/5 · Platform _/5)_
- **Top Risk:** The portfolio's value is tied to compliance demand and integration plumbing. Regulation is shrinking the first, and ERP-native AI is commoditising the second, so the portfolio risks being reframed as a cost centre that a vendor module could replace.
- **Confidence:** M
- **Prototype:**
- **Kill Criteria:**

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:**
- **Weakest Loop:** **Fix for weakest loop:**
- **Top Encroachment Threat:** **Vector:**
- **Encroachment Defense:** ---
- **Vendor Portability:** _(add: Ready / Partial / Locked)_

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 50%
- **Gross Margin (AI-adjusted):** 7%
- **Pricing Model:** **hybrid.** Hardware bundle (leader + filler) covers customer acquisition, the App+ add-on (killer features) gives recurring revenue, and the return credit is outcome-based: it is paid only when a pair is physically returned and spent on our next pair.
- **Pricing Today → Tomorrow:** one-time shoe sale at €180. No recurring revenue and no data after the sale. → shoe €180 plus pod €30 for the first pair (€210 bundle); later pairs €180. Free app with the basic €30 return credit. App+ at €39 a year for bonus rewards, the tuned next pair, repair coverage and deeper training.
- **Total AI COGS / unit:**
- **Cascading Strategy:** Triage: fixed rules first, then a small model that classifies each request (topic, claim sensitivity, confidence) and answers routine ones itself.; frontier: a frontier model from the primary provider, behind our own interface so a second provider can replace it within days (see the Kill Switch Audit). A mid-tier model from the same family handles medium requests.; ratio 95% / 5% (template, small and mid / frontier). Full split 60 / 25 / 10 / 5. App+ members run closer to 50 / 25 / 17 / 8 because of deeper training summaries.
- **Net Margin Shift:** gross margin per runner falls from about 50% to about 35%, because the model invests in returns, repair and data. It pays back through retention.…
- **Break-even at:**

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** ≥ 95% of golden dataset cases pass; 100% pass on sustainability-claim and safety cases
- **Golden Dataset:** 22 rows, 5 adversarial
- **Confidence UX:** tiered confidence with a human-in-loop trigger. Confidence is not a model's self-rating alone: it combines whether the answer is grounded in a source of truth, whether rule checks pass, and the topic's risk level.
- **HITL Architecture:** A human steps in when: - The answer is low confidence (no source, or the source conflicts with another). - The topic is high-risk: health or allergy, pet or child safety, defects and warranty claims, or any sustainability claim that goes be…
- **Failure Mode Coverage:** *What failure mode did your partner find that you missed?*

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | |------|-------|--------|-----------|--------| | 1 · Recursive Learning | Structured return codes, insole-tag wear data, lab degradation tests, all joined by formulation ID…
- **Governance Posture:** The AI models that influence formulation, fit, customer answers or product claims: the material performance & fit model (Loops 1–4), the sizing & support assistant (Loop 5), the returns failure-code classifier, and AI-as…
- **Autonomy Boundaries:** - Models **recommend**, humans **decide and act**. No model releases a formulation, issues a refund or exchange, publishes a claim, changes a supplier or sends data externally.
- **Escalation Triggers:** - Recommended formulation within 10% of the compostability floor → sustainability lead sign-off.
- **Audit Cadence:** - Monthly: retrain review (accuracy, drift, guardrail metric, failure cases).
- **Shadow AI Audit (user-side):** 8 workarounds found · 6 (2 killed, 5 governed, 1 kept) build candidates · adjacent spend ~€1,100/month (≈€13k/year) across individual subscriptions and expensed seats (illustrative estimate; confirm from expense data)
- **Agent Boundaries:** _Not shipping agents this version._ All model outputs are recommendations acted on by named people (see Autonomy boundaries).…
- **Regulatory Exposure:** _(checked against current sources, 17 Nov 2026)_

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** **The case:**
- **Ask:** ## M1 Baseline vs. Now
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
