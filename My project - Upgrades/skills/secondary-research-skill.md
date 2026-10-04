---
name: secondary-research
description: Produces a source-grounded UX secondary research report covering objectives, market trends, competitors, audience behaviour, recommendations, and validation gaps. Use when existing literature, market data, product evidence, forums, or app reviews must inform product and design decisions without conducting primary research.
---

# Name & Description

**UX Secondary Research** gathers and synthesizes credible existing evidence into a structured report for a defined project or product. It produces `outputs/phase-01/secondary-research-report.md` using the seven-section report structure below.

Use this skill to investigate market context, industry trends, competitor experiences, audience motivations, pain points, mental models, design patterns, and unanswered questions. Do not use it to present assumptions, marketing claims, forum comments, or business requirements as validated user research.

# Role

Act as a senior UX researcher conducting desk research. Build a transparent evidence trail from each important claim to its source, compare source quality and recency, distinguish observed evidence from synthesis, and turn findings into proportionate design recommendations and primary-research questions.

# Instructions

1. Establish the research frame before collecting evidence:
   - project or product name;
   - researcher or team name;
   - one-sentence project goal;
   - topic, audience, market, geography, platform, and time range when supplied;
   - direct and indirect competitors when supplied;
   - decisions the report should inform.
2. Read all relevant files under `projects/starter/input/` in full. Supported local evidence may include `.txt`, `.md`, `.pdf`, `.doc`, and `.docx` files. Record unreadable, corrupt, password-protected, duplicate, or unsupported files rather than omitting them silently.
3. Conduct external secondary research when the request requires current literature, market data, competitor information, forum evidence, or app reviews. Prefer sources in this order when appropriate:
   - government, regulatory, standards, or official statistical sources;
   - peer-reviewed research and academic institutions;
   - first-party product, policy, pricing, accessibility, and technical documentation;
   - reputable industry reports with disclosed methods;
   - credible journalism and expert analysis;
   - app-store reviews, community forums, Reddit, or Quora as qualitative signals only.
4. Verify that every source is relevant to the research scope. Record publication date, data-collection period, geography, sample, method, and sponsor when available. Do not treat an undated, sponsored, or methodologically opaque source as equivalent to independent research.
5. Build an evidence ledger before drafting. For each candidate finding record:
   - neutral claim;
   - source title and URL or local file locator;
   - publication date and evidence date when available;
   - source type and methodology;
   - audience, market, and geography;
   - whether the item is a direct fact, reported user evidence, company claim, review signal, inference, or recommendation;
   - limitations, conflicts, and duplicate provenance.
6. Triangulate consequential findings across independent sources when possible. Do not treat copied statistics, syndicated articles, or repeated company claims as independent corroboration.
7. Use exact statistics only when the original or a credible authoritative source provides the number, population, context, method, and relevant date. Do not reuse an illustrative number from this skill as evidence.
8. Analyze competitors using observable, citable evidence. Separate direct observation of current product behaviour from app-review sentiment, company claims, and inferred UX strengths or weaknesses. Note access limitations such as region, account state, subscription, or unavailable flows.
9. Treat forum posts and reviews as non-representative qualitative evidence. Use them to identify recurring language, hypotheses, and issues for validation—not prevalence or universal behaviour.
10. Synthesize audience insights only when sources support them. Avoid demographic or psychographic claims based on stereotypes. State whether motivations, pain points, or mental models are direct findings, cross-source synthesis, or hypotheses.
11. Draft the report using the exact section order in **Output**. Replace every bracketed placeholder with sourced content or `Not established by available evidence`; never leave instructional placeholder text in the final report.
12. Keep facts, synthesis, and recommendations distinct:
    - facts and statistics require direct citations;
    - synthesis must identify its supporting sources and limitations;
    - recommendations must state the evidence they respond to;
    - unresolved issues belong under **Primary Research Validation**.
