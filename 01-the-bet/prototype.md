# The Prototype Bet

> Product: certified biomaterial sports shoe with a reusable sensor pod and app. The bet follows the diagnostic and the data flywheel: one closed loop of certified material → measured use → repair, return or pass-on → verified Impact Record → better replacement deal → **next pair built from what the last pair learned**.

## What I Built
A clickable mock-up of the **Long Use app**. A fit session at purchase personalises from day one; the runner sees how much life their pair has left, earns a bigger replacement credit the longer they use it, and returns the worn pair. Their **next pair is tuned from the returned pair's wear data**. Usable pairs are passed on through the community, runners can join a test pilot programme for new materials, and everything builds a verified, shareable Impact Record. A brand-side dashboard shows whether the loop pays for itself and publishes durability data openly.

## Tool Used
Lovable

## Prototype Link
<!-- Paste the shareable Lovable URL here after publishing -->

## AI Value Archetype
**Oracle.** The app predicts each pair's remaining useful life and the best-fitting variant for the next pair, from foot-level use and real-world material wear data. The prediction drives the repair and replace advice, the credit, the tuned next pair and the Impact Record.

## The Bet in One Sentence
For runners who want their footwear choices to count, we build a certified biomaterial shoe whose next pair is tuned from how they wore the last one, with a replacement credit that grows with long use and a verified Impact Record, now, because EU rules since 27 September 2026 ban vague green claims, and software platforms can track kilometres but can't make the shoe.

## Kill Criteria
Stop the bet if any of these holds after a 6-month pilot with 300–500 runners, compared with a control group without the reward:

1. **No behaviour change:** average kilometres per pair rise by less than 15% against the control group.
2. **Low returns:** fewer than 60% of worn-out pairs are returned.
3. **No loyalty:** repurchase rate within 3 months of return is below 50%, or less than 15 percentage points above the control group.
4. **Credit doesn't pay:** credit cost per returning customer exceeds the combined retention, recovered material and data value.
5. **Gaming:** more than 5% of returned pairs show a large mismatch between recorded kilometres and physical wear.
6. **Evidence fails:** any shared Impact Record claim cannot be backed by its evidence, or the whole-shoe bio-based certification can't be obtained.
7. **Nobody shares:** fewer than 15% of active users share their Impact Record at least once.
8. **Tuning doesn't work:** tuned "Your Pair" variants deliver less than 10% more kilometres than the standard variant for comparable runners.
9. **Tuning costs too much:** the extra production cost of variants exceeds the value of the extra kilometres and retention they bring.

---

# MVP Mock-up Specification (for Lovable)

## 1. Purpose and scope

The mock-up shows the full loop from the runner's side and the business result from the brand's side: **fit → wear → see remaining life → earn credit → repair → return → tuned next pair → pass on or recover → share**. It uses **mock data only**: no real sensor, no Bluetooth or NFC, no camera, no payment, no authentication, no real sharing. Every action that would affect the real world is simulated and labelled as such. Predictions, gait profiles and tuning recommendations are pre-calculated in the mock data.

**Out of scope:** real pod pairing, real gait scanning, real shop and checkout, real certification lookups, user accounts, push notifications, real over-the-air updates.

## 2. Users

| Persona | Goal in the mock-up |
|---|---|
| Runner (primary, mobile view) | Get a well-fitting pair from day one, know how much life it has left, earn and use the credit, get a better-tuned next pair, show a credible record |
| Run club lead | See the club's shared record and run a local return and fit point |
| Brand team / product manager (desktop view) | See whether the loop works: kilometres per pair, returns, repurchase, tuning benefit, credit economics, test pilot results, open durability data |

A switcher in the header toggles between **Runner app** (shown in a phone-sized frame on desktop) and **Brand dashboard**. The run club view is a tab inside the Runner app.

Brand name in the mock-up: **"BRAND"** as a placeholder, easy to replace. All runner, model, club and partner names are fictional.

## 3. Screens: Runner app (mobile-first)

