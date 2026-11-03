# Three-Axis Vulnerability Diagnostic

## Product

**Product:** Enterprise ESG data portfolio (operational, supplier and third-party sustainability data, plus the models, lineage and governance around it)
**Your Role:** Lead Information Architect

> Assumption: the portfolio is used internally to feed sustainability reporting, management steering and investor/customer requests. It is not sold externally.
> Scoring note: for Platform Exposure, 5 = most exposed (high is bad). For the other two axes, 5 = strongest.

---

## Scores

### Contextual Moat — 3/5
*Workflow depth × switching cost. Would users leave in a weekend if a competitor showed up?*

**Score rationale:**
The workflow is deep. The portfolio pulls from ERP, HR, energy, procurement and supplier sources, and its lineage and audit trail are what the auditor relies on for assurance. Nobody replaces that in a weekend. But the moat protects the *integration work*, not the *design*. If a vendor ships a ready-made ESRS-aligned data model on our core platform, migrating becomes a project rather than a rebuild. The real lock-in is assurance, because auditors dislike changes to data lineage mid-cycle.

**Named attacker (from partner challenge):**
The ERP or data-platform vendor's native sustainability module, for example SAP's sustainability suite (if on SAP) or Microsoft's sustainability data solutions in Fabric (if on Azure). Reporting platforms such as Workiva are the second option.

---

### Data Advantage — 2/5
*Proprietary signal that compounds with usage. What do you see that OpenAI doesn't?*

**Score rationale:**
The data is proprietary, since no model provider has our site-level emissions, energy or supplier figures. But the axis asks for signal that *compounds with usage*, and compliance data mostly doesn't. Collecting the 2026 figures doesn't make 2027's smarter. Purchased outside-in ESG data (ratings, controversies) is something every competitor can buy too. The only compounding asset is supplier-specific primary data for Scope 3, if we are building it up over time.

**Named attacker (from partner challenge):**
Supplier-data networks such as CDP or EcoVadis, which aggregate the same supplier data across thousands of buyers and beat any single company's collection effort. MSCI, LSEG and Bloomberg cover outside-in data.

---

### Platform Exposure — 4/5 (high)
*Encroachment risk × pivot speed. If Apple/Google/OpenAI ships your hero feature native — then what?*

**Score rationale:**
There are two pressures at once:

- **Technology:** AI agents can now map messy source data to disclosure datapoints and draft the narrative text. Mapping and structuring are the team's core value, and that is exactly what is being automated.
- **Regulation:** Omnibus I (Directive (EU) 2026/470) is final law, in force since 18 March 2026. CSRD scope dropped from an estimated ~50,000 to ~5,000 companies. Only EU entities with more than 1,000 employees and over €450M net turnover are in scope. If the company sits near those thresholds, much of the demand for the portfolio could disappear.

Pivot speed is the saving grace. An information architecture team can reposition faster than a product team, for example by becoming the governed semantic layer that AI agents and vendor modules query rather than compete with.

**Named attacker (from partner challenge):**
An ERP vendor shipping a native, assurance-ready ESRS data model with AI-generated disclosures. The regulatory "attacker" is Omnibus I itself, which shrinks the reason the portfolio exists.

---

## Top Vulnerability

The portfolio's value is tied to compliance demand and integration plumbing. Regulation is shrinking the first, and ERP-native AI is commoditising the second, so the portfolio risks being reframed as a cost centre that a vendor module could replace.

## Confidence Level

**M**. Three facts would firm this up:

1. Does the company stay in CSRD scope after Omnibus I?
2. Which ERP or data platform does the portfolio run on?
3. Is the data used for decisions beyond reporting, such as pricing, procurement, financing or product? A real Data Advantage would come from that use.

---

### Sources

- [dcycle: CSRD reporting timeline after Omnibus I](https://dcycle.io/blog/csrd-reporting-timeline-post-omnibus/)
- [AKD: Changes to the CSRD, Omnibus Directive enters into force on 18 March 2026](https://www.akd.eu/insights/provisional-agreement-on-omnibus-i-changes-to-the-scope-and-reporting-obligations-under-the-csrd)
