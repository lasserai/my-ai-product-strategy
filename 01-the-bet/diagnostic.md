# Three-Axis Vulnerability Diagnostic

## Product

**Product:** Sports shoe made only from certified biomaterials, with a reusable sensor pod and an app that tracks how the shoe is used and gives the user a verified, shareable sustainability record
**Your Role:** Product Manager

> Assumption: a consumer product sold in the EU. The sensor is a removable pod that moves from pair to pair. The app does three things: (1) tracks foot-level use and material wear, (2) tells the user when to repair, rotate or return the shoe, and (3) builds a personal **Impact Record**, a verified, shareable account of the user's footwear choices.
> Scoring note: for Platform Exposure, 5 = most exposed (high is bad). For the other two axes, 5 = strongest.

---

## The sustainability image feature: Impact Record

The user's sustainability image is built from **verifiable facts, not scores or self-made badges**. Under the EU green claims rules that have applied since 27 September 2026, generic claims and self-created sustainability labels are banned, so the feature is designed to be compliant from the start. That compliance is also what competitors with vague claims can't copy.

What the Impact Record contains:

| Entry | Example the user can share | Proof behind it |
|---|---|---|
| Material passport per pair | "My shoes: 94% bio-based content, certified" | Third-party certification of bio-based content to a recognised standard, linked by QR code |
| Kilometres per pair | "This pair has carried me 820 km" | Sensor data, timestamped |
| Longer use | "I've kept this pair 40% longer than the average for this model" | Comparison with the anonymised user base |
| Repairs | "Resoled once, March 2027" | Repair partner record |
| Return and recovery | "Returned for material recovery on 12 Jan 2028" | Take-back scan at the store or by mail |
| Lifetime summary | "4 pairs, 3,100 km, 4 returned" | Sum of the entries above |

Sharing options: a public profile link, a shareable card for social media and Strava, and a "verified by" QR code that anyone can scan to see the evidence.

Design rules that keep it credible and legal:
- **No single green score, no "eco-hero" badges, no climate-neutral claims.** Only specific, measured facts, each with its evidence one tap away.
- **No implied biodegradability** unless that is separately certified.
- **The user controls sharing.** Nothing is public by default, and the location history behind the kilometres is never shared.

---

## Scores

### Contextual Moat — 3/5 (up from 2)
*Workflow depth × switching cost. Would users leave in a weekend if a competitor showed up?*

**Score rationale:**
Shoes are still a replacement purchase, so each new pair is a chance to switch brand. But the Impact Record changes what switching costs. A user who has built up years of verified kilometres, repairs and returns loses that continuous record by moving to another brand. They can export the raw data, but not the verification chain. The reusable pod pulls the same way: the user already owns it, and it only works with our shoes.

The take-back loop adds a physical lock-in. Returning a worn pair is the natural moment to buy the next one, and the return is itself an entry in the Impact Record.

It isn't higher than 3 because the identity value only holds while users care about showing it, and that depends on the community seeing it.

**Named attacker (from partner challenge):**
Large brands running their own circular programmes, for example On's Cyclon subscription, where shoes are returned for recycling. If such a brand adds a verified, shareable record, it can match the feature with much larger distribution.

---

### Data Advantage — 3/5 (upside to 4) (up from 2)
*Proprietary signal that compounds with usage. What do you see that OpenAI doesn't?*

**Score rationale:**
Dropping life balance removes the weak half of the data story. What's left is data nobody else has:

- **Material wear in real use:** how each biomaterial and batch ages per kilometre, per surface, per runner weight and gait. This feeds the next material choice, durability claims and replacement guidance.
- **The verified lifecycle chain:** material certification → use → repair → return → recovery, per pair. That chain is the evidence behind every claim, both the brand's and the user's.
- **Return and recovery outcomes:** which returned materials can actually be recovered, and in what quality.

This compounds: more kilometres make durability claims more precise, more returns improve recovery processes, and better claims attract users who generate more data.

It goes to 4 if the data starts changing the product, i.e. material and design decisions are visibly driven by wear data, and the durability claims on the box come from it.

**Named attacker (from partner challenge):**
Gear-mileage features in Strava and Garmin Connect, and foot pods such as Stryd. They capture kilometres and gait but not material, certification or recovery data. They can't verify the chain, but they make "kilometres per pair" alone a commodity.

---

### Platform Exposure — 3/5 (down from 4)
*Encroachment risk × pivot speed. If Apple/Google/OpenAI ships your hero feature native — then what?*

**Score rationale:**
Taking out life balance removes the direct conflict with Apple Watch, Garmin, Oura and Whoop. The app no longer competes with them; it can send kilometres and gait into Apple Health and Garmin Connect and benefit from their ecosystems. Their native features can't produce a verified material and lifecycle record, because they don't control the shoe.

Regulation now works for the product rather than against it. The EU green claims rules ban generic claims and self-made sustainability labels for all traders selling to EU consumers. A brand whose every claim is specific and evidenced is positioned well, while competitors relying on vague "eco" language are forced to retreat. Footwear is not on the EU's first priority list for digital product passports, which leaves room to lead voluntarily with a material passport before it becomes mandatory.

Remaining exposure:
- **Big brands with distribution** can launch certified bio-based shoes and copy the Impact Record.
- **Social platforms** decide how shared cards are shown, so reach depends on Strava, Instagram and others.
- **Hardware pivot speed is slow.** Material sourcing and tooling run on long cycles.

**Named attacker (from partner challenge):**
A major sports brand launching a certified bio-based line with a take-back programme and a shareable record. Secondarily, Strava adding verified gear and sustainability fields to its existing gear tracking.

---

## Top Vulnerability

The case now rests on **trust in the evidence chain**. If a single certification, durability or recovery claim proves wrong, the Impact Record stops being a sustainability asset and becomes a greenwashing liability, both for the brand and for the users who shared it. Credibility has to be engineered: third-party certification, public evidence behind every entry, and no claim larger than the data supports.

## Confidence Level

**M** (up from L). Removing life balance and adding the Impact Record ties the shoe, the pod and the app into one loop: certified material → measured use → repair and return → verified record → next purchase. Four facts would firm this up:

1. Can the bio-based content be certified for the whole shoe, including sole and adhesives?
2. Is there a take-back and material recovery partner ready at launch?
3. Will target users actually share their record? A quick test with 20–30 runners would show this.
4. How much does the pod cost compared with the price premium users accept?

---

### Sources

- [TLT: Empowering Consumers for the Green Transition Directive, what to do before September 2026](https://www.tlt.com/insights-and-events/insight/the-eu-is-empowering-consumers-for-the-green-transition-directive-what-your-business-needs-to-do-before-september-2026)
- [Sidley: European Commission releases list of priority products (ESPR)](https://www.sidley.com/ja/insights/newsupdates/2025/04/european-commission-releases-list-of-priority-products)
- [MobiHealthNews: After just two years, Under Armour is killing HealthBox suite of connected devices](https://www.mobihealthnews.com/news/after-just-two-years-under-armour-killing-healthbox-suite-connected-devices)
- [Retail Dive: Adidas, Allbirds release low-carbon running shoe](https://www.retaildive.com/news/adidas-allbirds-release-low-carbon-running-shoe/611671)