### 3.1 Fit Session (onboarding)
Solves the cold start: personalisation begins at purchase, not after the first pair.
1. **Choose how:** in store or at home with a short phone video (simulated: show a placeholder video frame and a progress bar).
2. **Three questions:** main surfaces (road / trail / track / mixed), typical weekly kilometres, preferred feel (softer / balanced / firmer).
3. **Result:** a **Fit Profile** card with foot strike (heel / mid / fore), wear zone to watch (e.g. "outer heel"), and the recommended model and variant (midsole Soft / Balanced / Firm × outsole Road / Trail grip).
4. **Pair the pod:** "Hold your phone near the shoe" with a simulated NFC animation and "Pod paired to Kanto Trail, Balanced".
Wording rule: fit and durability only. **No injury-prevention or health claims.**

### 3.2 My Pair (home)
- Current pair card: model, **variant**, purchase date, **kilometres run** (large number), and a **remaining-life bar** with the estimate in kilometres ("about 260 km left").
- Status message from the prediction: "Going strong", "Consider a resole in about 150 km", or "Time to replace: return this pair to unlock your full credit".
- **Credit card:** current credit percentage and euro value on the next pair, the next tier and kilometres to reach it ("140 km to 25%"). Show that the credit stops growing at the recommended lifespan.
- **"Your next pair is ready" banner** when about 100 km are left: links to the tuned recommendation in Return & Replace.
- **Feedback chip:** one tap "Feels worn already" / "Still feels fine". After tapping, show "Thanks: this goes into the next model update."
- Recent activity list: last 5 sessions with date, distance and surface.
- Buttons: **Book a repair**, **Return this pair**.

### 3.3 Material Passport
- Bio-based content (%) per component: upper, midsole, outsole, laces, adhesives.
- **Recovered content (%)**: share of the sole made from material recovered from returned pairs.
- Certification: scheme name (fictional), certificate number, valid until, and "View evidence" opening a mock certificate.
- Batch number and production site (fictional).
- Clear line: **"Bio-based does not mean biodegradable."**
- QR code the runner can show to anyone.

### 3.4 Rewards
- Tier table: Returned under 300 km = 10%; 300–599 km = 15%; 600–899 km = 25%; 900 km up to recommended lifespan = 35% (maximum). Bonuses: +5 points if the pair was repaired; +5 points permanently from the 3rd consecutive returned pair.
- Neutral tier names only: **Tier 1–4**.
- The runner's position highlighted, with a progress bar.
- Credit history with dates and amounts.
- "How it works": credit redeemed only by returning the worn pair; valid 12 months; usable on any model; kilometres count only when the pod is paired to the pair and detects walking or running.
- **Lifetime repair promise:** every pair can be repaired at partner prices for as long as the upper holds.

### 3.5 Return & Replace flow
1. **Confirm the pair:** model, variant, kilometres, repairs, calculated credit with breakdown (base tier + repair bonus + consecutive-return bonus).
2. **Choose how to return:** in store, at a run club point, or by mail (prepaid label).
3. **Your Pair, tuned:** the recommended next pair with a "Why this pair" panel built from the returned pair's data, e.g. "Your last pair wore fastest at the outer heel on trail. Kanto Trail, Firm midsole with Trail grip: runners with your pattern got 22% more kilometres from it." Show the alternative standard variant next to it, price, bio-based and recovered content, and price after credit ("€180 → €117"). The runner can pick either.
4. **Confirm:** summary badged **"Simulated — no order placed"**.

After confirming:
- The returned pair goes to **inspection** (simulated, after a short delay) with one of two outcomes: **"Passed on"** (refurbished and given to a new runner through the community) or **"Material recovered"** (goes into new soles). The outcome appears in the Impact Record.
- The pod shows "Ready to move to your new pair" and re-pairs with a simulated NFC tap.

