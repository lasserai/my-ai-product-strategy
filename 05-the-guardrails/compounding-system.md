# Compounding System Design

Product: biomaterial shoe (exercise product): material performance & fit model, sizing assistant, take-back and consortium data loops.

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| 1 · Recursive Learning | Structured return codes, insole-tag wear data, lab degradation tests, all joined by formulation ID (DTC + wholesale) | Monthly retrained performance & fit model that tunes the next formulation and last | Y | active |
| 2 · Cross-Domain Transfer | Material learnings in the shared materials vocabulary + supplier lot data | New products/categories start from learned priors; fewer failed prototypes | Y | active |
| 3 · Network Intelligence | Anonymised performance data from a partner-brand consortium (same suppliers, shared ID format) + retail returns | Region/climate recommendations (shown only above minimum sample size) and supplier benchmarks that improve with every member | Y | active |
| 4 · Circularity / Take-back | End-of-life scans from DTC and QR retail drop-off points; measured compost/recycle outcomes | Continuously updated LCA data fed into formulation scoring; verified product claims | Y | active |
| 5 · Sizing & Support Assistant | Sizing conversations, recommended vs kept size, fit-related returns | Better size recommendations + fit signals into last design and Loop 1 | Y | active |

**Broken loop identified by partner:** Loops 1 and 4 work against each other. Loop 1 learns that durable formulations get fewer returns; Loop 4 learns that durable formulations biodegrade more slowly. Left alone, the model drifts toward shoes that last longer but compost worse, undermining the product's core promise.

**Fix plan:**
1. Make formulation optimisation multi-objective with a **hard compostability floor** (must pass the certified compost standard), which no durability gain can override.
2. Add a guardrail metric next to return rate: **mean time-to-biodegrade per released formulation**. Alert on upward drift two releases in a row.
3. Sustainability lead signs off any recommended formulation within 10% of the floor.
4. Record the trade-off rule in this file and in the model card so it outlives the team that wrote it.

## Context Connectivity

**How knowledge flows:** One shared thread: every lab sample, batch, supplier lot, order, wholesale return, end-of-life scan and consortium submission carries the formulation ID and uses the shared materials vocabulary. R&D, production, support, procurement and sustainability read from and write to one joined dataset. Model outputs (failure predictions, fit adjustments, supplier scores) flow back into each team's own tools. LCA data feeds formulation scoring continuously, not once per collection. Retailers send structured return codes in exchange for size-curve recommendations.

**Where it silos:**
- **Vocabulary dependency on one team:** the materials vocabulary and ID scheme are maintained by one team. Needs named governance, versioning and a change process that includes consortium partners.
- **Wear-data consent:** insole-tag data depends on opt-in that isn't yet designed into the product; a privacy misstep would cut off Loops 1 and 5.
- **Cross-brand sharing rules:** consortium exchange needs anonymisation and competition-law rules before it grows past a few partners.

## Governance Policy

**Scope:** The AI models that influence formulation, fit, customer answers or product claims: the material performance & fit model (Loops 1–4), the sizing & support assistant (Loop 5), the returns failure-code classifier, and AI-assisted drafting of LCA/circularity claims. Also covers consortium data exchange and any third-party AI tool that touches customer, supplier or formulation data (see Shadow AI Audit). No autonomous agents in this version.

**Autonomy boundaries:**
- Models **recommend**, humans **decide and act**. No model releases a formulation, issues a refund or exchange, publishes a claim, changes a supplier or sends data externally.
- The sizing assistant can only recommend sizes and answer approved FAQs; exchanges and refunds are handled by support staff. It makes no health, injury or sustainability claims.
- The returns classifier proposes failure codes; support staff confirm low-confidence cases.
- The compostability floor is a hard constraint in the formulation model, not a weight it can trade off.
- Consortium exports are prepared by the model, released by the data governance owner after the anonymisation check.

