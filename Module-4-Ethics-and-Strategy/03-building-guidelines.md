# 03: Building Guidelines

![Governance](https://img.shields.io/badge/section-guidelines-7c3aed)

## Lesson Purpose

This lesson teaches you how to create practical AI usage guidelines for a business, department, or classroom. Good guidelines are short enough to actually use, specific enough to prevent common mistakes, and structured enough to be updated as AI tools and policies evolve.

Guidelines are not legal documents. They are working agreements. They answer the question every team member eventually asks: "Is it okay for me to use AI for this?"

## Lesson Overview

| Activity | Outcome |
| --- | --- |
| Understand why guidelines matter | You connect AI use to team accountability |
| Define approved and restricted uses | You establish clear boundaries |
| Set prompt quality standards | You define what a work-ready prompt looks like |
| Build review and escalation rules | You decide when human approval is required |
| Draft a one-page guideline | You produce a document your team can use today |
| Review and improve | You run the guideline through a quality check |

---

## Why Guidelines Matter

Without guidelines, teams default to two failure modes:

**Avoidance:** Nobody uses AI because nobody knows what is allowed. The tools sit unused while other teams accelerate.

**Overuse:** Everyone uses AI for everything, including tasks that require human judgment, involve private data, or produce output that should require review. Mistakes get published. Trust erodes.

Guidelines create a middle path: a clear set of approved uses that build confidence, restricted uses that prevent the most likely mistakes, and a review process that keeps humans in the loop on high-stakes work.

> **Note:** Guidelines should be one page. If a team member has to read more than one page to know what to do, the guidelines are too complicated. Use tables, bullet points, and plain language.

---

## The Seven Guideline Areas

| Area | The question your guideline answers |
| --- | --- |
| Approved use | What tasks can AI support at this organization? |
| Restricted use | What data or decisions must not involve AI? |
| Prompt quality | What must every work prompt include? |
| Output review | What must happen before AI output leaves your desk? |
| Escalation | When does a manager, legal team, or compliance officer need to review? |
| Tool approval | Which AI tools are approved, and which require explicit permission? |
| Improvement | How do we collect and share better prompts over time? |

---

## Approved Uses: Where AI Genuinely Helps

Start guidelines by listing what AI can do well, so team members feel empowered to use it:

**AI may be used to:**

- Draft outlines, first drafts, and rough summaries of non-confidential material.
- Summarize meeting notes that do not contain restricted information.
- Rewrite approved content for a different audience or reading level.
- Generate multiple versions of social posts, email subject lines, or headings.
- Create checklists and templates for repeatable tasks.
- Review drafts for tone, structure, and missing information.
- Research topics using public information (with source verification required).
- Build prompt libraries for team tasks.

The key word in most of these is "draft." AI assists the human. It does not finalize.

---

## Restricted Uses: Where AI Creates Risk

Be explicit about restrictions. Vague guidelines invite different interpretations:

**AI may not be used to:**

- Process private customer data — including names, contact details, and account information — in any tool not approved by IT and legal.
- Generate legal, financial, medical, or compliance advice without expert review.
- Make or recommend decisions about employment, eligibility, credit, safety, or access.
- Publish external claims, statistics, or outcome guarantees without source verification.
- Replace required human approval steps — sign-off still requires a person.
- Substitute for qualified professional judgment in high-stakes situations.

> **Warning:** "Restricted" means restricted. If team members see exceptions being made for convenience, the guideline becomes meaningless. Leadership needs to model the restrictions for them to hold.

---

## The Team Prompt Standard

Every work prompt — one that produces output used in business decisions, customer communication, or public content — should include these eight elements:

| Element | Purpose |
| --- | --- |
| Task | What you are asking AI to do |
| Audience | Who will read or use the output |
| Context | What background information the model needs |
| Source material | What evidence or data to work from |
| Constraints | What the output must not include or claim |
| Output format | How the output should be structured |
| Quality criteria | What a good output looks like |
| Review instruction | What the human reviewer should check |

A team that consistently includes these eight elements will get better, more consistent outputs — and will find errors much easier to catch during review.

---

## Scenario: A Corporate Department

A corporate training department wants to use AI for:

- Meeting summaries.
- First draft communications.
- Content calendar planning.
- Research outlines.
- Training materials.
- Internal guidelines.

The challenge: the team includes employees with different levels of AI familiarity, and the manager does not have time to review every output personally. The guidelines need to be clear enough for beginners and brief enough for experienced users.

---

## Guideline Drafting Prompt

```text
Act as an AI governance consultant.

Draft practical AI usage guidelines for this team:
[describe the team: size, function, industry]

Approved AI tasks:
[list the tasks your team wants to use AI for]

Restricted data types:
[list any data that must not be shared with AI tools]

Review requirements:
[describe when human review is required and who reviews]

Approved tools:
[list any tools that have been specifically approved by IT and legal]

Tone:
Plain English. Short sentences. Suitable for employees at all experience levels.

Format:
Return a one-page document with these sections:
1. Purpose (two sentences)
2. Approved uses (bullet list)
3. Restricted uses (bullet list)
4. Data handling rules (bullet list)
5. Prompt quality standards (table: element + purpose)
6. Review checklist (checkbox list)
7. Escalation rules (table: situation + who to contact)
8. Example workflow (numbered steps)
```

---

## Example Escalation Rules

| Situation | Who to contact |
| --- | --- |
| Output will be published externally | Manager + communications lead before publishing |
| Output includes statistics or research claims | Fact-check with subject expert before use |
| Customer data was accidentally included | IT security and data privacy officer immediately |
| Output is used in a legal or HR context | Legal team review required |
| You are not sure whether a use is allowed | Ask your manager — do not assume |

Escalation rules remove ambiguity. Without them, team members either escalate everything (slowing work) or escalate nothing (creating risk). A clear list tells them exactly when to pause.

---

## Example Workflow

This is what a responsible AI-assisted work task looks like end to end:

```text
1. Define the task and identify the audience.
2. Check whether the task is on the approved use list.
3. Remove or replace any restricted data before pasting into the AI tool.
4. Use the team prompt standard — all eight elements.
5. Review the output for accuracy, policy fit, tone, and risk.
6. Revise the draft as needed.
7. Apply the escalation rules — escalate if required.
8. Finalize with human approval.
9. Save useful prompts to the team prompt library.
```

---

## Guidelines Review Prompt

After drafting your guidelines, run this quality check:

```text
Review this AI usage guideline document.

Check for:
1. Any approved use that could create risk if misunderstood.
2. Any restriction that is too vague to enforce consistently.
3. Any escalation rule that has no named person or role.
4. Any missing scenario that your team is likely to encounter.
5. Any part of the document that is longer than it needs to be.

Return a table with:
Section | Issue | Severity | Fix
```

---

## Rolling Out AI in Your Team: A Practical Approach

Writing guidelines is the planning phase. Getting a team to actually use them consistently is a different challenge. Most AI rollouts fail because they try to change everything at once. A better approach is to start with one workflow, prove value with one person, and then expand.

Here is a practical step-by-step rollout that works for small and mid-sized teams:

**Step 1: Find the right recurring tasks**

Ask the team: "What do you write the same way every week?" Look for tasks that are repeated, predictable, and time-consuming — weekly reports, customer reply templates, meeting summaries, content drafts. These are where AI will have the most immediate impact and where a prompt standard is easiest to apply.

Limit the initial scope to three to five tasks. More than that is too much to change at once.

**Step 2: Build one production prompt per task**

For each recurring task, build a prompt using the team prompt standard (all eight elements from this lesson). Upload one real, approved example as a reference. Test it with actual source material from a real task — not invented content.

Save each prompt in a shared file, not in someone's private chat history. If a team member leaves, the prompt library should stay.

**Step 3: Write one-line launch templates**

For each prompt, write the shortest possible trigger — one line that launches the full workflow: "Run the weekly report summary. Source notes are below." Paste the full prompt after it.

Post these templates somewhere the team can find them in under ten seconds. A pinned message in your team chat, a shared folder, or a sticky note on the intranet all work. If it takes more than ten seconds to find, people will not use it.

**Step 4: Bring in one teammate**

Pick one person who would benefit most from one of the new workflows. Sit with them for fifteen minutes. Run the prompt on their actual work in real time. Let them see the output and do the review step themselves. Ask them to suggest one improvement to the prompt.

This converts a document into a habit. When one person experiences real time savings, they become a more convincing advocate than any policy memo.

**Step 5: Set the review and improvement schedule**

AI tools change. Approved tool lists become outdated. Prompts that work well today may need updates in three months. Set a fixed quarterly review date from day one. On each review date: check the approved tool list, update any prompts that are no longer producing good results, and add new approved workflows the team has discovered.

> **Tip:** The fastest way to introduce AI to a skeptical team member is to save them 20 minutes on something they already do every week. Find that task first. Everything else follows.

---

## Practice

Draft a one-page AI usage guideline for one of these settings:

- Small business (five to fifteen people).
- Corporate department (marketing, operations, HR, or finance).
- Training provider.
- Classroom or student project team.

Your guideline must include:

1. A purpose statement (two sentences).
2. An approved uses list (at least six items).
3. A restricted uses list (at least four items).
4. A data handling rules list.
5. A prompt quality standard table.
6. A review checklist with at least six items.
7. An escalation table with at least four scenarios.
8. A nine-step workflow.

Run the guidelines review prompt and revise at least two issues before submission.

---

## Review Checklist

- [ ] Is the guideline short enough to fit on one page?
- [ ] Are restricted data types named specifically — not just "sensitive data"?
- [ ] Does the escalation table include named roles, not just "ask someone"?
- [ ] Does the prompt standard include all eight elements?
- [ ] Is the workflow specific enough for a new employee to follow on their first day?
- [ ] Would you personally feel confident following this guideline in your work?
