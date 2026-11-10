# Cost Curve & Pricing Strategy

Leader feature: **shoes** (certified biomaterial shoe; the reason to buy)
Filler feature: **pod + app** (sensor pod and free Long Use app: remaining-life prediction, Fit Session, basic €30 return credit, Impact Record)
Killer feature: **rewards, tuned next pair and repair coverage, deeper training** (in App+)
Killer feature usage%: **25% of active runners take App+** (estimate, to be validated in the pilot). Among App+ members, expected use: bonus rewards 90%, deeper training insights 70% monthly, tuned next pair 60% at their next pair, repair coverage claimed by 15% a year.
Pricing strategy: **Bundle shoe + pod (€210 for the first pair) with add-on App+ (€39 a year)**. The pod is reused, so later pairs cost €180.
Add-on strategy: pod 30 eur, shoe 180 eur
App: free, App+: 39 eur a year
Long use reward credit: 30 eur

> **Unit:** one active runner, per month, at 50,000 active runners. All figures are example estimates in euros; replace them with pilot data and current provider prices before a decision.
> **Revenue per runner per month: €16.64** = shoe €15.00 (one pair a year) + pod €0.83 (€30 over three years) + App+ €0.81 (25% × €39 ÷ 12).
> **Non-AI COGS per runner per month: €10.31** = shoe €7.50 + pod €0.42 + return credit €1.75 (€30 redeemed on 70% of pairs) + return logistics and inspection €0.47 + repair coverage €0.17.
> **Decision point:** the basic €30 return credit stays in the free app for everyone, because returns feed every model. App+ adds bonus rewards on top. Moving the whole credit into App+ would cut returns from 75% of runners and weaken the data flywheel.

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | €0.012 | Frontier model for 5% of text requests: claim-sensitive answers and "Why this pair". Every answer passes the text compliance check. See the tier table below. |
| Inference (cascading/triage) | €0.006 | Small model (25% of requests) and mid model (10%) for routine insight cards, support and App+ training summaries. 60% of text needs no model, because it is pre-generated from known states. |
| Infrastructure | €0.15 | Own models (remaining-life, tuning for App+ members, material design), gated retraining and evaluation, pod data ingestion and app backend. Gait scan runs on the phone with an open model. |
| Data/storage | €0.03 | Pod data, Fit Profiles, return inspections and the Impact Record evidence chain. Raw gait video is deleted after the Fit Profile is extracted. |
| Human-in-the-loop | €0.36 | Support escalations (15% of conversations, about 10 minutes each), monthly review of AI text samples, and review of material-model proposals. |
| **Total AI COGS** | **€0.56** | **Free app runner about €0.45; App+ member about €0.85** (more insights, tuning and repair-related support). AI COGS is about 3% of revenue. |

**App+ unit check:** each member pays €3.25 a month. The extra cost is about €0.40 of AI and €0.67 of repair coverage, so each member adds about €2.18 of margin a month (67%).

## Cascading Strategy

### Features → tiers → blended cost

About 6 text requests per runner per month. Token sizes and model prices are estimates (small €0.25 / €1.25, mid €1 / €5, frontier €3 / €15 per million input / output tokens); replace with current list prices.

| Feature | Complexity | Model tier | Cost/req | Volume % | Weighted |
|---|---|---|---|---|---|
| Status texts, credit balance, return reminders, wear alerts | None | Template | €0.000 | 60% | €0.0000 |
| Routine insight cards, routine support (pod sync, return points, how the credit works) | Simple | Small | €0.0009 | 25% | €0.0002 |
| App+ deeper training summaries, support needing the runner's history | Medium | Mid | €0.008 | 10% | €0.0008 |
| "Why this pair", sustainability figures, Impact Record, credit or repair disputes | Complex | Frontier | €0.039 | 5% | €0.0020 |
| **Blended** | | | | **100%** | **€0.0030 per request** |

**Blended inference cost per runner per month: about €0.018** (6 requests × €0.003). Frontier is 5% of requests but two-thirds of inference cost.

Token assumptions per request: small 2,000 in / 300 out; mid 5,000 in / 600 out; frontier 8,000 in / 900 out, plus a small-model compliance check (€0.001).

### Routing

**Triage model:** fixed rules first, then a small model that classifies each request (topic, claim sensitivity, confidence) and answers routine ones itself.

**Frontier model:** a frontier model from the primary provider, behind our own interface so a second provider can replace it within days (see the Kill Switch Audit). A mid-tier model from the same family handles medium requests.

**Routing rule:**
1. **Template first** for anything that depends only on known states (pair status, credit tier, repair state, variant). No model call.
2. **Small model** for routine insight cards and routine support.
3. **Mid model** for App+ training summaries and support that needs the runner's own history.
4. **Frontier model** for sustainability figures, recovered content, the Impact Record, "Why this pair", credit or repair disputes, or when a cheaper model's confidence is low.
5. **Person, no model answer,** for any mention of injury, pain or health, and when the runner asks to escalate.

**Expected cascade ratio:** 95% / 5% (template, small and mid / frontier). Full split 60 / 25 / 10 / 5. App+ members run closer to 50 / 25 / 17 / 8 because of deeper training summaries.

