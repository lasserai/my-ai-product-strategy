# Data Flywheel Map

> Product: certified biomaterial sports shoe with a reusable sensor pod and the "Long Use" app (fit session, remaining-life prediction, Long Use Reward credit, tuned next pair, pass-on and test pilot community, verified Impact Record).
> The AI outputs being scored are the **remaining-life prediction** per pair and the **tuned next-pair recommendation**.
> Score each loop 1-5. Your weakest loop is where competitors attack first.
> Each loop shows the baseline score and the target after the strengthening plan, which is built into the updated prototype spec (`01-the-bet/prototype-biomaterial-shoe.md`).

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Baseline | Target |
|------|------------------|---------|---------|----------|--------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 3/5 | 5/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 2/5 | 4/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 3/5 | 4/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 2/5 | 4/5 |

### Correction Loop - 3/5 → target 5/5
**What you capture today:**
- **Physical wear at return.** Every returned pair is inspected and compared with its predicted remaining life. The credit is paid only on return, so this is a labelled sample per pair.
- **Runner feedback.** One tap "Feels worn already" / "Still feels fine" on My Pair.
- **Repairs.** A resole booked earlier or later than predicted corrects the wear curve.
- **Gaming flags.** Mismatches between recorded kilometres and physical wear correct the kilometre counting itself.

**How it compounds:**
More returns give more precise wear curves per batch, surface and runner profile. Better predictions make the credit fairer and the durability figures defensible, which builds trust and drives more returns.

**Strengthening move:**
- Return inspections and feedback taps feed a **scheduled, automated model update**; an update is also triggered automatically when prediction error on recent returns crosses a threshold.
- Pod firmware gets **over-the-air updates**, so kilometre counting improves for every pod already in use.
- Runners see the effect in **"Your data at work"**: "Prediction for Virta Road adjusted by 40 km using 214 returned pairs, including yours." Seeing their correction used makes runners keep correcting.

### Preference Loop - 2/5 → target 4/5
**What you capture today:**
- Gait pattern, surfaces, session length and weekly kilometres from the pod.
- Repair choices and which model the runner picked at replacement.

**How it compounds (baseline):**
Barely. Advice is generic until the first pair is worn out, and app-level advice is where Strava and Garmin are stronger, because they hold the runner's whole training history.

**Strengthening move: make personalisation physical.** Software platforms track kilometres; only we make the shoe.
- **Fit Session at purchase** (in store or by phone video) creates a Fit Profile: foot strike, wear zone, surfaces, preferred feel. Personalisation starts on day one, which fixes the cold start.
- **"Your Pair, tuned"** at replacement: the returned pair's wear pattern picks the next pair's midsole firmness and outsole compound, starting with 3 × 2 variants per model rather than full custom. "Why this pair" explains it in the runner's own data.
- **"Your next pair is ready"** about 100 km before end of life, so the replacement moment is ours before any trade-in offer arrives.
- **Training context** imported with consent from Apple Health and Garmin Connect where their terms allow use in models. **Not from Strava**, whose API agreement prohibits using its data in AI models.
- Preference compounds pair by pair: each return makes the next pair fit better, better fit gives more kilometres, more kilometres give a bigger credit, and the runner comes back.
- Not 5 until variants show a measured benefit at scale; the pilot kill criterion is +10% kilometres from tuned vs standard variants.

### Domain Context Loop - 3/5 → target 4/5
**What you capture today:**
- Wear by material batch, component, surface, climate and runner weight.
- Return outcomes: passed on, recovered, downcycled or not recoverable.
- Repair outcomes: how much life each repair type adds.

**How it compounds:**
- **Use → material R&D:** trail wear data improves compounds for road models too.
- **Use → production:** a batch wearing faster than predicted triggers a quality review before the next run.
- **Use → recovery:** knowing which materials come back in which condition improves recovery.
- **Use → claims:** real-world durability replaces lab-only figures.

**Strengthening move:**
- **Closed material loop:** recovered material goes back into new soles, shown as "recovered content %" in the Material Passport. Recovery becomes a material supply, not just a cost, which helps pay for the credit.
- **Wear data becomes a required input** to material, variant and production decisions, not just a dashboard people may read.
- **Open durability data:** a public page per model and batch, including batches that underperformed. It turns internal learning into external trust and holds the brand to its own evidence.

### Network Loop - 2/5 → target 4/5
**What you capture today:**
- Pooled wear data per model and batch.
- Population averages for Impact Record comparisons.
- Shared Impact Record cards (a reach effect, not a network effect).

**How it compounds (baseline):**
Each new runner improves predictions for others on the same model, but this flattens out after a few thousand runners per model.