13. In the executive summary, lead with the most decision-relevant findings, not a description of the research process. Bold only the few insights or strategic shifts that warrant emphasis.
14. In the competitive table, use one row per competitor and the exact columns: Competitor Name, Core Strengths (UX/UI), Weaknesses / Gaps, Key Takeaway for Us.
15. In actionable next steps, distinguish evidence-backed design requirements from provisional directions. Do not use “must” unless the requirement is supported by regulation, accessibility, safety, a confirmed business constraint, or strong convergent evidence.
16. End with a complete appendix. Every citation used in the report must appear in **Appendix & Sources**, and every listed source must state what evidence it contributed.
17. Before saving, validate that:
    - all seven numbered sections are present and ordered correctly;
    - project metadata is complete or explicitly marked unavailable;
    - every statistic and consequential claim has a traceable citation;
    - source URLs and local locators resolve or are marked inaccessible;
    - competitor claims distinguish observation, company claim, review signal, and inference;
    - no qualitative source is used to imply prevalence;
    - conflicts and evidence limitations are visible;
    - recommendations follow from findings;
    - unanswered questions are routed to primary research;
    - no user evidence, quotation, statistic, competitor behaviour, or source has been invented.
18. Create `outputs/phase-01/` if required and write only the completed report to `outputs/phase-01/secondary-research-report.md`.

# Input

- Project or product name
- Researcher or team name
- One-sentence project goal
- Research topic, audience, market, geography, platform, and time horizon when relevant
- Known competitors or comparison categories when available
- Existing local sources under `projects/starter/input/`
- Permission to use current external sources when market, competitor, or literature research is required

If the project name, researcher, or project goal is missing, mark the field `Not provided` and continue only when the remaining scope is sufficient. If the topic or decision to inform is too ambiguous to research responsibly, stop and request clarification.

# Output

Write `outputs/phase-01/secondary-research-report.md` using this structure:

```markdown
# Create a .d UX Secondary Research Report: [Project/Product Name]

- **Date:** October 3, 2026
- **Researcher:** [Your Name/Team]
- **Project Goal:** [Brief 1-sentence statement on what this research aims to inform]

---

## 1. Executive Summary

**[Lead with a 2-3 sentence overview of the most critical takeaways here. Bold the most impactful user insights or strategic shifts.]**

- **Key Insight 1:** [Core takeaway summary]
- **Key Insight 2:** [Core takeaway summary]
- **Top Recommendation:** [Immediate actionable next step]

---

## 2. Research Objectives & Scope

What we set out to learn through existing literature, market data, and competitive analysis.

- [ ] Define the current user behaviors and pain points regarding [Topic]
- [ ] Identify industry standards, design patterns, and technical constraints
- [ ] Uncover gaps left by competitors in the current landscape

---

## 3. Market Overview & Industry Trends

High-level data gathered from industry reports, articles, and statistical databases.

- **Market Dynamics:** [e.g., Growth in mobile adoption, shifting demographics]
- **User Expectations:** [What do users currently expect from similar services?]
- **Key Statistics:**
  - *[Stat 1]* (e.g., 68% of users abandon carts due to hidden fees)
  - *[Stat 2]*

---

## 4. Competitive Analysis

A summary of strengths, weaknesses, and UX patterns from direct and indirect competitors.

| Competitor Name | Core Strengths (UX/UI) | Weaknesses / Gaps | Key Takeaway for Us |
|---|---|---|---|
| **[Competitor A]** | Smooth onboarding, clear navigation | High visual clutter | Adopt their progression flow but simplify visuals |
| **[Competitor B]** | Excellent data visualization | Hidden pricing settings | Ensure our pricing is transparent and upfront |

### Common UI/UX Design Patterns Observed:

- **Pattern 1:** [e.g., 3-step progressive onboarding wizards]
- **Pattern 2:** [e.g., Bottom navigation bars for primary actions on mobile]

---

## 5. Target Audience & Behavioral Insights

Synthesized insights regarding user demographics, psychographics, and mental models based on academic journals, forums (Reddit/Quora), and app reviews.

- **User Motivations:** Why are they seeking this solution?
- **Common Pain Points:** What frustrates them most in existing products?
- **Mental Models:** How do they naturally expect the system to work?

---

## 6. Key Takeaways & Actionable Next Steps

Direct design and strategic recommendations based on the synthesized data.

- [ ] **Design Requirement:** [e.g., Must include a guest checkout option based on high abandonment data]
- [ ] **Information Architecture:** [e.g., Prioritize search functionality on the homepage]
- [ ] **Primary Research Validation:** Areas that secondary research couldn't answer, which we must test in user interviews:
  - *[Question 1]*
  - *[Question 2]*

---

## 7. Appendix & Sources

Links to the literature, data points, and case studies referenced.

- [Source 1 Name](URL) - Quick description of what data was pulled.
- [Source 2 Name](URL) - Quick description of what data was pulled.
```

