# Pain Points

## Source

- **Primary input**: `outputs/phase-01/persona.md`
- **Skill used**: `skills/pain-point-extractor.md`
- **Evidence limitations**:
  - All personas were synthesized from one business requirements document, so repeated statements across its sections are not independent corroboration.
  - The source contains no participant count, recruitment criteria, raw research notes, interview transcripts, observations, survey data, behavioural analytics, support-contact analysis, or source dates.
  - Statements presented as things users “often say” have no participant or study provenance and are business claims rather than verified quotations.
  - The three personas are provisional, overlapping need-based archetypes rather than validated, mutually exclusive customer segments.
  - The source does not establish the prevalence or relative priority of the personas or pain themes.
  - Proposed percentages and improvements are success targets, not observed outcomes.
  - Assumptions about self-service preference, pricing comprehension, and the value of AI-assisted guidance remain unvalidated.

## Pain Themes

### Unclear Eligibility and Upgrade Path

**Affected personas**: Continuity-Focused Upgrader, Price-Certainty Upgrader

**Pain summary**: Customers may begin the upgrade journey without knowing whether their line is eligible, what remains due on the current device, or which payoff, return, or early-upgrade option applies. This ambiguity prevents confident progress and can push customers toward assisted support before they reach device selection.

**Evidence strength**: Moderate

**Evidence notes**:

- The Continuity-Focused Upgrader may not know whether a line is eligible or how much remains due on the current device; this is a HIGH-confidence business claim, not validated user research. — `[outputs/phase-01/persona.md, Continuity-Focused Upgrader, Pain points]`
- This persona needs quick eligibility confirmation, a clear balance, and an approved next step. — `[outputs/phase-01/persona.md, Continuity-Focused Upgrader, Goals]`
- Eligibility or balance data may be outdated unless authoritative systems are used and the values are revalidated. — `[outputs/phase-01/persona.md, Price-Certainty Upgrader, Pain points]`

**Why it matters**:

- Eligibility and balance uncertainty can block the core upgrade journey, reduce trust in the displayed options, and generate avoidable support contacts.

**Design opportunity**:

- How might we help existing customers understand eligibility, remaining obligations, and valid next steps before they invest effort in choosing a device?

**Likely feature direction**:

- Hypothesis: an authoritative eligibility checkpoint showing the selected line, remaining balance, eligibility date, and available payoff or return paths could reduce uncertainty and abandonment.

**Open validation question**:

- Which eligibility or balance scenarios cause customers to stop self-service, and what explanation enables them to continue confidently?

---

### Pricing and Trade-In Uncertainty

**Affected personas**: Price-Certainty Upgrader, Continuity-Focused Upgrader

**Pain summary**: Customers may struggle to understand the complete financial commitment when monthly installments, taxes, fees, promotions, credits, remaining balances, trade-in estimates, and bill impact appear at different points. Conditional trade-in values and prices that seem to change at checkout can further erode confidence.

**Evidence strength**: Moderate

**Evidence notes**:

- The monthly price can appear to change by checkout. — `[outputs/phase-01/persona.md, Price-Certainty Upgrader, Pain points]`
- Customers may not understand how trade-in value is calculated. — `[outputs/phase-01/persona.md, Price-Certainty Upgrader, Pain points]`
- The persona needs a complete monthly and one-time breakdown, payment comparison, trade-in conditions, and confirmation of bill impact. — `[outputs/phase-01/persona.md, Price-Certainty Upgrader, Summary]`
- The assumption that presenting all cost components together will produce understanding has not been validated through comprehension testing. — `[outputs/phase-01/persona.md, Price-Certainty Upgrader, Assumptions]`

**Why it matters**:

- Unclear costs can undermine trust, increase checkout abandonment, and lead customers to accept an upgrade without understanding the amount due today or the future bill impact.

**Design opportunity**:

- How might we help price-conscious customers understand and compare the full upgrade cost without overwhelming them with dense financial information?

**Likely feature direction**:

- Hypothesis: a persistent, plain-language cost summary separating due-today charges, recurring charges, credits, remaining balance treatment, and conditional trade-in value could improve comprehension.

**Open validation question**:

- Which presentation enables customers to accurately explain the amount due today, ongoing monthly impact, promotion conditions, and possible trade-in adjustment?

---

### Compatibility and Choice Overload

**Affected personas**: Continuity-Focused Upgrader, Guidance-Seeking Device Chooser

**Pain summary**: Customers may be uncertain which devices will work with their line or plan, while those unfamiliar with specifications may face too many models, features, and technical terms. The challenge is to narrow choices without hiding eligible options or taking control away from the customer.

**Evidence strength**: Moderate

**Evidence notes**:

- Customers may be uncertain which devices work with their plan. — `[outputs/phase-01/persona.md, Continuity-Focused Upgrader, Pain points]`
- Some customers need help choosing a phone without comparing every model. — `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser, Pain points]`
- Technical jargon and overconfident recommendation language are inappropriate for the Guidance-Seeking Device Chooser. — `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser, Pain points]`
- The persona needs compatible, available recommendations with plain-language reasons, easy comparison, and the freedom to browse independently. — `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser, Summary]`

**Why it matters**:

