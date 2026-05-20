# 01: Writing Blog Posts

![Writing](https://img.shields.io/badge/section-blog%20writing-f97316)

## Lesson Purpose

This lesson teaches a structured AI-assisted workflow for writing blog posts and articles. You will learn how to brief, research, outline, draft section by section, and review — using AI as a controlled writing assistant at every stage.

The single most important principle here is this: do not ask for the whole article at once. When you give AI an undirected write command, you get a generic, forgettable article that sounds like every other AI-generated article on the same topic. The workflow in this lesson is designed to prevent that.

## Lesson Overview

| Activity | Outcome |
| --- | --- |
| Define the content job | You identify audience, topic, and business goal |
| Write the content brief | You gather angles and required evidence before drafting |
| Generate and choose the outline | You build structure before writing |
| Draft one section at a time | You divide labor and maintain creative control |
| Run the review prompt | You check claims, style, structure, and usefulness |
| Finalize and discuss | You compare the AI-assisted version to the original brief |

---

## Why One-Shot Article Prompts Fail

Asking AI to "write a blog post about AI for managers" produces a five-section article that:

- Covers everything without emphasis.
- Uses generic examples.
- Sounds like a summary of other articles.
- Has no original perspective or specific evidence.
- Will not rank, share, or be remembered.

The difference between a useful article and a generic one is not the technology — it is the structure and specificity of the workflow.

| What you skip | What you lose |
| --- | --- |
| Content brief | No clear reason why this article should exist |
| Interview or research step | No original evidence or perspective |
| Outline review | Sections that repeat instead of building |
| Section-by-section drafting | No place to correct direction early |
| Quality review | Unsupported claims, wrong tone, missing examples |

> **Key insight:** The content brief is a contract between you and the AI. It tells the model exactly who the article is for, what problem it solves, and what the reader should be able to do after reading. Without it, you are hoping AI guesses correctly. With it, every section becomes reviewable against a clear standard.

---

## The Writing Workflow

Use this five-step sequence for every article:

1. Write a content brief that defines the audience, problem, goal, and evidence required.
2. Ask interview questions to surface original perspective or experience.
3. Generate an outline and review it before drafting.
4. Write one section at a time, correcting direction before continuing.
5. Run a review prompt against clear quality criteria before publishing.

---

## Step 1: Content Brief Prompt

A content brief is the most important document in any content project. It takes five minutes to write and saves hours of revision.

```text
Act as a content strategist.

Create a content brief for a blog post.

Topic:
[your topic]

Target audience:
[describe the reader: role, situation, level of familiarity with the topic]

Business goal:
[what action do you want the reader to take after reading?]

Return:
1. The specific problem this article solves for the reader
2. What the reader wants to be able to do after reading
3. Five questions the article must answer
4. Two or three claims that will need evidence or examples
5. What this article should NOT cover (scope boundaries)
6. Recommended article length
7. Suggested structure (headings only)
8. One practical example or scenario to include

Rules:
- Use plain English.
- Do not invent statistics or market data.
- Mark any assumption clearly.
```

---

## Step 2: Interview Prompt

Use this when the article should include original insight rather than a summary of commonly available information. The interview prompt helps you surface what you actually know — which is usually more specific and more valuable than what AI knows.

```text
I am writing an article about [topic] for [audience].

Please ask me five interview questions.

Your goal is to discover:
1. Practical experience I have with this topic.
2. Strong opinions that differ from standard advice.
3. Mistakes I have seen or made.
4. Specific examples from real work.
5. Advice that does not appear in a generic article.

Ask one question at a time.
Wait for my answer before continuing.
```

After answering the questions, feed your answers back into the outline and drafting steps. These answers become the original parts of the article — the sections that cannot be easily replicated by another writer or another AI.

---

## Step 3: Outline Prompt

```text
Based on the content brief below, create an outline for a blog article.

Content brief:
[paste your brief]

Return:
1. Ten title options with different angles (curious, practical, direct, challenging)
2. Recommended title with reason
3. Opening angle — what the reader will encounter in the first paragraph
4. Section headings with one-sentence description of each
5. A practical example or scenario for each section
6. Final reader checklist or next-step section
7. What the article avoids (based on scope boundaries in the brief)

Constraints:
- No personal names.
- Plain, direct language.
- Each section should build on the previous one.
```

Review the outline before drafting. If a section does not earn its place — if removing it would not hurt the article — cut it. An article with five strong sections is better than an article with eight mediocre ones.

---

## Step 4: Draft One Section at a Time

```text
Write only Section 1: [heading].

Use:
- Two to four short paragraphs.
- Plain English that a busy professional can read at normal speed.
- At least one specific, realistic workplace scenario or example.
- No unsupported claims.
- No generic advice that could apply to any topic.

After the section, briefly tell me:
- What you assumed about the reader.
- What you left out because it belongs in a later section.
- What I should check before continuing.
```

The "tell me what you assumed" instruction is critical. It surfaces the model's assumptions before they accumulate across the whole article. Correcting one wrong assumption in Section 1 takes a minute. Finding and fixing it in every section takes an hour.

> **Tip:** After each section, ask yourself: "Is this good enough to read aloud to my target audience?" If it feels vague or obvious, send it back with a specific question. "Make this more specific" is not a useful revision instruction. "This section describes what AI can do generally — add a concrete example of what a manager at a 10-person company would actually type into the prompt" is.

---

## Scenario: The Manager's Weekly Update

A training provider wants a blog post aimed at managers:

**Working title:** How Managers Can Use AI to Create Better Weekly Updates

**Audience:** Managers who are curious about AI but worried about accuracy and privacy.

**Business goal:** Demonstrate a practical workflow that addresses the accuracy and privacy concerns, then invite readers to join a workshop.

**What it must answer:**
- Can AI actually help with weekly reporting without making things up?
- What do I give AI to work with?
- How do I review the output before sending it?
- What should I not share with an AI tool?
- How long does this workflow take?

**What it must not do:**
- Oversell. Do not promise results the article cannot prove.
- Use technical language the audience does not need.
- Ignore privacy or accuracy concerns.

The brief answers all of these before a single word is drafted.

---

## Step 5: Review Prompt

```text
Review the draft article below.

Check against the content brief:
1. Does each section answer one of the questions in the brief?
2. Are there any unsupported claims or statistics?
3. Which sections are too generic — could apply to any topic, not specifically this one?
4. Where does the tone shift from professional to promotional?
5. Is there at least one practical example in every section?
6. Does the article mention when a human should review AI output?
7. Is there a specific, actionable next step for the reader?

Return a table with:
Section | Issue | Severity (high/medium/low) | Recommended fix
```

---

## Quality Criteria

Use this table to evaluate any article draft before publishing:

| Criterion | What a strong article looks like |
| --- | --- |
| Audience fit | One specific reader with one specific problem is addressed throughout |
| Originality | Includes an example, experience, or angle that is not generic AI output |
| Usefulness | Gives the reader a workflow, checklist, or decision they can apply today |
| Evidence | Does not invent statistics, case studies, or outcomes |
| Structure | Clear headings, short sections, logical progression |
| Tone | Professional and direct — not hyped, not academic |
| Risk control | Notes where human review is required |
| Scope | Stays within the brief — does not drift into adjacent topics |

---

## Common Article Writing Mistakes

**Mistake 1: Opening with the definition.**
"Artificial intelligence is..." is how every generic AI article starts. Open with the problem your reader has right now.

**Mistake 2: Too many sections, not enough depth.**
Seven headings with two sentences each is an outline, not an article. Three headings with real examples and clear reasoning is a useful piece.

**Mistake 3: Claiming results without evidence.**
"AI can save managers two hours per week" is a claim that requires a source. Either cite it or remove it.

**Mistake 4: Skipping the review step.**
AI will confidently state things that are incorrect, outdated, or context-dependent. Publish nothing without a human review pass.

---

## Practice

Build a full article workflow for one topic:

- AI for meeting summaries
- AI for customer email drafts
- AI for market research reports
- AI for student study planning

Produce and submit:

1. A completed content brief.
2. Five interview questions.
3. An outline with title options and section descriptions.
4. One fully drafted section.
5. A review table with at least three issues identified and fixed.

---

## Review Checklist

- [ ] Does the content brief define a specific reader, problem, and goal?
- [ ] Does the outline earn every section — does each heading have a purpose?
- [ ] Is there at least one specific example in each drafted section?
- [ ] Are all claims supported or explicitly marked as hypotheses?
- [ ] Did you run the review prompt and address the issues it found?
- [ ] Does the article end with a specific, actionable next step?