### 3.6 Impact Record
- Lifetime summary: pairs, total kilometres, repairs, pairs returned, **pairs passed on**.
- One entry per pair: model, variant, kilometres, months in use, repairs, return outcome ("Passed on to a runner in Tampere" / "Material recovered into new soles").
- Comparison line where the data supports it: "Kept 40% longer than the average for this model".
- Every entry has an **"Evidence"** link: sensor record, repair record, return scan, inspection result, certificate.
- **Share card preview** with lifetime summary, current pair kilometres and a "verified by" QR code. Share buttons simulated ("Simulated — not posted"), including "Share to Strava" as a card image only.
- Privacy controls: public profile off by default, choose entries to show. Route and location data are never shown. Data imported from other apps is never shown on the card.
- No single green score, no "eco" badges, no climate-neutral wording.

### 3.7 Community
- **Run club:** the runner's club (fictional, e.g. "Kallio Runners") with a shared club record (members, total kilometres, pairs returned, pairs passed on), next fit-session day, and the club's return point.
- **Pass-on:** list of refurbished pairs available to club members at a reduced price, each with its own record ("Previous life: 410 km, inspected, new insole"). Reserve button simulated.
- **Test Pilot programme:** opt-in card explaining that test pilots run on small batches of new compounds, their wear data improves the next batch for everyone, and they get a +5 point credit bonus on the test pair. Join button with clear consent text.
- **Your data at work:** list of recent model updates the runner contributed to, e.g. "12 Oct: remaining-life prediction for Virta Road adjusted by 40 km using 214 returned pairs, including yours."

### 3.8 Book a Repair
- Options (resole, heel repair, upper patch) from a fictional repair partner or the club's repair day, with price, turnaround and added kilometres.
- Note that a repaired pair earns the +5 point bonus.
- Booking confirmation badged "Simulated".

## 4. Screens: Brand dashboard (desktop)

### 4.1 Loop Health
KPI tiles, each with its kill-criteria threshold and a status label (On track / At risk / Fails):
- Average kilometres per pair: pilot vs control (target +15%).
- Return rate of worn-out pairs (target 60%).
- Repurchase within 3 months: pilot vs control (target 50% and +15 points).
- **Tuning benefit:** kilometres from tuned variants vs standard variant (target +10%).
- Share rate (target 15%).
- Gaming flag rate (limit 5%).
- Evidence coverage (target 100%).
- **Pass-on rate:** share of returned pairs passed on rather than recovered.

Trend charts over 6 months: kilometres per pair, return rate and repurchase rate, pilot vs control.

### 4.2 Credit & Tuning Economics
- Per tier: credits issued, average credit, total cost.
- Value side as editable sliders: retention value, recovered material value, pass-on resale value, data value per returned pair, **extra production cost per tuned variant**.
- Result: cost vs value per returning customer, bar comparison and net figure. Turns red with "Credit doesn't pay" or "Tuning costs too much" when the relevant kill criterion is hit.

### 4.3 Material Wear Insights
- Remaining life vs kilometres per material batch (line per batch).
- Table: batch, material, average kilometres at return, predicted vs actual wear, outcome (Passed on / Recovered / Downcycled / Not recoverable).
- **Recovered content in production:** share of recovered material in new soles per month.
- 2–3 insight cards, e.g. "Midsole batch M-07 wears 18% faster on trail: review compound before next production run."

### 4.4 Test Pilot Fleet
- Active test batches: compound name, number of test pilots, average kilometres, wear rate vs the standard compound (chart with two lines).
- Decision column: Continue / Promote to production / Stop.
- Model update log: date, model, data used (number of returned pairs and feedback taps), change in prediction error, **"Automated"** or "Manual review" label.

### 4.5 Open Durability Data
- Preview of the **public durability page**: per model and batch, average kilometres at return, share passed on or recovered, and **batches that underperformed**, shown as plainly as the good ones.
- Toggle "Published" (simulated) and a "Last updated" date.
- Note: aggregated and anonymised; no individual runner data.

### 4.6 Gaming & Evidence Review
- Flagged returns with recorded kilometres, assessed wear and verdict (Accepted / Bonus voided).
- Impact Record entries missing evidence, with owner and status.

## 5. Data model (mock)

