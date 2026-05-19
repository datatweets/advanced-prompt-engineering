# 01: Understanding Your Audience

![Research](https://img.shields.io/badge/section-audience%20research-0891b2)

## Lesson Purpose

This lesson teaches you how to use AI to turn business goals, customer feedback, survey responses, and sales notes into actionable audience insights. You will learn how to structure the analysis, separate evidence from assumptions, and translate insights directly into content requirements.

AI is a powerful tool for organizing large volumes of audience information. It cannot replace real customer conversations, but it can help you see patterns in the evidence you already have — faster and more clearly than reviewing notes manually.

## Timing Plan

| Time | Activity | Outcome |
| ---: | --- | --- |
| 0-5 min | Define the research question | You move from vague goals to specific questions |
| 5-15 min | Identify and prepare source material | You choose relevant notes, comments, surveys, or interviews |
| 15-25 min | Extract themes with AI | You use AI to summarize and classify audience needs |
| 25-35 min | Separate evidence from assumptions | You avoid treating guesses as facts |
| 35-45 min | Build content requirements | You connect audience needs to content topics |

---

## Start With a Sharp Research Question

Most audience research fails before it starts because the question is too vague. "Who is my audience?" is not a research question. It is a starting point for conversation.

A sharp research question has a specific focus and an answer that could directly inform a decision.

**Vague:**
```text
Who is my audience?
```

**Sharp:**
```text
What specific problems do our corporate clients mention most often 
in the first three months of working with us?
```

Here are more examples of research questions that produce usable findings:

- What words do customers use to describe the problem before they found us?
- What objections appear most often before someone decides to buy?
- Which audience segments are asking beginner questions, and which need advanced proof?
- What questions should our content answer before a customer makes contact?
- Which concerns disappear after a customer starts using the product, and which persist?

The research question shapes every prompt you write after it. A sharp question leads to a useful prompt. A vague question leads to a generic summary.

> **Tip:** Write your research question before you open any AI tool. It is the clearest test of whether you are ready to start. If you cannot write a single-sentence research question, you are not ready to analyze your audience yet.

---

## What Good Source Material Looks Like

AI can only analyze what you give it. Garbage in, garbage out — but also, incomplete input in, incomplete picture out.

Before running any analysis, collect and review your source material:

| Source type | What it gives you | Reliability |
| --- | --- | --- |
| Direct customer quotes | Exact language your audience uses | High — if recorded accurately |
| Support tickets | Real problems, real frustration | High — context is clear |
| Sales call notes | Objections, hesitations, triggers | Medium — depends on note quality |
| Survey responses | Patterns at scale | Medium — depends on question quality |
| Webinar Q&A | Live questions from real interested people | High — strong intent signal |
| Social media comments | Public sentiment, common questions | Medium — may not represent buyers |
| Internal team opinions | Assumptions about customers | Low — must be validated |

> **Warning:** Internal opinions about what customers want are not the same as evidence. They are hypotheses. Treat them accordingly — useful as a starting point, never as a conclusion.

---

## Scenario: The Corporate Client Problem

A service business wants to attract more corporate clients. The team has:

- 40 website inquiry messages from the past six months.
- Notes from 15 sales calls.
- 60 support tickets from existing clients.
- Questions asked during a webinar.

The goal: find repeated patterns, identify what is blocking new clients, and generate content ideas that address real concerns.

The challenge: the team does not have time to read 115 items carefully. They want AI to find the patterns.

The right approach is not to paste all 115 items and ask "What should we do?" That produces a surface answer. The right approach is to structure the analysis in stages:

1. Classify the items by type of concern.
2. Extract themes within each type.
3. Identify patterns across types.
4. Generate content requirements based on the strongest patterns.
5. Flag everything that is inference rather than direct evidence.

---

## The Audience Research Prompt

This prompt works for any set of customer-facing notes, comments, or feedback. Paste it into your AI tool and add your source material at the bottom.

```text
Act as a market research analyst.

Analyze the customer notes below.

Research question:
[state your specific research question here]

Goals:
1. Identify the three to five most repeated pain points.
2. Group concerns by audience type (role or situation, not personal name).
3. Identify the top three buying barriers — things that slow or stop a decision.
4. Suggest content topics that would address each barrier.
5. Clearly separate evidence (directly stated in the notes) from 
   assumptions (inferred by you).

Format:
Return a structured table with these columns:
Audience segment | Evidence from notes | Pain point | 
Buying barrier | Content requirement | Confidence (high / medium / low)

Then add a second section:
Assumptions to validate — a list of inferences that need real-world confirmation.

Rules:
- Use only the notes I have provided. Do not add external information.
- Do not invent quotes. If paraphrasing, make that clear.
- If evidence for a claim is weak, mark it as "hypothesis — needs validation."
- Use plain English throughout.
- Do not use personal names.

Customer notes:
[paste your notes here]
```

---

## The Classification Pattern

Before you can analyze patterns, you often need to sort the raw input. Classification is the first step in any research workflow with messy data.

This prompt works for comments, tickets, survey responses, or any short text items:

```text
Act as a research analyst.

Classify each customer comment using exactly one label from this list:
- Pricing concern
- Feature request or gap
- Confusion about process or product
- Trust or credibility concern
- Positive experience
- Urgent complaint
- Comparison with competitor
- Other (describe briefly)

For each item, return:
Comment number | Label | One-sentence reason | Suggested follow-up question

Do not add labels that are not in the list.
If a comment fits two labels equally, choose the one with the higher urgency.

Comments:
[paste numbered comments here]
```

Once comments are classified, you can run a separate prompt on each category:

```text
Here are all comments labeled "trust or credibility concern."

Summarize the top three themes that appear across these comments.
What is the customer worried about, specifically?
What content would address this concern most directly?
```

This two-step approach — classify first, analyze second — is more reliable and more reviewable than asking for everything at once.

---

## From Raw Insight to Content Requirement

Every insight should end with a content action. If a finding does not suggest something to create, write, or change, it is not yet a finished insight.

| Audience evidence | What it suggests | Content requirement |
| --- | --- | --- |
| Many questions about pricing and value | Buyers are uncertain about return on investment | Pricing explainer with real use-case comparisons |
| Repeated confusion about how to get started | Onboarding feels unclear or intimidating | Step-by-step getting-started guide with screenshots |
| Managers asking about time savings | Decision-makers need workflow evidence, not feature lists | Before-and-after workflow article showing real time savings |
| Basic vocabulary questions from new users | Some learners need foundational knowledge before features | Glossary page and beginner-oriented intro content |
| Customers actively comparing alternatives | Buyers are in evaluation mode, not yet decided | Honest comparison guide that builds trust |
| Questions about security and data handling | Enterprise buyers need compliance reassurance | Data security FAQ and privacy policy in plain English |

> **Key insight:** The content requirement column is the payoff of market research. Everything before it is preparation. If you end your research at "pain point" without reaching "content requirement," you have done research without doing analysis.

---

## Avoiding Common Research Mistakes

**Mistake 1: Confirming what you already believe.**
If you paste only the evidence that supports your existing opinion, AI will confirm your bias with confidence. Include contradictory evidence and let the model surface tension.

**Mistake 2: Treating all audience segments as one group.**
A business owner and a department manager have different concerns, different buying criteria, and different levels of AI familiarity. Segment your audience before drawing conclusions.

**Mistake 3: Accepting AI summary as final.**
AI organizes and patterns your input. It does not verify it. If you only have 10 support tickets, the themes from those 10 tickets may not represent your full audience. Flag the gap.

**Mistake 4: Using internal opinions as customer evidence.**
"Our team thinks customers are worried about cost" is a hypothesis. "Seven of the last ten sales calls included a direct question about pricing" is evidence. Know the difference.

---

## Discussion Questions

1. Which type of source material available to you right now is strongest — direct customer quotes, support tickets, sales notes, or internal assumptions?
2. What research question would most directly improve your next piece of content?
3. What would AI need to do well with your source material, and what are the risks of misclassification?
4. How would you tell your manager that some findings are evidence and some are hypotheses?

---

## Practice

Gather five to ten real or realistic customer comments, survey answers, or sales notes.

Run the audience research prompt and produce:

- Three audience segments with role-based labels (not personal names).
- Three pain points with evidence citations.
- Three content requirements linked to the pain points.
- At least one assumption that still needs validation.
- A classification table for all input items.

---

## Review Checklist

- [ ] Is your research question specific enough to guide a decision?
- [ ] Is each insight tied to at least one piece of source evidence?
- [ ] Are assumptions clearly labeled as hypotheses?
- [ ] Are audience segments based on roles and situations, not stereotypes?
- [ ] Does every insight lead to a practical content requirement?
- [ ] Have you flagged what the AI cannot know from your source material alone?
