# Concept Direction

## Research Basis

- **Primary persona:** Continuity-Focused Upgrader — a provisional, BRD-defined existing postpaid customer seeking to replace a device while retaining the same phone number and wireless line. `[outputs/phase-01/persona.md, Persona 1 — User type]`
- **Primary pain or goal:** Complete a dependable device upgrade on the existing line with early clarity about eligibility and obligations, a compatible device choice, understood costs, and recoverable fulfillment and activation. `[outputs/phase-01/persona.md, Persona 1 — Goals and Pain points]` `[outputs/phase-01/pain-points.md, Unclear Eligibility and Upgrade Path; Pricing and Trade-In Uncertainty; Compatibility and Choice Overload; Fulfillment and Activation Failure]`
- **Feature opportunities included:** Clear upgrade eligibility and resolution paths (Critical); Complete and comprehensible upgrade cost view (Critical); Compatible device discovery and decision support (Important); Safe order, fulfillment, and activation recovery (Important). `[outputs/phase-02/feature-opportunities.md, Features 1–4]`
- **Secondary-research source:** `outputs/phase-01/secondary-research-report.md` provides contextual evidence from a U.S. wireless-retail study, public carrier program documentation, WCAG 2.2, Apple activation guidance, global market reporting, and limited community signals.
- **Evidence limitations:** The concept's project-user evidence traces to one business-authored BRD rather than primary user research. The personas are provisional and overlapping; their prevalence and relative priority are unknown. Pain frequency and severity are not quantified. Fulfillment and activation concerns have Weak project evidence because they are documented risks rather than observed failures. External user research is primarily U.S.-specific; the target geography is unspecified; public carrier pages describe intended processes rather than authenticated usability; global market data is not evidence about this upgrade journey; and community posts are anecdotal. Pricing comprehension, support-channel preference, trade-in understanding, transferability across markets, and the usefulness of preference-based guidance still require validation. No contradictions were found within the single project source, but that absence is not corroboration. `[outputs/phase-01/persona.md, Source coverage; Evidence gaps and weaknesses; Contradictions requiring review]` `[outputs/phase-01/pain-points.md, Gaps]` `[outputs/phase-01/secondary-research-report.md, Research Objectives & Scope; Evidence limitations]`

## Concept Statement

Help an existing postpaid customer move through one understandable device-upgrade journey that establishes what they can do, limits choices to compatible options, keeps the full financial commitment clear, and protects progress through fulfillment and activation—without changing their existing number or line.

## Core Journey

1. The customer starts with an existing line and wants to replace its device without changing the phone number or service.
2. The customer confirms eligibility and any remaining obligation, then selects a compatible device and reviews the complete financial commitment.
3. The service revalidates eligibility, price, promotions, inventory, payment, identity, fulfillment, and line compatibility before accepting the order, while preserving clear status and safe recovery paths.
4. The customer receives the device, follows activation guidance on the existing line, and either completes activation or enters a supported recovery path without duplicating the order or disrupting service unnecessarily.

## Key Experience Moments