```
Runner        { id, name, joinedAt, consecutiveReturns, profilePublic, clubId, testPilot }
FitProfile    { runnerId, footStrike, wearZone, surfaces[], weeklyKm, feel, createdAt }
ShoeModel     { id, name, price, bioBasedPct, recoveredPct, recommendedLifespanKm, components[] }
Variant       { id, modelId, midsole, outsole, extraCostEur }
Component     { name, bioBasedPct }
Certificate   { id, scheme, number, validUntil, modelId }
Pair          { id, runnerId, modelId, variantId, batchId, purchasedAt, km, predictedRemainingKm, status, repairs[], returnedAt, returnOutcome }
Session       { id, pairId, date, km, surface }
Feedback      { id, pairId, value, date }
Repair        { id, pairId, type, date, partner, addedKm }
CreditTier    { minKm, maxKm, pct }
Credit        { id, runnerId, pairId, basePct, repairBonus, loyaltyBonus, testPilotBonus, amountEur, issuedAt, redeemedAt, expiresAt }
Recommendation { id, runnerId, fromPairId, variantId, reason, expectedKmGainPct }
ImpactEntry   { id, runnerId, pairId, text, evidenceType, evidenceRef, shared }
Club          { id, name, city, members, returnPoint, nextFitDay }
PassOnPair    { id, pairId, previousKm, refurbishment, price, reservedBy }
Batch         { id, material, site, avgKmAtReturn, outcome, isTestBatch, decision }
ModelUpdate   { id, date, model, returnsUsed, feedbackUsed, errorChangeKm, mode }
GamingFlag    { id, pairId, recordedKm, assessedWearKm, verdict }
PilotMetric   { month, group, kmPerPair, returnRate, repurchaseRate, shareRate, tunedKmGainPct, passOnRate }
```

## 6. Mock data requirements
- Runner "Aino K." with a Fit Profile (midfoot strike, outer-heel wear zone, mixed road and trail, 35 km a week, balanced feel), 3 returned pairs (2 recovered, 1 passed on), 1 current pair at 760 km of a 1,000 km lifespan with one repair, member of "Kallio Runners", not yet a test pilot.
- 4 fictional models ("Kanto Trail", "Virta Road", "Tuuli Race", "Polku Daily"), €150–€210, bio-based 88–96%, recovered content 0–20%, lifespan 800–1,100 km, each with 3 midsole × 2 outsole variants.
- 30 sessions; 3 fictional stores; 1 repair partner; 1 run club with 64 members and 5 pass-on pairs available.
- Dashboard: pilot 420 runners vs control 400 over 6 months. Kilometres per pair, return rate, share rate and tuning benefit (+14%) **On track**; repurchase **At risk** just under target; gaming 2.4%; pass-on rate 22%.
- 6 production batches (one wearing clearly faster on trail) and 2 test batches with 40 test pilots each, one outperforming the standard compound.
- 8 model updates over 6 months, the last 4 labelled "Automated".
- 12 gaming flags (10 accepted, 2 bonus voided).
- All names fictional. No real brands, certification bodies, stores, clubs or people.

## 7. Interactions and state
- Completing the Fit Session creates the Fit Profile and the first recommendation.
- A "simulate a run" slider on My Pair adds kilometres; remaining life, credit tier, next-tier progress and the "next pair is ready" banner update immediately.
- Feedback taps are added to the "Your data at work" count.
- Completing Return & Replace creates a credit, a new current pair with the chosen variant, an inspection outcome after a short simulated delay, and an Impact Record entry.
- Joining the Test Pilot programme sets the flag and adds the bonus to the next credit.
- Booking a repair extends remaining life and applies the repair bonus.
- Privacy toggles update the share card preview.
- Value sliders in Credit & Tuning Economics recalculate the net result live.
- **"Reset demo"** restores the original mock data. No data persists.

## 8. Visual design
- Runner app: warm, natural palette (off-white background, deep forest green accent, earthy neutrals), large numbers, generous spacing, rounded cards, in a phone frame on desktop. One hero number per screen.
- Brand dashboard: calm, dense layout with the same accent; status colours green / amber / red **always with a text label**.
- One clean sans-serif; kilometres and euros as the visual heroes.
- Formats: "760 km", "€117"; percentages without decimals in the runner app, one decimal in the dashboard.
- "Simulated" badges on anything that would order, post, book, scan or ship.
- Wording rules: specific measured facts only. Never "eco-friendly", "green", "planet-positive", "biodegradable" or "climate neutral" as claims. Never claim injury prevention or health benefits; fit and durability only.

