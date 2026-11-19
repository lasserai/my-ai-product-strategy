# Kill Switch Audit

> Product: certified biomaterial sports shoe with a reusable sensor pod and the "Long Use" app (fit session, remaining-life prediction, Long Use Reward credit, tuned next pair, pass-on and test pilot community, verified Impact Record).
> Assumed stack, to be confirmed:
> - **Own models:** remaining-life prediction and next-pair tuning, trained on pod data, fit profiles and return inspections, hosted on one cloud platform, with **automated retraining**.
> - **Gait scan:** the at-home Fit Session uses a computer-vision pose-estimation model, either a vendor API or an open model.
> - **LLM API** from one provider writes plain-language text: "Why this pair", insight cards and support answers.
> - **Sensor pod** and its firmware, including over-the-air updates, from one supplier.
> - **Variant production** (3 midsoles × 2 outsoles per model) at one contract manufacturer; **material recovery** at one partner.
> - **Training context** imported with consent from Apple Health and Garmin Connect only. Strava is a sharing channel, never a data source.

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Single source for each critical piece: one LLM provider, one cloud platform, one gait-scan model, one pod supplier, one contract manufacturer for variants, one recovery partner. The strengthening plan added three new dependencies (gait scan, variant production, closed material loop), and each one now sits on the path to the weakest-loop fix. | **H** | List every dependency with owner, contract term, exit option and which flywheel loop it feeds. Name a second candidate for the gait-scan model (an open pose-estimation model we can host), the pod and the recovery partner. Confirm that Apple Health and Garmin terms allow use of their data in our models; if not, drop them. Confirm no Strava data enters any model or shared card. |
| **Abstraction** | Prototype built fast, so LLM and vision calls are likely embedded in app code. Fit Profiles may be stored in the vision vendor's format. Variant specifications may live only in the manufacturer's systems. | **M** | Put LLM and vision calls behind internal interfaces. Store Fit Profiles as our own schema (foot strike, wear zone, surfaces, feel), not as vendor output. Keep model features, training data and model files in open formats. Own the variant specifications and the pod data format as our documents, shareable with a second manufacturer or supplier. |
| **Routing** | No fallbacks defined. If the gait-scan API fails, the Fit Session stops. If the LLM fails, "Why this pair" is empty. The core functions must not depend on either, but this isn't verified. | **H** | Confirm prediction, tuning, credit and Impact Record run with **no LLM and no vision vendor in the path**. Fallbacks: the Fit Session falls back to an in-store fit or the 3-question profile; "Why this pair" falls back to templated text filled from the runner's own data; routine text routes to a smaller, cheaper model. |
| **Eval** | Strong ground truth: every returned pair's physical wear, and tuned vs standard variant kilometres. Automated retraining is planned but has **no gate**, so a bad update could reach every runner. LLM text has no compliance check. | **H** | (1) Golden set of 200 returned pairs: every automated model update must beat the current model on it before release, with automatic rollback if prediction error on new returns worsens. (2) Tuning eval: tuned vs standard kilometres for comparable runners, reported monthly. (3) Text compliance eval on 100 samples: no banned green claims ("eco-friendly", "green", "biodegradable", "climate neutral"), **no injury or health claims**, and every number traceable to evidence. (4) Gait-scan check: scan result vs in-store fit for 50 runners. |

## Portability Score
**Partial.**

- **Ready:** remaining-life and tuning models (own models, own data, own ground truth from returns), credit rules, Impact Record evidence chain, Fit Profile schema once stored in our format.
- **Partial:** the LLM text layer and the gait-scan model, until each sits behind an interface with an eval set and fallback; the cloud platform, until data and models are in open formats.
- **Locked:** the sensor pod (single supplier, proprietary firmware and update channel), variant production (single contract manufacturer with our variant tooling), and the material recovery partner (the closed loop depends on their process).

The strengthening plan moved risk from software into **physical operations**. Software dependencies can be swapped in days; the pod, the manufacturer and the recovery partner take months.