- Compatibility uncertainty risks failed purchases, while excessive choice and jargon can increase cognitive load, reduce decision confidence, and slow completion.

**Design opportunity**:

- How might we help customers find a compatible device that fits their priorities without forcing them to compare every model or surrender control to a recommendation system?

**Likely feature direction**:

- Hypothesis: a compatibility-filtered catalog with a lightweight preference flow, explainable recommendations, a concise comparison view, and a visible “browse all” option could reduce choice effort.

**Open validation question**:

- Which device attributes and explanation formats help customers narrow choices while preserving confidence that relevant options were not hidden?

---

### Fulfillment and Activation Failure

**Affected personas**: Continuity-Focused Upgrader

**Pain summary**: Inventory can change during checkout, and activation can fail after a customer has committed to a device. These late-stage failures threaten the primary goal of replacing the device while preserving the existing line and number.

**Evidence strength**: Weak

**Evidence notes**:

- Inventory changes or activation failures are identified as risks that can interrupt the journey after selection or delivery. — `[outputs/phase-01/persona.md, Continuity-Focused Upgrader, Pain points]`
- The persona needs order tracking, clear activation instructions, and recovery support. — `[outputs/phase-01/persona.md, Continuity-Focused Upgrader, Goals]`
- The assumption that customers prefer self-service through activation is unvalidated, and the point at which they seek support is unknown. — `[outputs/phase-01/persona.md, Continuity-Focused Upgrader, Assumptions]`

**Why it matters**:

- A late failure can leave customers without a usable device or service, increase duplicate retries, damage trust, and require urgent support intervention.

**Design opportunity**:

- How might we help customers recover from inventory, fulfillment, or activation problems without losing order state, duplicating charges, or disrupting their existing service?

**Likely feature direction**:

- Hypothesis: pre-submission revalidation, persistent order state, clear processing feedback, guided retries, and context-rich assisted handoff could make failures safer and easier to recover from.

**Open validation question**:

- Which failure states can customers resolve independently, and which require immediate handoff with order and line context preserved?

---

### Low Trust in Automated Recommendations

**Affected personas**: Guidance-Seeking Device Chooser

**Pain summary**: Device guidance can reduce comparison effort, but an unsuitable, unexplained, or overconfident recommendation may undermine trust. Customers need recommendations to remain optional, understandable, constrained to eligible devices, and easy to bypass when the service is unavailable or unhelpful.

**Evidence strength**: Weak

**Evidence notes**:

- An AI recommendation may not meet the customer's needs. — `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser, Pain points]`
- The persona wants understandable reasons and the ability to choose independently. — `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser, Motivations]`
- Whether preference questions reduce enough effort to justify an AI-assisted step remains a LOW-confidence assumption. — `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser, Assumptions]`
- The standard compatible catalog remains available when recommendations are unavailable. — `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser, Evidence]`

**Why it matters**:

- Poor recommendations can reduce confidence in both the suggested device and the broader upgrade journey, while opaque guidance can make customers feel manipulated or constrained.

**Design opportunity**:

- How might we help guidance-seeking customers use recommendations confidently without making AI a gatekeeper or presenting its suggestions as certain?

**Likely feature direction**:

- Hypothesis: optional recommendations with plain-language reasons, adjustable preferences, transparent constraints, feedback controls, and an immediate catalog fallback could preserve trust and autonomy.

**Open validation question**:

- What explanation, control, and fallback mechanisms make recommendations feel useful rather than restrictive or promotional?

---

## Priority Table

| Priority | Pain theme | Affected personas | Why now |
| :--- | :--- | :--- | :--- |
| **Critical** | Unclear Eligibility and Upgrade Path | Continuity-Focused Upgrader, Price-Certainty Upgrader | Blocks entry into the core upgrade journey and can prevent customers from understanding whether or how they may proceed. |
| **Critical** | Pricing and Trade-In Uncertainty | Price-Certainty Upgrader, Continuity-Focused Upgrader | Directly affects informed consent, checkout trust, and willingness to complete a financially consequential purchase. |
| **Critical** | Fulfillment and Activation Failure | Continuity-Focused Upgrader | Can prevent completion after commitment and may disrupt service, duplicate actions, or require urgent support. |
| **Important** | Compatibility and Choice Overload | Continuity-Focused Upgrader, Guidance-Seeking Device Chooser | Strongly affects decision confidence, purchase accuracy, and the effort required to choose a device. |
| **Helpful** | Low Trust in Automated Recommendations | Guidance-Seeking Device Chooser | Guidance may improve choice efficiency, but the standard compatible catalog can still support the journey when recommendations are bypassed or unavailable. |

---

## Gaps

- No pain theme is supported by primary user-research evidence; all direct support traces back to one business-authored BRD.
- The three personas overlap, so affected-persona assignments should not be interpreted as mutually exclusive segments.
- No prevalence, severity, frequency, or business-impact data is available to validate the priority ordering.
- Fulfillment, activation, and recommendation concerns are primarily documented risks rather than observed user failures, so their evidence strength is Weak.
- Pricing comprehension, preferred support channel, and the value of preference-based recommendations remain assumptions requiring testing.
- The source contains no evidence about unaddressed customer groups, including prepaid customers or unsupported account and plan types.
