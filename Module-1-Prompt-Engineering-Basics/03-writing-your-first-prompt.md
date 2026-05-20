# 03: Writing Your First Prompt

![Workflow](https://img.shields.io/badge/section-workflow-2563eb)

## Lesson Purpose

This lesson turns the five principles into a repeatable writing workflow. You will build a prompt from scratch, test it, evaluate the output, and improve the prompt based on what you find.

This is the lesson where everything becomes practical. You are not learning about prompts — you are writing them.

By the end, you will have a working prompt structure you can adapt to dozens of real tasks, a habit of testing before trusting, and a review process you can apply to any AI output.

## Lesson Overview

| Activity | Outcome |
| --- | --- |
| Choose a real task | You pick a task from your own work or study |
| Build the first prompt | You add role, task, audience, context, and format |
| Test and evaluate the output | You identify vague, missing, or risky content |
| Add examples and quality criteria | You improve reliability |
| Run a review prompt | You produce and assess an improved second version |
| Reflect and share | You explain what changed and why |

---

## The Universal Prompt Builder

This structure works for most business and educational tasks. You do not need to use every section every time. Start with Role, Task, and Format. Add the others as the task grows more complex.

```text
Role:
Act as [a specific role relevant to the task].

Task:
[One clear, specific action. Use a verb: summarize, classify, draft, compare, explain.]

Audience:
[Who will read or use the output? Be specific about their background and needs.]

Context:
[Background information: business situation, goals, constraints, source material.]

Constraints:
[What the model must not do: invent data, use jargon, include personal names, 
claim legal advice, etc.]

Format:
[Exact structure of the output: table with named columns, checklist, numbered list, 
email draft, outline, JSON, etc.]

Quality criteria:
[How will you judge whether the answer is good? Be explicit.]
```

The more real work you put into the Context and Constraints sections, the better the output. Most beginner mistakes come from leaving those two sections empty.

---

## Why Weak Prompts Fail

Here are four common weak prompts and an explanation of exactly why they produce poor output:

| Weak prompt | Why it fails | What is missing |
| --- | --- | --- |
| Tell me about AI | No audience, no goal, no format | Produces a generic overview useful to no one |
| Make a plan | No context, no constraints, no scope | Returns a 10-step generic plan for an unknown goal |
| Summarize this | No format, no length, no purpose | Produces whatever length and structure the model prefers |
| Write something longer | No topic, no audience, no criteria | Adds words without adding value |

The pattern is the same every time: the model fills gaps with its best guess. Its guesses may be reasonable but they are not tailored to your situation.

---

## The Bad, Better, Best Pattern

One of the fastest ways to improve your prompting is to look at the same task at three quality levels and understand exactly what changes at each step. This pattern works for any task.

**The task:** Write a professional social media post about AI tools.

**Bad prompt:**
```text
Write me a post about AI tools.
```
What you get: A generic, surface-level post that could have been written about any tool, for any industry, for any audience. It looks polished. It belongs to no one in particular. This is the statistical average of all social media posts about AI — which is exactly what you do not want.

**Better prompt:**
```text
I want to write a social media post about the AI tools I use daily.
Don't start yet.
Ask me clarifying questions first — angle, audience, and tone —
so we can align before you write anything.
```
What changes: You stopped guessing and let the AI help you get clear on what you actually want. The first draft will be significantly stronger because the back-and-forth forced you to think before committing to a direction. The key phrase here is: *"Don't start yet."*

**Best prompt:**
```text
[ABOUT ME: paste three to five sentences about your background, role, and what you actually do]
[WRITING STYLE: paste two to three sentences from something you have already written that you are proud of]

I want to write a social media post about the AI tools I use daily.

First, read the context above completely before responding.
Do not start writing yet.
Ask me three clarifying questions so we can refine the approach together, one question at a time.
```
What changes: You replaced a description of yourself with actual source material. The model now knows your voice, your audience, and your standards — not from your description of yourself, but from real evidence. This produces a fundamentally different quality of output.

> **Key insight:** The gap between a weak AI output and a strong one is almost never the AI. It is how much useful context and direction the prompt contained. Bad prompts assume the model knows your audience, your style, and your goal. Best prompts give it real material and ask it to confirm understanding before it writes a word.

**What this pattern teaches you:**

| Level | What it assumes | What you actually give the model |
| --- | --- | --- |
| Bad | The model knows your audience and goal | A task description with no context |
| Better | You need help getting clear first | A task + permission to ask questions |
| Best | Source material is more reliable than description | Real context files + structured prompt |

---

## The "Ask Me First" Technique

One of the most underused prompt techniques is also one of the simplest: tell the model to ask you questions before it starts writing.

This works because the model has absorbed patterns from millions of writing, planning, and analysis tasks. It has a reliable sense of what information is typically missing from a vague request. When you ask it to surface those gaps first, you get a much better output — and you usually learn something about what you actually want.

```text
I want to [describe the task broadly].
Don't start yet.

First, ask me the questions you need answered before you can do this well.
One question at a time. Wait for my answer before asking the next one.
```

The "one question at a time" instruction is important. Without it, the model gives you a long list of questions all at once, and the conversation becomes a form to fill out rather than a productive exchange.

**When to use it:**
- When you know what you want but cannot describe it precisely yet.
- When the task involves your personal opinion, your brand voice, or your specific context.
- When previous attempts came back too generic and you are not sure exactly why.

**When not to use it:**
- When the task is simple and fully defined.
- When you already have complete source material ready to paste.
- When you are on a tight deadline and cannot afford a back-and-forth.

---

## Building a Prompt: Step by Step

Let's walk through building a real prompt together. The task: a manager needs a clean weekly update from messy project notes.

### Step 1: Start with the Basics

Write the minimum viable prompt:

```text
Summarize these project notes.

Notes:
[paste notes]
```

This will produce something. It will not be great. It will be too vague, the wrong length, and missing the structure the manager actually needs.

### Step 2: Add Role and Audience

```text
Act as an operations assistant.

Summarize the project notes below for a department manager 
who needs a clear update to share with their director.

Notes:
[paste notes]
```

Better. Now the model knows who it is and who the reader is. But the output is still unstructured.

### Step 3: Specify the Format

```text
Act as an operations assistant.

Summarize the project notes below for a department manager 
who needs a clean weekly update.

Return:
1. Executive summary (80 words or less)
2. Decisions made this week
3. Open questions (with who is responsible for each)
4. Action items as a table: Owner role | Task | Deadline | Risk level

Notes:
[paste notes]
```

Much better. The format is explicit, and the output is now directly usable.

### Step 4: Add Constraints

```text
Act as an operations assistant.

Summarize the project notes below for a department manager 
who needs a clean weekly update.

Return:
1. Executive summary (80 words or less)
2. Decisions made this week
3. Open questions (with who is responsible for each)
4. Action items as a table: Owner role | Task | Deadline | Risk level

Rules:
- Do not invent deadlines or owners that are not mentioned in the notes.
- If information is unclear, write "[needs confirmation]" rather than guessing.
- Use concise business language.
- Do not include personal names — use role titles only.

Notes:
[paste notes]
```

Now the model knows what it must not do. This is just as important as knowing what it should do.

### Step 5: Add Quality Criteria

```text
Act as an operations assistant.

Summarize the project notes below for a department manager 
who needs a clean weekly update.

Return:
1. Executive summary (80 words or less)
2. Decisions made this week
3. Open questions (with who is responsible for each)
4. Action items as a table: Owner role | Task | Deadline | Risk level

Rules:
- Do not invent deadlines or owners that are not mentioned in the notes.
- If information is unclear, write "[needs confirmation]."
- Use concise business language.
- Do not include personal names — use role titles only.

Quality criteria:
A good summary can be read in under 90 seconds. Every action item has a role and deadline 
or a "[needs confirmation]" flag. No claim is invented.

Notes:
[paste notes]
```

This is a production-ready prompt. You can reuse this structure with any set of project notes by simply swapping the content.

---

## The Prompt Builder in Practice

### Quick Reference: Weak vs. Strong

| Situation | Weak prompt | Strong prompt |
| --- | --- | --- |
| Meeting summary | "Summarize this meeting" | Role + audience + format with sections + constraint on inventing facts |
| Customer email draft | "Write a reply" | Role + customer message context + tone constraint + format + review flag |
| Content planning | "Make a content plan" | Role + audience + channels + table format with named columns + capacity constraint |
| Research summary | "What do people think about X?" | Role + source material provided + format + "only use provided sources" constraint |

---

## The Review Prompt: Your Second Pass

After the first AI output, always run a review prompt. This is how you catch the problems the model introduced.

```text
Review the output you just produced.

Check it against these criteria:
1. Are there any claims not supported by the input?
2. Are there any format errors or missing sections?
3. Is the tone appropriate for the intended audience?
4. Are there any items that need human confirmation before use?
5. Is anything unclear or ambiguous?

Return a table with:
Issue | Severity (high / medium / low) | Recommended fix
```

This two-pass approach — generate, then review — is a professional standard. It is not a sign that the first prompt was wrong. It is a recognition that AI output needs a second set of eyes, even if that second set is the same AI.

> **Important:** The review prompt is not foolproof. The model will not always catch its own errors. Use it to identify obvious issues quickly, then do a final human read for any important output.

---

## Adding Examples When Needed

If the output still does not match what you want after adding constraints and format, add an example. Show the model one correct output before asking for the real one.

```text
Use this format as the example for how to summarize a note:

Input note:
Customer asked why delivery takes three business days.

Output:
Customer concern: Delivery timeline.
Likely underlying need: Clear explanation of why three days is normal.
Recommended content: Short FAQ explaining the logistics process.

Now analyze these notes using the same format:
[paste notes]
```

One well-chosen example is often worth more than a page of instructions.

---

## Choosing Your Example Level

| Situation | Use | Why |
| --- | --- | --- |
| First draft, common format | Zero-shot | Fast, enough context in the model's training |
| Specific format or unusual tone | One-shot | One clear example sets the pattern |
| Repeated task, consistency needed | Few-shot | Multiple examples create reliable consistency |
| Complex judgment required | Step-by-step with review | Visible reasoning makes the output auditable |

### Zero-Shot Version
```text
Act as a project analyst.
Summarize the notes below.

Return:
1. Key decisions
2. Open questions
3. Action items

Notes:
[paste notes]
```

### One-Shot Version
```text
Act as a project analyst.
Use this example format:

Input:
Team approved the launch date. Pricing not yet confirmed.

Output:
Decision: Launch date approved.
Open question: Pricing — finance team to confirm.
Action item: Confirm pricing before sending launch communication.

Now summarize these notes:
[paste notes]
```

### Few-Shot Version
```text
Act as a project analyst.
Use these three examples:

Input: Campaign starts Monday. Design approved.
Output:
Decision: Campaign starts Monday, design approved.
Action item: None listed.

Input: Budget not approved. Finance needs revised estimate.
Output:
Open question: Budget approval pending.
Action item: Send revised estimate to finance.

Input: Support team needs FAQ before launch.
Output:
Action item: Prepare launch FAQ for support team. Deadline not stated.

Now summarize these notes using the same format:
[paste notes]
```

---

## Adding Step-by-Step Reasoning

When the task involves judgment, planning, or risk, ask the model to show its work before giving the final answer:

```text
Before writing the final summary, list:
1. What information is clearly stated in the notes.
2. What information is implied but not confirmed.
3. What is missing and needs human follow-up.
4. Any risk or sensitivity to flag for the reviewer.

Then produce the final summary.
```

This is especially useful when the output will be reviewed by someone else, shared with a client, or used to make a decision.

---

## Practice

Choose one task from this list, or use a real task from your work or studies:

- Summarize a set of meeting notes.
- Draft a response to a customer enquiry.
- Create a LinkedIn post promoting a course or event.
- Classify a set of feedback comments as positive, neutral, or negative.
- Explain a concept to a beginner audience.

**Build your prompt in five steps:**

1. Write a weak first version (two lines).
2. Add role and audience.
3. Add a specific output format.
4. Add at least two constraints.
5. Add quality criteria.

Run each version. Compare the outputs. Note exactly which addition made the biggest improvement.

Then write a review prompt and run a second pass on your best output.

---

## Completion Standard

You have completed this lesson when you can show:

1. A weak first prompt and the output it produced.
2. An improved, structured prompt with all five elements.
3. A review prompt and its output.
4. Two to three sentences explaining what each addition changed and why.

---

## Review Checklist

- [ ] Does your prompt include a role, task, audience, and format?
- [ ] Did you add at least one constraint that prevents invented content?
- [ ] Did you test and compare weak and strong versions?
- [ ] Did you run a review prompt on the output?
- [ ] Can you explain in plain English what each prompt element does?
Action item: None listed.

Input: The budget is not approved. Finance needs a revised estimate.
Output:
Open question: Budget approval.
Action item: Send revised estimate to finance.

Input: Support needs the FAQ before launch.
Output:
Action item: Prepare launch FAQ for support.

Now summarize these notes:
[paste notes]
```

## Add Step-By-Step Reasoning Safely

Use step-by-step prompting when the task needs planning or judgment. Ask for assumptions and checks that a human can review.

```text
Before the final answer, list:
1. What information is clear.
2. What information is missing.
3. What assumptions you are making.
4. What a human should verify.

Then produce the final answer.
```

## Practice

Choose one task:

- Summarize meeting notes.
- Create a customer survey.
- Draft a LinkedIn post.
- Classify customer feedback as positive, neutral, or negative.
- Explain a topic to students.

Write a first prompt. Then improve it by adding:

- Direction.
- Format.
- Zero-shot, one-shot, or few-shot examples.
- Quality criteria.
- A step-by-step planning or review step when the task needs judgment.

## Completion Standard

A learner has completed this lesson when they can show:

1. A weak first prompt.
2. An improved structured prompt.
3. A review prompt.
4. One sentence explaining what changed and why.