Target: **Ready** for software within one quarter; for physical dependencies, a qualified second source for each within two production cycles.

## If the LLM provider doubles pricing tomorrow:

**48-hour response:**
1. **Hour 0–4: confirm blast radius.** The LLM is not in the critical path. Prediction, tuning, credit, returns and the Impact Record keep working. Only explanation text, "Why this pair", insight cards and support answers are affected.
2. **Hour 4–12: cut volume.** Most text depends on a finite set of states (pair status × credit tier × repair state × variant recommendation). Pre-generate and cache it, or switch to templates filled with the runner's own data.
3. **Hour 12–24: reroute.** Move routine text to a smaller model or the second provider through the abstraction layer, after it passes the text compliance eval.
4. **Hour 24–48: decide.** Keep the original provider only for support answers if it clearly wins on the eval set.

**Worst case:** turn the LLM off. The app works with templated text.

**Same logic for the other vendors:**
- **Gait-scan model:** switch to a self-hosted open pose-estimation model, or fall back to in-store fit and the 3-question profile. Personalisation starts slightly less precise but still starts on day one.
- **Pod supplier:** a price doubling hits the hardware bill of materials. Absorb it for one season through the credit economics, use our published pod specification to qualify a second supplier, and keep the pod reusable across pairs so its cost spreads over many shoes.
- **Contract manufacturer:** if variant production doubles in cost, cut from 3 × 2 to the 2 or 3 variants with the largest measured benefit; the tuning eval shows which. The "Tuning costs too much" kill criterion in the pilot decides whether variants survive at all.
- **Recovery partner:** recovered content in new soles falls back to virgin bio-based material for a season; returns continue, pass-on increases.

## If a vendor ships a competing product:

The real competing-product risks come from the **data platforms** (Strava and Garmin adding wear prediction and trade-in offers) and the **contract manufacturer**, which now knows our variant specifications and could supply a large brand with the same approach.

**What's defensible that they can't replicate:**
- **The tuned next pair.** Built from each runner's returned pair and Fit Profile. A platform can predict wear but can't make the next shoe fit better.
- **Physical ground truth.** Every returned pair is inspected against its recorded use. Software platforms see kilometres, never the shoe.
- **Accumulated per-runner history** across several pairs, plus our own pod data, owned with the runner's consent and independent of any platform's API terms.
- **Certified material data and the closed material loop**, with recovered content shown per pair.
- **The credit tied to physical return**, which a mileage-based trade-in can't verify.
- **Community operations:** run club return and fit points, pass-on, the test pilot fleet and the repair network. These grow city by city and take years to copy.
- **Open durability data**, including failures. A competitor can match it only by publishing their own.
- **The evidence chain behind every claim.** Under EU rules since 27 September 2026, only evidence-backed sustainability claims can be shown.

**Against the manufacturer risk:** keep the tuning model and runner data in-house, so the manufacturer only ever receives variant specifications, not the logic that assigns them. Include confidentiality and exclusivity terms for the variant tooling in the contract, and qualify a second manufacturer.

**Implication for the Data Flywheel:** the Preference fix is only defensible while it rests on data we own: pod data, Fit Profiles, return inspections and tuned-variant results. Apple Health and Garmin data are useful extras, only where their terms allow; Strava stays a sharing channel.

---

### Sources

- [Cyclingnews: Strava plan to restrict third-party apps has users in an uproar](https://www.cyclingnews.com/news/strava-plan-to-restrict-third-party-apps-has-users-in-an-uproar)
- [Velo: Strava API update means changes to the fitness app ecosystem](https://velo.outsideonline.com/news/strava-api-update-means-changes-to-the-fitness-app-ecosystem?scope=anon)
- [TLT: Empowering Consumers for the Green Transition Directive, what to do before September 2026](https://www.tlt.com/insights-and-events/insight/the-eu-is-empowering-consumers-for-the-green-transition-directive-what-your-business-needs-to-do-before-september-2026)
