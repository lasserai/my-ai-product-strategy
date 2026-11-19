# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1 — Now (0-3 months)
*Quick wins. Ship with existing capabilities.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |
| | | H / M / L |

Initiative
Strategy Component
Why it ships now
Confidence
SHOE-1 · Fit Session & first-pair personalisation
Bet
Core product differentiation and defence against Strava/Garmin.
H
SHOE-2 · Sensor pod & wear-data pipeline
Moat
Establishes the proprietary physical-product data source.
H
SHOE-5 · AI reliability contract & human review
Contract
Trust infrastructure is a prerequisite for AI-generated advice and claims.
H
SHOE-9 · Fit Session v1
Bet
Delivers the first usable personalisation experience.
H
SHOE-10 · Rules-based fit recommendation
Contract
Implements the rules-first architecture without expensive frontier inference.
H
SHOE-12 · Pod firmware
Moat
Enables collection of real-world wear signals.
H
SHOE-13 · Wear-data pipeline linked to shoe ID + formulation batch
Moat
Creates traceable data needed for the learning flywheel.
H
SHOE-14 · Data consent & GDPR DPIA
Guardrails
Privacy approval must precede sensor-data collection at scale.
H
SHOE-15 · Structured return codes
Moat
Makes return data usable for formulation learning.
H
SHOE-16 · €30 return credit mechanism
Margin
Implements the outcome-based incentive while preventing uncontrolled credit issuance.
H
SHOE-19 · Impact Record v1 (private)
Bet
Delivers initial user value without premature public sustainability claims.
H
SHOE-20 · Certification provenance
Guardrails
Prevents unsupported material claims entering the evidence chain.
H
SHOE-23 · Expand golden dataset to 150 cases
Contract
Strengthens reliability coverage before wider deployment.
H
SHOE-24 · Reliability gate in CI
Contract
Makes reliability requirements enforceable release criteria.
H
SHOE-25 · Human review queue
Contract
Operationalises human approval for conflicting evidence and high-risk claims.
H
SHOE-27 · Compostability-floor guardrail
Guardrails
Enforces the non-negotiable material-performance boundary.
H
SHOE-38 · Monthly retraining review
Guardrails
Establishes the operating cadence for drift, quality and governance.
M
H1 execution principle: Build the evidence infrastructure before building more AI features. In particular, SHOE-13, SHOE-20, SHOE-23 and SHOE-24 are foundational dependencies, not optional platform improvements.
### Horizon 2 — Next (3-9 months)
*Bets. Requires new capabilities or integrations.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |
| | | H / M / L |
SHOE-3 · Return, repair & credit loop
Bet
A physical return and repair loop creates measurable retention and repeat-purchase value.
If returned-pair participation does not materially exceed the agreed control threshold by pilot week 12, stop expanding the incentive.
M
SHOE-4 · Impact Record & certification chain
Contract
Verifiable provenance can support credible per-pair sustainability records.
If any material claim cannot be traced to valid certification and batch evidence by week 6, block that claim and stop public-record development.
M
SHOE-6 · Unit economics & pricing model
Margin
The €210 first-pair bundle, €180 repeat pair and €39 App+ subscription can support sustainable contribution margin.
If the validated model cannot reach the agreed 35% net-margin target at realistic retention and return assumptions by week 8, revisit pricing and costs.
M
SHOE-7 · Controlled pilot & enterprise design partners
Bet
A controlled pilot can establish whether the complete proposition outperforms a standard shoe.
If the pilot cannot demonstrate a meaningful improvement on the pre-agreed primary outcome by month 3, stop or redesign the bet.
M
SHOE-11 · Fit outcome survey after 50 km
Bet
Personalisation produces a measurable improvement in comfort and fit.
If the treatment group does not outperform control on the pre-agreed fit score after sufficient 50 km observations, stop expanding personalisation investment.
M
SHOE-17 · Repair-or-replace recommendation
Moat
Observed wear data can produce more useful repair decisions than generic mileage thresholds.
If recommendations do not outperform the existing repair team's baseline agreement rate after 100 assessed pairs, stop model development.
M
SHOE-18 · Reverse-logistics partner
Margin
Returns can be collected at a cost compatible with the circular business model.
If cost per successful return exceeds the approved unit-economics ceiling after the first 50 returns, renegotiate or replace the partner.
M
SHOE-21 · Independent durability & recovery validation
Contract
Third-party testing can substantiate the product's durability and recovery claims.
If independent testing fails the pre-agreed durability or recovery thresholds by week 8, withdraw the corresponding claim and reconsider the material formulation.
M
SHOE-26 · Human-review workload and AI cost at 10x
Margin
Human review and inference costs remain manageable as usage scales.
If projected review and inference costs push the model below the approved contribution-margin floor at 10x usage, redesign routing before scaling.
M
SHOE-28 · Verified AI COGS per unit
Margin
The 95% rules-first / 5% frontier routing target produces acceptable actual AI costs.
If measured AI COGS exceeds the approved per-runner budget after four weeks of production-like traffic, stop scaling the current architecture.
M
SHOE-29 · Gross-to-net margin bridge
Margin
The apparent 7% AI-adjusted margin can be reconciled with a viable 35% net-margin model.
If verified costs and realistic retention cannot reconcile the 35% target by week 6, revisit the business model before further investment.
M
SHOE-30 · Break-even volume and repeat-purchase rate
Margin
The hybrid pricing model can reach break-even at an achievable volume and repurchase rate.
If break-even requires a repeat-purchase rate unsupported by pilot evidence by week 8, stop treating the current pricing model as viable.
M
SHOE-31 · App+ subscription (€39/year)
Margin
A meaningful segment of runners will pay for repair coverage, insights and tuned next-pair benefits.
If fewer than the pre-agreed percentage of eligible pilot users convert at €39/year after the price test, stop the current subscription rollout.
M
SHOE-32 · Agree numerical kill thresholds
Bet
The team can agree objective conditions for continuing or stopping the bet before collecting pilot evidence.
If sponsor-approved numerical thresholds are not signed off before the first enrolment, do not start the pilot.
H
SHOE-33 · Recruit and run controlled pilot
Bet
The integrated product and incentive model improves retention, returns and repurchase against control.
If the treatment group fails the pre-registered primary outcome or breaches a critical product-safety threshold at six months, stop the bet.
M
Important sequencing correction: SHOE-32 must happen before SHOE-33. SHOE-21 must happen before SHOE-22. SHOE-28 and SHOE-29 should precede any board-level claims that the economics are validated.
### Horizon 3 — Bet (9-18 months)
*Moonshots. High uncertainty, high potential.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |

SHOE-8 · Next-generation formulation learning
Moat
Returned-pair data, formulation traceability and lab degradation evidence must be sufficiently reliable to influence product design.
L
SHOE-22 · Shareable Impact Record (public)
Bet
SHOE-20 certification provenance, SHOE-21 independent validation and 100% sustainability-claim golden-case reliability must pass, with legal approval.
M
SHOE-36 · Lab degradation testing linked to returned pairs
Moat
Enough returned pairs and structured wear data must exist to correlate real-world use with laboratory degradation.
L
SHOE-37 · Gen-2 tuned pair from returned-pair data
Moat
The preference and formulation learning loops must produce evidence that a tuned next pair improves fit or durability for the same runner.
L
## Board Pitch

**Thesis (1 sentence):**

**The case:**
1. Why now:
2. What's defensible:
3. The economics:

**The risks:**
1. Trust / failure modes:
2. Scale / governance:
3. Competitive:

**The ask:**

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

**Now:**