**Escalation triggers:**
- Recommended formulation within 10% of the compostability floor → sustainability lead sign-off.
- Return rate for a formulation above 2× baseline within 60 days of launch → R&D lead; pause further production of it.
- Customer mentions injury, pain or a medical condition, or sizing confidence below threshold → hand off to a support agent.
- Anonymisation check fails, or a partner asks for non-aggregated data → data governance owner + legal.
- Any public sustainability claim drafted with AI → legal + sustainability review before publication.
- Drift alert on model accuracy or time-to-biodegrade → model owner within 5 working days.

**Audit cadence:**
- Monthly: retrain review (accuracy, drift, guardrail metric, failure cases).
- Quarterly: escalation log, shadow AI re-scan, consortium data-sharing audit.
- Per model release: model card + data lineage check.
- Annually: external review of LCA/circularity claims; policy refresh.

**Regulatory exposure (EU AI Act / other):** _(checked against current sources, 17 Nov 2026)_
- **EU AI Act:** Formulation and supplier models likely minimal-risk (no Annex III use). The sizing assistant's duty to tell customers they are talking to AI (Art. 50(1)) **has applied since 2 Aug 2026**; the Digital Omnibus did not delay it. Commission Art. 50 guidelines adopted 20 Jul 2026. The Omnibus moved stand-alone high-risk (Annex III) obligations to Dec 2027, which does not affect this product.
- **Green claims (EmpCo / ECGT Directive 2024/825):** **applies since 27 Sep 2026**, no general transition period (some Member States allow old-stock tolerance). Generic claims like "eco-friendly", "green" or "biodegradable" are banned unless backed by recognised excellent performance. Product claims must be specific ("industrially compostable to EN 13432 within X weeks") and evidenced by Loop 4 data; AI-drafted claims need legal + sustainability review.
- **ESPR / Digital Product Passport:** **no footwear DPP yet.** Footwear is not a priority group in the 2025–2030 working plan; a Commission study on footwear is due by end 2027. Textiles delegated act expected 2027. Keep the formulation ID + LCA data model passport-ready, but treat the DPP as a 2028+ horizon.
- **ESPR unsold-goods destruction ban:** **already applies to footwear** for large enterprises since 19 Jul 2026 (medium-sized enterprises later). Relevant to returns and failed batches: destruction needs a listed exemption and must be reported; Loop 4 take-back/recycling routes are the compliant path.
- **GDPR:** insole wear and sizing data are personal data; gait-like data may approach health/biometric territory. Needs DPIA, explicit opt-in, minimisation, retention policy.
- **Competition law (Art. 101 TFEU):** consortium shares aggregated, anonymised performance data only; never prices, volumes or plans.

## Agent Topology

_Not shipping agents this version._ All model outputs are recommendations acted on by named people (see Autonomy boundaries). Revisit before automating any action: exchanges, failure-code confirmation or consortium exports are the likely first candidates, each needing its own can/can't/approver definition.

## Shadow AI Audit (internal)

<!-- Example inventory for the exercise; replace with real findings from expense reports, SSO logs and team interviews. -->

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| Personal ChatGPT accounts for marketing & sustainability copy | Marketing | H | govern: move to company workspace; all green claims through legal + sustainability review |
| Freelancer-built AI size-finder plugin on webshop | E-commerce | H | kill: replaced by the sizing & support assistant (Loop 5) |
| AI spreadsheet add-in on R&D lab data | R&D | M | govern: approved vendor + DPA, or move analysis into the joined dataset |
| AI meeting-notes tool recording supplier negotiations | Procurement | M | govern: disable for supplier calls with pricing; company-managed tenant |
| Supplier-provided AI quality scoring portal | Procurement | M | govern: contract clause on data use; feed scores into Loop 3 |
| AI image generator for product visuals | Marketing | M | govern: label AI images; never show unreleased materials as real |
| Free online AI translation for product pages | E-commerce | L | kill: switch to approved translation tool (claims text must stay accurate) |
| AI writing assistant (grammar/style) | All | L | keep |