## Pricing Model

**Current pricing:** one-time shoe sale at €180. No recurring revenue and no data after the sale.

**Proposed AI pricing:** shoe €180 plus pod €30 for the first pair (€210 bundle); later pairs €180. Free app with the basic €30 return credit. App+ at €39 a year for bonus rewards, the tuned next pair, repair coverage and deeper training.

**Model:** **hybrid.** Hardware bundle (leader + filler) covers customer acquisition, the App+ add-on (killer features) gives recurring revenue, and the return credit is outcome-based: it is paid only when a pair is physically returned and spent on our next pair.

AI text is not sold as a feature in its own right. App+ is priced on the tuned next pair and repair coverage, which depend on data and operations competitors don't have.

### Pricing Strategy Block

- **Strategy posture:** retention-led value pricing. The shoe sells at full price with no discount war, the core AI is free, and money is made on the next pair and premium services.
- **Pricing model:** hybrid. A hardware bundle (shoe + pod), an optional App+ subscription, and an outcome-based €30 credit paid only on a verified physical return.
- **Unit of work metered:** the pair of shoes, with the next sale triggered by a verified return. AI requests and kilometres are deliberately not metered: charging for them would discourage the usage that generates our data.
- **Base fee:** €0.81 a month blended (App+ €39 a year = €3.25 a month per member × 25% attach rate)
- **Price per unit:** €180 per pair (€150 effective for a returning runner after the credit)
- **Estimated units/user/month:** 0.083 pairs (about one pair a year)
- **Implied revenue/user/month:** €16.64 = €0.81 base fee + €15.00 shoes (€180 × 0.083) + €0.83 pod (€30 spread over three years)

**Decision note:** The buyer is a runner who wants shoes that fit better and last longer, and who wants proof that the materials are what the brand says. The value shows up as lower cost per kilometre: at about 700 km a pair, €180 is about €0.26 per km, and a tuned next pair that lasts longer, bought at €150 with the credit, brings that down further. Pricing the pair, not the AI, keeps the price tied to what the runner values.

The structure fits the cost curve. AI costs about €0.56 per runner per month, around 3% of revenue, so usage-based pricing would add billing friction without protecting margin. The core loop stays free because every return improves the models. App+ charges only for things that cost real money to deliver and that competitors can't copy: the tuned next pair, repair coverage, bonus rewards and deeper training.

The risk is retention. Margin per runner falls to about 35%, so the structure only works if at least about 58% of runners buy their next pair from us. The pilot should measure the repeat purchase rate and the App+ attach rate before prices are fixed.

## Stress Tests

Base case gross margin: **34.7%** (€5.77 per runner per month).

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | Inference rises from €0.018 to €0.054. Margin 34.7% → **34.5%**. | No price change. Check template coverage stays at 60% or above. |
| Heaviest segment doubles | Heavy runners (about 10%) use about 3x the average AI cost and claim repairs more often. AI COGS rises about 30% and repair cost about €0.10. Margin → **33.1%**. | Accept it: heavy runners buy the most pairs. Contain support with self-serve answers; cap repair coverage at one claim per pair. |
| Frontier costs 10x mid (€0.08 per request instead of €0.039) | Blended cost per request €0.003 → €0.005; inference €0.018 → €0.030 per runner per month; frontier becomes 80% of inference cost. Margin 34.7% → **34.6%**. If frontier traffic also slips from 5% to 10% of requests, inference reaches about €0.054 and margin **34.5%**. | Hold the routing rule: templates at 60% or above, frontier only for claim-sensitive answers. Track frontier share monthly; each extra percentage point costs about €0.005 per runner per month at this price. |
| Model provider raises prices 50% | Inference rises by about €0.01. Margin 34.7% → **34.6%**. | Follow the 48-hour plan in the Kill Switch Audit; reroute routine text to the second provider after it passes the compliance eval. |
| Requests 5x (automated) | More insight cards and model updates; support contacts unchanged. AI COGS about €1.20. Margin → **30.8%**. | Batch model updates per run sync; put extra insight volume in App+, not the free app. |

The risk that matters is not inference. **A doubled support escalation rate costs €0.30 a month (margin → 32.9%),** and a lower App+ attach rate removes the most profitable revenue line.

## Board One-Pager

**Before (traditional SaaS):** shoe sold once at €180 with about 50% gross margin (€90 a pair). Example repeat rate: 35% of runners buy their next pair from us. Margin per acquired runner over three years: about **€132**.

**After (AI-enabled):** about €200 revenue per active runner a year (shoe, pod, App+) at 34.7% gross margin, about **€69 per active year**. AI costs about €6.70 a year, 3% of revenue. The return credit, return logistics and repair coverage cost about €28 a year, more than four times the AI.

**Net margin shift:** gross margin per runner falls from about 50% to about 35%, because the model invests in returns, repair and data. It pays back through retention. **The new model beats the old one if at least about 58% of runners buy their next pair from us** (approximate, over three years), against an assumed 35% today. At the target of 70%, margin per acquired runner is about **€152**, 15% above today, plus the owned data that powers the tuned next pair and the material model. The pilot must measure two numbers: repeat purchase rate and App+ attach rate. Inference cost does not decide this case.
