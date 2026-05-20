# 03: Customer Personas

![Personas](https://img.shields.io/badge/section-personas-0891b2)

## Lesson Purpose

This lesson teaches you how to build practical customer personas from research evidence. A good persona is a tool, not a character. It helps a team decide what to write, what to explain, what objections to address, and what proof to include.

By the end of this lesson, you will be able to build role-based personas from your audience research and competitor analysis, map each persona to specific content requirements, and identify which parts of your persona are still hypotheses that need validation.

## Lesson Overview

| Activity | Outcome |
| --- | --- |
| Distinguish useful from weak personas | You avoid the most common persona mistakes |
| Select and organize evidence | You choose notes, comments, and findings |
| Generate persona cards with AI | You build role-based audience segments |
| Map personas to content | You connect needs to formats and topics |
| Review and refine | You improve evidence quality |

---

## What Makes a Persona Actually Useful

Most personas fail because they describe a fictional person instead of a real audience pattern. A persona that tells you someone is "35–45 years old, lives in the suburbs, and enjoys hiking" does not help you write better content. It has nothing to do with why they buy, what they fear, or what would help them decide.

A useful persona is built around decisions and tasks, not demographics.

**Useful persona elements:**

| Element | What it tells you |
| --- | --- |
| Role and situation | What this person is trying to accomplish at work |
| Goal | What success looks like for them |
| Pain points | What is blocking progress right now |
| Questions they ask | What they need answered before they can move forward |
| Decision criteria | What would make them choose this over alternatives |
| Content needs | What type of content would actually help them |
| Evidence | Where this insight came from |
| Assumptions | What still needs real-world confirmation |

**A weak persona:**
- Built from guesses.
- Includes invented age, location, and lifestyle details.
- Too broad to guide any specific decision.
- Based on internal opinions rather than customer evidence.
- Not connected to a real content or workflow decision.

**A strong persona:**
- Tied to direct evidence from research.
- Based on role and situation rather than demographics.
- Clear about what this segment needs to believe before they commit.
- Connected to specific content topics and formats.
- Honest about what is evidence and what is still a hypothesis.

---

## The Persona Card Structure

Use this structure for every persona you build:

| Field | Purpose |
| --- | --- |
| Segment label | A role-based label that the whole team can use |
| Situation | What this person is currently dealing with |
| Goal | What they are trying to achieve |
| Pain points | What is blocking them or causing frustration |
| Questions they ask | The actual questions from your research |
| Decision criteria | What they need to see before they commit |
| Objections | What might stop them even if they are interested |
| Content needs | What specific content would help this segment |
| Evidence | What research supports this persona |
| Assumptions to validate | What the team still needs to confirm |

---

## Scenario: The AI Productivity Course

A company is developing an AI productivity course. The research — from audience analysis, competitor gaps, and customer conversations — suggests four distinct audience types with very different needs:

**Business owners** need practical, immediate time savings. They are skeptical of anything that sounds like hype and will not invest time in theory.

**Department managers** need to understand how AI affects their team's workflow, what review processes to establish, and how to avoid accountability risks.

**Corporate employees** need confidence with daily tools. They are worried about doing something wrong, using AI on sensitive data, or producing output that embarrasses them.

**Students** need workplace-ready skills. They want to learn what employers expect, not generic AI tutorials.

Each of these segments requires different examples, different tone, different depth, and different content formats. A single generic persona would obscure all of these differences.

---

## The Persona Generation Prompt

```text
Act as a customer research analyst.

Create evidence-based persona cards from the research notes below.

Research context:
[brief description of your product, service, or course and the market it serves]

Rules:
- Do not use personal names for personas — use role-based labels.
- Do not invent demographic details such as age, location, or income.
- Ground each element in the research notes.
- If you are inferring something not directly stated, mark it as an assumption.
- Keep each card practical enough to guide a content decision.

For each persona, return:
1. Segment label
2. Situation (what they are currently dealing with)
3. Goals (what success looks like)
4. Pain points (what is blocking them)
5. Questions they ask (direct or paraphrased from the research)
6. Decision criteria (what they need to see before committing)
7. Objections (what might stop them)
8. Recommended content (two to three specific pieces)
9. Evidence (which research notes support this)
10. Assumptions to validate (what needs real-world confirmation)

Research notes:
[paste your audience research and competitor analysis findings here]
```

---

## Example Persona: Fully Developed

Here is what a fully developed, evidence-grounded persona looks like:

| Field | Content |
| --- | --- |
| Segment label | Time-constrained department manager |
| Situation | Responsible for weekly team reporting; spends 3–4 hours each week compiling notes from three or more contributors |
| Goal | Reduce the time spent on internal reporting while maintaining the accuracy the director expects |
| Pain points | Messy, inconsistent notes from team members; unclear ownership of action items; repeated follow-up needed for missing information |
| Questions they ask | "Can AI summarize without inventing details?" / "How do I review the output quickly?" / "What happens if the summary is wrong?" |
| Decision criteria | Must be accurate, must not expose private information, must fit into existing workflow without training the whole team |
| Objections | "I don't have time to learn a new tool" / "My team will be skeptical" / "What if it makes errors that I miss?" |
| Recommended content | Meeting-summary prompt template; review checklist for AI output; two-page responsible use guide for managers |
| Evidence | Repeated mentions of reporting time in sales call notes; three support tickets about AI accuracy concerns |
| Assumptions to validate | Whether the team uses a standard meeting format; what tools are approved by IT |

This persona is immediately useful. Any team member can read it and know what to write, what angle to take, and what objections to address.

---

## Mapping Personas to Content

Once personas are built, map each one to specific content types. This is where research becomes a production plan:

| Persona need | Best content type | Why |
| --- | --- | --- |
| Understand AI terms before starting | Glossary or beginner guide | Reduces friction before deeper content |
| See AI working in a real scenario | Scenario-based lesson or case example | Builds credibility and applicability |
| Compare AI options or approaches | Decision checklist or comparison table | Supports evaluation-stage buyers |
| Reduce worry about accuracy or privacy | Responsible use guide or FAQ | Addresses trust concerns directly |
| Start using AI today | Prompt template with instructions | Gives immediate practical value |
| Train others on the team | Facilitator notes and group exercise | Serves managers with team responsibilities |

Create a mapping table for your personas using this format:

```text
Persona | Content need | Recommended content type | 
Topic or title | Journey stage | Priority
```

---

## The Persona Review Prompt

After generating your personas, run this quality check:

```text
Review these persona cards.

For each persona, identify:
1. Any element that is an assumption rather than supported evidence.
2. Any important field that is missing or too vague.
3. Whether the content recommendations are specific enough to act on.
4. Whether any two personas could be merged without losing important distinction.
5. Whether any segment is too broad to guide a real content decision.

Return a table with:
Persona | Issue | Why it matters | Recommended fix
```

---

## Practice

Using the audience insights from Lesson 1 and the competitor analysis from Lesson 2, build at least two personas:

- One business or management persona.
- One employee or student persona.

For each persona:
- Complete all 10 fields in the persona card.
- Map the persona to at least three specific content requirements.
- Identify at least one assumption that needs validation.

Then run the persona review prompt and improve at least one card based on the output.

---

## Review Checklist

- [ ] Are segment labels role-based rather than demographic?
- [ ] Is every claim tied to at least one piece of source evidence?
- [ ] Are assumptions explicitly marked?
- [ ] Are content recommendations specific enough that a writer could act on them today?
- [ ] Have you mapped each persona to at least three content requirements?
- [ ] Could each persona help a team make a real content or strategy decision?