**Total tools found:** 8
**Tools after triage:** 6 (2 killed, 5 governed, 1 kept)
**Estimated hidden spend:** ~€1,100/month (≈€13k/year) across individual subscriptions and expensed seats (illustrative estimate; confirm from expense data)

## Shadow AI Audit (user-side), Module 5

### Discover, User-Side Workarounds

| # | Workaround | Signal | Frequency | Decision |
|---|-----------|--------|-----------|----------|
| 1 | Customers paste our size chart + shoes they already own into ChatGPT to convert sizes across brands | capability | H | build |
| 2 | Customers ask ChatGPT whether "compostable mycelium leather" is real and how to actually compost the shoe | trust | H | build |
| 3 | Retailers pipe our returns CSV through Zapier/Make into an AI step that categorises free-text return reasons | workflow | M | build |
| 4 | B2B / corporate buyers paste our LCA PDF into ChatGPT to extract footprint numbers for their Scope 3 reporting | workflow | M | build |
| 5 | Customers ask ChatGPT how to clean and care for biomaterial (water, conditioner, drying) | capability | M | build |
| 6 | Customers use AI to write resale listings or find repairers because a new pair is expensive and take-back isn't attractive | pricing | L | partner |
| 7 | Customers machine-translate product pages with AI tools | capability | L | ignore |

<!-- Frequencies and spend are illustrative estimates for the exercise; validate against support-ticket tags (size, compost, care), retailer integration logs and the Zapier/Make directory. -->

### Pattern Assessment
- Workarounds found: 7
- Build candidates: 5
- Partner candidates: 1
- Ignore decisions: 1
- Adjacent spend: ~$1,400/mo
- Dominant signal: capability (3 of 7). Weighted by frequency, capability + trust: both high-frequency workarounds are about buying confidence in a new material.

### Action Plan
#### Build
1. **Cross-brand size translation in the sizing assistant** (#1, H): customers enter shoes they own and get a size back; fit signals feed Loops 1 and 5.
2. **Verified end-of-life page behind the insole QR code** (#2, H): specific, evidence-backed compostability claim (named standard, timeframe, where) from Loop 4 data, plus take-back. Also required for EmpCo compliance (in force since 27 Sep 2026).
3. **Structured return-codes API for retailers** (#3, M): replaces their Zapier + AI workaround and closes the wholesale data gap in Loop 1.
4. **Machine-readable footprint data per product** (#4, M): JSON/API, DPP-ready; replaces PDF-to-ChatGPT extraction.
5. **Care guide on the same QR page** (#5, M): small; ship with item 2.

#### Partner
- **Resale / repair platform** (#6, L): certified resale channel and repair network, linked to take-back. Confirm with the platform's partnerships team.

#### Ignore + Monitor
- **Machine translation of product pages** (#7, L): resolved by our own approved translations; monitor support tickets for mistranslated care or claim text (claims must stay accurate under EmpCo).

### Roadmap Brief
Based on your audit: 7 user-side workarounds discovered.
Decisions: 5 build · 1 partner · 1 ignore · 0 TBD.
Estimated adjacent spend: ~$1,400/mo across surveyed users (≈15 retailers on Zapier/Make at ~$70/mo, plus 3–4 paying ~$100/mo for AI return categorisation; consumer ChatGPT subscriptions excluded as not attributable).
Dominant signal: capability (with trust close behind among the high-frequency items).

Recommended next step: Ship builds 1 and 2 first. Both are high-frequency, and both remove the main purchase-confidence barriers for a new material. Build 2 also closes a live compliance exposure. Then build 3, because it unlocks wholesale data for the learning loop and retailers are already paying ~$1,050/mo to work around its absence.

Sequence the Build column by frequency × strategic relevance. Confirm Partner candidates with the external tools' partnership teams. Re-run this audit each quarter, workarounds shift fast.