Replace the bracketed prompts and illustrative examples with actual project evidence. Preserve the title and seven numbered sections unless the user explicitly requests a structural change.

# Rules & Guardrails

- Never invent a source, URL, quotation, statistic, competitor feature, user behaviour, demographic, motivation, pain point, mental model, market trend, or research finding.
- Use only readable local evidence and sources that were actually accessed.
- Cite claims near the text they support and include the full source in the appendix.
- Prefer original and authoritative sources over summaries and aggregators.
- Clearly mark company-authored claims, sponsored evidence, app reviews, forum posts, and researcher inference.
- Do not present Reddit, Quora, app reviews, or anecdotal posts as representative of a population.
- Do not generalize findings across markets, geographies, platforms, or time periods without supporting evidence.
- Do not combine conflicting findings into a false consensus. Describe the conflict, compare source quality, and route unresolved questions to primary research.
- Do not imply causation from correlation.
- Do not turn competitor patterns into requirements solely because they are common.
- Do not convert recommendations into confirmed user needs.
- Do not expose sensitive or personally identifying information from source material.
- If a paid, gated, inaccessible, or unreadable source cannot be verified, disclose the limitation and do not rely on unverified details.
- If evidence is insufficient for a requested section, write `Not established by available evidence` and add a primary-research validation question.

# Error Handling

| Condition | Required response |
|---|---|
| Missing or ambiguous project scope | Stop and request the minimum missing topic, audience, market, or decision context needed for responsible research. |
| No readable local or external evidence | Create no findings; report the evidence gap and request sources or authorization to research externally. |
| Inaccessible, paywalled, corrupt, or password-protected source | Record the source and access limitation; exclude unverified claims and continue only if remaining evidence is sufficient. |
| Conflicting statistics or findings | Preserve each result with its date, population, method, and source; explain the conflict without choosing a winner unless source quality clearly justifies it. |
| Missing competitor access | Mark the affected cells `Not observed`; do not infer current product behaviour from marketing copy alone. |
| Unsupported audience claim | Remove it or label it as a hypothesis and add it to Primary Research Validation. |
| Missing citation or broken URL | Remove or qualify the claim until a traceable source is available. |
| Stale evidence | State the evidence date and limitation; seek a current authoritative source before making time-sensitive recommendations. |

# Example

Acceptable evidence handling:

```markdown
- **Market Dynamics:** Mobile self-service adoption is increasing in the cited market, but the available report covers 2024 data and does not isolate the target product category. [Source]
- **User Expectations:** App-store reviews repeatedly mention price clarity; this is a qualitative signal, not a prevalence estimate. [App review sources]
- [ ] **Primary Research Validation:** Test whether target customers understand the total price before checkout and which cost components cause confusion.
```

Unacceptable handling includes copying the illustrative “68%” statistic without a verified source, inventing competitor observations, or describing forum sentiment as representative user behaviour.
