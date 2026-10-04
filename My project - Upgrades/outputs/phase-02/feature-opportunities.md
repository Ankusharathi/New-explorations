# Feature Opportunities

## Research Basis

- **Personas used:** Continuity-Focused Upgrader, Price-Certainty Upgrader, and Guidance-Seeking Device Chooser. These are provisional, overlapping need-based archetypes rather than validated or mutually exclusive customer segments.
- **Pain-point source:** `outputs/phase-01/pain-points.md`
- **Secondary-research source:** `outputs/phase-01/secondary-research-report.md`
- **Evidence limitations:** Project-user evidence still originates from one business-authored BRD. No participant research, transcripts, observations, surveys, behavioural analytics, support-contact analysis, prevalence data, or independent project-user corroboration was supplied. The secondary report adds external market research, standards, public carrier documentation, device-support guidance, and anecdotal community signals; most user research is U.S.-specific, public carrier pages describe intended processes rather than authenticated usability, global data is not upgrade-UX evidence, and Reddit posts are non-representative. The target geography remains unspecified. Pain-theme priorities are therefore provisional. Fulfillment, activation, and recommendation concerns have Weak project evidence; pricing comprehension, channel preference, trade-in understanding, and the usefulness of AI-assisted guidance remain unvalidated.
- **Cross-cutting constraint:** WCAG 2.2 Level AA applies across the opportunities. The secondary report highlights focus visibility, target size, reduced redundant entry, accessible authentication, understandable errors, and error prevention as relevant to consequential checkout flows. `[outputs/phase-01/persona.md, Cross-persona design considerations]` `[outputs/phase-01/secondary-research-report.md, Sections 4 and 6]` [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)

## Feature 1: Clear upgrade eligibility and resolution paths

**Priority**: Critical

**User outcome**: Customers can determine whether the selected line can be upgraded, understand any remaining obligation, and identify a valid next step before investing effort in device selection.

**Research trace**:

- Unclear Eligibility and Upgrade Path is a Critical pain theme affecting the Continuity-Focused Upgrader and Price-Certainty Upgrader. — `[outputs/phase-01/pain-points.md, Unclear Eligibility and Upgrade Path; Priority Table]`
- The Continuity-Focused Upgrader's goals include confirming eligibility, remaining balance, and an approved next step. — `[outputs/phase-01/persona.md, Persona 1 — Goals]`
- Eligibility and balance information must come from authoritative systems and be revalidated. — `[outputs/phase-01/persona.md, Cross-persona design considerations]`
- Public Verizon, AT&T, and T-Mobile guidance independently shows a recurring account-aware sequence of line selection, eligibility and balance checks, and program-specific payoff, return, financing, or trade-in conditions. This corroborates the journey pattern, not project-user behaviour. — `[outputs/phase-01/secondary-research-report.md, Executive Summary; Competitive Analysis; Common UI/UX Design Patterns Observed — Pattern 1]` [Verizon Support](https://www.verizon.com/support/knowledge-base-205644/) · [AT&T Support](https://www.att.com/support/article-modal/wireless/KM1002380/) · [T-Mobile Support](https://www.t-mobile.com/support/plans-features/upgrade-ready-every-year/)

**Description**:

- Provide an authoritative upgrade checkpoint for the selected line that explains eligibility, remaining balance, eligibility timing, and the available payoff, return, or supported recovery path. This is a hypothesis based on the Phase 1 design opportunity.

**Success signals**:

- Customers can accurately state whether the selected line is eligible and what action is required next.
- Customers with a remaining obligation can choose a valid resolution path without first contacting support.
- The journey prevents customers from proceeding on stale or invalid eligibility information.

**Assumptions and validation needs**:

- Validate which eligibility and balance scenarios cause customers to abandon self-service.
- Test whether the explanations and resolution paths are understandable across supported account situations.
- Confirm when assisted support is necessary and which context must accompany the handoff.
- Validate whether the U.S. carrier patterns transfer to the intended market, regulatory environment, currency, financing model, and account rules.

## Feature 2: Complete and comprehensible upgrade cost view

**Priority**: Critical

**User outcome**: Customers can understand and compare the amount due today, ongoing bill impact, promotion conditions, remaining-device obligations, and conditional trade-in value before ordering.

**Research trace**:

- Pricing and Trade-In Uncertainty is a Critical pain theme affecting the Price-Certainty Upgrader and Continuity-Focused Upgrader. — `[outputs/phase-01/pain-points.md, Pricing and Trade-In Uncertainty; Priority Table]`
- The Price-Certainty Upgrader needs a complete monthly and one-time breakdown, payment comparison, trade-in conditions, and confirmation of bill impact. — `[outputs/phase-01/persona.md, Persona 2 — Summary and Goals]`
- The assumption that presenting all cost components together creates understanding has not been validated. — `[outputs/phase-01/persona.md, Persona 2 — Assumptions]`
- J.D. Power's 2025 U.S. Wireless Retail Experience Study reported lower cost-and-promotion satisfaction and a strong association between plan comprehension and satisfaction. This supports cost clarity as an industry concern but does not establish causality or validate a specific interface. — `[outputs/phase-01/secondary-research-report.md, Executive Summary; Market Overview & Industry Trends — Key Statistics]` [J.D. Power, 2025](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1)

**Description**:

- Maintain a plain-language view of the full financial commitment, clearly distinguishing due-today charges, recurring charges, credits and conditions, remaining-balance treatment, and conditional trade-in value. This is a hypothesis and not a prescribed interface.

**Success signals**:

- Before submission, customers can explain the amount due today and expected ongoing bill impact.
- Customers can identify promotion conditions and why a trade-in estimate may change.
- Price revalidation does not silently alter the commitment; customers can recognize and review any change.

**Assumptions and validation needs**:

- Test comprehension and recall without overwhelming customers, particularly on small screens.
- Research how customers interpret conditional trade-in estimates and value-adjustment notices.
- Validate which comparisons help customers choose among eligible payment options.
- Test applicability outside the U.S. market represented in the external customer-experience evidence.

## Feature 3: Safe order, fulfillment, and activation recovery

**Priority**: Important

**User outcome**: Customers can complete or recover the upgrade when inventory, fulfillment, or activation problems occur without losing order context, duplicating actions, or unnecessarily disrupting existing service.

**Research trace**:

- Fulfillment and Activation Failure is a Critical pain theme, but its evidence strength is Weak because it is based mainly on documented risks rather than observed failures. — `[outputs/phase-01/pain-points.md, Fulfillment and Activation Failure; Priority Table; Gaps]`
- The Continuity-Focused Upgrader needs order tracking, activation instructions, and recovery support. — `[outputs/phase-01/persona.md, Persona 1 — Goals]`
- Repeated taps or retries must not create duplicate orders, payments, financing agreements, trade-ins, or activations. — `[outputs/phase-01/persona.md, Cross-persona design considerations]`
- Apple activation guidance documents multiple eSIM and carrier-assisted transfer paths whose availability varies by carrier, device, operating system, country, and connectivity. This supports capability-aware fallback, not the frequency of project-user failures. — `[outputs/phase-01/secondary-research-report.md, Competitive Analysis — Apple device setup; Common UI/UX Design Patterns Observed — Pattern 4]` [Apple eSIM support](https://support.apple.com/en-us/118669)

**Description**:

- Preserve order state, revalidate critical data before commitment, communicate processing and failure states, support safe retries where appropriate, and carry relevant order and line context into assisted recovery. These capabilities remain hypotheses pending failure-state research.

**Success signals**:

- Customers can determine order, fulfillment, and activation status after an interruption.
- Retrying does not create duplicate commercial or activation actions.
- Customers reaching assisted support do not need to reconstruct information already supplied in the journey.

**Assumptions and validation needs**:

- Determine which failure states customers can resolve independently and which require immediate support.
- Validate whether customers prefer self-service through activation; current evidence does not establish channel preference.
- Study actual failure frequency, severity, recovery time, and service-continuity impact before increasing priority.
- Validate activation paths for the intended carriers, devices, operating systems, countries, and connectivity conditions.

## Feature 4: Compatible device discovery and decision support

**Priority**: Important

**User outcome**: Customers can narrow the catalog to compatible, available choices and compare relevant options without understanding every technical specification or losing control over selection.

**Research trace**:

- Compatibility and Choice Overload is an Important pain theme affecting the Continuity-Focused Upgrader and Guidance-Seeking Device Chooser. — `[outputs/phase-01/pain-points.md, Compatibility and Choice Overload; Priority Table]`
- The Guidance-Seeking Device Chooser needs compatible and available recommendations, plain-language reasons, comparison, and the freedom to browse independently. — `[outputs/phase-01/persona.md, Persona 3 — Summary and Goals]`
- Only compatible and commercially eligible devices should be shown for the selected line. — `[outputs/phase-01/persona.md, Cross-persona design considerations]`
- Public carrier documentation reinforces account-aware line and eligibility gating before purchase, but authenticated catalog behaviour and account-specific offers were not observed. — `[outputs/phase-01/secondary-research-report.md, Competitive Analysis; Common UI/UX Design Patterns Observed — Pattern 1]` [Verizon Support](https://www.verizon.com/support/knowledge-base-205644/) · [AT&T Support](https://www.att.com/support/article-modal/wireless/KM1002380/) · [T-Mobile Support](https://www.t-mobile.com/support/plans-features/upgrade-ready-every-year/)

**Description**:

- Support an eligibility-filtered catalog, simple preference-based narrowing, plain-language explanations, concise comparison, and an always-available route to browse all eligible devices. The specific interaction pattern must be tested rather than treated as established.

**Success signals**:

- Customers can identify a compatible device that matches their stated priorities.
- Customers can explain why a narrowed option may suit them and can still inspect other eligible options.
- Customers can complete device selection when preference-based guidance is bypassed or unavailable.

**Assumptions and validation needs**:

- Identify which device attributes and explanations genuinely support decisions.
- Compare assisted and standard catalog journeys for effort, confidence, suitability, completion, and bypass behaviour.
- Validate whether preference questions reduce enough effort to justify an additional step.

## Feature 5: Explainable and optional device recommendations

**Priority**: Helpful

**User outcome**: Guidance-seeking customers can use device recommendations with appropriate context and control while retaining a clear path to independent browsing.

**Research trace**:

- Low Trust in Automated Recommendations is a Helpful pain theme with Weak evidence. — `[outputs/phase-01/pain-points.md, Low Trust in Automated Recommendations; Priority Table; Gaps]`
- The Guidance-Seeking Device Chooser wants understandable reasons and the ability to choose independently. — `[outputs/phase-01/persona.md, Persona 3 — Motivations]`
- Recommendations must remain optional, constrained to compatible and available devices, and replaceable by a standard catalog path. — `[outputs/phase-01/persona.md, Persona 3 — Evidence; Cross-persona design considerations]`

**Description**:

- Offer optional recommendations with plain-language reasons, adjustable stated preferences, transparent constraints, and an immediate fallback to the eligible catalog. Recommendations may assist choice but must not determine eligibility, pricing, financing, fraud, or order acceptance.

**Success signals**:

- Customers can explain why a recommendation was offered and change the preferences informing it.
- Customers can ignore or exit recommendations without losing access to the eligible catalog.
- Recommendations never include incompatible or unavailable devices and do not present uncertain suitability as fact.

**Assumptions and validation needs**:

- Test what explanation and control make recommendations useful rather than restrictive or promotional.
- Validate privacy expectations and comprehension of how account data and stated preferences are used.
- Establish recommendation acceptance, perceived suitability, decision confidence, and bypass behaviour through research.

## Coverage Check

| Pain theme | Feature opportunity | Coverage status |
|---|---|---|
| Unclear Eligibility and Upgrade Path | Clear upgrade eligibility and resolution paths | Covered |
| Pricing and Trade-In Uncertainty | Complete and comprehensible upgrade cost view | Covered |
| Fulfillment and Activation Failure | Safe order, fulfillment, and activation recovery | Covered; weak evidence requires validation |
| Compatibility and Choice Overload | Compatible device discovery and decision support | Covered |
| Low Trust in Automated Recommendations | Explainable and optional device recommendations | Covered; weak evidence requires validation |

## Gaps

- No opportunity is backed by primary user-research evidence; all traces ultimately derive from one BRD.
- Persona overlap, prevalence, pain frequency, severity, and relative priority remain unknown.
- The Critical priority assigned to Fulfillment and Activation Failure in Phase 1 is not matched by strong evidence; its opportunity is therefore Important pending research into actual incidents and impact.
- Pricing comprehension, support-channel preference, trade-in understanding, and the usefulness of preference-based recommendations require direct validation.
- The source does not cover prepaid customers or unsupported account and plan types, so the opportunities should not be generalized to those groups.
- The external findings are largely U.S.-specific, while the intended market is unspecified; transferability of carrier rules, financing, trade-in, regulatory, currency, and activation patterns must be tested.
- Competitor findings come from public support documentation rather than authenticated, account-specific usability inspection.
- No critical pain theme is uncovered, but coverage indicates hypotheses to test rather than confirmed solution requirements.