| Moment | Purpose | Research trace |
|---|---|---|
| Line and eligibility check | Establish whether the selected line can be upgraded, explain any remaining obligation, and identify a valid next step before device comparison. | `[outputs/phase-01/pain-points.md, Unclear Eligibility and Upgrade Path]`; `[outputs/phase-01/secondary-research-report.md, Competitive Analysis; Common UI/UX Design Patterns Observed — Pattern 1]`; [Verizon](https://www.verizon.com/support/knowledge-base-205644/), [AT&T](https://www.att.com/support/article-modal/wireless/KM1002380/), and [T-Mobile](https://www.t-mobile.com/support/plans-features/upgrade-ready-every-year/) public guidance; `[outputs/phase-02/feature-opportunities.md, Feature 1]` |
| Compatible device discovery | Limit choices to compatible, available, commercially eligible devices while allowing the customer to narrow and compare without losing access to other eligible options. | `[outputs/phase-01/pain-points.md, Compatibility and Choice Overload]`; `[outputs/phase-02/feature-opportunities.md, Feature 4]` |
| Financial commitment review | Help the customer distinguish charges due today, recurring bill impact, credits and conditions, remaining balance treatment, and conditional trade-in value before ordering. | `[outputs/phase-01/pain-points.md, Pricing and Trade-In Uncertainty]`; `[outputs/phase-01/secondary-research-report.md, Executive Summary; Market Overview & Industry Trends — Key Statistics]`; [J.D. Power, 2025](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1); `[outputs/phase-02/feature-opportunities.md, Feature 2]` |
| Pre-submission revalidation | Surface material changes in authoritative eligibility, price, promotion, inventory, payment, identity, or fulfillment data before commitment. | `[outputs/phase-01/persona.md, Cross-persona design considerations]`; `[outputs/phase-02/feature-opportunities.md, Features 1–3]` |
| Order and fulfillment continuity | Preserve understandable status and prevent duplicate commercial actions when processing is delayed, interrupted, or retried. | `[outputs/phase-01/pain-points.md, Fulfillment and Activation Failure]`; `[outputs/phase-02/feature-opportunities.md, Feature 3]` |
| Activation or supported recovery | Help the customer activate on the existing line or move into a context-rich recovery path when self-service cannot safely continue. | `[outputs/phase-01/persona.md, Persona 1 — Goals and Assumptions]`; `[outputs/phase-01/secondary-research-report.md, Competitive Analysis — Apple device setup; Common UI/UX Design Patterns Observed — Pattern 4]`; [Apple eSIM support](https://support.apple.com/en-us/118669); `[outputs/phase-02/feature-opportunities.md, Feature 3]` |

## Scope

### Included

- **Clear upgrade eligibility and resolution paths:** authoritative eligibility, remaining-obligation context, and valid next-step guidance for the selected existing line.
- **Compatible device discovery and decision support:** eligible-device narrowing and comparison framed around customer priorities, without prescribing a particular interface.
- **Complete and comprehensible upgrade cost view:** an understandable account of due-today and ongoing financial effects, including conditional items.
- **Safe order, fulfillment, and activation recovery:** critical-data revalidation, persistent status, duplicate-action protection, guided recovery, and context preservation for assisted support.
- **Accessible and error-tolerant execution across the included journey:** apply the confirmed WCAG 2.2 Level AA requirement, including relevant focus, target-size, authentication, redundant-entry, understandable-error, and error-prevention considerations. This is a cross-cutting constraint rather than a separate feature opportunity. `[outputs/phase-01/persona.md, Cross-persona design considerations]` `[outputs/phase-01/secondary-research-report.md, Common UI/UX Design Patterns Observed — Pattern 5; Key Takeaways & Actionable Next Steps]` [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)

### Excluded for now

- **Explainable and optional device recommendations:** excluded from the focused concept because this Helpful opportunity has Weak evidence and the Phase 1 material does not establish that an AI-assisted step reduces effort enough to justify inclusion. Compatible catalog discovery remains included. `[outputs/phase-02/feature-opportunities.md, Feature 5; Gaps]`
- **Support for prepaid customers or unsupported account and plan types:** excluded because the supplied evidence does not cover these groups. `[outputs/phase-01/pain-points.md, Gaps]`
- **A specific visual layout, component system, recommendation model, technical architecture, delivery estimate, or implementation commitment:** excluded because the current work defines a testable experience direction rather than a designed or committed solution.

## Assumptions and Validation Questions

- **Assumption requiring validation:** Customers want and can complete self-service through activation. Where do they switch to support, and why? `[outputs/phase-01/persona.md, Persona 1 — Assumptions]`
- Which eligibility and remaining-balance scenarios most often prevent confident progress, and what explanation enables recovery? `[outputs/phase-01/pain-points.md, Unclear Eligibility and Upgrade Path — Open validation question]`
- Can customers accurately explain due-today cost, recurring bill impact, promotion conditions, and possible trade-in adjustments without being overwhelmed? `[outputs/phase-01/pain-points.md, Pricing and Trade-In Uncertainty — Open validation question]`
- Which device attributes and explanation formats help customers narrow compatible choices while preserving confidence that relevant options were not hidden? `[outputs/phase-01/pain-points.md, Compatibility and Choice Overload — Open validation question]`
- Which fulfillment and activation failures can customers safely resolve independently, and which require immediate context-rich assistance? `[outputs/phase-01/pain-points.md, Fulfillment and Activation Failure — Open validation question]`
- Do the three provisional personas represent distinct patterns or overlapping needs that should be served adaptively within one journey? `[outputs/phase-01/persona.md, Hypotheses and assumptions to test; Persona relationship]`
- What are the actual frequency, severity, and service-continuity effects of fulfillment and activation failures? Current evidence is too weak to confirm their relative priority. `[outputs/phase-01/pain-points.md, Fulfillment and Activation Failure; Gaps]`
- Do the U.S.-specific carrier, financing, promotion, and trade-in patterns transfer to the intended market, regulatory environment, currency, and device ecosystem? `[outputs/phase-01/secondary-research-report.md, Research Objectives & Scope; Key Takeaways & Actionable Next Steps — Primary Research Validation]`
- Which eSIM, physical-SIM, carrier, device, operating-system, country, and connectivity combinations require assisted activation or different recovery paths? `[outputs/phase-01/secondary-research-report.md, Competitive Analysis — Apple device setup]`

## Design Handoff

- Explore the sequence and transitions among eligibility, compatible choice, financial review, confirmation, fulfillment status, and activation or recovery; do not assume a specific screen pattern.
- Prototype the high-risk comprehension moments: remaining obligations, full cost and bill impact, conditional trade-in value, and material changes found during revalidation.
- Test both successful and interrupted journeys, including stale data, inventory changes, delayed processing, repeated actions, and activation failure.
- Evaluate the journey against WCAG 2.2 Level AA and test accessible authentication, error prevention, focus, target size, redundant-entry reduction, and understandable recovery with representative users.
- Validate market-specific eligibility, financing, promotion, trade-in, tax, currency, and activation rules before treating public U.S. carrier patterns as applicable.
- Preserve the evidence locators, Weak-evidence labels, exclusions, and validation questions when developing journey maps, flows, or prototypes.
- Treat all included capabilities as hypotheses. Do not translate them into confirmed requirements until the open questions are researched and reviewed.
