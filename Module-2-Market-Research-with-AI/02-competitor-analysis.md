# 02: Competitor Analysis

![Analysis](https://img.shields.io/badge/section-competitor%20analysis-0891b2)

## Lesson Purpose

This lesson teaches source-grounded competitor analysis. You will learn how to use AI to compare offers, positioning, content, and proof points across competitors — while keeping the analysis tied to real evidence rather than AI speculation.

The five prompt principles from Module 1 all apply here. Competitor analysis is a perfect test case for why grounding (giving the model real source material) matters so much: without it, AI will generate plausible-sounding claims about competitors that may be completely fabricated.

## Lesson Overview

| Activity | Outcome |
| --- | --- |
| Define the comparison question | You identify what you need to learn |
| Collect source excerpts | You understand why AI needs grounded inputs |
| Build comparison table | You compare positioning, proof, and content |
| Identify gaps and risky claims | You separate facts from interpretation |
| Turn findings into strategic options | You produce positioning ideas and content priorities |

---

## Why Grounding Is Non-Negotiable Here

If you ask an AI model "What are the weaknesses of Company X?" without providing source material, it will tell you. Confidently. With detail. And most of what it says will be either outdated, incomplete, or invented.

This is one of the most dangerous areas for AI hallucination because the output sounds authoritative. Competitor analysis from ungrounded AI prompts has led teams to:

- Build campaigns based on competitor weaknesses that did not exist.
- Dismiss real competition that the model was unaware of.
- Make positioning decisions based on fabricated market data.

The rule for this lesson is absolute: **if it is not in the source text you provided, it does not belong in the analysis.**

> **Warning:** Never ask AI to describe competitors without providing the source text. Always paste in the actual content — website excerpts, brochure text, public descriptions — that you want AI to analyze.

---

## What to Compare

A useful competitor analysis covers six areas:

| Area | Key questions |
| --- | --- |
| Audience | Who is the competitor trying to reach? Who is explicitly mentioned? |
| Offer | What product, service, course, or promise is being presented? |
| Positioning | What makes the offer sound different or better? What claim is repeated most? |
| Proof | What evidence is used: testimonials, case studies, statistics, certifications? |
| Content | What topics and formats appear most often in their public material? |
| Gap | What useful information is missing, vague, or conspicuously absent? |

The gap column is often the most valuable. What a competitor does not say can be as revealing as what they do say. Missing proof, vague claims, and avoided topics are opportunities.

---

## Step 1: Prepare Your Source Excerpts

Before writing any prompt, collect and organize your source material. This takes time, but it is the most important step.

**What to collect:**
- Short excerpts from official product or course pages (100–300 words per source).
- Public descriptions from brochures, event listings, or landing pages.
- Sample social posts or public articles if relevant.

**What to record for each source:**
- Source name or label (do not use real company names in the AI tool if confidential).
- Where you found it (URL or document name).
- Date collected.
- Short excerpt (paste exactly — do not paraphrase before analysis).
- Your initial notes on anything that stood out.

**What not to collect:**
- Customer reviews from third parties (treat separately — different analysis type).
- Internal opinions about competitors (hypothesis, not evidence).
- Outdated content (check dates).

---

## Step 2: Run the Grounded Comparison Prompt

```text
Act as a competitive analysis assistant.

Analyze the competitor descriptions below. Use only the text I have provided.

Our offer:
[describe your product, course, or service in 50–100 words]

Research question:
[what specifically are you trying to learn?]

For each competitor, extract:
1. Target audience as stated (not assumed)
2. Main promise or positioning claim
3. Evidence or proof used (type and strength)
4. Content topics or themes visible in the excerpt
5. One clear gap — something important that is missing or vague

Then add a synthesis section with:
- Three themes that appear across most competitors
- Three audience needs that are not fully addressed by anyone
- Three positioning angles our offer could explore
- A list of claims that require verification before we use them

Rules:
- Use only the provided source text.
- Do not invent prices, outcomes, statistics, or testimonials.
- If something is unclear from the source, write "unclear from source."
- Separate facts (directly stated) from interpretation (inferred).

Competitor sources:
Source 1 — [label]:
[paste excerpt]

Source 2 — [label]:
[paste excerpt]

Source 3 — [label]:
[paste excerpt]
```

---

## Step 3: Run a Quality Evaluation Prompt

Before using the analysis for any decision, run a second prompt to check the quality of the first:

```text
Review the competitor analysis you just produced.

Check each section for:
1. Any claim that goes beyond the source text provided.
2. Any vague recommendation that does not specify an action.
3. Any missing comparison category that would strengthen the analysis.
4. Any competitor that received more attention than the evidence supports.
5. Opportunities to make the table more useful.

Return a table with:
Issue | Where it appears | Risk level | Recommended fix
```

This second-pass evaluation is not optional for important work. The first analysis will always have something that can be tightened.

---

## Step 4: Turn Findings into Strategy

After a clean analysis, use a third prompt to generate strategic options:

```text
Based on the competitor analysis, suggest three strategic positioning options 
for our offer.

For each option:
1. Positioning statement (one sentence, clear and specific)
2. Audience it targets best
3. Content it requires (two to three pieces)
4. Risk or assumption to validate before committing

Rules:
- Do not invent market data.
- Base recommendations on gaps identified in the analysis.
- Flag anything that needs external validation.
```

---

## Example Output Structure

This is what a clean comparison table looks like after running the analysis prompt:

| Competitor | Target audience | Main promise | Proof type | Content themes | Key gap |
| --- | --- | --- | --- | --- | --- |
| Provider A | Corporate teams and managers | Faster AI adoption across departments | One case study mentioned | Executive briefings, workflow guides | No beginner practice content |
| Provider B | Students and early-career workers | Career readiness in an AI-driven market | Course outcomes listed | Job skill mapping, portfolio projects | Business governance not covered |
| Provider C | Small business owners | AI for marketing productivity | Examples in text, no external data | Social content, email tools | Risk management missing entirely |
| Provider D | General audience, no specific segment | Be better at AI | None visible | Generic how-to articles | No audience-specific differentiation |

From this table, a team can immediately see that practical exercises for beginners, responsible AI guidelines, and business governance are underserved areas across the competitive landscape.

---

## Evaluating Competitor Claims

One section of the analysis should always be a claims risk table. Public claims that are vague, unverified, or easily challenged are both a competitive intelligence finding and a warning about your own content.

| Claim type | Example | Risk level | Action |
| --- | --- | --- | --- |
| Outcome guarantee | "Get results in 30 days" | High | Verify or avoid in your own copy |
| Unsourced statistic | "Used by 10,000 businesses" | High | Do not use without verification |
| Vague proof | "Industry-leading quality" | Medium | Use specific evidence instead |
| Missing exclusions | "Works for all teams" | Medium | Clarify your scope |
| Strong testimonial | Quoted customer result | Low | Match or exceed in your proof strategy |

---

## Comparing Two Sources Side by Side

When you have two competitor pages, two market articles, or two versions of similar content, a direct comparison prompt is faster and more precise than analyzing each source separately. It forces the model to treat the sources in parallel rather than sequentially — and produces a more actionable result.

```text
Below are two descriptions of the same type of offer. Read both completely before responding.

Source 1:
"""
[paste first excerpt]
"""

Source 2:
"""
[paste second excerpt]
"""

For each source, provide:
1. The main positioning claim in one sentence.
2. The evidence used and its type (testimonial, statistic, case study, general claim).
3. The audience this source appears to be written for.

Then answer:
- Which source presents a more credible case, and why?
- What specific evidence is missing from each source?
- What audience need does neither source address?

Rules:
- Use only the provided text.
- Mark any inference with "inferred — not stated directly."
- Do not invent statistics or competitor information.
```

The triple-quote delimiters (`"""`) tell the model clearly where one source ends and the next begins. You can use any consistent delimiter — triple quotes, angle brackets, or dashes — as long as the same pattern is used throughout the prompt.

> **Tip:** This technique works for internal content comparison too. Compare two draft subject lines, two versions of the same landing page, or two positioning statements before a final decision.

---

## Practice

Choose two or three competing offers, alternative resources, or market alternatives in your field. Collect short public excerpts (100–200 words each).

Run the grounded comparison prompt and produce:

- One comparison table covering all six analysis areas.
- Three repeated themes across competitors.
- Three gaps or underserved needs.
- One positioning recommendation.
- A claims verification list with at least three items.

---

## Review Checklist

- [ ] Did you provide actual source text rather than asking AI to research competitors independently?
- [ ] Are all comparison points grounded in the provided excerpts?
- [ ] Are assumptions and interpretations clearly separated from direct evidence?
- [ ] Are identified gaps specific enough to guide a content or positioning decision?
- [ ] Did you run a quality evaluation prompt on the analysis?
- [ ] Does the positioning recommendation connect directly to a documented gap?