## 9. Demo script (7 minutes)
1. **Fit Session:** run the 3 questions, show the Fit Profile and the recommended variant, pair the pod with the simulated NFC tap.
2. **My Pair:** 760 km, about 240 km left. Move the slider past 900 km; the credit reaches its maximum and "Your next pair is ready" appears.
3. **Return & Replace:** credit breakdown, return at the run club point, then "Your Pair, tuned" with its "Why this pair" explanation. Confirm; the inspection marks the old pair "Passed on".
4. **Impact Record:** new entry with evidence; open the share card.
5. **Community:** club record, a pass-on pair, join the Test Pilot programme, and "Your data at work".
6. **Brand dashboard:** Loop Health (tuning benefit on track, repurchase at risk), then Test Pilot Fleet and the automated model updates.
7. **Open Durability Data:** show the underperforming batch published plainly; then raise the tuned-variant cost slider in Economics until "Tuning costs too much" appears.

## 10. Copy-paste prompt for Lovable

```
Build a clickable MVP mock-up called "Long Use" for a sports shoe brand (placeholder brand name "BRAND"). The shoes are made from certified bio-based materials and carry a reusable sensor pod. Use React with mock data in local state only: no backend, no auth, no Bluetooth/NFC, no camera, no payments, no real sharing. Anything that would order, post, book, scan or ship is badged "Simulated".

Header switcher: "Runner app" (rendered in a phone-sized frame on desktop) and "Brand dashboard" (desktop).

Runner app screens:
1. Fit Session (onboarding): choose in store or at-home phone video (placeholder frame + progress bar); 3 questions (surfaces road/trail/track/mixed, weekly km, preferred feel softer/balanced/firmer); result Fit Profile card (foot strike, wear zone to watch, recommended model and variant: midsole Soft/Balanced/Firm × outsole Road/Trail grip); pod pairing with a simulated NFC animation. Fit and durability wording only, no injury or health claims.
2. My Pair (home): model, variant, purchase date, km run (large), remaining-life bar "about X km left", status message ("Going strong" / "Consider a resole in about X km" / "Time to replace: return this pair to unlock your full credit"), credit card with current % and € value and progress to next tier ("140 km to 25%"), a "Your next pair is ready" banner when about 100 km are left, a one-tap feedback chip ("Feels worn already" / "Still feels fine") that confirms "Thanks: this goes into the next model update", last 5 sessions, buttons "Book a repair" and "Return this pair". Include a "simulate a run" slider that updates everything live.
3. Material Passport: bio-based % per component (upper, midsole, outsole, laces, adhesives), recovered content % from returned pairs, certification scheme, certificate number, valid-until, "View evidence" mock certificate, batch, QR code, and the line "Bio-based does not mean biodegradable."
4. Rewards: tiers (under 300 km = 10%, 300–599 = 15%, 600–899 = 25%, 900 up to recommended lifespan = 35% max; +5 points if repaired; +5 points permanently from the 3rd consecutive return). Neutral names Tier 1–4. Runner's position, credit history, "How it works" (redeemed only by returning the worn pair, valid 12 months, any model, km counted only when pod is paired and detects walking or running), and a lifetime repair promise.
5. Return & Replace: 4 steps — confirm pair with credit breakdown; return in store, at a run club point, or by mail; "Your Pair, tuned": recommended next pair with a "Why this pair" panel from the returned pair's wear data (e.g. "Your last pair wore fastest at the outer heel on trail. Kanto Trail, Firm midsole with Trail grip: runners with your pattern got 22% more kilometres from it.") beside the standard variant, with price, bio-based and recovered %, and price after credit ("€180 → €117"); confirm, badged "Simulated — no order placed". Afterwards a simulated inspection marks the old pair "Passed on" or "Material recovered", it becomes an Impact Record entry, and the pod re-pairs with a simulated NFC tap.
6. Impact Record: lifetime summary (pairs, km, repairs, returned, passed on); entries per pair (model, variant, km, months, repairs, return outcome) each with an "Evidence" link (sensor, repair, return scan, inspection, certificate); comparison line; share card with "verified by" QR; share buttons including "Share to Strava" (image only), badged "Simulated — not posted"; privacy controls (public off by default, choose entries; route, location and imported data never shown). No green score, no eco badges, no climate-neutral wording.
7. Community: run club "Kallio Runners" with shared club record (members, km, pairs returned, pairs passed on), next fit-session day and return point; pass-on list of refurbished pairs with "Previous life" records and a simulated Reserve button; Test Pilot programme opt-in (small batches of new compounds, data improves the next batch for everyone, +5 point bonus, clear consent text); "Your data at work" list of model updates the runner contributed to.
8. Book a Repair: resole, heel repair, upper patch from a fictional partner or the club repair day, with price, turnaround and added km; booking extends remaining life and applies the +5 bonus.

Brand dashboard screens:
1. Loop Health: KPI tiles with targets and status labels (On track / At risk / Fails): km per pair pilot vs control (+15%), return rate (60%), repurchase in 3 months pilot vs control (50% and +15 points), tuning benefit tuned vs standard variant (+10%), share rate (15%), gaming rate (limit 5%), evidence coverage (100%), pass-on rate. Trend lines over 6 months, pilot vs control.
2. Credit & Tuning Economics: per-tier credits, average credit, total cost; sliders for retention value, recovered material value, pass-on resale value, data value per returned pair and extra production cost per tuned variant; live cost vs value with red states "Credit doesn't pay" and "Tuning costs too much".
3. Material Wear Insights: remaining life vs km per batch; table (batch, material, avg km at return, predicted vs actual wear, outcome Passed on / Recovered / Downcycled / Not recoverable); recovered content in production per month; 2–3 insight cards.
4. Test Pilot Fleet: test batches with pilots, avg km, wear vs standard compound (two-line chart), decision Continue / Promote / Stop; model update log (date, model, returns and feedback used, change in prediction error, label "Automated" or "Manual review").
5. Open Durability Data: preview of a public page per model and batch (avg km at return, share passed on or recovered) showing underperforming batches as plainly as good ones; simulated "Published" toggle and last-updated date; aggregated and anonymised only.
6. Gaming & Evidence Review: flagged returns (recorded km, assessed wear, verdict Accepted / Bonus voided); entries missing evidence.

Mock data: runner "Aino K." with Fit Profile (midfoot strike, outer-heel wear zone, mixed road and trail, 35 km/week, balanced), 3 returned pairs (2 recovered, 1 passed on), current pair at 760 of 1,000 km with one repair, member of "Kallio Runners" (64 members, 5 pass-on pairs), not yet a test pilot. 4 fictional models ("Kanto Trail", "Virta Road", "Tuuli Race", "Polku Daily") €150–€210, bio-based 88–96%, recovered 0–20%, lifespan 800–1,100 km, each with 3 midsole × 2 outsole variants. 30 sessions, 3 stores, 1 repair partner. Dashboard: pilot 420 vs control 400 over 6 months; km per pair, return rate, share rate and tuning benefit (+14%) On track; repurchase At risk; gaming 2.4%; pass-on 22%; 6 production batches (one wearing faster on trail); 2 test batches of 40 pilots, one outperforming standard; 8 model updates, last 4 Automated; 12 gaming flags (10 accepted, 2 voided). All names fictional.

Add a "Reset demo" button. No data persists.

Style: runner app warm and natural (off-white, deep forest green accent, earthy neutrals, rounded cards, one hero number per screen); dashboard calm and dense with the same accent; status colours always with text labels; formats "760 km", "€117". Never use eco-friendly, green, planet-positive, biodegradable or climate neutral as claims, and never claim injury prevention or health benefits. Responsive down to tablet width.
```
