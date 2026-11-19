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
We are building a running shoe that gets more personal and more valuable with every kilometre, turning verified material performance, individual fit data and physical returns into a repeat-purchase advantage that conventional footwear brands cannot replicate with a software update.
**The case:**
1. Why now: The opportunity is to move sustainability in footwear from brand-level promises to product-level evidence. Our proposition connects three things that are usually disconnected: how a shoe is made, how it performs in real-world use, and what happens when it is returned. The immediate timing opportunity is our Q3 enterprise design-partner conversion, which gives us a commercial window to validate the proposition before committing to broader production. However, the strategy does not yet establish a specific market shift in the last 6–12 months, nor quantify competitor adoption or customer willingness to pay. We should not present market timing as proven. The six-month window is a validation opportunity, not evidence of an expiring market window.

2. What's defensible: The moat is the physical-product learning loop (M2), not the app or the AI. Fit Session establishes an individual baseline; the reusable sensor pod captures real-world wear; structured return codes connect actual product failures to formulation batches; laboratory degradation tests validate what happens to the materials; and returned-pair data informs the next formulation and the next pair. This creates a relationship between runner, physical shoe and material performance that Strava or Garmin cannot reproduce simply by adding another shoe-mileage reminder. We are explicitly weak on the preference loop (2/5): those platforms already own training histories and gear mileage. Our defence is to own the fit session, physical wear evidence and tuned replacement product rather than compete for another dashboard. The moat is not established yet. It must be earned through wear-data pipeline linked to shoe ID and formulation batch, structured return codes, lab degradation testing linked to returned pairs, and Gen-2 tuned pair from returned-pair data. Six months of execution should establish whether this data advantage is real.

3. The economics: 50% current gross margin falls to approximately 35% under the proposed retention and circular-service model; the current AI-adjusted gross-margin estimate is only 7%. That gap is the commercial problem we must resolve before scaling. The proposed pricing is €210 for the first shoe-and-pod bundle, €180 for repeat shoes, and €39/year for App+. The basic app includes a €30 return credit, issued only against a physical return and spent on the next pair. This makes the incentive outcome-based rather than an unconditional discount. Inference costs are controlled through a 95% rules-first / small-and-mid-model routing target, with frontier inference reserved for approximately 5% of requests. App+ usage is expected to cost more because of deeper training summaries. The intended margin recovery comes from returns, repair, retention and repeat purchases, not cheaper inference alone. But the 35% net-margin target, actual AI COGS per runner, reverse-logistics cost and break-even repeat-purchase rate are not validated. 10x human-review workload and AI cost testing, verified AI COGS per unit, the gross-to-net margin bridge, and break-even volume and repeat-purchase rate must establish those numbers before we claim a scalable business model.

**The risks:**
1. Trust / failure modes: The biggest reputational risk is a publicly shared Impact Record containing a false sustainability claim. A certification could be invalid, a material batch could fail independent testing, a durability prediction could be wrong, or a compostability claim could be contradicted by actual recovery performance. That turns our strongest proposed differentiator into a greenwashing liability for both the company and the runner sharing the record. Our reliability contract requires at least 95% of golden-dataset cases to pass and 100% of sustainability-claim and safety cases to pass. Confidence is determined by source quality, rule checks and topic risk, not simply by the model's own confidence score. Conflicting evidence, missing sources and high-risk claims go to human review. Certification provenance, independent durability and recovery testing, a 150-case golden dataset and release gates are prerequisites. The public Impact Record stays blocked until the evidence chain and legal approval are complete. The current 22-case dataset is a starting point, not proof of production reliability. We also have an unresolved evaluation gap: the partner-identified failure mode is not documented in the strategy. That must be closed before the board treats the reliability assessment as complete.

2. Scale / governance: At 10x usage, two things can break the business: inference and human-review costs can consume contribution margin, while weak evidence and model drift can allow incorrect product or sustainability advice to reach customers. 10x human-review workload and AI cost testing explicitly tests the 10x cost and review workload; verified AI COGS per unit measures actual AI COGS; the gross-to-net margin bridge reconciles gross and net margin. The operating design uses rules first, a small classifier for routine routing and a replaceable frontier provider for genuinely difficult requests. We will not ship autonomous agents in this version. Models recommend; named people approve and execute formulation changes, refunds, exchanges, supplier changes and external data sharing. A formulation recommendation within 10% of the compostability floor requires sustainability-lead approval. Monthly reviews cover accuracy, drift, guardrail metrics and failures. Vendor portability is ready, but operational resilience and the economics of human review still need validation. No scale-up decision should precede that evidence.

3. Competitive: The single scenario that forces a kill is Strava or Garmin launching a credible shoe-personalisation and replacement proposition that matches our user value while we fail to demonstrate that physical-product data produces a measurable advantage in fit, durability or repeat purchase. We cannot win an app-level feature race against platforms that already own runner relationships. Our defence is a better physical product informed by the runner's actual returned pair. The kill test is the controlled 300–500-runner pilot against a control group without the reward, with numerical thresholds agreed before enrolment. If treatment does not outperform control on the pre-registered primary outcome by six months, or breaches a critical safety threshold, stop or redesign the bet. More specifically, if fit personalisation fails to improve the agreed fit score after sufficient 50 km observations, stop expanding that investment. If returned-pair recommendations fail to outperform the repair team's baseline after 100 assessed pairs, stop model development. We fund evidence of product advantage, not feature parity.

**The ask:**
Approve €1.2M for six months, with 3 engineers, 1 product manager and 1 legal SME, to take this proposition from product concept to validated enterprise design-partner conversion. The funding buys three outcomes: first, an integrated shoe, sensor and fit-personalisation experience with traceable product and formulation data; second, independently validated durability, recovery and certification evidence, with a controlled pilot of 300–500 runners and explicit continuation criteria; third, a verified commercial model covering return economics, App+ conversion, actual AI COGS, contribution margin and repeat-purchase behaviour. The first four weeks establish the evidence infrastructure and working product. Months 2–3 validate fit, returns, repair, certification and unit economics. Months 3–6 test formulation learning, next-pair personalisation and enterprise conversion, with public Impact Records remaining gated by independent validation and legal approval. We will prioritise Fit Session & first-pair personalisation, sensor pod & wear-data pipeline, AI reliability contract & human review, wear-data pipeline linked to shoe ID and formulation batch, certification provenance, and expansion of the golden dataset to 150 cases, and the associated release and governance controls before expanding AI functionality. What gets paused is speculative autonomous-agent development, broad app-feature expansion, public sustainability marketing ahead of validation, and frontier-model investment beyond the small proportion of requests that demonstrably require it. The board gets a six-month decision backed by product, customer and financial evidence: scale, redesign or kill.
## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**
Baseline (M1): We are building a certified-biomaterial sports shoe with a reusable sensor pod and an app that tracks usage, predicts remaining useful life and recommends the best-fitting next pair. AI acts as an Oracle, turning real-world wear and fit data into repair, replacement and personalisation decisions. A verified, shareable Impact Record makes each pair's sustainability performance transparent.**Now:**
Now: We are building a physical-product learning loop that makes every returned shoe an input into a better-fitting, better-performing next generation. Our competitive advantage is not AI-powered advice that Strava or Garmin can replicate; it is proprietary evidence connecting individual fit, real-world material degradation, formulation batches and product returns. AI enables that loop, but independently verified evidence, measurable product improvement and repeat-purchase economics determine whether it becomes a defensible business.
