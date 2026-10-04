# Create a .d UX Secondary Research Report: Device Upgrade on an Existing Line

- **Date:** October 3, 2026
- **Researcher:** Not provided
- **Project Goal:** Inform a transparent, accessible, and resilient self-service journey for existing postpaid customers upgrading a device while keeping the same wireless line and phone number.

---

## 1. Executive Summary

**Customers need certainty before commitment: eligibility, remaining balance, trade-in conditions, promotions, and total bill impact should be understandable before they invest in device comparison or submit an order.** External wireless-retail research reinforces the importance of cost and promotion clarity, while public carrier flows show that upgrade eligibility commonly depends on account status, installment progress, plan rules, device condition, and trade-in terms. **Activation is part of the purchase journey, not an afterthought:** growing eSIM adoption enables digital transfer, but carrier, device, operating-system, and connectivity dependencies still require visible recovery paths.

- **Key Insight 1:** Price and promotion understanding is a trust issue, not merely a disclosure task. J.D. Power's 2025 U.S. study found cost-and-promotion satisfaction fell 12 points, while customers who strongly agreed their plan and features were easy to understand had substantially higher satisfaction. [J.D. Power, 2025](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1)
- **Key Insight 2:** Major carrier upgrade programs expose a recurring mental model: sign in, select a line, verify eligibility and balance, satisfy financing or trade-in conditions, choose a device, review cost, and then activate. The exact rules differ materially by carrier and program. [Verizon Support](https://www.verizon.com/support/knowledge-base-205644/) · [AT&T Support](https://www.att.com/support/article-modal/wireless/KM1002380/) · [T-Mobile Support](https://www.t-mobile.com/support/plans-features/upgrade-ready-every-year/)
- **Top Recommendation:** Make eligibility and full-cost certainty the first design checkpoint, preserve the confirmed offer through checkout, and connect order completion directly to capability-aware activation and assisted recovery.

---

## 2. Research Objectives & Scope

What we set out to learn through existing literature, market data, and competitive analysis.

- [x] Define current user behaviours and pain-point hypotheses for upgrading a device on an existing postpaid line.
- [x] Identify industry standards, common carrier patterns, and technical constraints affecting selection, pricing, trade-in, fulfillment, and activation.
- [x] Identify gaps in public competitor journeys that the proposed experience should validate or address.

**Scope:** Mobile app and responsive web self-service for an existing postpaid line. Evidence includes the local BRD-derived persona synthesis, the local pain-point analysis, 2025–2026 market and customer-experience research, official carrier support content, W3C accessibility standards, device activation guidance, and limited community evidence.

**Geographic limitation:** The intended market was not explicitly provided. The local BRD uses ₹, but that alone does not establish geography. Global data is used for industry direction; Pew, J.D. Power, and the compared carrier flows are U.S.-specific and should not be generalized to another market without validation.

**Method limitation:** No authenticated carrier checkout was available. Competitive findings describe public support content and documented program rules, not a full usability inspection of logged-in, account-specific flows.

---

## 3. Market Overview & Industry Trends

High-level data gathered from industry reports, articles, and statistical databases.

- **Market Dynamics:** Mobile is a mature, high-scale ecosystem. GSMA reports 8 billion unique mobile subscribers—around 70% of the world population—and projects 5G to represent 80% of global mobile connections by 2030. Its 2026 report also describes eSIM adoption as accelerating across consumer and enterprise markets as device support and digital connectivity management improve. These are global industry indicators, not evidence about the project's target market or upgrade conversion. [GSMA, *The Mobile Economy 2026*](https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-economy/) · [GSMA report PDF](https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-economy/wp-content/uploads/2026/02/The-Mobile-Economy-2026.pdf)
- **User Expectations:** Directional evidence points to clear cost and promotion explanations, visible eligibility and financing status, confidence that the selected device works with the line, continuity of the phone number, and recoverable digital activation. The local personas frame these as BRD-derived needs; public carrier instructions reinforce the journey pattern but do not validate the personas. `[outputs/phase-01/persona.md, Source coverage and persona summaries]`
- **Key Statistics:**
  - *91% of U.S. adults owned a smartphone in Pew Research Center's survey of 5,022 adults conducted February 5–June 18, 2025.* The result establishes U.S. smartphone reach, not device-upgrade intent. [Pew Research Center, 2025](https://www.pewresearch.org/internet/fact-sheet/mobile/)
  - *J.D. Power's 2025 U.S. Wireless Retail Experience Study—Volume 1 included 17,331 customers across phone, store, and digital purchase channels.* Overall satisfaction declined 8 points to 827/1,000; cost-and-promotion satisfaction declined 12 points to 804. [J.D. Power, 2025](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1)
  - *Only 34% of respondents in that study believed their wireless service had improved in value, while 45% strongly agreed their plans and features were easy to understand.* Among the latter group, cost-and-promotion satisfaction was 203 points higher. This is an association within the study, not proof that a particular interface causes higher satisfaction. [J.D. Power, 2025](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1)
  - *98% of U.S. adults owned a cellphone and 91% owned a smartphone in Pew's 2025 survey.* Smartphone ownership varied by age, income, and education, reinforcing the need not to assume uniform digital literacy. [Pew Research Center, 2025](https://www.pewresearch.org/internet/fact-sheet/mobile/)

---

## 4. Competitive Analysis

A summary of strengths, weaknesses, and UX patterns from direct and indirect competitors. Strengths and gaps below are researcher synthesis from public documentation; account-specific screens, offers, inventory, and final checkout were not observed.

| Competitor Name | Core Strengths (UX/UI) | Weaknesses / Gaps | Key Takeaway for Us |
|---|---|---|---|
| **Verizon / My Verizon** | Public instructions support upgrading an existing line in the app, reviewing total device cost, adding trade-in details, and submitting an order. [Verizon app upgrade guide](https://www.verizon.com/support/knowledge-base-205644/) | Public FAQs show eligibility, account standing, upgrade fees, SIM changes, plan offers, and trade-in rules can affect the journey. The logged-in presentation of those dependencies was not observed. [Verizon upgrade FAQs](https://ws01.static-verizon.com/support/upgrade-device-faqs/) | Surface offer qualifications, fees, line context, and trade-in conditions before checkout; retain a reviewable offer record. |
| **AT&T / myAT&T** | Customers can check upgrade eligibility and remaining balance after signing in; support content explains balance payoff, early-upgrade options, and eligibility transfer. [AT&T eligibility support](https://www.att.com/support/article-modal/wireless/KM1002380/) | Public rules vary by installment program, payment progress, plan, account standing, trade-in condition, and optional upgrade charges. This creates a comprehension risk even when each rule is documented. [AT&T installment support](https://lsreg.att.com/support/article/wireless/KM1106686/) | Explain why a line is or is not eligible and show the consequences of each payoff, return, or financing path in one place. |
| **T-Mobile / T-Life** | The Yearly Upgrade page states core eligibility rules and points users to an EIP or Upgrade Dashboard in the app or website. [T-Mobile Yearly Upgrade](https://www.t-mobile.com/support/plans-features/upgrade-ready-every-year/) | The program requires an eligible plan, at least six months on financing, 50% of device cost paid, and a device in good working condition; treatment of the remaining finance agreement and promotions adds decision complexity. | Show progress toward eligibility and clearly distinguish device return, trade-in value, remaining balance, and promotional consequences. |
| **Apple device setup** *(indirect)* | Device setup supports eSIM Quick Transfer, carrier activation, QR codes, carrier apps, and manual entry depending on carrier and device support. [Apple eSIM support](https://support.apple.com/en-us/118669) | Transfer capability varies by carrier, device, operating system, country, and connectivity. Unsupported transfers may require carrier contact, and the previous SIM deactivates after transfer. | Detect capability, set prerequisites before activation, confirm line transfer explicitly, and provide a context-aware carrier fallback. |

### Common UI/UX Design Patterns Observed:

- **Pattern 1: Account-aware line selection and eligibility gating.** Public carrier journeys begin with authentication or account context, then identify the line and determine upgrade status before the customer completes device purchase. [Verizon](https://www.verizon.com/support/knowledge-base-205644/) · [AT&T](https://www.att.com/support/article-modal/wireless/KM1002380/) · [T-Mobile](https://www.t-mobile.com/support/plans-features/upgrade-ready-every-year/)
- **Pattern 2: Installment and trade-in rules shape the offer.** Eligibility commonly depends on payment progress, account standing, plan, device return or condition, and a new financing agreement.
- **Pattern 3: The displayed deal is conditional.** Public documents use eligibility qualifiers, maximum credits, eligible plans, trade-in requirements, and installment terms; the UX challenge is making those conditions visible before the final commitment.
- **Pattern 4: Activation uses progressive fallback.** Supported devices may transfer a line digitally, while unsupported combinations fall back to carrier activation, QR code, carrier app, manual entry, or assisted support. [Apple eSIM support](https://support.apple.com/en-us/118669)
- **Pattern 5: Accessible, error-tolerant transactions are a standards issue.** WCAG 2.2 includes requirements related to focus visibility, target size, redundant entry, accessible authentication, and error prevention that are relevant to long, consequential checkout flows. [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) · [What's New in WCAG 2.2](https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/)

---

## 5. Target Audience & Behavioral Insights

Synthesized insights regarding user motivations, pain points, and mental models. These are provisional: the local personas derive from a BRD, public carrier documentation describes intended processes, and community posts are non-representative qualitative signals.

- **User Motivations:** Existing customers want to replace a device without losing their number or service; price-conscious customers want to understand due-today and monthly impact; guidance-seeking customers want to reduce comparison effort without losing control. These motivations are local BRD-derived claims, not findings from primary research. `[outputs/phase-01/persona.md, Persona summaries and motivations]`
- **Common Pain Points:** The local synthesis highlights eligibility and balance uncertainty, compatibility uncertainty, price changes at checkout, unclear trade-in valuation, activation risk, and unsuitable recommendations. J.D. Power's independent U.S. retail study supports cost and promotion clarity as a broader satisfaction issue. Community posts also describe trade-in values or plan requirements appearing to change during checkout, but these posts are anecdotal and cannot establish frequency. `[outputs/phase-01/pain-points.md, Pain Themes and Priority Table]` · [J.D. Power, 2025](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1) · [Reddit qualitative signal, 2025](https://www.reddit.com/r/verizon/comments/1ocuda8/verizon_tried_to_screw_me_out_of_300_on_a_tradein/) · [Reddit qualitative signal, 2025](https://www.reddit.com/r/verizon/comments/1oty7hz/confused_by_upgrade_offers_1100_vs_830_plan/)
- **Mental Models:** A defensible synthesis is that customers expect the carrier to know their line, eligibility, balance, compatible devices, and applicable offers after sign-in; they expect a quoted price to remain explainable through checkout; and they expect activation to move the existing number to the new device. These expectations should be validated because public support flows show intended system behaviour, not users' actual mental models.

---

## 6. Key Takeaways & Actionable Next Steps

Direct design and strategic recommendations based on the synthesized data.

- [ ] **Design Requirement:** Meet WCAG 2.2 Level AA for app and web flows, including visible focus, adequate targets, accessible authentication, understandable errors, reduced redundant entry, and appropriate error prevention. This is supported by the local confirmed requirement and the W3C standard. `[outputs/phase-01/persona.md, Cross-persona design considerations]` · [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [ ] **Design Requirement:** Display the selected line, eligibility state, remaining balance, approved next steps, and reason for any ineligible state before device comparison. This recommendation addresses the highest-priority local pain theme and mirrors the account-aware pattern documented by major carriers. `[outputs/phase-01/pain-points.md, Unclear Eligibility and Upgrade Path]`
- [ ] **Design Requirement:** Before consent, present a stable, reviewable breakdown of retail price, installments and term, amount due today, taxes and fees, remaining balance treatment, promotions and credit timing, trade-in estimate and conditions, add-ons, and expected bill impact. Preserve the accepted disclosure with the order record. `[outputs/phase-01/persona.md, Price-Certainty Upgrader]` · [J.D. Power, 2025](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1)
- [ ] **Information Architecture:** Sequence the primary journey as line and authority → eligibility and obligations → compatible catalog or optional guidance → configuration and trade-in → full price review → fulfillment → confirmation, tracking, and activation.
- [ ] **Information Architecture:** Keep recommendations optional and explainable, with persistent access to the full compatible catalog. Do not allow recommendation logic to determine eligibility, pricing, financing, fraud, or order acceptance. `[outputs/phase-01/persona.md, Guidance-Seeking Device Chooser and Cross-persona design considerations]`
- [ ] **Reliability:** Revalidate eligibility, inventory, price, promotions, payment, and fulfillment before submission; make retries idempotent; and preserve context for assisted recovery. `[outputs/phase-01/persona.md, Cross-persona design considerations]`
- [ ] **Activation:** Detect eSIM and transfer capability, show prerequisites before the customer begins, confirm that the intended line and number will move, and provide safe carrier-assisted fallback when the device combination is unsupported. [Apple eSIM support](https://support.apple.com/en-us/118669)
- [ ] **Primary Research Validation:** Areas that secondary research could not answer and should be tested with target customers:
  - At which eligibility, balance, pricing, trade-in, fulfillment, or activation state do customers abandon self-service or seek support?
  - Can customers accurately explain the amount due today, ongoing monthly charge, credit timing, remaining balance, and trade-in adjustment risk after reviewing the proposed disclosure?
  - Are the three provisional personas distinct segments, overlapping needs, or temporary journey states?
  - Which comparison attributes and recommendation explanations improve decision confidence without making customers feel steered?
  - What privacy expectations apply to using account data and stated preferences for recommendations?
  - Which activation failures can target customers resolve digitally, and what context must transfer to assisted support?
  - Do findings from U.S. carrier programs transfer to the intended market, regulatory environment, currency, financing model, and device ecosystem?

---

## 7. Appendix & Sources

Links to the literature, data points, and case studies referenced.

- [`outputs/phase-01/persona.md`](persona.md) — Local BRD-derived personas, confidence labels, evidence citations, assumptions, and evidence-quality limitations.
- [`outputs/phase-01/pain-points.md`](pain-points.md) — Canonical local synthesis of prioritized journey problems, evidence strengths, design opportunities, and research gaps derived only from the persona document.
- [Pew Research Center, “Mobile Fact Sheet” (November 20, 2025)](https://www.pewresearch.org/internet/fact-sheet/mobile/) — U.S. cellphone and smartphone ownership; survey of 5,022 adults conducted February 5–June 18, 2025.
- [J.D. Power, “2025 U.S. Wireless Retail Experience Study—Volume 1”](https://www.jdpower.com/business/press-releases/2025-us-wireless-retail-experience-study-volume-1) — Cost-and-promotion satisfaction, plan comprehension association, channel scope, sample size, and field dates.
- [GSMA, “The Mobile Economy 2026”](https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-economy/) — Global subscriber scale, 5G outlook, and mobile-industry context.
- [GSMA, “The Mobile Economy 2026” report PDF](https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-economy/wp-content/uploads/2026/02/The-Mobile-Economy-2026.pdf) — Qualitative evidence on accelerating eSIM adoption and digital connectivity management.
- [W3C, Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/) — Normative accessibility requirements relevant to app and web transactions.
- [W3C, “What's New in WCAG 2.2”](https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/) — Explanation of WCAG 2.2 additions including focus, target size, redundant entry, accessible authentication, and error-prevention criteria.
- [Verizon Support, “My Verizon app — Upgrade Device”](https://www.verizon.com/support/knowledge-base-205644/) — Publicly documented existing-line upgrade steps, trade-in questions, and total-device-cost review.
- [Verizon Support, “Upgrade your Verizon mobile device FAQs”](https://ws01.static-verizon.com/support/upgrade-device-faqs/) — Public eligibility, account standing, offers, and upgrade-fee information.
- [AT&T Support, “Check Upgrade Eligibility and Options”](https://www.att.com/support/article-modal/wireless/KM1002380/) — Public eligibility, remaining-balance, early-upgrade, and eligibility-transfer guidance.
- [AT&T Support, “Learn About Smartphone Installment Plans”](https://lsreg.att.com/support/article/wireless/KM1106686/) — Public installment and Next Up Anytime rules and charges.
- [T-Mobile Support, “Upgrade ready every year with Yearly Upgrade”](https://www.t-mobile.com/support/plans-features/upgrade-ready-every-year/) — Public program eligibility, financing progress, trade-in condition, and upgrade-dashboard guidance.
- [Apple Support, “Set up eSIM on iPhone”](https://support.apple.com/en-us/118669) — Device and carrier dependencies, eSIM transfer methods, and fallback activation options.
- [Reddit r/verizon trade-in thread (October 22, 2025)](https://www.reddit.com/r/verizon/comments/1ocuda8/verizon_tried_to_screw_me_out_of_300_on_a_tradein/) — Non-representative qualitative signal about a displayed trade-in offer changing at checkout.
- [Reddit r/verizon upgrade-offer thread (November 11, 2025)](https://www.reddit.com/r/verizon/comments/1oty7hz/confused_by_upgrade_offers_1100_vs_830_plan/) — Non-representative qualitative signal about plan requirements and offer interpretation.

**Evidence limitations:** The target geography is unspecified; external user research is primarily U.S.-based; global GSMA data is not specific to device-upgrade UX; carrier pages describe intended public processes rather than authenticated usability; Reddit evidence is anecdotal and non-representative; and the local persona and pain-point artifacts ultimately trace back to one business-authored BRD rather than primary research.