**Strengthening move: give runners direct value from each other.**
- **Test Pilot fleet:** volunteers run small batches of new compounds. Their wear data decides which compound goes into production, so every test pilot improves the next shoe for everyone. Test pilots earn a credit bonus.
- **Pass-on:** returned pairs with life left are refurbished and offered to club members at a reduced price, each with its "previous life" record. More runners means more pairs passed on and more choice for everyone.
- **Run club hubs:** clubs act as local return, repair and fit-session points with a shared club record. The denser the network, the more convenient returns and repairs become for each runner, which raises return rates and data for all.
- Not 5 because the network is local and physical: it grows city by city, not virally.

**Total Flywheel Score: 10/20 baseline → 17/20 target**
**Weakest Loop:** Preference (2/5). It is where an attacker strikes first: Strava and Garmin already hold each runner's training history and gear mileage, so they win any contest of app-level advice.
**Fix for weakest loop:**
Move the contest from advice to the product. Fit Session for day-one personalisation, "Your Pair, tuned" from the returned pair's wear data, and "Your next pair is ready" before end of life. Build it on our own pod data, return inspections and consented Apple Health or Garmin data, never Strava data. Measure it with the pilot kill criterion: tuned variants must deliver at least 10% more kilometres, at a production cost the extra kilometres and retention can carry.

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** Strava, with Garmin Connect close behind. Both already track shoe mileage as gear and can remind runners to replace.
**Vector:** Upgrade gear tracking into personalised wear prediction for every brand, using the full training history they hold, and sell the replacement moment to brands and retailers as in-app trade-in offers.
**Time-to-threat:** 12–24 months.
**% of value at risk:** ~30% at baseline, falling to ~15% once tuned pairs and the "next pair is ready" moment are live. Tracking and reminders are exposed; the tuned physical product, inspection, credit and take-back are not.

### 2. Vertical Competitor
**Attacker:** A major sports brand with a circular programme, for example On, whose Cyclon subscription already takes shoes back for recycling.
**Vector:** Certified bio-based line plus trade-in credit, shareable record and possibly personalised variants, with global distribution.
**Time-to-threat:** 18–36 months.
**% of value at risk:** 40–50%. They can copy the loop; the defence is accumulated wear data per runner, published durability data and community density in our cities, all of which take years to build.

### 3. Adjacent Expansion
**Attacker:** Multi-brand running retailers and resale or recycling platforms offering brand-agnostic trade-in.
**Vector:** "Bring any worn pair, get credit on any brand" removes our replacement-moment lock-in without a sensor or app.
**Time-to-threat:** 6–12 months.
**% of value at risk:** 20–30%, falling as the tuned next pair gives a reason to stay that a flat trade-in can't match. Run clubs as return points compete directly with retailer counters.

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:** Strava

**Attack vector (target the weakest loop):** Preference. Strava knows every runner's full training history, routes, pace and gear across all brands, personalises shoe advice better than our app, then owns the replacement moment.

**Weeks 1-4 - what they ship:**
"Smart Gear": personalised remaining-life estimates for every shoe in a runner's gear list, from mileage, pace, surface and body weight. Replace alerts in the activity feed. No hardware needed.

**Weeks 5-8 - how they poach users:**
- Trade-in offers from partner brands and retailers at the alert: "Your shoes hit 750 km: €30 off your next pair."
- A "Gear story" share card in the feed where runners already share.
- Our runners already log runs in Strava, so they see this without installing anything.

**Weeks 9-12 - why users don't come back:**
The runner's identity and community live in Strava. Our app becomes the second place to look, and a runner without a big credit takes the partner offer.

**Your defense:**
1. **Win on the product, not the advice.** Strava can predict wear; it can't make the next pair fit better. "Your Pair, tuned" and the Fit Session are the answer to "Smart Gear".
2. **Get to the replacement moment first.** "Your next pair is ready" fires about 100 km before end of life, with the credit and the tuned pair already shown.
3. **Own what software can't:** physical inspection at return, certified material data, recovered content, repair and pass-on, and a credit tied to physical return.
4. **Be inside Strava as a sharing channel only.** Runners share their own Impact Record card, with the evidence QR, to Strava. We never use Strava data in our models, which its API terms prohibit.
5. **Raise exit cost early and locally.** Credit visible from the first kilometre, the permanent bonus from the 3rd return, the test pilot bonus, and the run club where returns, repairs and pass-on happen. Leaving means leaving the club's loop, not just an app.
6. **Make credibility the brand.** Publish durability data openly, including what failed. Under EU rules since 27 September 2026, only evidence-backed claims can be shown, and we hold the evidence.

---

### Sources

- [TLT: Empowering Consumers for the Green Transition Directive, what to do before September 2026](https://www.tlt.com/insights-and-events/insight/the-eu-is-empowering-consumers-for-the-green-transition-directive-what-your-business-needs-to-do-before-september-2026)
- [Cyclingnews: Strava plan to restrict third-party apps has users in an uproar](https://www.cyclingnews.com/news/strava-plan-to-restrict-third-party-apps-has-users-in-an-uproar)
- [Retail Dive: Adidas, Allbirds release low-carbon running shoe](https://www.retaildive.com/news/adidas-allbirds-release-low-carbon-running-shoe/611671)
